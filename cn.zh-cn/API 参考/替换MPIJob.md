# 替换MPIJob<a name="cci_02_3177"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

替换MPIJob。如下字段可被替换：

-   metadata.labels
-   metadata.annotations
-   spec.activeDeadlineSeconds
-   spec.cleanPodPolicy

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

PUT /apis/kubeflow.org/v1alpha2/namespaces/\{namespace\}/mpijobs/\{name\}

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
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p1734317114912"><a name="p1734317114912"></a><a name="p1734317114912"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p834171714492"><a name="p834171714492"></a><a name="p834171714492"></a>name of the MPIJob</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row136701220114011"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p113531734914"><a name="p113531734914"></a><a name="p113531734914"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p1635151712493"><a name="p1635151712493"></a><a name="p1635151712493"></a>Yes</p>
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

## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

**请求参数**：

请求参数的详细描述请参见[表170](数据结构.md#table23131833144416)。

**请求示例：**

更改MPIJob的结束存活时间cleanPodPolicy：

```
{
    "apiVersion": "kubeflow.org/v1alpha2",
    "kind": "MPIJob",
    "metadata": {
        "creationTimestamp": "2019-07-29T03:27:49Z",
        "generation": 2,
        "labels": {
            "app": "test"
        },
        "name": "mpi-test",
        "namespace": "kube-test",
        "resourceVersion": "75613585",
        "selfLink": "/apis/kubeflow.org/v1alpha2/namespaces/kube-test/mpijobs/mpi-test",
        "uid": "d72c3331-b1b0-11e9-8d90-340a9837e413"
    },
    "spec": {
        "cleanPodPolicy": "Running",
        "mpiReplicaSpecs": {
            "Launcher": {
                "replicas": 1,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "-c",
                                    "mpirun --allow-run-as-root python mxnet_mnist.py --batch-size 32 --no-cuda --epoch 1"
                                ],
                                "command": [
                                    "/bin/bash"
                                ],
                                "image": "100.79.1.215:20202/paas_cci_w00427225/horovod-mxnet:mnist",
                                "name": "mpi",
                                "resources": {
                                    "limits": {
                                        "cpu": 1,
                                        "memory": "2Gi"
                                    },
                                    "requests": {
                                        "cpu": 1,
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
                "replicas": 2,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "image": "100.79.1.215:20202/paas_cci_w00427225/horovod-mxnet:mnist",
                                "name": "mpi",
                                "resources": {
                                    "limits": {
                                        "cpu": 1,
                                        "memory": "2Gi"
                                    },
                                    "requests": {
                                        "cpu": 1,
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
        },
        "slotsPerWorker": 1
    },
    "status": {
        "completionTime": "2019-07-29T03:30:24Z",
        "conditions": [
            {
                "lastTransitionTime": "2019-07-29T03:27:03Z",
                "lastUpdateTime": "2019-07-29T03:27:03Z",
                "message": "MPIJob kube-test/mpi-test is created.",
                "reason": "MPIJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-29T03:27:16Z",
                "lastUpdateTime": "2019-07-29T03:27:16Z",
                "message": "MPIJob kube-test/mpi-test is running.",
                "reason": "MPIJobRunning",
                "status": "False",
                "type": "Running"
            },
            {
                "lastTransitionTime": "2019-07-29T03:30:24Z",
                "lastUpdateTime": "2019-07-29T03:30:24Z",
                "message": "MPIJob kube-test/mpi-test successfully completed.",
                "reason": "MPIJobSucceeded",
                "status": "True",
                "type": "Succeeded"
            }
        ],
        "replicaStatuses": {
            "Launcher": {
                "succeeded": 1
            },
            "Worker": {}
        },
        "startTime": "2019-07-29T03:27:03Z"
    }
}
```

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表170](数据结构.md#table23131833144416)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1alpha2",
    "kind": "MPIJob",
    "metadata": {
        "creationTimestamp": "2019-07-29T03:27:49Z",
        "generation": 2,
        "labels": {
            "app": "test"
        },
        "name": "mpi-test",
        "namespace": "kube-test",
        "resourceVersion": "75613585",
        "selfLink": "/apis/kubeflow.org/v1alpha2/namespaces/kube-test/mpijobs/mpi-test",
        "uid": "d72c3331-b1b0-11e9-8d90-340a9837e413"
    },
    "spec": {
        "cleanPodPolicy": "Running",
        "mpiReplicaSpecs": {
            "Launcher": {
                "replicas": 1,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "args": [
                                    "-c",
                                    "mpirun --allow-run-as-root python mxnet_mnist.py --batch-size 32 --no-cuda --epoch 1"
                                ],
                                "command": [
                                    "/bin/bash"
                                ],
                                "image": "100.79.1.215:20202/paas_cci_w00427225/horovod-mxnet:mnist",
                                "name": "mpi",
                                "resources": {
                                    "limits": {
                                        "cpu": 1,
                                        "memory": "2Gi"
                                    },
                                    "requests": {
                                        "cpu": 1,
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
                "replicas": 2,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "image": "100.79.1.215:20202/paas_cci_w00427225/horovod-mxnet:mnist",
                                "name": "mpi",
                                "resources": {
                                    "limits": {
                                        "cpu": 1,
                                        "memory": "2Gi"
                                    },
                                    "requests": {
                                        "cpu": 1,
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
        },
        "slotsPerWorker": 1
    },
    "status": {
        "completionTime": "2019-07-29T03:30:24Z",
        "conditions": [
            {
                "lastTransitionTime": "2019-07-29T03:27:03Z",
                "lastUpdateTime": "2019-07-29T03:27:03Z",
                "message": "MPIJob kube-test/mpi-test is created.",
                "reason": "MPIJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-29T03:27:16Z",
                "lastUpdateTime": "2019-07-29T03:27:16Z",
                "message": "MPIJob kube-test/mpi-test is running.",
                "reason": "MPIJobRunning",
                "status": "False",
                "type": "Running"
            },
            {
                "lastTransitionTime": "2019-07-29T03:30:24Z",
                "lastUpdateTime": "2019-07-29T03:30:24Z",
                "message": "MPIJob kube-test/mpi-test successfully completed.",
                "reason": "MPIJobSucceeded",
                "status": "True",
                "type": "Succeeded"
            }
        ],
        "replicaStatuses": {
            "Launcher": {
                "succeeded": 1
            },
            "Worker": {}
        },
        "startTime": "2019-07-29T03:27:03Z"
    }
}
```

## 状态码<a name="zh-cn_topic_0083864910_section16509142112516"></a>

**表 3**  状态码

<a name="table76801012163815"></a>
<table><thead align="left"><tr id="row166182493817"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0083864910_p189627299518"><a name="zh-cn_topic_0083864910_p189627299518"></a><a name="zh-cn_topic_0083864910_p189627299518"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0083864910_p1596342917515"><a name="zh-cn_topic_0083864910_p1596342917515"></a><a name="zh-cn_topic_0083864910_p1596342917515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13777151217387"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p8777131243816"><a name="p8777131243816"></a><a name="p8777131243816"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p87771612203811"><a name="p87771612203811"></a><a name="p87771612203811"></a>OK</p>
</td>
</tr>
<tr id="row1377711263815"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p15777161233811"><a name="p15777161233811"></a><a name="p15777161233811"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p977711217385"><a name="p977711217385"></a><a name="p977711217385"></a>Created</p>
</td>
</tr>
<tr id="row127776122381"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p6777121283812"><a name="p6777121283812"></a><a name="p6777121283812"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p17777121219387"><a name="p17777121219387"></a><a name="p17777121219387"></a>Unauthorized</p>
</td>
</tr>
<tr id="row7777131253811"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p10777141253817"><a name="p10777141253817"></a><a name="p10777141253817"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p577717125387"><a name="p577717125387"></a><a name="p577717125387"></a>BadRequest</p>
</td>
</tr>
<tr id="row1277771211389"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p9777171218387"><a name="p9777171218387"></a><a name="p9777171218387"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1777512153810"><a name="p1777512153810"></a><a name="p1777512153810"></a>Internal Error</p>
</td>
</tr>
<tr id="row1477719124386"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p187776127381"><a name="p187776127381"></a><a name="p187776127381"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9777151283817"><a name="p9777151283817"></a><a name="p9777151283817"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

