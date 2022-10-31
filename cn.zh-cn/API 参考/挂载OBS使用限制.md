# 挂载OBS使用限制<a name="cci_02_2026"></a>

云容器实例通过辅助容器（SideCar Container）挂载OBS路径，并将路径共享给主容器，如[图1](#fig82821406355)所示。

**图 1**  SideCar Container<a name="fig82821406355"></a>  
![](figures/SideCar-Container.png "SideCar-Container")

## 限制条件<a name="section099695820470"></a>

挂载OBS时有如下限制：

-   创建Pod时需要添加annotations字段：**obssidecar-injector-webhook/inject: 'true'**。
    -   **obssidecar-injector-webhook/inject: 'true'**  : 表示挂载OBS需要创建obssidecar容器。

-   挂载obs并行文件系统时，obssidecar容器需预留一定内存以保障业务可靠性，防止容器因资源不足异常退出。当业务容器挂载单个obs并行文件系统时，CPU和内存规格建议配置如下：

    "obssidecar-injector-webhook/cpu": "500m",

    "obssidecar-injector-webhook/memory": "1024Mi"

    当业务容器挂载多个obs并行文件系统时，相应CPU和内存规格逐倍增加。

    -   **obssidecar-injector-webhook/cpu**: 表示obssidecar容器cpu规格。
    -   **obssidecar-injector-webhook/memory**: 表示obssidecar容器memory规格。


启动命令。

-   使用yaml配置容器启动命令时，推荐使用bash方式。

    **trap '\[ -d /obssidecar/terminate \] && echo \> /obssidecar/terminate/0' EXIT && sleep 10**

    示例：

    ```
    {
        "command": [
            "/bin/sh",
            "-c",
            "trap '[ -d /obssidecar/terminate ] && echo > /obssidecar/terminate/0' EXIT && sleep 10"
        ]
    }
    ```


-   用户容器自带启动命令或者容器本身就不会退出时，无需配置启动命令。

    其中，用户容器自带启动命令时，需要保证命令退出时向/obssidecar/terminate/写入任意一个文件，保证sidecar容器感知用户容器的退出。


示例如下：

```
{
    "apiVersion": "batch/v1",
    "kind": "Job",
    "metadata": {
        "annotations": {
            "description": ""
        },
        "enable": true,
        "name": "obs-casoffinder",
        "namespace": "cci-namespace-tibgpu",
        "labels": {}
    },
    "spec": {
        "template": {
            "metadata": {
                "enable": true,
                "name": "obs-casoffinder",
                "annotations": {
                    "obssidecar-injector-webhook/inject": "true",
                    "obssidecar-injector-webhook/cpu": "500m",
                    "obssidecar-injector-webhook/memory": "2048Mi",
                    "cri.cci.io/gpu-driver": "gpu-418.126"
                }
            },
            "spec": {
                "containers": [
                    {
                        "image": "swr.cn-north-1.myhuaweicloud.com/aeocdc/opencl1:v1",
                        "name": "casoffinder-obs",
                        "terminationMessagePolicy": "File",
                        "resources": {
                            "limits": {
                                "cpu": "4",
                                "memory": "32Gi",
                                "nvidia.com/gpu-tesla-v100-32GB":"1"
                            },
                            "requests": {
                                "cpu": "4",
                                "memory": "32Gi",
                                "nvidia.com/gpu-tesla-v100-32GB":"1"
                            }
                        },
                        "command": [
                            "/bin/sh",
                            "-c",
                            "/tmp/obs0/gBIG/cas-offinder /tmp/obs0/gBIG/off_targetInput.txt G /tmp/obs0/gBIG/off_targetOutput.txt  && echo >/obssidecar/terminate/0"
                        ],
                        "lifecycle": {},
                        "volumeMounts": [
                            {
                                "name": "cci-obs-import-jzt9g50x-tunn",
                                "mountPath": "/tmp/obs0"
                            }
                        ]
                    }
                ],
                "imagePullSecrets": [
                    {
                        "name": "imagepull-secret"
                    }
                ],
                "restartPolicy": "Never",
                "volumes": [
                    {
                        "persistentVolumeClaim": {
                            "claimName": "cci-obs-import-jzt9g50x-tunn"
                        },
                        "name": "cci-obs-import-jzt9g50x-tunn"
                    }
                ]
            }
        },
        "activeDeadlineSeconds": 200
    }
}
```

