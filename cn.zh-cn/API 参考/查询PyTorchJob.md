# 查询PyTorchJob<a name="cci_02_3162"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

查询PyTorchJob的详细信息。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

GET /apis/kubeflow.org/v1/namespaces/\{namespace\}/pytorchjobs/\{name\}

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

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表165](数据结构-0.md#table1729624017556)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "PyTorchJob",
    "metadata": {
        "creationTimestamp": "2019-07-24T10:29:45Z",
        "generation": 1,
        "name": "pytorch-test",
        "namespace": "kube-test",
        "resourceVersion": "72516798",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/pytorchjobs/pytorch-test",
        "uid": "f4c79668-adfd-11e9-8041-340a9837e2a7"
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
                "lastTransitionTime": "2019-07-24T10:30:34Z",
                "lastUpdateTime": "2019-07-24T10:30:34Z",
                "message": "PyTorchJob pytorch-test is created.",
                "reason": "PyTorchJobCreated",
                "status": "True",
                "type": "Created"
            }
        ],
        "replicaStatuses": {
            "Master": {}
        },
        "startTime": "2019-07-24T10:30:34Z"
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


