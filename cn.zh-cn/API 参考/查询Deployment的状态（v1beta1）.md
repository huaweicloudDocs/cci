# 查询Deployment的状态（v1beta1）<a name="cci_02_0030"></a>

## 功能介绍<a name="zh-cn_topic_0091433676_section37553505"></a>

This API is used to read the status of a specified Deployment object under a specified Namespace.

## URI<a name="zh-cn_topic_0091433676_section2437233"></a>

GET /apis/apps/v1beta1/namespaces/\{namespace\}/deployments/\{name\}/status

[表1](#zh-cn_topic_0091433676_d0e35701)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433676_d0e35701"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433676_row65104669"><th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433676_p65652297517"><a name="zh-cn_topic_0091433676_p65652297517"></a><a name="zh-cn_topic_0091433676_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433676_p165661629135114"><a name="zh-cn_topic_0091433676_p165661629135114"></a><a name="zh-cn_topic_0091433676_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="67.34326567343265%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433676_p14567629115114"><a name="zh-cn_topic_0091433676_p14567629115114"></a><a name="zh-cn_topic_0091433676_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433676_row31480888"><td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433676_p66924004"><a name="zh-cn_topic_0091433676_p66924004"></a><a name="zh-cn_topic_0091433676_p66924004"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433676_p52135240"><a name="zh-cn_topic_0091433676_p52135240"></a><a name="zh-cn_topic_0091433676_p52135240"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="67.34326567343265%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433676_p62204941"><a name="zh-cn_topic_0091433676_p62204941"></a><a name="zh-cn_topic_0091433676_p62204941"></a>name of the Deployment</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433676_row22973563"><td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433676_p48919348"><a name="zh-cn_topic_0091433676_p48919348"></a><a name="zh-cn_topic_0091433676_p48919348"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433676_p3044257"><a name="zh-cn_topic_0091433676_p3044257"></a><a name="zh-cn_topic_0091433676_p3044257"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="67.34326567343265%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433676_row4671366"><td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433676_p42836357"><a name="zh-cn_topic_0091433676_p42836357"></a><a name="zh-cn_topic_0091433676_p42836357"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433676_p47192917"><a name="zh-cn_topic_0091433676_p47192917"></a><a name="zh-cn_topic_0091433676_p47192917"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="67.34326567343265%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433676_p64529950"><a name="zh-cn_topic_0091433676_p64529950"></a><a name="zh-cn_topic_0091433676_p64529950"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433676_section21935102"></a>

N/A

## 响应消息<a name="zh-cn_topic_0091433676_section63198193"></a>

**响应参数：**

响应参数的详细描述请参见[表2](创建Deployment（v1beta1）.md#zh-cn_topic_0083864910_table12862324102610)。

**响应示例：**

```
{
    "kind": "Deployment", 
    "apiVersion": "apps/v1beta1", 
    "metadata": {
        "name": "deployment-test", 
        "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments/deployment-test/status", 
        "uid": "ed89a51c-2728-11e8-b891-84a9c46e8c8b", 
        "resourceVersion": "4510941", 
        "generation": 2, 
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
                                "memory": "1536Mi"
                            }, 
                            "requests": {
                                "cpu": "1", 
                                "memory": "1536Mi"
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
        "observedGeneration": 2, 
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
}
```

## 状态码<a name="zh-cn_topic_0091433676_section31912827"></a>

[表2](#zh-cn_topic_0091433676_d0e35779)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433676_d0e35779"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433676_row14389536"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433676_p24701750"><a name="zh-cn_topic_0091433676_p24701750"></a><a name="zh-cn_topic_0091433676_p24701750"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433676_p54684770"><a name="zh-cn_topic_0091433676_p54684770"></a><a name="zh-cn_topic_0091433676_p54684770"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433676_row281353"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433676_p22789653"><a name="zh-cn_topic_0091433676_p22789653"></a><a name="zh-cn_topic_0091433676_p22789653"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433676_p34022638"><a name="zh-cn_topic_0091433676_p34022638"></a><a name="zh-cn_topic_0091433676_p34022638"></a>This operation succeeds, and a Deployment resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

