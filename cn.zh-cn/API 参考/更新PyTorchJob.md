# 更新PyTorchJob<a name="cci_02_3166"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

更新PyTorchJob。如下字段可被更新：

-   metadata.labels
-   metadata.annotations
-   spec.activeDeadlineSeconds
-   spec.ttlSecondsAfterFinished
-   spec.cleanPodPolicy

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

PATCH /apis/kubeflow.org/v1/namespaces/\{namespace\}/pytorchjobs/\{name\}

**表 1**  Path参数

|参数|是否必选|描述|
|--|--|--|
|name|Yes|name of the PyTorchJob|
|namespace|Yes|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|描述|
|--|--|--|
|pretty|No|If 'true’, then the output is pretty printed.|


## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

**请求参数**：

“Content-Type“消息头说明请参见[PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

>![](public_sys-resources/icon-note.gif) **说明：** 
>目前只支持“Merge Patch”。

**请求示例：**

```
Content-Type: application/merge-patch+json
```

```
{
    "metadata": {
        "labels": {
            "app": "test"
        }
    }
}
```

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表165](数据结构-0.md#table1729624017556)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "PyTorchJob",
    "metadata": {
        "creationTimestamp": "2019-07-24T10:35:38Z",
        "generation": 1,
        "labels": {
            "app": "test"
        },
        "name": "pytorch-test",
        "namespace": "kube-test",
        "resourceVersion": "72519229",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/pytorchjobs/pytorch-test",
        "uid": "c6e548f1-adfe-11e9-ba3a-b44326d0c915"
    },
    "spec": {
        "pytorchReplicaSpecs": {
            "Master": {
                "replicas": 1,
                "restartPolicy": "Never",
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "--backend",
                                    "gloo"
                                ],
                                "command": [
                                    "python",
                                    "/var/mnist.py"
                                ],
                                "image": "*.*.*.215:20202/gcs/pytorch-cpu:v1",
                                "name": "pytorch",
                                "resources": {
                                    "limits": {
                                        "cpu": 2,
                                        "memory": "4Gi"
                                    },
                                    "requests": {
                                        "cpu": 2,
                                        "memory": "4Gi"
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
                "restartPolicy": "OnFailure",
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "--backend",
                                    "gloo"
                                ],
                                "command": [
                                    "python",
                                    "/var/mnist.py"
                                ],
                                "image": "*.*.*.215:20202/gcs/pytorch-cpu:v1",
                                "name": "pytorch",
                                "resources": {
                                    "limits": {
                                        "cpu": 2,
                                        "memory": "4Gi"
                                    },
                                    "requests": {
                                        "cpu": 2,
                                        "memory": "4Gi"
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
                "lastTransitionTime": "2019-07-24T10:36:26Z",
                "lastUpdateTime": "2019-07-24T10:36:26Z",
                "message": "PyTorchJob pytorch-test is created.",
                "reason": "PyTorchJobCreated",
                "status": "True",
                "type": "Created"
            }
        ],
        "replicaStatuses": {
            "Master": {}
        },
        "startTime": "2019-07-24T10:36:26Z"
    }
}
```

## 状态码<a name="zh-cn_topic_0083864910_section16509142112516"></a>

**表 3**  状态码

|状态码|描述|
|--|--|
|200|OK|
|401|Unauthorized|
|500|Internal Error|
|403|Forbidden|
|409|Conflict|
|400|BadRequest|


