# 查询所有ReplicaSets<a name="cci_02_3128"></a>

## 功能介绍<a name="section19030251"></a>

查询命名空间下所有的ReplicaSets

## URI<a name="section37054533"></a>

GET /apis/apps/v1/namespaces/\{namespace\}/replicasets

**表 1**  Path参数

<a name="d0e45179"></a>
<table><thead align="left"><tr id="row64943380"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.318368163183685%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.273672632736734%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row61989525"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p55095590"><a name="p55095590"></a><a name="p55095590"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p33557800"><a name="p33557800"></a><a name="p33557800"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p33827266"><a name="p33827266"></a><a name="p33827266"></a>Object name and auth scope, such as for teams and projects.</p>
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
<tbody><tr id="row10334449142116"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p2337114918211"><a name="p2337114918211"></a><a name="p2337114918211"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p133375498219"><a name="p133375498219"></a><a name="p133375498219"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p133911495210"><a name="p133911495210"></a><a name="p133911495210"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row13340949102114"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p103421492216"><a name="p103421492216"></a><a name="p103421492216"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p203445494217"><a name="p203445494217"></a><a name="p203445494217"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p14346104915219"><a name="p14346104915219"></a><a name="p14346104915219"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row1934684942112"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p15349164912212"><a name="p15349164912212"></a><a name="p15349164912212"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1034919496213"><a name="p1034919496213"></a><a name="p1034919496213"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p035124962111"><a name="p035124962111"></a><a name="p035124962111"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row1235224982117"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p16355749182117"><a name="p16355749182117"></a><a name="p16355749182117"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p16357124992115"><a name="p16357124992115"></a><a name="p16357124992115"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p5359449182111"><a name="p5359449182111"></a><a name="p5359449182111"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row6360204912217"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p193631549102114"><a name="p193631549102114"></a><a name="p193631549102114"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p3366154911216"><a name="p3366154911216"></a><a name="p3366154911216"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p636854916215"><a name="p636854916215"></a><a name="p636854916215"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="row0370549162119"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p13372749142111"><a name="p13372749142111"></a><a name="p13372749142111"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p837604932111"><a name="p837604932111"></a><a name="p837604932111"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p9376184917213"><a name="p9376184917213"></a><a name="p9376184917213"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row037764911210"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p138014492216"><a name="p138014492216"></a><a name="p138014492216"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p438111490219"><a name="p438111490219"></a><a name="p438111490219"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p63837493219"><a name="p63837493219"></a><a name="p63837493219"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section65055348"></a>

N/A

## 响应消息<a name="section48627224"></a>

**响应参数：**

