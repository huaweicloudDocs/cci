# 查询Deployment<a name="cci_02_3022"></a>

## 功能介绍<a name="section530813545496"></a>

查询Deployment的详细信息。

## URI<a name="section158974212501"></a>

GET /apis/apps/v1/namespaces/\{namespace\}/deployments/\{name\}

**表 1**  Path参数

<a name="table1696332124519"></a>
<table><thead align="left"><tr id="row11961332194516"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.3.1.1"><p id="p396032144518"><a name="p396032144518"></a><a name="p396032144518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="76%" id="mcps1.2.3.1.2"><p id="p18962325454"><a name="p18962325454"></a><a name="p18962325454"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9960327457"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1496113214456"><a name="p1496113214456"></a><a name="p1496113214456"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p141902036155717"><a name="p141902036155717"></a><a name="p141902036155717"></a>Object name and auth scope, such as for teams and projects.</p>
</td>
</tr>
<tr id="row127506310151"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p19499173311150"><a name="p19499173311150"></a><a name="p19499173311150"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p1499123311158"><a name="p1499123311158"></a><a name="p1499123311158"></a>name of the Deployment</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table2027961241820"></a>
<table><thead align="left"><tr id="row122809120186"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.4.1.1"><p id="p91421758131813"><a name="p91421758131813"></a><a name="p91421758131813"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15%" id="mcps1.2.4.1.2"><p id="p101421758131816"><a name="p101421758131816"></a><a name="p101421758131816"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p19143115818187"><a name="p19143115818187"></a><a name="p19143115818187"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1744184023617"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.1 "><p id="p644184043617"><a name="p644184043617"></a><a name="p644184043617"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.2 "><p id="p194494017365"><a name="p194494017365"></a><a name="p194494017365"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p3447402366"><a name="p3447402366"></a><a name="p3447402366"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row2076664616361"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.1 "><p id="p13191114910562"><a name="p13191114910562"></a><a name="p13191114910562"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.2 "><p id="p99465435616"><a name="p99465435616"></a><a name="p99465435616"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p12191849135617"><a name="p12191849135617"></a><a name="p12191849135617"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="row1627094733719"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.1 "><p id="p319154955611"><a name="p319154955611"></a><a name="p319154955611"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.4.1.2 "><p id="p1294155405612"><a name="p1294155405612"></a><a name="p1294155405612"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p919118492563"><a name="p919118492563"></a><a name="p919118492563"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section106320105520"></a>

N/A

## 响应消息<a name="section12955134485515"></a>

**响应参数：**

响应消息请参见[表79](数据结构.md#table12862324102610)

**响应示例：**

```
{
    "kind": "Deployment",
    "apiVersion": "apps/v1",
    "metadata": {
        "name": "deployment-test",
        "namespace": "namespace-test",
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/deployments/deployment-test",
        "uid": "010506c7-af79-11e8-b6ef-f898ef6c78b4",
        "resourceVersion": "5036888",
        "generation": 1,
        "creationTimestamp": "2018-09-03T12:58:07Z",
        "labels": {
            "app": "redis"
        },
        "annotations": {
            "deployment.kubernetes.io/revision": "1"
        },
        "enable": true
    },
    "spec": {
        "replicas": 1,
        "selector": {
            "matchLabels": {
                "app": "redis"
            }
        },
        "template": {
            "metadata": {
                "creationTimestamp": null,
                "labels": {
                    "app": "redis"
                },
                "annotations": {
                    "cri.cci.io/container-type": "secure-container"
                },
                "enable": true
            },
            "spec": {
                "containers": [
                    {
                        "name": "container-0",
                        "image": "redis",
                        "resources": {
                            "limits": {
                                "cpu": "500m",
                                "memory": "1Gi"
                            },
                            "requests": {
                                "memory": "1Gi",
                                "cpu": "500m"
                            }
                        },
                        "terminationMessagePath": "/dev/termination-log",
                        "terminationMessagePolicy": "File",
                        "imagePullPolicy": "IfNotPresent"
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
                "schedulerName": "default-scheduler"
            }
        },
        "strategy": {
            "type": "RollingUpdate",
            "rollingUpdate": {
                "maxUnavailable": "25%",
                "maxSurge": "25%"
            }
        },
        "revisionHistoryLimit": 2,
        "progressDeadlineSeconds": 600
    },
    "status": {
        "observedGeneration": 1,
        "replicas": 1,
        "updatedReplicas": 1,
        "readyReplicas": 1,
        "availableReplicas": 1,
        "conditions": [
            {
                "type": "Available",
                "status": "True",
                "lastUpdateTime": "2018-09-03T12:58:12Z",
                "lastTransitionTime": "2018-09-03T12:58:12Z",
                "reason": "MinimumReplicasAvailable",
                "message": "Deployment has minimum availability."
            },
            {
                "type": "Progressing",
                "status": "True",
                "lastUpdateTime": "2018-09-03T12:58:12Z",
                "lastTransitionTime": "2018-09-03T12:58:07Z",
                "reason": "NewReplicaSetAvailable",
                "message": "ReplicaSet \"deployment-test-57f7cff77c\" has successfully progressed."
            }
        ]
    }
}
```

## 状态码<a name="section164701657181718"></a>

[表3](#zh-cn_topic_0079616894_zh-cn_topic_0079614986_table13421100171015)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079616894_zh-cn_topic_0079614986_table13421100171015"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079616894_zh-cn_topic_0079614986_row58580616171015"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p3324338133814"><a name="p3324338133814"></a><a name="p3324338133814"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p17324938123815"><a name="p17324938123815"></a><a name="p17324938123815"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079616894_zh-cn_topic_0079614986_row3769153171015"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079616894_zh-cn_topic_0079614986_p34614774161656"><a name="zh-cn_topic_0079616894_zh-cn_topic_0079614986_p34614774161656"></a><a name="zh-cn_topic_0079616894_zh-cn_topic_0079614986_p34614774161656"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079616894_zh-cn_topic_0079614986_p51022873161656"><a name="zh-cn_topic_0079616894_zh-cn_topic_0079614986_p51022873161656"></a><a name="zh-cn_topic_0079616894_zh-cn_topic_0079614986_p51022873161656"></a>This operation succeeds, and a deployment resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

