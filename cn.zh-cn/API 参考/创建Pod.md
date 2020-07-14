# 创建Pod<a name="cci_02_3006"></a>

## 功能介绍<a name="scc86678262934086bfbe32385da35788"></a>

创建一个Pod。

>![](public_sys-resources/icon-note.gif) **说明：** 
>Pod的生命周期是短暂的，Pod是用后即焚的实体。在实际使用中，请谨慎单独创建Pod，请使用Deployment、StatefulSet和Job这些控制器创建应用，从而保障应用高可用。

云容器实例中Pod规格有限制，具体的限制请参见[约束限制](https://support.huaweicloud.com/productdesc-cci/cci_03_0007.html)页面的“Pod规格“部分。

当前支持使用Nvidia GPU的驱动版本为**410.104和418.126**，您应用程序中使用的CUDA需满足如[表1](#table16459192015518)所示的配套关系。CUDA与驱动的配套关系来源于Nvidia官网，详细信息请参见[CUDA Compatibility](https://docs.nvidia.com/deploy/cuda-compatibility/index.html)。

**表 1**  NVIDIA GPU驱动与CUDA配套关系

<a name="table16459192015518"></a>
<table><thead align="left"><tr id="row194598204515"><th class="cellrowborder" valign="top" width="30.620000000000005%" id="mcps1.2.3.1.1"><p id="p1845932065111"><a name="p1845932065111"></a><a name="p1845932065111"></a>NVIDIA GPU驱动版本</p>
</th>
<th class="cellrowborder" valign="top" width="69.38%" id="mcps1.2.3.1.2"><p id="p1445910203518"><a name="p1445910203518"></a><a name="p1445910203518"></a>CUDA Toolkit版本</p>
</th>
</tr>
</thead>
<tbody><tr id="row9786192115398"><td class="cellrowborder" valign="top" width="30.620000000000005%" headers="mcps1.2.3.1.1 "><p id="p1178672103912"><a name="p1178672103912"></a><a name="p1178672103912"></a>410.104</p>
</td>
<td class="cellrowborder" valign="top" width="69.38%" headers="mcps1.2.3.1.2 "><p id="p20459152020519"><a name="p20459152020519"></a><a name="p20459152020519"></a>CUDA 10.0 (10.0.130)及以下</p>
</td>
</tr>
<tr id="row4823184321519"><td class="cellrowborder" valign="top" width="30.620000000000005%" headers="mcps1.2.3.1.1 "><p id="p10823114312154"><a name="p10823114312154"></a><a name="p10823114312154"></a>418.126</p>
</td>
<td class="cellrowborder" valign="top" width="69.38%" headers="mcps1.2.3.1.2 "><p id="p9459132010511"><a name="p9459132010511"></a><a name="p9459132010511"></a>CUDA 10.1 (10.1.105)及以下</p>
</td>
</tr>
</tbody>
</table>

如果选择GPU加速型Pod，您需要设置Pod的**metadata.annotations**中添加**cri.cci.io/gpu-driver**字段，指定使用哪个版本显卡驱动，取值如下：

-   gpu-410.104
-   gpu-418.126

创建Pod时挂载OBS的使用限制请参见[挂载OBS使用限制](挂载OBS使用限制.md)。

## URI<a name="s83bc1fb06185462cb2e2665b169bc85c"></a>

POST /api/v1/namespaces/\{namespace\}/pods

**表 2**  Path参数

<a name="table1696332124519"></a>
<table><thead align="left"><tr id="row11961332194516"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.3.1.1"><p id="p396032144518"><a name="p396032144518"></a><a name="p396032144518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="76%" id="mcps1.2.3.1.2"><p id="p18962325454"><a name="p18962325454"></a><a name="p18962325454"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9960327457"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1496113214456"><a name="p1496113214456"></a><a name="p1496113214456"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p141902036155717"><a name="p141902036155717"></a><a name="p141902036155717"></a>Object name and auth scope, such as for teams and projects.</p>
</td>
</tr>
</tbody>
</table>

**表 3**  参数描述

<a name="zh-cn_topic_0079615001_table32114614"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615001_row42303331"><th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615001_p4017754"><a name="zh-cn_topic_0079615001_p4017754"></a><a name="zh-cn_topic_0079615001_p4017754"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11%" id="mcps1.2.4.1.2"><p id="p27173000203043"><a name="p27173000203043"></a><a name="p27173000203043"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="75%" id="mcps1.2.4.1.3"><p id="p53529377203043"><a name="p53529377203043"></a><a name="p53529377203043"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615001_row29042598"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615001_p3640263"><a name="zh-cn_topic_0079615001_p3640263"></a><a name="zh-cn_topic_0079615001_p3640263"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615001_p26425925"><a name="zh-cn_topic_0079615001_p26425925"></a><a name="zh-cn_topic_0079615001_p26425925"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="75%" headers="mcps1.2.4.1.3 "><p id="p555410261514"><a name="p555410261514"></a><a name="p555410261514"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079615001_d0e16631"></a>

**请求参数：**

请求参数的详细描述请参见[表2](数据结构.md#zh-cn_topic_0079614925_table60388168)。

**请求示例：**

创建普通Pod示例：

```
{
    "apiVersion": "v1",
    "kind": "Pod",
    "metadata": {
        "labels": {
            "name": "pod-test"
        },
        "name": "pod-test"
    },
    "spec": {
        "containers": [
            {
                "image": "redis",
                "imagePullPolicy": "Always",
                "name": "test",
                "resources": {
                    "requests": {
                        "cpu": "0.5",
                        "memory": "1024Mi" 
                    },
                    "limits": {
                        "cpu": "0.5",
                        "memory": "1024Mi"
                    }
                }
            }
        ],
        "imagePullSecrets": [
            {
                "name": "imagepull-secret"
            }
        ],
        "restartPolicy": "Always",
        "priority": 0
    }
}
```

创建GPUpod示例：

```
{
    "apiVersion": "v1",
    "kind": "Pod",
    "metadata": {
        "labels": {
            "name": "pod-test"
        },
        "name": "pod-test",
        "annotations": {
            "cri.cci.io/gpu-driver": "gpu-410.104"
        }
    },
    "spec": {
        "containers": [
            {
                "image": "redis",
                "imagePullPolicy": "Always",
                "name": "test",
                "resources": {
                    "requests": {
                        "cpu": "4",
                        "memory": "32Gi",
                        "nvidia.com/gpu-tesla-v100-16GB": "1"
                    },
                    "limits": {
                        "cpu": "4",
                        "memory": "32Gi",
                        "nvidia.com/gpu-tesla-v100-16GB": "1"
                    }
                }
            }
        ],
        "imagePullSecrets": [
            {
                "name": "imagepull-secret"
            }
        ],
        "restartPolicy": "Always",
        "priority": 0
    }
}
```

通过LVM方式创建本地卷的Pod示例：

```
{
    "apiVersion": "v1",
    "kind": "Pod",
    "metadata": {
        "labels": {
            "app": "localvolume"
        },
        "name": "localvolume",
        "namespace": "cci-namespace-12192721"
    },
    "spec": {
        "containers": [
            {
                "command": [
                    "/bin/sh",
                    "-c",
                    "sleep 10000"
                ],
                "image": "100.79.1.215:20202/paas_cci_test/redis:v1",
                "imagePullPolicy": "Always",
                "lifecycle": {},
                "volumeMounts": [
                    {
                        "name": "innerevs123",
                        "mountPath": "/tmp/log"
                    }
                ],
                "name": "container-0",
                "resources": {
                    "limits": {
                        "cpu": "500m",
                        "memory": "1024Mi"
                    },
                    "requests": {
                        "cpu": "500m",
                        "memory": "1024Mi"
                    }
                },
                "terminationMessagePath": "/dev/termination-log",
                "terminationMessagePolicy": "File"
            }
        ],
        "dnsPolicy": "Default",
        "imagePullSecrets": [
            {
                "name": "imagepull-secret"
            }
        ],
        "restartPolicy": "Always",
        "schedulerName": "default-scheduler",
        "volumes": [
            {
                "emptyDir": {
                    "sizeLimit": "100Gi"
                },
                "name": "innerevs123"
            }
        ],
        "terminationGracePeriodSeconds": 30,
        "nodeSelector": {
            "node.cci.io/allowed-on-poc-dedicated-node": "sina"
        },
        "tolerations": [
            {
                "effect": "NoSchedule",
                "key": "node.cci.io/allowed-on-poc-dedicated-node",
                "operator": "Equal",
                "value": "sina"
            }
        ]
    }
}
```

## 响应消息<a name="s23649bc4d7154135b7153a5743022fcd"></a>

**响应参数：**

响应参数的详细描述请参见[表2](数据结构.md#zh-cn_topic_0079614925_table60388168)。

**响应示例：**

```
{
    "kind": "Pod",
    "apiVersion": "v1",
    "metadata": {
        "name": "pod-test",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/pods/pod-test",
        "uid": "8b985a27-af74-11e8-9d5d-c88d83be759f",
        "resourceVersion": "5030599",
        "creationTimestamp": "2018-09-03T12:26:12Z",
        "labels": {
            "name": "pod-test"
        },
        "annotations": {
            "cri.cci.io/container-type": "secure-container"
        },
        "enable": true
    },
    "spec": {
        "containers": [
            {
                "name": "test",
                "image": "redis",
                "resources": {
                    "limits": {
                        "cpu": "500m",
                        "memory": "1Gi"
                    },
                    "requests": {
                        "cpu": "500m",
                        "memory": "1Gi"
                    }
                },
                "terminationMessagePath": "/dev/termination-log",
                "terminationMessagePolicy": "File",
                "imagePullPolicy": "Always"
            }
        ],
        "restartPolicy": "Always",
        "priority": 0,
        "terminationGracePeriodSeconds": 30,
        "dnsPolicy": "ClusterFirst",
        "securityContext": {},
        "imagePullSecrets": [
            {
                "name": "imagepull-secret"
            }
        ],
        "schedulerName": "default-scheduler",
        "tolerations": [
            {
                "key": "node.kubernetes.io/not-ready",
                "operator": "Exists",
                "effect": "NoExecute",
                "tolerationSeconds": 300
            },
            {
                "key": "node.kubernetes.io/unreachable",
                "operator": "Exists",
                "effect": "NoExecute",
                "tolerationSeconds": 300
            }
        ]
    },
    "status": {
        "phase": "Pending",
        "qosClass": "Guaranteed"
    }
}
```

## 状态码<a name="sbb2d9f14fc4a4197a3a609e7c568ab4d"></a>

[表4](#zh-cn_topic_0079615001_table20596071)描述API的状态码。

**表 4**  状态码

<a name="zh-cn_topic_0079615001_table20596071"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615001_row9746163"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p57545694203043"><a name="p57545694203043"></a><a name="p57545694203043"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p30689603203043"><a name="p30689603203043"></a><a name="p30689603203043"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615001_row48621261"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615001_p46008046"><a name="zh-cn_topic_0079615001_p46008046"></a><a name="zh-cn_topic_0079615001_p46008046"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615001_p35664277"><a name="zh-cn_topic_0079615001_p35664277"></a><a name="zh-cn_topic_0079615001_p35664277"></a>This operation succeeds, and a Pod resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

