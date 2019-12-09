# 创建MXJob<a name="cci_02_3151"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

创建MXJob。

MXJob即MXNet任务，是基于MXNet开源框架的kubernetes自定义资源类型，有多种角色可以配置，能够帮助我们更简单地实现MXNet的训练。MXNet开源框架的信息详见：[https://mxnet.incubator.apache.org/](https://mxnet.incubator.apache.org/)。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

POST /apis/kubeflow.org/v1/namespaces/\{namespace\}/mxjobs

**表 1**  Path参数

<a name="table1759715547356"></a>
<table><thead align="left"><tr id="row185971854133514"><th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.4.1.1"><p id="p9597754123515"><a name="p9597754123515"></a><a name="p9597754123515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.772277227722775%" id="mcps1.2.4.1.2"><p id="p259755419357"><a name="p259755419357"></a><a name="p259755419357"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.4059405940594%" id="mcps1.2.4.1.3"><p id="p1159719545352"><a name="p1159719545352"></a><a name="p1159719545352"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2597175413510"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p20597125418357"><a name="p20597125418357"></a><a name="p20597125418357"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p1659717549353"><a name="p1659717549353"></a><a name="p1659717549353"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p6597354163517"><a name="p6597354163517"></a><a name="p6597354163517"></a>object name and auth scope, such as for teams and projects</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table280134110713"></a>
<table><thead align="left"><tr id="row1781134110713"><th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.4.1.1"><p id="p8811741771"><a name="p8811741771"></a><a name="p8811741771"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.772277227722775%" id="mcps1.2.4.1.2"><p id="p1081114118714"><a name="p1081114118714"></a><a name="p1081114118714"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.4059405940594%" id="mcps1.2.4.1.3"><p id="p188124114716"><a name="p188124114716"></a><a name="p188124114716"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row281641571"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p38112410716"><a name="p38112410716"></a><a name="p38112410716"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p168118411178"><a name="p168118411178"></a><a name="p168118411178"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p1083315596543"><a name="p1083315596543"></a><a name="p1083315596543"></a>If 'true’, then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

**请求参数**：

请求参数的详细描述请参考[表161](数据结构.md#table65611161418)。

**请求示例：**

```
{
    "apiVersion": "kubeflow.org/v1",
    "kind": "MXJob",
    "metadata": {
        "name": "mxnet-job"
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
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "containers": [
                            {
                                "name": "mxnet",
                                "image": "*.*.*.215:20202/cci/mxnet:xsw-dis",
                                "command": [
                                    "/bin/bash"
                                ],
                                "args": [
                                    "-c",
                                    "python train_imagenet.py"
                                ],
                                "resources": {
                                    "requests": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    },
                                    "limits": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    }
                                }
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
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "containers": [
                            {
                                "name": "mxnet",
                                "image": "*.*.*.215:20202/cci/mxnet:xsw-dis",
                                "command": [
                                    "/bin/bash"
                                ],
                                "args": [
                                    "-c",
                                    "python train_imagenet.py"
                                ],
                                "resources": {
                                    "requests": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    },
                                    "limits": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    }
                                }
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
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "containers": [
                            {
                                "name": "mxnet",
                                "image": "*.*.*.215:20202/cci/mxnet:xsw-dis",
                                "command": [
                                    "/bin/bash"
                                ],
                                "args": [
                                    "-c",
                                    "python train_imagenet.py --benchmark 1  --network resnet --batch-size 1 --num-epochs 1 --kv-store dist_sync --num-examples 500"
                                ],
                                "resources": {
                                    "requests": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    },
                                    "limits": {
                                        "cpu": "1000m",
                                        "memory": "2Gi"
                                    }
                                }
                            }
                        ]
                    }
                }
            }
        }
    }
}
```

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参考[表161](数据结构.md#table65611161418)。

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
<tbody><tr id="zh-cn_topic_0083864910_row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p15381416124912"><a name="p15381416124912"></a><a name="p15381416124912"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1438111674913"><a name="p1438111674913"></a><a name="p1438111674913"></a>OK</p>
</td>
</tr>
<tr id="row152711838114813"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p33911694917"><a name="p33911694917"></a><a name="p33911694917"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1139916194913"><a name="p1139916194913"></a><a name="p1139916194913"></a>Created</p>
</td>
</tr>
<tr id="row936015439482"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1639141610491"><a name="p1639141610491"></a><a name="p1639141610491"></a>202</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p43961615495"><a name="p43961615495"></a><a name="p43961615495"></a>Accepted</p>
</td>
</tr>
<tr id="row166911440174818"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p103991604918"><a name="p103991604918"></a><a name="p103991604918"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p103961654915"><a name="p103961654915"></a><a name="p103961654915"></a>Unauthorized</p>
</td>
</tr>
<tr id="row1169811591483"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1039141611491"><a name="p1039141611491"></a><a name="p1039141611491"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p03912162491"><a name="p03912162491"></a><a name="p03912162491"></a>Badrequest</p>
</td>
</tr>
<tr id="row10537134714486"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1139816144917"><a name="p1139816144917"></a><a name="p1139816144917"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p739151614490"><a name="p739151614490"></a><a name="p739151614490"></a>Internal error</p>
</td>
</tr>
<tr id="row9812735174812"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1239181611499"><a name="p1239181611499"></a><a name="p1239181611499"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1739111614914"><a name="p1739111614914"></a><a name="p1739111614914"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

