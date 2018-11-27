# 更新Deployment（v1beta1）<a name="cci_02_0033"></a>

## 功能介绍<a name="zh-cn_topic_0083864912_section172959268501"></a>

该API用于更新指定的Deployment对象。

其中以下字段支持更新：

-   metadata.labels
-   metadata.generateName
-   metadata.annotations
-   spec.template
-   spec.replicas
-   spec.revisionHistoryLimit
-   spec.progressDeadlineSeconds

## URI<a name="zh-cn_topic_0083864912_section1524832914503"></a>

PATCH /apis/apps/v1beta1/namespaces/\{namespace\}/deployments/\{name\}

[表1](#zh-cn_topic_0083864912_table14970324122818)描述该API的参数

**表 1**  参数

<a name="zh-cn_topic_0083864912_table14970324122818"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864912_row0971162417289"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_p54329699"><a name="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_p54329699"></a><a name="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_p54329699"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0083864912_p6151164282819"><a name="zh-cn_topic_0083864912_p6151164282819"></a><a name="zh-cn_topic_0083864912_p6151164282819"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="56.99999999999999%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0083864912_p21518421288"><a name="zh-cn_topic_0083864912_p21518421288"></a><a name="zh-cn_topic_0083864912_p21518421288"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864912_row83198295289"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864912_p153191729102818"><a name="zh-cn_topic_0083864912_p153191729102818"></a><a name="zh-cn_topic_0083864912_p153191729102818"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864912_p63193293289"><a name="zh-cn_topic_0083864912_p63193293289"></a><a name="zh-cn_topic_0083864912_p63193293289"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0083864912_p231992915285"><a name="zh-cn_topic_0083864912_p231992915285"></a><a name="zh-cn_topic_0083864912_p231992915285"></a>name of the Deployment</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864912_row6971102432818"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864912_p397172413282"><a name="zh-cn_topic_0083864912_p397172413282"></a><a name="zh-cn_topic_0083864912_p397172413282"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864912_p14971824142810"><a name="zh-cn_topic_0083864912_p14971824142810"></a><a name="zh-cn_topic_0083864912_p14971824142810"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864912_row11971122412819"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864912_p1597142412282"><a name="zh-cn_topic_0083864912_p1597142412282"></a><a name="zh-cn_topic_0083864912_p1597142412282"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864912_p497132410288"><a name="zh-cn_topic_0083864912_p497132410288"></a><a name="zh-cn_topic_0083864912_p497132410288"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0083864912_p1597132420289"><a name="zh-cn_topic_0083864912_p1597132420289"></a><a name="zh-cn_topic_0083864912_p1597132420289"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864912_section1244125315509"></a>

**请求参数：**

“Content-Type“的详细描述请参见 [PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

请求参数的详细描述请参见[表2](创建Deployment（v1beta1）.md#zh-cn_topic_0083864910_table12862324102610)。

**请求示例：**

```
{
    "metadata": {
        "annotations": {
            "description": "test"
        }
    }
}
```

## 响应消息<a name="zh-cn_topic_0083864912_section59181834162920"></a>

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
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments/deployment-test", 
        "uid": "ed89a51c-2728-11e8-b891-84a9c46e8c8b", 
        "resourceVersion": "4510945", 
        "generation": 4, 
        "creationTimestamp": "2018-03-14T01:42:17Z", 
        "labels": {
            "appgroup": ""
        }, 
        "annotations": {
            "deployment.kubernetes.io/revision": "1", 
            "description": "test"
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
}
```

状态码

[表2](#zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_table12683857)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_table12683857"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_row49320909"><th class="cellrowborder" valign="top" width="47%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0083864912_p7478104103014"><a name="zh-cn_topic_0083864912_p7478104103014"></a><a name="zh-cn_topic_0083864912_p7478104103014"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="53%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0083864912_p1847954163013"><a name="zh-cn_topic_0083864912_p1847954163013"></a><a name="zh-cn_topic_0083864912_p1847954163013"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_row41609976"><td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_p14964925"><a name="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_p14964925"></a><a name="zh-cn_topic_0083864912_zh-cn_topic_0079616860_zh-cn_topic_0079614957_p14964925"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433681_p21206673"><a name="zh-cn_topic_0091433681_p21206673"></a><a name="zh-cn_topic_0091433681_p21206673"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

