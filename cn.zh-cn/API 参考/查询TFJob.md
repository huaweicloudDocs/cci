# 查询TFJob<a name="cci_02_3142"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

查询TFJob的详细信息。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

GET /apis/kubeflow.org/v1/namespaces/\{namespace\}/tfjobs/\{name\}

**表 1**  Path参数

|参数|是否必选|描述|
|--|--|--|
|name|Yes|name of the TFJob|
|namespace|Yes|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|描述|
|--|--|--|
|pretty|No|If 'true’, then the output is pretty printed.|


## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参考[表154](数据结构-0.md#table2587194916400)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "TFJob",
    "metadata": {
        "creationTimestamp": "2019-07-23T12:39:47Z",
        "generation": 1,
        "name": "tfjob-test",
        "namespace": "kube-test",
        "resourceVersion": "72050567",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/tfjobs/tfjob-test",
        "uid": "f461f966-ad46-11e9-aaa4-340a9837e413"
    },
    "spec": {
        "backoffLimit": 6,
        "tfReplicaSpecs": {
            "Ps": {
                "replicas": 1,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "python",
                                    "/opt/tf-benchmarks/scripts/tf_cnn_benchmarks/tf_cnn_benchmarks.py",
                                    "--batch_size=1",
                                    "--model=resnet50",
                                    "--variable_update=parameter_server",
                                    "--flush_stdout=true",
                                    "--num_gpus=1",
                                    "--local_parameter_device=cpu",
                                    "--device=cpu",
                                    "--data_format=NHWC"
                                ],
                                "image": "*.*.*.215:20202/cci/tf-benchmarks-cpu:v1",
                                "name": "tensorflow",
                                "ports": [
                                    {
                                        "containerPort": 2222,
                                        "name": "tfjob-port"
                                    }
                                ],
                                "resources": {
                                    "limits": {
                                        "cpu": "2",
                                        "memory": "4Gi"
                                    },
                                    "requests": {
                                        "cpu": "2",
                                        "memory": "4Gi"
                                    }
                                }
                            }
                        ],
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "restartPolicy": "OnFailure"
                    }
                }
            },
            "Worker": {
                "replicas": 1,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "python",
                                    "/opt/tf-benchmarks/scripts/tf_cnn_benchmarks/tf_cnn_benchmarks.py",
                                    "--batch_size=1",
                                    "--model=resnet50",
                                    "--variable_update=parameter_server",
                                    "--flush_stdout=true",
                                    "--local_parameter_device=cpu",
                                    "--device=cpu",
                                    "--data_format=NHWC"
                                ],
                                "image": "*.*.*.215:20202/cci/tf-benchmarks-cpu:v1",
                                "name": "tensorflow",
                                "ports": [
                                    {
                                        "containerPort": 2222,
                                        "name": "tfjob-port"
                                    }
                                ],
                                "resources": {
                                    "limits": {
                                        "cpu": "2",
                                        "memory": "4Gi"
                                    },
                                    "requests": {
                                        "cpu": "2",
                                        "memory": "4Gi"
                                    }
                                }
                            }
                        ],
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "restartPolicy": "OnFailure"
                    }
                }
            }
        }
    },
    "status": {
        "conditions": [
            {
                "lastTransitionTime": "2019-07-23T12:38:58Z",
                "lastUpdateTime": "2019-07-23T12:38:58Z",
                "message": "TFJob tfjob-test is created.",
                "reason": "TFJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-23T12:39:30Z",
                "lastUpdateTime": "2019-07-23T12:39:30Z",
                "message": "TFJob tfjob-test is running.",
                "reason": "TFJobRunning",
                "status": "True",
                "type": "Running"
            }
        ],
        "replicaStatuses": {
            "PS": {
                "active": 1
            },
            "Worker": {
                "active": 1
            }
        },
        "startTime": "2019-07-23T12:38:58Z"
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


