# 查询所有StatefulSet<a name="cci_02_0041"></a>

## 功能介绍<a name="zh-cn_topic_0091433694_section55184758"></a>

This API is used to list all StatefulSet resource objects under a specified Namespace.

## URI<a name="zh-cn_topic_0091433694_section26900781"></a>

GET /apis/apps/v1beta1/namespaces/\{namespace\}/statefulsets

[表1](#zh-cn_topic_0091433694_d0e39332)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433694_d0e39332"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433694_row16249415"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433694_p65652297517"><a name="zh-cn_topic_0091433694_p65652297517"></a><a name="zh-cn_topic_0091433694_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433694_p165661629135114"><a name="zh-cn_topic_0091433694_p165661629135114"></a><a name="zh-cn_topic_0091433694_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.26367363263674%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433694_p14567629115114"><a name="zh-cn_topic_0091433694_p14567629115114"></a><a name="zh-cn_topic_0091433694_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433694_row33792834"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p52865065"><a name="zh-cn_topic_0091433694_p52865065"></a><a name="zh-cn_topic_0091433694_p52865065"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p54211835"><a name="zh-cn_topic_0091433694_p54211835"></a><a name="zh-cn_topic_0091433694_p54211835"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433694_row60416185"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p61872826"><a name="zh-cn_topic_0091433694_p61872826"></a><a name="zh-cn_topic_0091433694_p61872826"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p45643011"><a name="zh-cn_topic_0091433694_p45643011"></a><a name="zh-cn_topic_0091433694_p45643011"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433694_p6096445"><a name="zh-cn_topic_0091433694_p6096445"></a><a name="zh-cn_topic_0091433694_p6096445"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433694_row54868012"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p15123986"><a name="zh-cn_topic_0091433694_p15123986"></a><a name="zh-cn_topic_0091433694_p15123986"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p17083324"><a name="zh-cn_topic_0091433694_p17083324"></a><a name="zh-cn_topic_0091433694_p17083324"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433694_p41571986"><a name="zh-cn_topic_0091433694_p41571986"></a><a name="zh-cn_topic_0091433694_p41571986"></a></p>
<p id="zh-cn_topic_0091433694_p38603562"><a name="zh-cn_topic_0091433694_p38603562"></a><a name="zh-cn_topic_0091433694_p38603562"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433694_row11887742"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p23383013"><a name="zh-cn_topic_0091433694_p23383013"></a><a name="zh-cn_topic_0091433694_p23383013"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p14975921"><a name="zh-cn_topic_0091433694_p14975921"></a><a name="zh-cn_topic_0091433694_p14975921"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433694_p5090122"><a name="zh-cn_topic_0091433694_p5090122"></a><a name="zh-cn_topic_0091433694_p5090122"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433694_row45811103"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p19711829"><a name="zh-cn_topic_0091433694_p19711829"></a><a name="zh-cn_topic_0091433694_p19711829"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p53154316"><a name="zh-cn_topic_0091433694_p53154316"></a><a name="zh-cn_topic_0091433694_p53154316"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433694_p10532331"><a name="zh-cn_topic_0091433694_p10532331"></a><a name="zh-cn_topic_0091433694_p10532331"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433694_row27682122"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p27659385"><a name="zh-cn_topic_0091433694_p27659385"></a><a name="zh-cn_topic_0091433694_p27659385"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p25817701"><a name="zh-cn_topic_0091433694_p25817701"></a><a name="zh-cn_topic_0091433694_p25817701"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433694_p10858997"><a name="zh-cn_topic_0091433694_p10858997"></a><a name="zh-cn_topic_0091433694_p10858997"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433694_row30622110"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p64471840"><a name="zh-cn_topic_0091433694_p64471840"></a><a name="zh-cn_topic_0091433694_p64471840"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p54836538"><a name="zh-cn_topic_0091433694_p54836538"></a><a name="zh-cn_topic_0091433694_p54836538"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433694_p12574613"><a name="zh-cn_topic_0091433694_p12574613"></a><a name="zh-cn_topic_0091433694_p12574613"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433694_row46062658"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433694_p40087841"><a name="zh-cn_topic_0091433694_p40087841"></a><a name="zh-cn_topic_0091433694_p40087841"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433694_p25889684"><a name="zh-cn_topic_0091433694_p25889684"></a><a name="zh-cn_topic_0091433694_p25889684"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433694_p16689668"><a name="zh-cn_topic_0091433694_p16689668"></a><a name="zh-cn_topic_0091433694_p16689668"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433694_section40780438"></a>

N/A

## 响应消息<a name="zh-cn_topic_0091433694_section31479628"></a>

**响应参数：**

响应参数如[表2](#table1047518519551)所示。

**表 2**  参数解释

<a name="table1047518519551"></a>
<table><thead align="left"><tr id="row174803514555"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p1848145113557"><a name="p1848145113557"></a><a name="p1848145113557"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="p548285117556"><a name="p548285117556"></a><a name="p548285117556"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="61.62%" id="mcps1.2.4.1.3"><p id="p114831051115519"><a name="p114831051115519"></a><a name="p114831051115519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1748555110551"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p164862515556"><a name="p164862515556"></a><a name="p164862515556"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p8488125113553"><a name="p8488125113553"></a><a name="p8488125113553"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p47800291226"><a name="p47800291226"></a><a name="p47800291226"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
</td>
</tr>
<tr id="row648925119558"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1249019517555"><a name="p1249019517555"></a><a name="p1249019517555"></a>items</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p1549165135519"><a name="p1549165135519"></a><a name="p1549165135519"></a><a href="创建StatefulSet（v1beta1）.md#zh-cn_topic_0091433687_d0e37568">表2</a> array</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p2076743510211"><a name="p2076743510211"></a><a name="p2076743510211"></a>List of services</p>
</td>
</tr>
<tr id="row164935510551"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p5494145175517"><a name="p5494145175517"></a><a name="p5494145175517"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p64957519552"><a name="p64957519552"></a><a name="p64957519552"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p8647944422"><a name="p8647944422"></a><a name="p8647944422"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase.</p>
</td>
</tr>
<tr id="row174981651165519"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1850045165517"><a name="p1850045165517"></a><a name="p1850045165517"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p54849240"><a name="zh-cn_topic_0079614912_p54849240"></a><a name="zh-cn_topic_0079614912_p54849240"></a><a href="请求数据结构（废弃）.md#zh-cn_topic_0083857342_tfec585109f8845e287eebb730ed9214e">表15</a></p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p1170818516218"><a name="p1170818516218"></a><a name="p1170818516218"></a>Standard list metadata.</p>
</td>
</tr>
</tbody>
</table>

**响应示例：**

```
{
    "kind": "StatefulSetList", 
    "apiVersion": "apps/v1beta1", 
    "metadata": {
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/statefulsets", 
        "resourceVersion": "4510960"
    }, 
    "items": [
        {
            "metadata": {
                "name": "statefulset-test", 
                "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
                "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/statefulsets/statefulset-test", 
                "uid": "ee0ef0d0-2728-11e8-8930-84a9c46e8ca3", 
                "resourceVersion": "4510960", 
                "generation": 2, 
                "creationTimestamp": "2018-03-14T01:42:18Z", 
                "labels": {
                    "appgroup": ""
                }, 
                "annotations": {
                    "description": ""
                }, 
                "enable": true
            }, 
            "spec": {
                "replicas": 2, 
                "selector": {
                    "matchLabels": {
                        "app": "statefulset-test"
                    }
                }, 
                "template": {
                    "metadata": {
                        "creationTimestamp": null, 
                        "labels": {
                            "app": "statefulset-test"
                        }, 
                        "annotations": {
                            "com.huawei.scheduler/container-type": "secure-container", 
                            "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]", 
                            "pod.alpha.kubernetes.io/initialized": "true"
                        }, 
                        "enable": true
                    }, 
                    "spec": {
                        "containers": [
                            {
                                "name": "container-0", 
                                "image": "mysql:latest", 
                                "resources": {
                                    "limits": {
                                        "cpu": "1", 
                                        "memory": "2Gi"
                                    }, 
                                    "requests": {
                                        "cpu": "1", 
                                        "memory": "2Gi"
                                    }
                                }, 
                                "lifecycle": {}, 
                                "terminationMessagePath": "/dev/termination-log", 
                                "terminationMessagePolicy": "File", 
                                "imagePullPolicy": "IfNotPresent"
                            }, 
                            {
                                "name": "container-1", 
                                "image": "nginx:latest", 
                                "resources": {
                                    "limits": {
                                        "cpu": "1", 
                                        "memory": "2Gi"
                                    }, 
                                    "requests": {
                                        "cpu": "1", 
                                        "memory": "2Gi"
                                    }
                                }, 
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
                                "name": "imagepull-secret"
                            }
                        ], 
                        "affinity": {}, 
                        "schedulerName": "default-scheduler"
                    }
                }, 
                "serviceName": "test", 
                "podManagementPolicy": "OrderedReady", 
                "updateStrategy": {
                    "type": "RollingUpdate"
                }, 
                "revisionHistoryLimit": 10
            }, 
            "status": {
                "observedGeneration": 2, 
                "replicas": 1, 
                "currentReplicas": 1, 
                "currentRevision": "statefulset-test-2238135242", 
                "updateRevision": "statefulset-test-4168075007"
            }
        }, 
        {
            "metadata": {
                "name": "test", 
                "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
                "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/statefulsets/test", 
                "uid": "3a03904a-25fb-11e8-a5eb-84a9c46e8c8b", 
                "resourceVersion": "4183808", 
                "generation": 4, 
                "creationTimestamp": "2018-03-12T13:42:37Z", 
                "labels": {
                    "appgroup": ""
                }, 
                "annotations": {
                    "description": ""
                }, 
                "enable": true
            }, 
            "spec": {
                "replicas": 5, 
                "selector": {
                    "matchLabels": {
                        "app": "test"
                    }
                }, 
                "template": {
                    "metadata": {
                        "creationTimestamp": null, 
                        "labels": {
                            "app": "test"
                        }, 
                        "annotations": {
                            "com.huawei.scheduler/container-type": "secure-container", 
                            "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]", 
                            "pod.alpha.kubernetes.io/initialized": "true"
                        }, 
                        "enable": true
                    }, 
                    "spec": {
                        "volumes": [
                            {
                                "name": "ccilocal-mb3osj6m", 
                                "persistentVolumeClaim": {
                                    "claimName": "ccilocal-mb3osj6m"
                                }
                            }, 
                            {
                                "name": "ccilocal-59tbq76l", 
                                "persistentVolumeClaim": {
                                    "claimName": "ccilocal-59tbq76l"
                                }
                            }
                        ], 
                        "containers": [
                            {
                                "name": "container-0", 
                                "image": "nginx:latest", 
                                "resources": {
                                    "limits": {
                                        "cpu": "250m", 
                                        "memory": "214748364800m"
                                    }, 
                                    "requests": {
                                        "cpu": "250m", 
                                        "memory": "214748364800m"
                                    }
                                }, 
                                "volumeMounts": [
                                    {
                                        "name": "ccilocal-mb3osj6m", 
                                        "mountPath": "/tmp/local0"
                                    }, 
                                    {
                                        "name": "ccilocal-59tbq76l", 
                                        "mountPath": "/tmp/local1"
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
                                "name": "imagepull-secret"
                            }
                        ], 
                        "affinity": {}, 
                        "schedulerName": "default-scheduler"
                    }
                }, 
                "volumeClaimTemplates": [
                    {
                        "metadata": {
                            "name": "ccilocal-mb3osj6m", 
                            "creationTimestamp": null, 
                            "enable": true
                        }, 
                        "spec": {
                            "accessModes": [
                                "ReadWriteOnce"
                            ], 
                            "resources": {
                                "requests": {
                                    "storage": "1Gi"
                                }
                            }, 
                            "storageClassName": "localvolumeccihuawei"
                        }, 
                        "status": {
                            "phase": "Pending"
                        }
                    }, 
                    {
                        "metadata": {
                            "name": "ccilocal-59tbq76l", 
                            "creationTimestamp": null, 
                            "enable": true
                        }, 
                        "spec": {
                            "accessModes": [
                                "ReadWriteOnce"
                            ], 
                            "resources": {
                                "requests": {
                                    "storage": "1Gi"
                                }
                            }, 
                            "storageClassName": "localvolumeccihuawei"
                        }, 
                        "status": {
                            "phase": "Pending"
                        }
                    }
                ], 
                "serviceName": "test", 
                "podManagementPolicy": "OrderedReady", 
                "updateStrategy": {
                    "type": "RollingUpdate"
                }, 
                "revisionHistoryLimit": 10
            }, 
            "status": {
                "observedGeneration": 4, 
                "replicas": 5, 
                "readyReplicas": 5, 
                "currentReplicas": 5, 
                "currentRevision": "test-3275405408", 
                "updateRevision": "test-3275405408"
            }
        }
    ]
}
```

## 状态码<a name="zh-cn_topic_0091433694_section14881199"></a>

[表3](#zh-cn_topic_0091433694_d0e39461)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0091433694_d0e39461"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433694_row5459157"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433694_p39538597"><a name="zh-cn_topic_0091433694_p39538597"></a><a name="zh-cn_topic_0091433694_p39538597"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433694_p48509806"><a name="zh-cn_topic_0091433694_p48509806"></a><a name="zh-cn_topic_0091433694_p48509806"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433694_row36980183"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433694_p42604808"><a name="zh-cn_topic_0091433694_p42604808"></a><a name="zh-cn_topic_0091433694_p42604808"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433694_p28437418"><a name="zh-cn_topic_0091433694_p28437418"></a><a name="zh-cn_topic_0091433694_p28437418"></a>This operation succeeds, and a StatefulSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

