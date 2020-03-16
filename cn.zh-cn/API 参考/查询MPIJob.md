# 查询MPIJob<a name="cci_02_3172"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

查询MPIJob的详细信息。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

GET /apis/kubeflow.org/v1alpha2/namespaces/\{namespace\}/mpijobs/\{name\}

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
<tbody><tr id="zh-cn_topic_0083864910_row1670122004014"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p1834011925520"><a name="p1834011925520"></a><a name="p1834011925520"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p568363455610"><a name="p568363455610"></a><a name="p568363455610"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p143381019155512"><a name="p143381019155512"></a><a name="p143381019155512"></a>name of the MPIJob</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row136701220114011"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p2541201454120"><a name="p2541201454120"></a><a name="p2541201454120"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p1868743414568"><a name="p1868743414568"></a><a name="p1868743414568"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p165414146415"><a name="p165414146415"></a><a name="p165414146415"></a>object name and auth scope, such as for teams and projects</p>
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
<tbody><tr id="row10334449142116"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p883818599545"><a name="p883818599545"></a><a name="p883818599545"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p283845919544"><a name="p283845919544"></a><a name="p283845919544"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p19837859165418"><a name="p19837859165418"></a><a name="p19837859165418"></a>If 'true’, then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表171](数据结构.md#table23131833144416)。

**响应示例：**

```
{
    "apiVersion": "kubeflow.org/v1alpha2",
    "kind": "MPIJob",
    "metadata": {
        "creationTimestamp": "2019-07-29T03:05:59Z",
        "generation": 1,
        "name": "mpi-test",
        "namespace": "kube-test",
        "resourceVersion": "75602217",
        "selfLink": "/apis/kubeflow.org/v1alpha2/namespaces/kube-test/mpijobs/mpi-test",
        "uid": "ca55275f-b1ad-11e9-b7c9-340a9837e2a7"
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
        "conditions": [
            {
                "lastTransitionTime": "2019-07-29T03:05:59Z",
                "lastUpdateTime": "2019-07-29T03:05:59Z",
                "message": "MPIJob kube-test/mpi-test is created.",
                "reason": "MPIJobCreated",
                "status": "True",
                "type": "Created"
            },
            {
                "lastTransitionTime": "2019-07-29T03:06:24Z",
                "lastUpdateTime": "2019-07-29T03:06:24Z",
                "message": "MPIJob kube-test/mpi-test is running.",
                "reason": "MPIJobRunning",
                "status": "True",
                "type": "Running"
            }
        ],
        "replicaStatuses": {
            "Launcher": {
                "active": 1
            },
            "Worker": {
                "active": 2
            }
        },
        "startTime": "2019-07-29T03:05:59Z"
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
<tbody><tr id="row187671830658"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1367711985419"><a name="p1367711985419"></a><a name="p1367711985419"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1767541915544"><a name="p1767541915544"></a><a name="p1767541915544"></a>OK</p>
</td>
</tr>
<tr id="row197671730650"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1850718294311"><a name="p1850718294311"></a><a name="p1850718294311"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1350717216431"><a name="p1350717216431"></a><a name="p1350717216431"></a>Unauthorized</p>
</td>
</tr>
<tr id="row17674305511"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1657775011315"><a name="p1657775011315"></a><a name="p1657775011315"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p15577750123113"><a name="p15577750123113"></a><a name="p15577750123113"></a>Not found</p>
</td>
</tr>
<tr id="row07673303516"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5328175573120"><a name="p5328175573120"></a><a name="p5328175573120"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p183291755193118"><a name="p183291755193118"></a><a name="p183291755193118"></a>Internal error</p>
</td>
</tr>
<tr id="row676617302511"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p10659425153815"><a name="p10659425153815"></a><a name="p10659425153815"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p19659825203817"><a name="p19659825203817"></a><a name="p19659825203817"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

