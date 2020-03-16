# 创建MPIJob<a name="cci_02_3171"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

创建MPIJob。

MPIJob即MPI任务，是基于allreduce架构的kubernetes自定义资源类型，能够帮助我们更简单地实现allreduce的分布式训练。MPI开源框架的信息详见：[https://www.open-mpi.org/](https://www.open-mpi.org/)。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

POST /apis/kubeflow.org/v1alpha2/namespaces/\{namespace\}/mpijobs

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
<tbody><tr id="zh-cn_topic_0083864910_row1670122004014"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p10593162912503"><a name="p10593162912503"></a><a name="p10593162912503"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p145911629115011"><a name="p145911629115011"></a><a name="p145911629115011"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p19590192910505"><a name="p19590192910505"></a><a name="p19590192910505"></a>object name and auth scope, such as for teams and projects</p>
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

请求参数的详细描述请参见[表171](数据结构.md#table23131833144416)。

**请求示例：**

```
{
    "apiVersion": "kubeflow.org/v1alpha2",
    "kind": "MPIJob",
    "metadata": {
        "name": "mpi-test"
    },
    "spec": {
        "cleanPodPolicy": "All",
        "slotsPerWorker": 1,
        "mpiReplicaSpecs": {
            "Launcher": {
                "replicas": 1,
                "template": {
                    "spec": {
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "containers": [
                            {
                                "image": "*.*.*.215:20202/cci/horovod-mxnet:mnist",
                                "command": [
                                    "/bin/bash"
                                ],
                                "args": [
                                    "-c",
                                    "mpirun --allow-run-as-root python mxnet_mnist.py --batch-size 32 --no-cuda --epoch 1"
                                ],
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
                        ]
                    }
                }
            },
            "Worker": {
                "replicas": 2,
                "template": {
                    "spec": {
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "containers": [
                            {
                                "image": "*.*.*.215:20202/cci/horovod-mxnet:mnist",
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

响应参数的详细描述请参见[表171](数据结构.md#table23131833144416)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1alpha2",
    "kind": "MPIJob",
    "metadata": {
        "creationTimestamp": "2019-07-24T11:07:16Z",
        "generation": 1,
        "name": "mpi-test",
        "namespace": "kube-test",
        "resourceVersion": "72530790",
        "selfLink": "/apis/kubeflow.org/v1alpha2/namespaces/kube-test/mpijobs/mpi-test",
        "uid": "32a808c5-ae03-11e9-aaa4-340a9837e413"
    },
    "spec": {
        "cleanPodPolicy": "All",
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
                                "image": "*.*.*.215:20202/cci/horovod-mxnet:mnist",
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
                                "image": "*.*.*.215:20202/cci/horovod-mxnet:mnist",
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
<tbody><tr id="zh-cn_topic_0083864910_row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1367711985419"><a name="p1367711985419"></a><a name="p1367711985419"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1767541915544"><a name="p1767541915544"></a><a name="p1767541915544"></a>OK</p>
</td>
</tr>
<tr id="row19391645125517"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p47871755163319"><a name="p47871755163319"></a><a name="p47871755163319"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1787955113318"><a name="p1787955113318"></a><a name="p1787955113318"></a>Created</p>
</td>
</tr>
<tr id="row1627435314555"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1876246203420"><a name="p1876246203420"></a><a name="p1876246203420"></a>202</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p77622693411"><a name="p77622693411"></a><a name="p77622693411"></a>Accepted</p>
</td>
</tr>
<tr id="row18202157175518"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p14949421183410"><a name="p14949421183410"></a><a name="p14949421183410"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1794922133417"><a name="p1794922133417"></a><a name="p1794922133417"></a>Unauthorized</p>
</td>
</tr>
<tr id="row197342000566"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1777215672810"><a name="p1777215672810"></a><a name="p1777215672810"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1877275619281"><a name="p1877275619281"></a><a name="p1877275619281"></a>Badrequest</p>
</td>
</tr>
<tr id="row858313205613"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p114411511294"><a name="p114411511294"></a><a name="p114411511294"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8144175192919"><a name="p8144175192919"></a><a name="p8144175192919"></a>Internal error</p>
</td>
</tr>
<tr id="row198381911567"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p520911524449"><a name="p520911524449"></a><a name="p520911524449"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p32096525448"><a name="p32096525448"></a><a name="p32096525448"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

