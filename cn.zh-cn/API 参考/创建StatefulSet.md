# 创建StatefulSet<a name="cci_02_3028"></a>

## 功能介绍<a name="section40975543"></a>

创建StatefulSet。

## URI<a name="section33235568"></a>

POST /apis/apps/v1/namespaces/\{namespace\}/statefulsets

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
</tbody>
</table>

**表 2**  Query参数

<a name="d0e37523"></a>
<table><thead align="left"><tr id="row5993206"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.169999999999998%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row55956597"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p36190548"><a name="p36190548"></a><a name="p36190548"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p45753308"><a name="p45753308"></a><a name="p45753308"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p15030452"><a name="p15030452"></a><a name="p15030452"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section30684661"></a>

**请求参数：**

请求参数如[表86](数据结构.md#d0e37568)所示。

**请求示例：**

```
{
    "apiVersion": "apps/v1",
    "kind": "StatefulSet",
    "metadata": {
        "name": "statefulset-test"
    },
    "spec": {
        "replicas": "3",
        "selector": {
            "matchLabels": {
                "app": "statefulset-test"
            }
        },
        "template": {
            "metadata": {
                "labels": {
                    "app": "statefulset-test"
                }
            },
            "spec": {
                "containers": [
                    {
                        "image": "redis:3.0",
                        "name": "container-0",
                        "resources": {
                            "limits": {
                                "cpu": "500m",
                                "memory": "1024Mi"
                            },
                            "requests": {
                                "cpu": "500m",
                                "memory": "1024Mi"
                            }
                        }
                    }
                ],
                "imagePullSecrets": [
                    {
                        "name": "imagepull-secret"
                    }
                ],
                "priority": "0",
            }
        }
    }
}
```

## 响应消息<a name="section7726493"></a>

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
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/statefulsets/statefulset-test",
        "uid": "f4a35f35-b011-11e8-b6ef-f898ef6c78b4",
        "resourceVersion": "5207623",
        "generation": 1,
        "creationTimestamp": "2018-09-04T07:13:00Z",
        "labels": {
            "app": "statefulset-test"
        },
        "enable": true
    },
    "spec": {
        "replicas": 3,
        "priority": "0",
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
                        "image": "redis:3.0",
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
        "serviceName": "",
        "podManagementPolicy": "OrderedReady",
        "updateStrategy": {
            "type": "OnDelete"
        },
        "revisionHistoryLimit": 10
    },
    "status": {
        "replicas": 0
    }
}
```

## 状态码<a name="section2429579"></a>

[表3](#d0e38203)描述API的状态码。

**表 3**  状态码

<a name="d0e38203"></a>
<table><thead align="left"><tr id="row26900678"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p31471277"><a name="p31471277"></a><a name="p31471277"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p66145529"><a name="p66145529"></a><a name="p66145529"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row56187666"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p54907103"><a name="p54907103"></a><a name="p54907103"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p18290377"><a name="p18290377"></a><a name="p18290377"></a>The request has been fulfilled, resulting in the creation of a new resource.</p>
</td>
</tr>
</tbody>
</table>

