# 查询指定namespace下的所有TFJob<a name="cci_02_3143"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

查询Namespace下所有TFJob的详细信息。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

GET /apis/kubeflow.org/v1/namespaces/\{namespace\}/tfjobs

**表 1**  Path参数

<a name="zh-cn_topic_0083864910_table167042013408"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row2067022020405"><th class="cellrowborder" valign="top" width="18%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0083864910_p65652297517"><a name="zh-cn_topic_0083864910_p65652297517"></a><a name="zh-cn_topic_0083864910_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.720000000000002%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0083864910_p165661629135114"><a name="zh-cn_topic_0083864910_p165661629135114"></a><a name="zh-cn_topic_0083864910_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.28%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0083864910_p14567629115114"><a name="zh-cn_topic_0083864910_p14567629115114"></a><a name="zh-cn_topic_0083864910_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row1670122004014"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.4.1.1 "><p id="p2541201454120"><a name="p2541201454120"></a><a name="p2541201454120"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.720000000000002%" headers="mcps1.2.4.1.2 "><p id="p14541814164110"><a name="p14541814164110"></a><a name="p14541814164110"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.28%" headers="mcps1.2.4.1.3 "><p id="p165414146415"><a name="p165414146415"></a><a name="p165414146415"></a>object name and auth scope, such as for teams and projects</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table11308949102120"></a>
<table><thead align="left"><tr id="row23131949192118"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p8316349122119"><a name="p8316349122119"></a><a name="p8316349122119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.318368163183685%" id="mcps1.2.4.1.2"><p id="p1231884913215"><a name="p1231884913215"></a><a name="p1231884913215"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.273672632736734%" id="mcps1.2.4.1.3"><p id="p2321124920215"><a name="p2321124920215"></a><a name="p2321124920215"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10334449142116"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p883818599545"><a name="p883818599545"></a><a name="p883818599545"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p283845919544"><a name="p283845919544"></a><a name="p283845919544"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p19837859165418"><a name="p19837859165418"></a><a name="p19837859165418"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row13340949102114"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1837105955414"><a name="p1837105955414"></a><a name="p1837105955414"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1836259105419"><a name="p1836259105419"></a><a name="p1836259105419"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1835159115412"><a name="p1835159115412"></a><a name="p1835159115412"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row1934684942112"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p7834175920549"><a name="p7834175920549"></a><a name="p7834175920549"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p8834105912542"><a name="p8834105912542"></a><a name="p8834105912542"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1083315596543"><a name="p1083315596543"></a><a name="p1083315596543"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.</p>
<p id="p1260275671119"><a name="p1260275671119"></a><a name="p1260275671119"></a>The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row1235224982117"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p583285985414"><a name="p583285985414"></a><a name="p583285985414"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1583165995419"><a name="p1583165995419"></a><a name="p1583165995419"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p11831185919540"><a name="p11831185919540"></a><a name="p11831185919540"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it’s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row6360204912217"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p78302591540"><a name="p78302591540"></a><a name="p78302591540"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p8829135919541"><a name="p8829135919541"></a><a name="p8829135919541"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p782915915547"><a name="p782915915547"></a><a name="p782915915547"></a>Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.</p>
</td>
</tr>
<tr id="row0370549162119"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p128281598548"><a name="p128281598548"></a><a name="p128281598548"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p118271359115410"><a name="p118271359115410"></a><a name="p118271359115410"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p682665918549"><a name="p682665918549"></a><a name="p682665918549"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表168](数据结构.md#table720016262237)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "items": [
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
    ],
    "kind": "TFJobList",
    "metadata": {
        "continue": "",
        "resourceVersion": "72353810",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/tfjobs"
    }
}
```

## 状态码<a name="zh-cn_topic_0083864910_section16509142112516"></a>

**表 3**  状态码

<a name="zh-cn_topic_0083864910_table6957182913514"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row12961162965119"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0083864910_p189627299518"><a name="zh-cn_topic_0083864910_p189627299518"></a><a name="zh-cn_topic_0083864910_p189627299518"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0083864910_p1596342917515"><a name="zh-cn_topic_0083864910_p1596342917515"></a><a name="zh-cn_topic_0083864910_p1596342917515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1130214385217"><a name="p1130214385217"></a><a name="p1130214385217"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p12302113812216"><a name="p12302113812216"></a><a name="p12302113812216"></a>OK</p>
</td>
</tr>
<tr id="row971529629"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p83021638123"><a name="p83021638123"></a><a name="p83021638123"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1530263818212"><a name="p1530263818212"></a><a name="p1530263818212"></a>Unauthorized</p>
</td>
</tr>
<tr id="row153415323220"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p330216388211"><a name="p330216388211"></a><a name="p330216388211"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p113021238520"><a name="p113021238520"></a><a name="p113021238520"></a>Not found</p>
</td>
</tr>
<tr id="row466313341722"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1930263815217"><a name="p1930263815217"></a><a name="p1930263815217"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1430213385215"><a name="p1430213385215"></a><a name="p1430213385215"></a>Internal error</p>
</td>
</tr>
</tbody>
</table>

