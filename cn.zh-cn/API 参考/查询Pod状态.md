# 查询Pod状态<a name="cci_02_3011"></a>

## 功能介绍<a name="s14b3085e84f44f248c15900b7a9ae75e"></a>

查询Pod对象的状态。

## URI<a name="s2146020c33a84ca5aa9bc6e54586edc9"></a>

GET /api/v1/namespaces/\{namespace\}/pods/\{name\}/status

**Path 参数**

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
<tr id="row115455519446"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p15341161164510"><a name="p15341161164510"></a><a name="p15341161164510"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p1234131114458"><a name="p1234131114458"></a><a name="p1234131114458"></a>Name of the Pod.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079614904_table61950116"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614904_row42466880"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614904_p17265247"><a name="zh-cn_topic_0079614904_p17265247"></a><a name="zh-cn_topic_0079614904_p17265247"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="30.303030303030305%" id="mcps1.2.4.1.2"><p id="p25470926205834"><a name="p25470926205834"></a><a name="p25470926205834"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.2.4.1.3"><p id="p49879135205834"><a name="p49879135205834"></a><a name="p49879135205834"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614904_row1125057"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614904_p24020754"><a name="zh-cn_topic_0079614904_p24020754"></a><a name="zh-cn_topic_0079614904_p24020754"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614904_p66632916"><a name="zh-cn_topic_0079614904_p66632916"></a><a name="zh-cn_topic_0079614904_p66632916"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614904_p28557102"><a name="zh-cn_topic_0079614904_p28557102"></a><a name="zh-cn_topic_0079614904_p28557102"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="s279a234cda4443f0afa7d8de9b799a5a"></a>

**响应参数：**

响应参数的详细描述请参见[表2](公共参数.md#zh-cn_topic_0079614925_table60388168)。

**响应示例：**

```
{
  "kind": "Pod",
  "apiVersion": "v1",
  "metadata": {
    "name": "pod-test",
    "namespace": "namespace-test",
    "selfLink": "/api/v1/namespaces/namespace-test/pods/pod-test",
    "uid": "8b985a27-af74-11e8-9d5d-c88d83be759f",
    "resourceVersion": "5030610",
    "creationTimestamp": "2018-09-03T12:26:12Z",
    "labels": {
      "name": "pod-test"
    },
    "annotations": {
      "cri.cci.io/container-type": "secure-container",
      "kubernetes.io/availablezone": "dc1",
      "network.alpha.kubernetes.io/network": "[{\"name\":\"namespace-test-dc1-default-network\",\"interface\":\"eth0\",\"network_plane\":\"default\"}]"
    },
    "enable": true
  },
  "spec": {
    "containers": [
      {
        "name": "test",
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
        "lastTransitionTime": "2018-09-03T12:26:12Z"
      },
      {
        "type": "Ready",
        "status": "True",
        "lastProbeTime": null,
        "lastTransitionTime": "2018-09-03T12:26:16Z"
      },
      {
        "type": "PodScheduled",
        "status": "True",
        "lastProbeTime": null,
        "lastTransitionTime": "2018-09-03T12:26:12Z"
      }
    ],
    "podIP": "192.168.245.185",
    "startTime": "2018-09-03T12:26:12Z",
    "containerStatuses": [
      {
        "name": "test",
        "state": {
          "running": {
            "startedAt": "2018-09-03T12:26:16Z"
          }
        },
        "lastState": {

        },
        "ready": true,
        "restartCount": 0,
        "image": "redis:3.0",
        "imageID": "docker-pullable://redis@sha256:3ab7046bd035a47aa06963d8240651d00b57e82dab07ba374ad01f84dfa1230c",
        "containerID": "docker://aee55d8dedb8371f96aa5d5116f69a53bf1cb23afe1802567c24081514d3b048"
      }
    ],
    "qosClass": "Guaranteed",
    "managementIP": "172.28.0.17"
  }
}
```

## 状态码<a name="s8a2da3e1bb8a49d2af7cf2027ab3fea0"></a>

[表3](#zh-cn_topic_0079614908_table56267310)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079614908_table56267310"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614908_row31065142"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p26385296203057"><a name="p26385296203057"></a><a name="p26385296203057"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p56834228203057"><a name="p56834228203057"></a><a name="p56834228203057"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614908_row39832915"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614908_p5240702"><a name="zh-cn_topic_0079614908_p5240702"></a><a name="zh-cn_topic_0079614908_p5240702"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614908_p21843730"><a name="zh-cn_topic_0079614908_p21843730"></a><a name="zh-cn_topic_0079614908_p21843730"></a>This operation succeeds, and the JSON of a Pod object is returned.</p>
</td>
</tr>
</tbody>
</table>

