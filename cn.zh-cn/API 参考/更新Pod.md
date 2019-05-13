# 更新Pod<a name="cci_02_3014"></a>

## 功能介绍<a name="sa4fea4daced64d1888668eec5dfdf81e"></a>

更新Pod。

其中以下字段支持更新：

-   metadata.generateName
-   metadata.labels
-   metadata.annotations
-   spec.initContainers\[\*\].image
-   spec.containers\[\*\].image
-   spec.activeDeadlineSeconds
-   spec.tolerations

其余部分不支持更新。

## URI<a name="s325d88a5c7a84313849b743675883694"></a>

PATCH /api/v1/namespaces/\{namespace\}/pods/\{name\}

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
<tr id="row465691211311"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p14829111716318"><a name="p14829111716318"></a><a name="p14829111716318"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p3844917931"><a name="p3844917931"></a><a name="p3844917931"></a>Name of the Pod.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079614948_table57906594"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614948_row34327759"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614948_p29085133"><a name="zh-cn_topic_0079614948_p29085133"></a><a name="zh-cn_topic_0079614948_p29085133"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p21409415201616"><a name="p21409415201616"></a><a name="p21409415201616"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p56441034201616"><a name="p56441034201616"></a><a name="p56441034201616"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614948_row49181313"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614948_p24263425"><a name="zh-cn_topic_0079614948_p24263425"></a><a name="zh-cn_topic_0079614948_p24263425"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614948_p19180389"><a name="zh-cn_topic_0079614948_p19180389"></a><a name="zh-cn_topic_0079614948_p19180389"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614948_p10107670"><a name="zh-cn_topic_0079614948_p10107670"></a><a name="zh-cn_topic_0079614948_p10107670"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s6a7fc85aeb5e45b0b6b5f3c3337f3c4e"></a>

请求参数：

“Content-Type“的详细描述请参见 [PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

**请求示例：**

将[创建Pod](创建Pod.md)创建的Pod的label更新为pod-test2。

Content-Type: application/merge-patch+json

```
{
    "metadata": {
        "labels": {
            "name": "pod-test2"
        }
    }
}
```

## 响应消息<a name="s55aebe546007422f85cedc60f252aeb0"></a>

**响应参数：**

响应参数的详细描述请参见[表2](数据结构.md#zh-cn_topic_0079614925_table60388168)。

**响应示例：**

```
{
  "kind": "Pod",
  "apiVersion": "v1",
  "metadata": {
    "name": "pod-test",
    "namespace": "namespace-test",
    "selfLink": "/api/v1/namespaces/namespace-test/pods/pod-test",
    "uid": "3b99abe8-b032-11e8-9d5d-c88d83be759f",
    "resourceVersion": "5254098",
    "creationTimestamp": "2018-09-04T11:04:02Z",
    "labels": {
      "name": "pod-test2"
    },
    "annotations": {
      "kubernetes.io/availablezone": "dc1",
      "network.alpha.kubernetes.io/network": "[{\"name\":\"namespace-test-dc1-default-network\",\"interface\":\"eth0\",\"network_plane\":\"default\"}]"
    },
    "enable": true
  },
  "spec": {
    "containers": [
      {
        "name": "test",
        "image": "redis:latest",
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
        "imagePullPolicy": "Always"
      }
    ],
    "restartPolicy": "Always",
    "terminationGracePeriodSeconds": 30,
    "dnsPolicy": "ClusterFirst",
    "nodeName": "c0dd6256-195a-e811-90a2-10c17294fcbc",
    "securityContext": {

    },
    "imagePullSecrets": [
      {
        "name": "imagepull-secret"
      }
    ],
    "schedulerName": "default-scheduler",
    "tolerations": [
      {
        "key": "node.kubernetes.io/not-ready",
        "operator": "Exists",
        "effect": "NoExecute",
        "tolerationSeconds": 300
      },
      {
        "key": "node.kubernetes.io/unreachable",
        "operator": "Exists",
        "effect": "NoExecute",
        "tolerationSeconds": 300
      }
    ]
  },
  "status": {
    "phase": "Running",
    "conditions": [
      {
        "type": "Initialized",
        "status": "True",
        "lastProbeTime": null,
        "lastTransitionTime": "2018-09-04T11:04:03Z"
      },
      {
        "type": "Ready",
        "status": "False",
        "lastProbeTime": null,
        "lastTransitionTime": "2018-09-04T11:08:55Z",
        "reason": "ContainersNotReady",
        "message": "containers with unready status: [test]"
      },
      {
        "type": "PodScheduled",
        "status": "True",
        "lastProbeTime": null,
        "lastTransitionTime": "2018-09-04T11:04:02Z"
      }
    ],
    "hostIP": "192.149.117.100",
    "startTime": "2018-09-04T11:04:03Z",
    "containerStatuses": [
      {
        "name": "test",
        "state": {
          "waiting": {
            "reason": "ErrImagePull",
            "message": "rpc error: code = Unknown desc = Error response from daemon: Get https://registry-1.docker.io/v2/: net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers)"
          }
        },
        "lastState": {
          "terminated": {
            "exitCode": 0,
            "reason": "Completed",
            "startedAt": "2018-09-04T11:04:23Z",
            "finishedAt": "2018-09-04T11:08:33Z",
            "containerID": "docker://f867ab7d5c68a86fc695e4d3e5f1912fdb8f98f5029ca96032b4d5d407d9a75c"
          }
        },
        "ready": false,
        "restartCount": 0,
        "image": "redis:latest",
        "imageID": ""
      }
    ],
    "qosClass": "Guaranteed",
    "managementIP": "172.28.0.17"
  }
}
```

## 状态码<a name="s1475b257e1dc4d05a32f69a2a126377c"></a>

[表3](#zh-cn_topic_0079614948_table51397302)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079614948_table51397302"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614948_row10764825"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p58289285201616"><a name="p58289285201616"></a><a name="p58289285201616"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p23811654201616"><a name="p23811654201616"></a><a name="p23811654201616"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614948_row40433035"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614948_p53850421"><a name="zh-cn_topic_0079614948_p53850421"></a><a name="zh-cn_topic_0079614948_p53850421"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614948_p66916835"><a name="zh-cn_topic_0079614948_p66916835"></a><a name="zh-cn_topic_0079614948_p66916835"></a>This operation succeeds, and the JSON of a Pod object is returned.</p>
</td>
</tr>
</tbody>
</table>