响应参数的详细描述请参见[表144](数据结构.md#table1272015014015)。

**响应示例**：

```
{
    "kind": "ReplicaSetList",
    "apiVersion": "apps/v1",
    "metadata": {
        "selfLink": "/apis/apps/v1/namespaces/default/replicasets",
        "resourceVersion": "793174"
    },
    "items": [
        {
            "metadata": {
                "name": "deployment-test-800400086",
                "namespace": "default",
                "selfLink": "/apis/extensions/v1beta1/namespaces/default/replicasets/deployment-test-800400086",
                "uid": "67775454-df2f-11e7-961f-fa163ed139d5",
                "resourceVersion": "784294",
                "generation": 1,
                "creationTimestamp": "2017-12-12T11:27:15Z",
                "labels": {
                    "name": "deployment-test",
                    "pod-template-hash": "800400086"
                },
                "annotations": {
                    "deployment.kubernetes.io/desired-replicas": "1",
                    "deployment.kubernetes.io/max-replicas": "2",
                    "deployment.kubernetes.io/revision": "1"
                },
                "ownerReferences": [
                    {
                        "apiVersion": "extensions/v1beta1",
                        "kind": "Deployment",
                        "name": "deployment-test",
                        "uid": "6776d16b-df2f-11e7-961f-fa163ed139d5",
                        "controller": true,
                        "blockOwnerDeletion": true
                    }
                ],
                "enable": true
            },
            "spec": {
                "replicas": 1,
                "selector": {
                    "matchLabels": {
                        "name": "deployment-test",
                        "pod-template-hash": "800400086"
                    }
                },
                "template": {
                    "metadata": {
                        "creationTimestamp": null,
                        "labels": {
                            "name": "deployment-test",
                            "pod-template-hash": "800400086"
                        },
                        "enable": true
                    },
                    "spec": {
                        "containers": [
                            {
                                "name": "deployment-test",
                                "image": "172.16.5.235:20202/test/testnginx:v3",
                                "resources": {},
                                "terminationMessagePath": "/dev/termination-log",
                                "terminationMessagePolicy": "File",
                                "imagePullPolicy": "IfNotPresent"
                            }
                        ],
                        "restartPolicy": "Always",
                        "terminationGracePeriodSeconds": 30,
                        "dnsPolicy": "ClusterFirst",
                        "securityContext": {},
                        "schedulerName": "default-scheduler"
                    }
                }
            },
            "status": {
                "replicas": 1,
                "fullyLabeledReplicas": 1,
                "observedGeneration": 1
            }
        },
        {
            "metadata": {
                "name": "test-pv-446136006",
                "namespace": "default",
                "selfLink": "/apis/extensions/v1beta1/namespaces/default/replicasets/test-pv-446136006",
                "uid": "3b3dee35-dfd7-11e7-961f-fa163ed139d5",
                "resourceVersion": "784441",
                "generation": 1,
                "creationTimestamp": "2017-12-13T07:28:36Z",
                "labels": {
                    "app": "test-pv",
                    "pod-template-hash": "446136006"
                },
                "annotations": {
                    "deployment.kubernetes.io/desired-replicas": "2",
                    "deployment.kubernetes.io/max-replicas": "2",
                    "deployment.kubernetes.io/revision": "1"
                },
                "ownerReferences": [
                    {
                        "apiVersion": "extensions/v1beta1",
                        "kind": "Deployment",
                        "name": "test-pv",
                        "uid": "3b3d3a22-dfd7-11e7-961f-fa163ed139d5",
                        "controller": true,
                        "blockOwnerDeletion": true
                    }
                ],
                "enable": true
            },
            "spec": {
                "replicas": 2,
                "selector": {
                    "matchLabels": {
                        "app": "test-pv",
                        "pod-template-hash": "446136006"
                    }
                },
                "template": {
                    "metadata": {
                        "creationTimestamp": null,
                        "labels": {
                            "app": "test-pv",
                            "pod-template-hash": "446136006"
                        },
                        "annotations": {
                            "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]"
                        },
                        "enable": true
                    },
                    "spec": {
                        "volumes": [
                            {
                                "name": "wwww",
                                "persistentVolumeClaim": {
                                    "claimName": "pvc1513149915389"
                                }
                            }
                        ],
                        "containers": [
                            {
                                "name": "container-0",
                                "image": "172.16.5.235:20202/test/nginx:latest",
                                "resources": {},
                                "volumeMounts": [
                                    {
                                        "name": "wwww",
                                        "readOnly": true,
                                        "mountPath": "/tmp0"
                                    }
                                ],
                                "lifecycle": {},
                                "terminationMessagePath": "/dev/termination-log",
                                "terminationMessagePolicy": "File",
                                "imagePullPolicy": "Always"
                            }
                        ],
                        "restartPolicy": "Always",
                        "terminationGracePeriodSeconds": 30,
                        "dnsPolicy": "ClusterFirst",
                        "securityContext": {},
                        "imagePullSecrets": [
                            {
                                "name": "default-secret"
                            }
                        ],
                        "affinity": {},
                        "schedulerName": "default-scheduler"
                    }
                }
            },
            "status": {
                "replicas": 2,
                "fullyLabeledReplicas": 2,
                "readyReplicas": 2,
                "availableReplicas": 2,
                "observedGeneration": 1
            }
        }
    ]
}
```

## 状态码<a name="section34991834"></a>

**表 3**  状态码

<a name="d0e45308"></a>
<table><thead align="left"><tr id="row6630185"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p174074"><a name="p174074"></a><a name="p174074"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p14100028"><a name="p14100028"></a><a name="p14100028"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1251606"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p34271281"><a name="p34271281"></a><a name="p34271281"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p24510389"><a name="p24510389"></a><a name="p24510389"></a>This operation succeeds, and a ReplicaSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

