# 查询StatefulSet（v1beta1）<a name="cci_02_0038"></a>

## 功能介绍<a name="zh-cn_topic_0091433690_section15132207"></a>

This API is used to read a StatefulSet object under a specified Namespace.

## URI<a name="zh-cn_topic_0091433690_section1972143"></a>

GET /apis/apps/v1beta1/namespaces/\{namespace\}/statefulsets/\{name\}

[表1](#zh-cn_topic_0091433690_d0e38675)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433690_d0e38675"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433690_row60367007"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433690_p65652297517"><a name="zh-cn_topic_0091433690_p65652297517"></a><a name="zh-cn_topic_0091433690_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433690_p165661629135114"><a name="zh-cn_topic_0091433690_p165661629135114"></a><a name="zh-cn_topic_0091433690_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.26367363263674%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433690_p14567629115114"><a name="zh-cn_topic_0091433690_p14567629115114"></a><a name="zh-cn_topic_0091433690_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433690_row35644311"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433690_p1508084"><a name="zh-cn_topic_0091433690_p1508084"></a><a name="zh-cn_topic_0091433690_p1508084"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433690_p55045998"><a name="zh-cn_topic_0091433690_p55045998"></a><a name="zh-cn_topic_0091433690_p55045998"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433690_p29540844"><a name="zh-cn_topic_0091433690_p29540844"></a><a name="zh-cn_topic_0091433690_p29540844"></a>Name of the StatefulSet.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433690_row64541008"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433690_p60439184"><a name="zh-cn_topic_0091433690_p60439184"></a><a name="zh-cn_topic_0091433690_p60439184"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433690_p63735753"><a name="zh-cn_topic_0091433690_p63735753"></a><a name="zh-cn_topic_0091433690_p63735753"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433690_row24030130"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433690_p283486"><a name="zh-cn_topic_0091433690_p283486"></a><a name="zh-cn_topic_0091433690_p283486"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433690_p22962431"><a name="zh-cn_topic_0091433690_p22962431"></a><a name="zh-cn_topic_0091433690_p22962431"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433690_p48017661"><a name="zh-cn_topic_0091433690_p48017661"></a><a name="zh-cn_topic_0091433690_p48017661"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433690_row29505770"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433690_p41157182"><a name="zh-cn_topic_0091433690_p41157182"></a><a name="zh-cn_topic_0091433690_p41157182"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433690_p45397409"><a name="zh-cn_topic_0091433690_p45397409"></a><a name="zh-cn_topic_0091433690_p45397409"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433690_p53311550"><a name="zh-cn_topic_0091433690_p53311550"></a><a name="zh-cn_topic_0091433690_p53311550"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433690_row10041905"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433690_p8087957"><a name="zh-cn_topic_0091433690_p8087957"></a><a name="zh-cn_topic_0091433690_p8087957"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433690_p51144774"><a name="zh-cn_topic_0091433690_p51144774"></a><a name="zh-cn_topic_0091433690_p51144774"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433690_p49085995"><a name="zh-cn_topic_0091433690_p49085995"></a><a name="zh-cn_topic_0091433690_p49085995"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433690_section17749294"></a>

N/A

## 响应消息<a name="zh-cn_topic_0091433690_section25525926"></a>

**响应参数：**

响应参数的详细描述请参见[表2](创建StatefulSet（v1beta1）.md#zh-cn_topic_0091433687_d0e37568)。

**响应示例：**

```
{
    "kind": "StatefulSet", 
    "apiVersion": "apps/v1beta1", 
    "metadata": {
        "name": "statefulset-test", 
        "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/statefulsets/statefulset-test", 
        "uid": "ee0ef0d0-2728-11e8-8930-84a9c46e8ca3", 
        "resourceVersion": "4510955", 
        "generation": 1, 
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
                        "image": "undefined:undefined", 
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
        "observedGeneration": 1, 
        "replicas": 1, 
        "currentReplicas": 1, 
        "currentRevision": "statefulset-test-2238135242", 
        "updateRevision": "statefulset-test-2238135242"
    }
}
```

## 状态码<a name="zh-cn_topic_0091433690_section28406742"></a>

[表2](#zh-cn_topic_0091433690_d0e38773)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433690_d0e38773"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433690_row48797355"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433690_p60271674"><a name="zh-cn_topic_0091433690_p60271674"></a><a name="zh-cn_topic_0091433690_p60271674"></a>Status Code</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433690_p50167450"><a name="zh-cn_topic_0091433690_p50167450"></a><a name="zh-cn_topic_0091433690_p50167450"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433690_row37031667"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433690_p46775020"><a name="zh-cn_topic_0091433690_p46775020"></a><a name="zh-cn_topic_0091433690_p46775020"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433690_p30680237"><a name="zh-cn_topic_0091433690_p30680237"></a><a name="zh-cn_topic_0091433690_p30680237"></a>This operation succeeds, and a StatefulSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

