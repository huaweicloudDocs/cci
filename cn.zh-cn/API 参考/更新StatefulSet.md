# 更新StatefulSet<a name="cci_02_3035"></a>

## 功能介绍<a name="section40645355"></a>

更新StatefulSet。

The following fields can be updated:

-   metadata.labels
-   metadata.annotations
-   spec.replicas
-   spec.template
-   spec.restartPolicy
-   spec.revisionHistoryLimit
-   spec.progressDeadlineSeconds

The other fields cannot be updated.

## URI<a name="section30263877"></a>

PATCH /apis/apps/v1/namespaces/\{namespace\}/statefulsets/\{name\}

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
<tr id="row5851195019584"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1085113505585"><a name="p1085113505585"></a><a name="p1085113505585"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p19851950125818"><a name="p19851950125818"></a><a name="p19851950125818"></a>Name of the StatefulSet.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="d0e39827"></a>
<table><thead align="left"><tr id="row21309757"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.15%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="62.629999999999995%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10075143"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p10780286"><a name="p10780286"></a><a name="p10780286"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="p787936"><a name="p787936"></a><a name="p787936"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="p63822871"><a name="p63822871"></a><a name="p63822871"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section3939444"></a>

**请求参数：**

“Content-Type“消息头说明请参见[PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

**请求示例：**

将[创建StatefulSet](创建StatefulSet.md)创建的StatefulSet的metadata.labels更新为"app": "statefulset-test2"。

```
Content-Type: application/merge-patch+json
{
    "metadata": {
        "labels": {
            "app": "statefulset-test2"
        }
    }
}
```

## 响应消息<a name="section35455000"></a>

**响应参数：**

响应参数的详细描述请参见[表87](数据结构.md#d0e37568)。

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
    "resourceVersion": "5231369",
    "generation": 2,
    "creationTimestamp": "2018-09-04T07:13:00Z",
    "labels": {
      "app": "statefulset-test2"
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
    "observedGeneration": 2,
    "replicas": 2,
    "updatedReplicas": 2,
    "currentRevision": "statefulset-test-f986b645b",
    "updateRevision": "statefulset-test-7748d5459",
    "collisionCount": 0
  }
}
```

## 状态码<a name="section50659546"></a>

[表3](#d0e39922)描述API的状态码。

**表 3**  状态码

<a name="d0e39922"></a>
<table><thead align="left"><tr id="row43842358"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p61570118"><a name="p61570118"></a><a name="p61570118"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p21123642"><a name="p21123642"></a><a name="p21123642"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row33293435"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p12413680"><a name="p12413680"></a><a name="p12413680"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p65984001"><a name="p65984001"></a><a name="p65984001"></a>This operation succeeds, and a StatefulSet resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

