# 替换StatefulSet<a name="cci_02_3033"></a>

## 功能介绍<a name="section53648226"></a>

替换StatefulSet。

The following fields can be updated:

-   metadata.labels
-   metadata.annotations

-   spec.template
-   spec.replicas
-   spec.revisionHistoryLimit
-   spec.progressDeadlineSeconds

The other fields cannot be updated.

## URI<a name="section13071992"></a>

PUT /apis/apps/v1/namespaces/\{namespace\}/statefulsets/\{name\}

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

<a name="d0e39017"></a>
<table><thead align="left"><tr id="row47561193"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.26367363263674%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row40214539"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p36152249"><a name="p36152249"></a><a name="p36152249"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p42651031"><a name="p42651031"></a><a name="p42651031"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p32181453"><a name="p32181453"></a><a name="p32181453"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section50539068"></a>

**请求参数：**

请求参数的详细描述请参见[表86](数据结构.md#d0e37568)。

**请求示例：**

将[创建StatefulSet](创建StatefulSet.md)创建的StatefulSet的replica改为2。

```
{
    "apiVersion": "apps/v1",
    "kind": "StatefulSet",
    "metadata": {
        "name": "statefulset-test"
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
                "labels": {
                    "app": "statefulset-test"
                }
            },
            "spec": {
                "containers": [
                    {
                        "image": "*.*.*.*:20202/cci/redis:V1",
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
                ]
            }
        }
    }
}
```

## 响应消息<a name="section52198431"></a>

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
    "resourceVersion": "5223616",
    "generation": 2,
    "creationTimestamp": "2018-09-04T07:13:00Z",
    "labels": {
      "app": "statefulset-test"
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
        "securityContext": {

        },
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

## 状态码<a name="section23834"></a>

[表3](#d0e39106)描述API的状态码。

**表 3**  状态码

<a name="d0e39106"></a>
<table><thead align="left"><tr id="row46918656"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p42314824"><a name="p42314824"></a><a name="p42314824"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p4948704"><a name="p4948704"></a><a name="p4948704"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row65300720"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p54866977"><a name="p54866977"></a><a name="p54866977"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p15040154"><a name="p15040154"></a><a name="p15040154"></a>This operation succeeds, and a StatefulSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

