# 更新MXJob<a name="cci_02_3156"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

更新MXJob。如下字段可被更新：

-   metadata.labels
-   metadata.annotations
-   spec.activeDeadlineSeconds
-   spec.ttlSecondsAfterFinished
-   spec.cleanPodPolicy

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

PATCH /apis/kubeflow.org/v1/namespaces/\{namespace\}/mxjobs/\{name\}

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
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p234564210556"><a name="p234564210556"></a><a name="p234564210556"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p834171714492"><a name="p834171714492"></a><a name="p834171714492"></a>name of the MXJob</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row136701220114011"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p113531734914"><a name="p113531734914"></a><a name="p113531734914"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p113536423558"><a name="p113536423558"></a><a name="p113536423558"></a>Yes</p>
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

响应参数的详细描述请参见[表162](数据结构.md#table65611161418)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "MXJob",
    "metadata": {
        "creationTimestamp": "2019-07-24T08:58:47Z",
        "generation": 1,
        "labels": {
            "app": "test"
        },
        "name": "mxnet-job",
        "namespace": "kube-test",
        "resourceVersion": "72482855",
        "selfLink": "/apis/kubeflow.org/v1/namespaces/kube-test/mxjobs/mxnet-job",
        "uid": "3f304b53-adf1-11e9-8041-340a9837e2a7"
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
                "lastTransitionTime": "2019-07-24T08:58:47Z",
                "lastUpdateTime": "2019-07-24T08:58:47Z",
                "message": "MXJob mxnet-job is created.",
                "reason": "MXJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-24T08:58:47Z",
                "lastUpdateTime": "2019-07-24T08:58:52Z",
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
        "startTime": "2019-07-24T08:58:47Z"
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
<tbody><tr id="zh-cn_topic_0083864910_row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p548235661415"><a name="p548235661415"></a><a name="p548235661415"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p114825561148"><a name="p114825561148"></a><a name="p114825561148"></a>OK</p>
</td>
</tr>
<tr id="row424110353336"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p18482756161413"><a name="p18482756161413"></a><a name="p18482756161413"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1048216569140"><a name="p1048216569140"></a><a name="p1048216569140"></a>Unauthorized</p>
</td>
</tr>
<tr id="row11188123823316"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p0482125613143"><a name="p0482125613143"></a><a name="p0482125613143"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1948225671418"><a name="p1948225671418"></a><a name="p1948225671418"></a>Internal Error</p>
</td>
</tr>
<tr id="row141041241183313"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p17482165661414"><a name="p17482165661414"></a><a name="p17482165661414"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p74828564141"><a name="p74828564141"></a><a name="p74828564141"></a>Forbidden</p>
</td>
</tr>
<tr id="row152631533123317"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1248217566142"><a name="p1248217566142"></a><a name="p1248217566142"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p048265621410"><a name="p048265621410"></a><a name="p048265621410"></a>Conflict</p>
</td>
</tr>
<tr id="row158073163310"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p184821356161410"><a name="p184821356161410"></a><a name="p184821356161410"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8482155691413"><a name="p8482155691413"></a><a name="p8482155691413"></a>BadRequest</p>
</td>
</tr>
</tbody>
</table>

