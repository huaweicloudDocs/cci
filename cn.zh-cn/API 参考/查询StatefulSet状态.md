# 查询StatefulSet状态<a name="cci_02_3032"></a>

## 功能介绍<a name="section27242258"></a>

查询StatefulSet状态。

## URI<a name="section43853730"></a>

GET /apis/apps/v1/namespaces/\{namespace\}/statefulsets/\{name\}/status

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
<tr id="row13794857171116"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p5984165818113"><a name="p5984165818113"></a><a name="p5984165818113"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the StatefulSet.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="d0e38842"></a>
<table><thead align="left"><tr id="row20375378"><th class="cellrowborder" valign="top" width="19.388061193880613%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.348265173482652%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.26367363263674%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row46037938"><td class="cellrowborder" valign="top" width="19.388061193880613%" headers="mcps1.2.4.1.1 "><p id="p38085530"><a name="p38085530"></a><a name="p38085530"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.2 "><p id="p65029074"><a name="p65029074"></a><a name="p65029074"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p32863618"><a name="p32863618"></a><a name="p32863618"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section59139257"></a>

N/A

## 响应消息<a name="section62491271"></a>

**响应参数：**

响应参数的详细描述请参见[表86](数据结构.md#d0e37568)。

**响应示例：**

```
{
    "kind": "StatefulSet",
    "apiVersion": "apps/v1",
    "metadata": {
        "name": "statefulset-test",
        "namespace": "namespace-test",
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/statefulsets/statefulset-test/status",
        "uid": "f4a35f35-b011-11e8-b6ef-f898ef6c78b4",
        "resourceVersion": "5217947",
        "generation": 1,
        "creationTimestamp": "2018-09-04T07:13:00Z",
        "labels": {
            "app": "statefulset-test"
        },
        "enable": true
    },
    "spec": {
        "replicas": 3,
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
                    "cri.cci.io/container-type": "secure-container"
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
        "serviceName": "",
        "podManagementPolicy": "OrderedReady",
        "updateStrategy": {
            "type": "OnDelete"
        },
        "revisionHistoryLimit": 10
    },
    "status": {
        "observedGeneration": 1,
        "replicas": 3,
        "readyReplicas": 1,
        "currentReplicas": 3,
        "currentRevision": "statefulset-test-f986b645b",
        "updateRevision": "statefulset-test-f986b645b",
        "collisionCount": 0
    }
}
```

## 状态码<a name="section25550533"></a>

[表3](#d0e38919)描述API的状态码。

**表 3**  状态码

<a name="d0e38919"></a>
<table><thead align="left"><tr id="row25379235"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p42452127"><a name="p42452127"></a><a name="p42452127"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p16070288"><a name="p16070288"></a><a name="p16070288"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row26624990"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p9140592"><a name="p9140592"></a><a name="p9140592"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2190511"><a name="p2190511"></a><a name="p2190511"></a>This operation succeeds, and a StatefulSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

