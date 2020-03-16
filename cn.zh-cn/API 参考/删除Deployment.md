# 删除Deployment<a name="cci_02_3020"></a>

## 功能介绍<a name="section65321233"></a>

删除Deployment。

## URI<a name="section51020189"></a>

DELETE /apis/apps/v1/namespaces/\{namespace\}/deployments/\{name\}

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

<a name="table2758112513516"></a>
<table><thead align="left"><tr id="row65815647"><th class="cellrowborder" valign="top" width="19.958004199580042%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.71862813718628%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="66.32336766323368%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row62561693"><td class="cellrowborder" valign="top" width="19.958004199580042%" headers="mcps1.2.4.1.1 "><p id="p34332366"><a name="p34332366"></a><a name="p34332366"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="13.71862813718628%" headers="mcps1.2.4.1.2 "><p id="p29458227"><a name="p29458227"></a><a name="p29458227"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="p37306164"><a name="p37306164"></a><a name="p37306164"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row211163"><td class="cellrowborder" valign="top" width="19.958004199580042%" headers="mcps1.2.4.1.1 "><p id="p17104275"><a name="p17104275"></a><a name="p17104275"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="13.71862813718628%" headers="mcps1.2.4.1.2 "><p id="p43269019"><a name="p43269019"></a><a name="p43269019"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="p15129627"><a name="p15129627"></a><a name="p15129627"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row1948920"><td class="cellrowborder" valign="top" width="19.958004199580042%" headers="mcps1.2.4.1.1 "><p id="p23644832"><a name="p23644832"></a><a name="p23644832"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="13.71862813718628%" headers="mcps1.2.4.1.2 "><p id="p36183253"><a name="p36183253"></a><a name="p36183253"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="p45162366"><a name="p45162366"></a><a name="p45162366"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row3808114"><td class="cellrowborder" valign="top" width="19.958004199580042%" headers="mcps1.2.4.1.1 "><p id="p40021797"><a name="p40021797"></a><a name="p40021797"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="13.71862813718628%" headers="mcps1.2.4.1.2 "><p id="p20540096"><a name="p20540096"></a><a name="p20540096"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="p8453712"><a name="p8453712"></a><a name="p8453712"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: 'Orphan' - orphan the dependents; 'Background' - allow the garbage collector to delete the dependents in the background; 'Foreground' - a cascading policy that deletes all dependents in the foreground.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section56528519"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

-   只删除Deployment（对应ReplicSet和Pod不删除）

    ```
    {
        "Kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Orphan"
    }
    ```

-   前台级联删除（按照Pod-\>ReplicaSet-\>Deployment的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Foreground"
    }
    ```

-   后台级联删除（按照Deployment-\>ReplicaSet-\>Pod的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Background"
    }
    ```


## 响应消息<a name="section38994624"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

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
        "resourceVersion": "5657791",
        "generation": 3,
        "creationTimestamp": "2018-09-06T03:39:32Z",
        "deletionTimestamp": "2018-09-06T06:36:54Z",
        "deletionGracePeriodSeconds": 0,
        "labels": {
            "app": "deployment-test2"
        },
        "annotations": {
            "deployment.kubernetes.io/revision": "2"
        },
        "finalizers": [
            "foregroundDeletion"
        ],
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
                                "cpu": "500m",
                                "memory": "1Gi"
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

## 状态码<a name="section15407297"></a>

[表3](#d0e35248)描述API的状态码。

**表 3**  状态码

<a name="d0e35248"></a>
<table><thead align="left"><tr id="row25883953"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p16225480"><a name="p16225480"></a><a name="p16225480"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p39195466"><a name="p39195466"></a><a name="p39195466"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row20716193"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p290101"><a name="p290101"></a><a name="p290101"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p28437418"><a name="p28437418"></a><a name="p28437418"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

