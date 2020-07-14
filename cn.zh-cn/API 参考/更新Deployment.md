# 更新Deployment<a name="cci_02_3026"></a>

## 功能介绍<a name="section59866645"></a>

更新Deployment。

The following fields can be updated:

-   metadata.labels
-   metadata.generateName
-   metadata.annotations
-   spec.template
-   spec.replicas
-   spec.revisionHistoryLimit
-   spec.progressDeadlineSeconds

## URI<a name="section1928895"></a>

PATCH /apis/apps/v1/namespaces/\{namespace\}/deployments/\{name\}

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

<a name="d0e36967"></a>
<table><thead align="left"><tr id="row62299817"><th class="cellrowborder" valign="top" width="17.348265173482652%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="66.32336766323368%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10278610"><td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.1 "><p id="p27261059"><a name="p27261059"></a><a name="p27261059"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p60662202"><a name="p60662202"></a><a name="p60662202"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="p14691292"><a name="p14691292"></a><a name="p14691292"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section17360061"></a>

**请求参数：**

“Content-Type“消息头说明请参见[PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

**请求示例：**

将[创建Deployment](创建Deployment.md)创建Deployment的label更新为deployment-test2。

```
Content-Type: application/merge-patch+json
{
    "metadata": {
        "labels": {
            "app": "deployment-test2"
        }
    }
}
```

## 响应消息<a name="section22022822"></a>

**响应参数：**

响应参数的详细描述请参见[表79](数据结构.md#table12862324102610)。

**响应示例：**

```
{
    "kind": "Deployment",
    "apiVersion": "apps/v1",
    "metadata": {
        "name": "deployment-test",
        "namespace": "namespace-test",
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/deployments/deployment-test",
        "uid": "777dce52-b186-11e8-8cb0-c81fbe371a17",
        "resourceVersion": "5657176",
        "generation": 2,
        "creationTimestamp": "2018-09-06T03:39:32Z",
        "labels": {
            "app": "deployment-test2"
        },
        "annotations": {
            "deployment.kubernetes.io/revision": "2"
        },
        "enable": true
    },
    "spec": {
        "replicas": 2,
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
                "enable": true
            },
            "spec": {
                "containers": [
                    {
                        "name": "container-0",
                        "image": "*.*.*.*:20202/cci/redis:V1",
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
        "revisionHistoryLimit": 10,
        "progressDeadlineSeconds": 600
    },
    "status": {
        "observedGeneration": 2,
        "replicas": 2,
        "updatedReplicas": 2,
        "readyReplicas": 2,
        "availableReplicas": 2,
        "conditions": [
            {
                "type": "Available",
                "status": "True",
                "lastUpdateTime": "2018-09-06T04:14:14Z",
                "lastTransitionTime": "2018-09-06T04:14:14Z",
                "reason": "MinimumReplicasAvailable",
                "message": "Deployment has minimum availability."
            },
            {
                "type": "Progressing",
                "status": "True",
                "lastUpdateTime": "2018-09-06T04:14:24Z",
                "lastTransitionTime": "2018-09-06T03:39:32Z",
                "reason": "NewReplicaSetAvailable",
                "message": "ReplicaSet \"deployment-test-68585dfddb\" has successfully progressed."
            }
        ]
    }
}
```

## 状态码<a name="section63987677"></a>

[表3](#d0e37060)描述API的状态码。

**表 3**  状态码

<a name="d0e37060"></a>
<table><thead align="left"><tr id="row44413743"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p40743437"><a name="p40743437"></a><a name="p40743437"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p11884140"><a name="p11884140"></a><a name="p11884140"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row23091316"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p58457292"><a name="p58457292"></a><a name="p58457292"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p37420188"><a name="p37420188"></a><a name="p37420188"></a>This operation succeeds, and a Deployment resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

