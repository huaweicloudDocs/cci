# 替换TFJob<a name="cci_02_3147"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

替换TFJob。如下字段可被替换：

-   metadata.labels
-   metadata.annotations
-   spec.activeDeadlineSeconds
-   spec.ttlSecondsAfterFinished
-   spec.cleanPodPolicy

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

PUT /apis/kubeflow.org/v1/namespaces/\{namespace\}/tfjobs/\{name\}

**表 1**  Path参数

<a name="zh-cn_topic_0083864910_table167042013408"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row2067022020405"><th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0083864910_p65652297517"><a name="zh-cn_topic_0083864910_p65652297517"></a><a name="zh-cn_topic_0083864910_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.772277227722775%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0083864910_p165661629135114"><a name="zh-cn_topic_0083864910_p165661629135114"></a><a name="zh-cn_topic_0083864910_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.4059405940594%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0083864910_p14567629115114"><a name="zh-cn_topic_0083864910_p14567629115114"></a><a name="zh-cn_topic_0083864910_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row1670122004014"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p534171718494"><a name="p534171718494"></a><a name="p534171718494"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p289919167553"><a name="p289919167553"></a><a name="p289919167553"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p834171714492"><a name="p834171714492"></a><a name="p834171714492"></a>name of the TFJob</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row136701220114011"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p113531734914"><a name="p113531734914"></a><a name="p113531734914"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p159531816165517"><a name="p159531816165517"></a><a name="p159531816165517"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p835151774919"><a name="p835151774919"></a><a name="p835151774919"></a>object name and auth scope, such as for teams and projects</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table2395432124915"></a>
<table><thead align="left"><tr id="row11396123274917"><th class="cellrowborder" valign="top" width="17.961796179617963%" id="mcps1.2.4.1.1"><p id="p957611471498"><a name="p957611471498"></a><a name="p957611471498"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.782278227822783%" id="mcps1.2.4.1.2"><p id="p1357674719491"><a name="p1357674719491"></a><a name="p1357674719491"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.25592559255926%" id="mcps1.2.4.1.3"><p id="p057654715492"><a name="p057654715492"></a><a name="p057654715492"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row339618327491"><td class="cellrowborder" valign="top" width="17.961796179617963%" headers="mcps1.2.4.1.1 "><p id="p280310559498"><a name="p280310559498"></a><a name="p280310559498"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="22.782278227822783%" headers="mcps1.2.4.1.2 "><p id="p5803125534918"><a name="p5803125534918"></a><a name="p5803125534918"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.25592559255926%" headers="mcps1.2.4.1.3 "><p id="p180395512497"><a name="p180395512497"></a><a name="p180395512497"></a>If 'true’, then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section89699412414"></a>

请求参数的详细描述请参见[表154](数据结构.md#table2587194916400)。

**请求示例：**

更改TFJob的结束存活时间ttlSecondsAfterFinished：

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "TFJob",
    "metadata": {
        "creationTimestamp": "2019-07-24T07:17:01Z",
        "generation": 2,
        "labels": {
            "app": "test"
        },
        "name": "tfjob-test",
        "namespace": "kube-test",
        "resourceVersion": "72447176",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/tfjobs/tfjob-test",
        "uid": "083cc6df-ade3-11e9-aaa4-340a9837e413"
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
        },
        "ttlSecondsAfterFinished": 1000
    },
    "status": {
        "conditions": [
            {
                "lastTransitionTime": "2019-07-24T07:16:13Z",
                "lastUpdateTime": "2019-07-24T07:16:13Z",
                "message": "TFJob tfjob-test is created.",
                "reason": "TFJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-24T07:16:18Z",
                "lastUpdateTime": "2019-07-24T07:16:18Z",
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
        "startTime": "2019-07-24T07:16:13Z"
    }
}
```

## 响应消息<a name="section13519020142"></a>

**响应参数：**

响应参数的详细描述请参考[表154](数据结构.md#table2587194916400)。

**响应示例**：

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "TFJob",
    "metadata": {
        "creationTimestamp": "2019-07-24T07:17:01Z",
        "generation": 2,
        "labels": {
            "app": "test"
        },
        "name": "tfjob-test",
        "namespace": "kube-test",
        "resourceVersion": "72447176",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/tfjobs/tfjob-test",
        "uid": "083cc6df-ade3-11e9-aaa4-340a9837e413"
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
        },
        "ttlSecondsAfterFinished": 1000
    },
    "status": {
        "conditions": [
            {
                "lastTransitionTime": "2019-07-24T07:16:13Z",
                "lastUpdateTime": "2019-07-24T07:16:13Z",
                "message": "TFJob tfjob-test is created.",
                "reason": "TFJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-24T07:16:18Z",
                "lastUpdateTime": "2019-07-24T07:16:18Z",
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
        "startTime": "2019-07-24T07:16:13Z"
    }
}
```

## 状态码<a name="section649511434414"></a>

**表 3**  状态码

<a name="table1557910359443"></a>
<table><thead align="left"><tr id="row1958063510446"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p966010481444"><a name="p966010481444"></a><a name="p966010481444"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p1660114813441"><a name="p1660114813441"></a><a name="p1660114813441"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row758019354448"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1466024814418"><a name="p1466024814418"></a><a name="p1466024814418"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p766164811448"><a name="p766164811448"></a><a name="p766164811448"></a>OK</p>
</td>
</tr>
<tr id="row55801135124418"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p166144814449"><a name="p166144814449"></a><a name="p166144814449"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p166611448104411"><a name="p166611448104411"></a><a name="p166611448104411"></a>Created</p>
</td>
</tr>
<tr id="row18580535124410"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p0661194824412"><a name="p0661194824412"></a><a name="p0661194824412"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p266154884410"><a name="p266154884410"></a><a name="p266154884410"></a>Unauthorized</p>
</td>
</tr>
<tr id="row15580135134412"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p136615487442"><a name="p136615487442"></a><a name="p136615487442"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p20661164818447"><a name="p20661164818447"></a><a name="p20661164818447"></a>BadRequest</p>
</td>
</tr>
<tr id="row458023517449"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p126611448134420"><a name="p126611448134420"></a><a name="p126611448134420"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5661104813448"><a name="p5661104813448"></a><a name="p5661104813448"></a>Internal Error</p>
</td>
</tr>
<tr id="row1658017359443"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1066212486444"><a name="p1066212486444"></a><a name="p1066212486444"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p66621548194415"><a name="p66621548194415"></a><a name="p66621548194415"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

