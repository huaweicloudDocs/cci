# 查询Deployment状态<a name="cci_02_3023"></a>

## 功能介绍<a name="section37553505"></a>

查询Deployment的状态。

## URI<a name="section2437233"></a>

GET /apis/apps/v1/namespaces/\{namespace\}/deployments/\{name\}/status

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

<a name="d0e35701"></a>
<table><thead align="left"><tr id="row65104669"><th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="67.34326567343265%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row4671366"><td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.1 "><p id="p42836357"><a name="p42836357"></a><a name="p42836357"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p47192917"><a name="p47192917"></a><a name="p47192917"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="67.34326567343265%" headers="mcps1.2.4.1.3 "><p id="p64529950"><a name="p64529950"></a><a name="p64529950"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section21935102"></a>

N/A

## 响应消息<a name="section63198193"></a>

**响应参数：**

响应参数的详细描述请参见[表80](公共参数.md#table12862324102610)。

**响应示例：**

```
{
  "kind": "Deployment",
  "apiVersion": "apps/v1",
  "metadata": {
    "name": "deployment-test",
    "namespace": "namespace-test",
    "selfLink": "/apis/apps/v1/namespaces/namespace-test/deployments/deployment-test/status",
    "uid": "777dce52-b186-11e8-8cb0-c81fbe371a17",
    "resourceVersion": "5630865",
    "generation": 1,
    "creationTimestamp": "2018-09-06T03:39:32Z",
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
            "image": "redis:3.0",
            "resources": {
              "limits": {
                "memory": "1Gi",
                "cpu": "500m"
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
    "observedGeneration": 1,
    "replicas": 1,
    "updatedReplicas": 1,
    "readyReplicas": 1,
    "availableReplicas": 1,
    "conditions": [
      {
        "type": "Available",
        "status": "True",
        "lastUpdateTime": "2018-09-06T03:39:40Z",
        "lastTransitionTime": "2018-09-06T03:39:40Z",
        "reason": "MinimumReplicasAvailable",
        "message": "Deployment has minimum availability."
      },
      {
        "type": "Progressing",
        "status": "True",
        "lastUpdateTime": "2018-09-06T03:39:40Z",
        "lastTransitionTime": "2018-09-06T03:39:32Z",
        "reason": "NewReplicaSetAvailable",
        "message": "ReplicaSet \"deployment-test-865578b586\" has successfully progressed."
      }
    ]
  }
}
```

## 状态码<a name="section31912827"></a>

[表3](#d0e35779)描述API的状态码。

**表 3**  状态码

<a name="d0e35779"></a>
<table><thead align="left"><tr id="row14389536"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p24701750"><a name="p24701750"></a><a name="p24701750"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p54684770"><a name="p54684770"></a><a name="p54684770"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row281353"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p22789653"><a name="p22789653"></a><a name="p22789653"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p34022638"><a name="p34022638"></a><a name="p34022638"></a>This operation succeeds, and a Deployment resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

