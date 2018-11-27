# 查询Deployment（v1beta1）<a name="cci_02_0029"></a>

## 功能介绍<a name="zh-cn_topic_0083864911_section530813545496"></a>

该API用于获取某个项目下指定的Deployment对象。

## URI<a name="zh-cn_topic_0083864911_section158974212501"></a>

GET /apis/apps/v1beta1/namespaces/\{namespace\}/deployments/\{name\}

[表1 参数描述 ](#zh-cn_topic_0083864911_table2027961241820)描述该API的参数。

**表 1**  参数描述

<a name="zh-cn_topic_0083864911_table2027961241820"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864911_row122809120186"><th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0083864911_p91421758131813"><a name="zh-cn_topic_0083864911_p91421758131813"></a><a name="zh-cn_topic_0083864911_p91421758131813"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.161616161616163%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0083864911_p101421758131816"><a name="zh-cn_topic_0083864911_p101421758131816"></a><a name="zh-cn_topic_0083864911_p101421758131816"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.61616161616161%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0083864911_p19143115818187"><a name="zh-cn_topic_0083864911_p19143115818187"></a><a name="zh-cn_topic_0083864911_p19143115818187"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864911_row32801312121810"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864911_p1063164520553"><a name="zh-cn_topic_0083864911_p1063164520553"></a><a name="zh-cn_topic_0083864911_p1063164520553"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864911_p12630545165513"><a name="zh-cn_topic_0083864911_p12630545165513"></a><a name="zh-cn_topic_0083864911_p12630545165513"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864911_row29001310466"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864911_p69007101268"><a name="zh-cn_topic_0083864911_p69007101268"></a><a name="zh-cn_topic_0083864911_p69007101268"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864911_p1790020109614"><a name="zh-cn_topic_0083864911_p1790020109614"></a><a name="zh-cn_topic_0083864911_p1790020109614"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0083864911_p1900110968"><a name="zh-cn_topic_0083864911_p1900110968"></a><a name="zh-cn_topic_0083864911_p1900110968"></a>name of the Deployment</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864911_row1744184023617"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864911_p644184043617"><a name="zh-cn_topic_0083864911_p644184043617"></a><a name="zh-cn_topic_0083864911_p644184043617"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864911_p194494017365"><a name="zh-cn_topic_0083864911_p194494017365"></a><a name="zh-cn_topic_0083864911_p194494017365"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0083864911_p3447402366"><a name="zh-cn_topic_0083864911_p3447402366"></a><a name="zh-cn_topic_0083864911_p3447402366"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864911_row2076664616361"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864911_p13191114910562"><a name="zh-cn_topic_0083864911_p13191114910562"></a><a name="zh-cn_topic_0083864911_p13191114910562"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864911_p99465435616"><a name="zh-cn_topic_0083864911_p99465435616"></a><a name="zh-cn_topic_0083864911_p99465435616"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0083864911_p12191849135617"><a name="zh-cn_topic_0083864911_p12191849135617"></a><a name="zh-cn_topic_0083864911_p12191849135617"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864911_row1627094733719"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864911_p319154955611"><a name="zh-cn_topic_0083864911_p319154955611"></a><a name="zh-cn_topic_0083864911_p319154955611"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="16.161616161616163%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864911_p1294155405612"><a name="zh-cn_topic_0083864911_p1294155405612"></a><a name="zh-cn_topic_0083864911_p1294155405612"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0083864911_p919118492563"><a name="zh-cn_topic_0083864911_p919118492563"></a><a name="zh-cn_topic_0083864911_p919118492563"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864911_section106320105520"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864911_section12955134485515"></a>

响应消息请参见[表2](创建Deployment（v1beta1）.md#zh-cn_topic_0083864910_table12862324102610)。

响应示例：

```
{
    "kind": "Deployment", 
    "apiVersion": "apps/v1beta1", 
    "metadata": {
        "name": "deployment-test", 
        "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments/deployment-test", 
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

## 状态码<a name="zh-cn_topic_0083864911_section164701657181718"></a>

[表2](#zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_table13421100171015)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_table13421100171015"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_row58580616171015"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0083864911_p3324338133814"><a name="zh-cn_topic_0083864911_p3324338133814"></a><a name="zh-cn_topic_0083864911_p3324338133814"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0083864911_p17324938123815"><a name="zh-cn_topic_0083864911_p17324938123815"></a><a name="zh-cn_topic_0083864911_p17324938123815"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_row3769153171015"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_p34614774161656"><a name="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_p34614774161656"></a><a name="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_p34614774161656"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_p51022873161656"><a name="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_p51022873161656"></a><a name="zh-cn_topic_0083864911_zh-cn_topic_0079616894_zh-cn_topic_0079614986_p51022873161656"></a>This operation succeeds, and a deployment resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

