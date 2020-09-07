# 查询所有Deployment<a name="cci_02_0032"></a>

## 功能介绍<a name="zh-cn_topic_0091433681_section51078739"></a>

This API is used to list all Deployment resource objects under a specified Namespace.

## URI<a name="zh-cn_topic_0091433681_section57055467"></a>

GET /apis/apps/v1beta1/namespaces/\{namespace\}/deployments

[表1](#zh-cn_topic_0091433681_d0e36539)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433681_d0e36539"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433681_row2135501"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433681_p65652297517"><a name="zh-cn_topic_0091433681_p65652297517"></a><a name="zh-cn_topic_0091433681_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433681_p165661629135114"><a name="zh-cn_topic_0091433681_p165661629135114"></a><a name="zh-cn_topic_0091433681_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.62%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433681_p14567629115114"><a name="zh-cn_topic_0091433681_p14567629115114"></a><a name="zh-cn_topic_0091433681_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433681_row59065999"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p19616629"><a name="zh-cn_topic_0091433681_p19616629"></a><a name="zh-cn_topic_0091433681_p19616629"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p45443123"><a name="zh-cn_topic_0091433681_p45443123"></a><a name="zh-cn_topic_0091433681_p45443123"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433681_row43367434"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p23101228"><a name="zh-cn_topic_0091433681_p23101228"></a><a name="zh-cn_topic_0091433681_p23101228"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p59260195"><a name="zh-cn_topic_0091433681_p59260195"></a><a name="zh-cn_topic_0091433681_p59260195"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433681_p35346519"><a name="zh-cn_topic_0091433681_p35346519"></a><a name="zh-cn_topic_0091433681_p35346519"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433681_row49683219"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p64917804"><a name="zh-cn_topic_0091433681_p64917804"></a><a name="zh-cn_topic_0091433681_p64917804"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p23850806"><a name="zh-cn_topic_0091433681_p23850806"></a><a name="zh-cn_topic_0091433681_p23850806"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433681_p52867161"><a name="zh-cn_topic_0091433681_p52867161"></a><a name="zh-cn_topic_0091433681_p52867161"></a></p>
<p id="zh-cn_topic_0091433681_p6042403"><a name="zh-cn_topic_0091433681_p6042403"></a><a name="zh-cn_topic_0091433681_p6042403"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433681_row54381628"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p42835719"><a name="zh-cn_topic_0091433681_p42835719"></a><a name="zh-cn_topic_0091433681_p42835719"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p47141219"><a name="zh-cn_topic_0091433681_p47141219"></a><a name="zh-cn_topic_0091433681_p47141219"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433681_p60342391"><a name="zh-cn_topic_0091433681_p60342391"></a><a name="zh-cn_topic_0091433681_p60342391"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433681_row6210614"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p33297746"><a name="zh-cn_topic_0091433681_p33297746"></a><a name="zh-cn_topic_0091433681_p33297746"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p12762939"><a name="zh-cn_topic_0091433681_p12762939"></a><a name="zh-cn_topic_0091433681_p12762939"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433681_p27165144"><a name="zh-cn_topic_0091433681_p27165144"></a><a name="zh-cn_topic_0091433681_p27165144"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433681_row43159710"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p6275621"><a name="zh-cn_topic_0091433681_p6275621"></a><a name="zh-cn_topic_0091433681_p6275621"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p38563284"><a name="zh-cn_topic_0091433681_p38563284"></a><a name="zh-cn_topic_0091433681_p38563284"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433681_p36618324"><a name="zh-cn_topic_0091433681_p36618324"></a><a name="zh-cn_topic_0091433681_p36618324"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433681_row61129466"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p52539702"><a name="zh-cn_topic_0091433681_p52539702"></a><a name="zh-cn_topic_0091433681_p52539702"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p27857430"><a name="zh-cn_topic_0091433681_p27857430"></a><a name="zh-cn_topic_0091433681_p27857430"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433681_p41859330"><a name="zh-cn_topic_0091433681_p41859330"></a><a name="zh-cn_topic_0091433681_p41859330"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433681_row41189657"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433681_p48027907"><a name="zh-cn_topic_0091433681_p48027907"></a><a name="zh-cn_topic_0091433681_p48027907"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433681_p65055278"><a name="zh-cn_topic_0091433681_p65055278"></a><a name="zh-cn_topic_0091433681_p65055278"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433681_p34986178"><a name="zh-cn_topic_0091433681_p34986178"></a><a name="zh-cn_topic_0091433681_p34986178"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433681_section43737161"></a>

N/A

## 响应消息<a name="zh-cn_topic_0091433681_section58090133"></a>

**响应参数：**

响应参数如[表2](#table1224473545420)所示。

**表 2**  响应参数解释

<a name="table1224473545420"></a>
<table><thead align="left"><tr id="row425573575412"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p132591835115416"><a name="p132591835115416"></a><a name="p132591835115416"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="p162624353549"><a name="p162624353549"></a><a name="p162624353549"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="61.62%" id="mcps1.2.4.1.3"><p id="p1726543565413"><a name="p1726543565413"></a><a name="p1726543565413"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row18268143513548"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1927193513545"><a name="p1927193513545"></a><a name="p1927193513545"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p627543516549"><a name="p627543516549"></a><a name="p627543516549"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p1927983585418"><a name="p1927983585418"></a><a name="p1927983585418"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
</td>
</tr>
<tr id="row3280123545414"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1028373510546"><a name="p1028373510546"></a><a name="p1028373510546"></a>items</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p14286173555419"><a name="p14286173555419"></a><a name="p14286173555419"></a><a href="创建Deployment（v1beta1）.md#zh-cn_topic_0083864910_table12862324102610">表2</a> array</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p1829223515411"><a name="p1829223515411"></a><a name="p1829223515411"></a>List of services</p>
</td>
</tr>
<tr id="row829510355545"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p72971735125418"><a name="p72971735125418"></a><a name="p72971735125418"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p430183516548"><a name="p430183516548"></a><a name="p430183516548"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p193046354543"><a name="p193046354543"></a><a name="p193046354543"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase.</p>
</td>
</tr>
<tr id="row7305335105418"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p43081535175413"><a name="p43081535175413"></a><a name="p43081535175413"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p1531113356548"><a name="p1531113356548"></a><a name="p1531113356548"></a><a href="响应数据结构（废弃）.md#zh-cn_topic_0083857396_zh-cn_topic_0079614930_table66688435">表13</a></p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p631817355548"><a name="p631817355548"></a><a name="p631817355548"></a>Standard list metadata.</p>
</td>
</tr>
</tbody>
</table>

响应示例：

```
{
    "kind": "DeploymentList", 
    "apiVersion": "apps/v1beta1", 
    "metadata": {
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments", 
        "resourceVersion": "4510944"
    }, 
    "items": [
        {
            "metadata": {
                "name": "deployment-test", 
                "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
                "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments/deployment-test", 
                "uid": "ed89a51c-2728-11e8-b891-84a9c46e8c8b", 
                "resourceVersion": "4510944", 
                "generation": 3, 
                "creationTimestamp": "2018-03-14T01:42:17Z", 
                "labels": {
                    "appgroup": ""
                }, 
                "annotations": {
                    "deployment.kubernetes.io/revision": "1", 
                    "description": ""
                }, 
                "enable": true
            }, 
            "spec": {
                "replicas": 1, 
                "selector": {
                    "matchLabels": {
                        "app": "deployment-test"
                    }
                }, 
                "template": {
                    "metadata": {
                        "creationTimestamp": null, 
                        "labels": {
                            "app": "deployment-test"
                        }, 
                        "annotations": {
                            "com.huawei.scheduler/container-type": "secure-container", 
                            "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]"
                        }, 
                        "enable": true
                    }, 
                    "spec": {
                        "containers": [
                            {
                                "name": "container-0", 
                                "image": "nginx:latest", 
                                "resources": {
                                    "limits": {
                                        "cpu": "1", 
                                        "memory": "1024Mi"
                                    }, 
                                    "requests": {
                                        "cpu": "1", 
                                        "memory": "1024Mi"
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
                "strategy": {
                    "type": "RollingUpdate", 
                    "rollingUpdate": {
                        "maxUnavailable": 1, 
                        "maxSurge": 0
                    }
                }, 
                "revisionHistoryLimit": 2, 
                "progressDeadlineSeconds": 600
            }, 
            "status": {
                "observedGeneration": 3, 
                "replicas": 1, 
                "updatedReplicas": 1, 
                "unavailableReplicas": 1, 
                "conditions": [
                    {
                        "type": "Available", 
                        "status": "True", 
                        "lastUpdateTime": "2018-03-14T01:42:17Z", 
                        "lastTransitionTime": "2018-03-14T01:42:17Z", 
                        "reason": "MinimumReplicasAvailable", 
                        "message": "Deployment has minimum availability."
                    }, 
                    {
                        "type": "Progressing", 
                        "status": "True", 
                        "lastUpdateTime": "2018-03-14T01:42:17Z", 
                        "lastTransitionTime": "2018-03-14T01:42:17Z", 
                        "reason": "ReplicaSetUpdated", 
                        "message": "ReplicaSet \"deployment-test-4094680052\" is progressing."
                    }
                ]
            }
        }, 
        {
            "metadata": {
                "name": "ocean", 
                "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
                "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments/ocean", 
                "uid": "f0bdbf83-25d8-11e8-a5eb-84a9c46e8c8b", 
                "resourceVersion": "4145374", 
                "generation": 1, 
                "creationTimestamp": "2018-03-12T09:37:11Z", 
                "labels": {
                    "appgroup": ""
                }, 
                "annotations": {
                    "deployment.kubernetes.io/revision": "1", 
                    "description": ""
                }, 
                "enable": true
            }, 
            "spec": {
                "replicas": 2, 
                "selector": {
                    "matchLabels": {
                        "app": "ocean"
                    }
                }, 
                "template": {
                    "metadata": {
                        "creationTimestamp": null, 
                        "labels": {
                            "app": "ocean"
                        }, 
                        "annotations": {
                            "com.huawei.scheduler/container-type": "secure-container", 
                            "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]"
                        }, 
                        "enable": true
                    }, 
                    "spec": {
                        "containers": [
                            {
                                "name": "container-0", 
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
                "strategy": {
                    "type": "RollingUpdate", 
                    "rollingUpdate": {
                        "maxUnavailable": 1, 
                        "maxSurge": 0
                    }
                }, 
                "revisionHistoryLimit": 2, 
                "progressDeadlineSeconds": 600
            }, 
            "status": {
                "observedGeneration": 1, 
                "replicas": 2, 
                "updatedReplicas": 2, 
                "readyReplicas": 2, 
                "availableReplicas": 2, 
                "conditions": [
                    {
                        "type": "Available", 
                        "status": "True", 
                        "lastUpdateTime": "2018-03-12T09:37:13Z", 
                        "lastTransitionTime": "2018-03-12T09:37:13Z", 
                        "reason": "MinimumReplicasAvailable", 
                        "message": "Deployment has minimum availability."
                    }, 
                    {
                        "type": "Progressing", 
                        "status": "True", 
                        "lastUpdateTime": "2018-03-12T09:37:17Z", 
                        "lastTransitionTime": "2018-03-12T09:37:11Z", 
                        "reason": "NewReplicaSetAvailable", 
                        "message": "ReplicaSet \"ocean-211195136\" has successfully progressed."
                    }
                ]
            }
        }, 
        {
            "metadata": {
                "name": "pzb-test", 
                "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
                "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments/pzb-test", 
                "uid": "198d874c-265e-11e8-b891-84a9c46e8c8b", 
                "resourceVersion": "4312987", 
                "generation": 4, 
                "creationTimestamp": "2018-03-13T01:30:23Z", 
                "labels": {
                    "appgroup": ""
                }, 
                "annotations": {
                    "deployment.kubernetes.io/revision": "2", 
                    "description": "test"
                }, 
                "enable": true
            }, 
            "spec": {
                "replicas": 1, 
                "selector": {
                    "matchLabels": {
                        "app": "pzb-test"
                    }
                }, 
                "template": {
                    "metadata": {
                        "creationTimestamp": null, 
                        "labels": {
                            "app": "pzb-test"
                        }, 
                        "annotations": {
                            "com.huawei.scheduler/container-type": "secure-container", 
                            "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]"
                        }, 
                        "enable": true
                    }, 
                    "spec": {
                        "containers": [
                            {
                                "name": "container-0", 
                                "image": "nginx:latest", 
                                "env": [
                                    {
                                        "name": "cci", 
                                        "value": "test"
                                    }
                                ], 
                                "resources": {
                                    "limits": {
                                        "cpu": "250m", 
                                        "memory": "107374182400m"
                                    }, 
                                    "requests": {
                                        "cpu": "250m", 
                                        "memory": "107374182400m"
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
                "strategy": {
                    "type": "RollingUpdate", 
                    "rollingUpdate": {
                        "maxUnavailable": 1, 
                        "maxSurge": 0
                    }
                }, 
                "revisionHistoryLimit": 2, 
                "progressDeadlineSeconds": 600
            }, 
            "status": {
                "observedGeneration": 4, 
                "replicas": 1, 
                "updatedReplicas": 1, 
                "readyReplicas": 1, 
                "availableReplicas": 1, 
                "conditions": [
                    {
                        "type": "Available", 
                        "status": "True", 
                        "lastUpdateTime": "2018-03-13T02:36:24Z", 
                        "lastTransitionTime": "2018-03-13T02:36:24Z", 
                        "reason": "MinimumReplicasAvailable", 
                        "message": "Deployment has minimum availability."
                    }, 
                    {
                        "type": "Progressing", 
                        "status": "True", 
                        "lastUpdateTime": "2018-03-13T03:57:57Z", 
                        "lastTransitionTime": "2018-03-13T01:30:23Z", 
                        "reason": "NewReplicaSetAvailable", 
                        "message": "ReplicaSet \"pzb-test-1040447754\" has successfully progressed."
                    }
                ]
            }
        }
    ]
}
```

## 状态码<a name="zh-cn_topic_0091433681_section53049152"></a>

[表3](#zh-cn_topic_0091433681_d0e36668)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0091433681_d0e36668"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433681_row17031726"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433681_p37392545"><a name="zh-cn_topic_0091433681_p37392545"></a><a name="zh-cn_topic_0091433681_p37392545"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433681_p8897276"><a name="zh-cn_topic_0091433681_p8897276"></a><a name="zh-cn_topic_0091433681_p8897276"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433681_row49590760"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433681_p57428620"><a name="zh-cn_topic_0091433681_p57428620"></a><a name="zh-cn_topic_0091433681_p57428620"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433681_p21206673"><a name="zh-cn_topic_0091433681_p21206673"></a><a name="zh-cn_topic_0091433681_p21206673"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

