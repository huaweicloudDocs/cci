# 查询MXJob<a name="cci_02_3152"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

查询MXJob的详细信息。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

GET /apis/kubeflow.org/v1/namespaces/\{namespace\}/mxjobs/\{name\}

**表 1**  Path参数

|参数|是否必选|描述|
|--|--|--|
|name|Yes|name of the MXJob|
|namespace|Yes|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|描述|
|--|--|--|
|pretty|No|If 'true’, then the output is pretty printed.|


## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参考[表162](数据结构-0.md#table65611161418)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "MXJob",
    "metadata": {
        "creationTimestamp": "2019-07-24T08:42:33Z",
        "generation": 1,
        "name": "mxnet-job",
        "namespace": "kube-test",
        "resourceVersion": "72476154",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/mxjobs/mxnet-job",
        "uid": "fac6dcd2-adee-11e9-8041-340a9837e2a7"
    },
    "spec": {
        "cleanPodPolicy": "Running",
        "jobMode": "MXTrain",
        "mxReplicaSpecs": {
            "Scheduler": {
                "replicas": 1,
                "restartPolicy": "Never",
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "-c",
                                    "python train_imagenet.py"
                                ],
                                "command": [
                                    "/bin/bash"
                                ],
                                "image": "*.*.*.215:20202/cci/mxnet:xsw-dis",
                                "name": "mxnet",
                                "resources": {
                                    "limits": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    },
                                    "requests": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    }
                                }
                            }
                        ],
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ]
                    }
                }
            },
            "Server": {
                "replicas": 1,
                "restartPolicy": "Never",
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "-c",
                                    "python train_imagenet.py"
                                ],
                                "command": [
                                    "/bin/bash"
                                ],
                                "image": "*.*.*.215:20202/cci/mxnet:xsw-dis",
                                "name": "mxnet",
                                "resources": {
                                    "limits": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    },
                                    "requests": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    }
                                }
                            }
                        ],
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ]
                    }
                }
            },
            "Worker": {
                "replicas": 1,
                "restartPolicy": "Never",
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "-c",
                                    "python train_imagenet.py --benchmark 1  --network resnet --batch-size 1 --num-epochs 1 --kv-store dist_sync --num-examples 500"
                                ],
                                "command": [
                                    "/bin/bash"
                                ],
                                "image": "*.*.*.215:20202/cci/mxnet:xsw-dis",
                                "name": "mxnet",
                                "resources": {
                                    "limits": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    },
                                    "requests": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    }
                                }
                            }
                        ],
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ]
                    }
                }
            }
        }
    },
    "status": {
        "conditions": [
            {
                "lastTransitionTime": "2019-07-24T08:42:33Z",
                "lastUpdateTime": "2019-07-24T08:42:33Z",
                "message": "MXJob mxnet-job is created.",
                "reason": "MXJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-24T08:42:33Z",
                "lastUpdateTime": "2019-07-24T08:42:52Z",
                "message": "MXJob mxnet-job is running.",
                "reason": "MXJobRunning",
                "status": "True",
                "type": "Running"
            }
        ],
        "mxReplicaStatuses": {
            "Scheduler": {
                "active": 1
            },
            "Server": {
                "active": 1
            },
            "Worker": {
                "active": 1
            }
        },
        "startTime": "2019-07-24T08:42:33Z"
    }
}
```

## 状态码<a name="zh-cn_topic_0083864910_section16509142112516"></a>

**表 3**  状态码

|状态码|描述|
|--|--|
|200|OK|
|401|Unauthorized|
|404|Not found|
|500|Internal error|
|403|Forbidden|


