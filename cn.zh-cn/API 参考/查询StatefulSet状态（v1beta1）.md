# 查询StatefulSet状态<a name="cci_02_0039"></a>

## 功能介绍<a name="zh-cn_topic_0091433691_section27242258"></a>

This API is used to read the status of a specified StatefulSet object under a specified Namespace.

## URI<a name="zh-cn_topic_0091433691_section43853730"></a>

GET /apis/apps/v1beta1/namespaces/\{namespace\}/statefulsets/\{name\}/status

[表1](#zh-cn_topic_0091433691_d0e38842)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433691_d0e38842"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433691_row20375378"><th class="cellrowborder" valign="top" width="19.388061193880613%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433691_p65652297517"><a name="zh-cn_topic_0091433691_p65652297517"></a><a name="zh-cn_topic_0091433691_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.348265173482652%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433691_p165661629135114"><a name="zh-cn_topic_0091433691_p165661629135114"></a><a name="zh-cn_topic_0091433691_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.26367363263674%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433691_p14567629115114"><a name="zh-cn_topic_0091433691_p14567629115114"></a><a name="zh-cn_topic_0091433691_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433691_row40697101"><td class="cellrowborder" valign="top" width="19.388061193880613%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433691_p8130848"><a name="zh-cn_topic_0091433691_p8130848"></a><a name="zh-cn_topic_0091433691_p8130848"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433691_p54618989"><a name="zh-cn_topic_0091433691_p54618989"></a><a name="zh-cn_topic_0091433691_p54618989"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433691_p62061978"><a name="zh-cn_topic_0091433691_p62061978"></a><a name="zh-cn_topic_0091433691_p62061978"></a>Name of the StatefulSet.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433691_row21686892"><td class="cellrowborder" valign="top" width="19.388061193880613%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433691_p11807821"><a name="zh-cn_topic_0091433691_p11807821"></a><a name="zh-cn_topic_0091433691_p11807821"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433691_p16909410"><a name="zh-cn_topic_0091433691_p16909410"></a><a name="zh-cn_topic_0091433691_p16909410"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433691_row46037938"><td class="cellrowborder" valign="top" width="19.388061193880613%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433691_p38085530"><a name="zh-cn_topic_0091433691_p38085530"></a><a name="zh-cn_topic_0091433691_p38085530"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433691_p65029074"><a name="zh-cn_topic_0091433691_p65029074"></a><a name="zh-cn_topic_0091433691_p65029074"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433691_p32863618"><a name="zh-cn_topic_0091433691_p32863618"></a><a name="zh-cn_topic_0091433691_p32863618"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433691_section59139257"></a>

N/A

## 响应消息<a name="zh-cn_topic_0091433691_section62491271"></a>

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
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/statefulsets/statefulset-test/status", 
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

## 状态码<a name="zh-cn_topic_0091433691_section25550533"></a>

[表2](#zh-cn_topic_0091433691_d0e38919)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433691_d0e38919"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433691_row25379235"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433691_p42452127"><a name="zh-cn_topic_0091433691_p42452127"></a><a name="zh-cn_topic_0091433691_p42452127"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433691_p16070288"><a name="zh-cn_topic_0091433691_p16070288"></a><a name="zh-cn_topic_0091433691_p16070288"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433691_row26624990"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433691_p9140592"><a name="zh-cn_topic_0091433691_p9140592"></a><a name="zh-cn_topic_0091433691_p9140592"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433691_p2190511"><a name="zh-cn_topic_0091433691_p2190511"></a><a name="zh-cn_topic_0091433691_p2190511"></a>This operation succeeds, and a StatefulSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

