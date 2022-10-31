# 查询指定namespace下的所有PyTorchJob<a name="cci_02_3163"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

查询Namespace下所有PyTorchJob的详细信息。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

GET /apis/kubeflow.org/v1/namespaces/\{namespace\}/pytorchjobs

**表 1**  Path参数

|参数|是否必选|描述|
|--|--|--|
|namespace|Yes|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|描述|
|--|--|--|
|fieldSelector|No|A selector to restrict the list of returned objects by their fields. Defaults to everything.|
|labelSelector|No|A selector to restrict the list of returned objects by their labels. Defaults to everything.|
|limit|No|limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.|
|resourceVersion|No|When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it’s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.|
|timeoutSeconds|No|Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.|
|watch|No|Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.|


## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表170](数据结构-0.md#table115583311221)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "items": [
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
    ],
    "kind": "PyTorchJobList",
    "metadata": {
        "continue": "",
        "resourceVersion": "72517974",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/pytorchjobs"
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


