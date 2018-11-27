# 更新StatefulSet（v1beta1）<a name="cci_02_0042"></a>

## 功能介绍<a name="zh-cn_topic_0091433692_section53648226"></a>

This API is used to replace a StatefulSet object under a specified Namespace.

The following fields can be updated:

-   metadata.labels
-   metadata.generateName
-   metadata.annotations
-   spec.replicas
-   spec.template
-   spec.restartPolicy
-   spec.revisionHistoryLimit
-   spec.progressDeadlineSeconds

## URI<a name="zh-cn_topic_0091433692_section13071992"></a>

PATCH /apis/apps/v1beta1/namespaces/\{namespace\}/statefulsets/\{name\}

[表1](#zh-cn_topic_0091433692_d0e39017)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433692_d0e39017"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433692_row47561193"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433692_p65652297517"><a name="zh-cn_topic_0091433692_p65652297517"></a><a name="zh-cn_topic_0091433692_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433692_p165661629135114"><a name="zh-cn_topic_0091433692_p165661629135114"></a><a name="zh-cn_topic_0091433692_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.26367363263674%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433692_p14567629115114"><a name="zh-cn_topic_0091433692_p14567629115114"></a><a name="zh-cn_topic_0091433692_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433692_row20654971"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433692_p62439989"><a name="zh-cn_topic_0091433692_p62439989"></a><a name="zh-cn_topic_0091433692_p62439989"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433692_p24474376"><a name="zh-cn_topic_0091433692_p24474376"></a><a name="zh-cn_topic_0091433692_p24474376"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433692_p36267419"><a name="zh-cn_topic_0091433692_p36267419"></a><a name="zh-cn_topic_0091433692_p36267419"></a>Name of the StatefulSet.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433692_row57971316"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433692_p65165002"><a name="zh-cn_topic_0091433692_p65165002"></a><a name="zh-cn_topic_0091433692_p65165002"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433692_p43873846"><a name="zh-cn_topic_0091433692_p43873846"></a><a name="zh-cn_topic_0091433692_p43873846"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433692_row40214539"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433692_p36152249"><a name="zh-cn_topic_0091433692_p36152249"></a><a name="zh-cn_topic_0091433692_p36152249"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433692_p42651031"><a name="zh-cn_topic_0091433692_p42651031"></a><a name="zh-cn_topic_0091433692_p42651031"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433692_p32181453"><a name="zh-cn_topic_0091433692_p32181453"></a><a name="zh-cn_topic_0091433692_p32181453"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433692_section50539068"></a>

**请求参数：**

请求参数的详细描述请参见[表2](创建StatefulSet（v1beta1）.md#zh-cn_topic_0091433687_d0e37568)。

“Content-Type“消息头说明请参见[PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

**请求示例：**

```
Content-Type: application/merge-patch+json
```

```
{
    "metadata": {
        "labels": {
            "app": "mysql-0"
        }
    }
}
```

## 响应消息<a name="zh-cn_topic_0091433692_section52198431"></a>

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
        "resourceVersion": "4510963", 
        "generation": 2, 
        "creationTimestamp": "2018-03-14T01:42:18Z", 
        "labels": {
            "app": "mysql-0", 
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
}
```

## 状态码<a name="zh-cn_topic_0091433692_section23834"></a>

[表2](#zh-cn_topic_0091433692_d0e39106)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433692_d0e39106"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433692_row46918656"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433692_p42314824"><a name="zh-cn_topic_0091433692_p42314824"></a><a name="zh-cn_topic_0091433692_p42314824"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433692_p4948704"><a name="zh-cn_topic_0091433692_p4948704"></a><a name="zh-cn_topic_0091433692_p4948704"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433692_row65300720"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433692_p54866977"><a name="zh-cn_topic_0091433692_p54866977"></a><a name="zh-cn_topic_0091433692_p54866977"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433692_p15040154"><a name="zh-cn_topic_0091433692_p15040154"></a><a name="zh-cn_topic_0091433692_p15040154"></a>This operation succeeds, and a StatefulSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

