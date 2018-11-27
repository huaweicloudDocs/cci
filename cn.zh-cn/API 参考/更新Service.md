# 更新Service<a name="cci_02_3054"></a>

## 功能介绍<a name="s79a46a3bbf834e65a768cf502c42239e"></a>

更新Service。

其中以下字段支持更新：

-   metadata.labels
-   metadata.annotations
-   spec.externalTrafficPolicy
-   spec.sessionAffinity
-   spec.type

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >spec.type的值，可更新的优先级为LoadBalancer\>ClusterIP，即当spec.type的值为ClusterIP时，可更新为LoadBalancer；当spec.type的值为LoadBalancer时，spec.type不可更新。  

-   spec.port
-   spec.selector
-   spec.externalIPs
-   spec.loadBalancerIP
-   spec.loadBalancerSourceRanges

## URI<a name="s2bcf1feaf0bc43ee938e4fcc63b3849c"></a>

PATCH /api/v1/namespaces/\{namespace\}/services/\{name\}

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the Service.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079614894_table66627661"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614894_row3622792"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614894_p25010772"><a name="zh-cn_topic_0079614894_p25010772"></a><a name="zh-cn_topic_0079614894_p25010772"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p38778720203035"><a name="p38778720203035"></a><a name="p38778720203035"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0079614894_p14503239"><a name="zh-cn_topic_0079614894_p14503239"></a><a name="zh-cn_topic_0079614894_p14503239"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614894_row33911744"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614894_p62496749"><a name="zh-cn_topic_0079614894_p62496749"></a><a name="zh-cn_topic_0079614894_p62496749"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614894_p29071927"><a name="zh-cn_topic_0079614894_p29071927"></a><a name="zh-cn_topic_0079614894_p29071927"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614894_p6015877"><a name="zh-cn_topic_0079614894_p6015877"></a><a name="zh-cn_topic_0079614894_p6015877"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s6972b4d28cf840328e55c95e180ccd87"></a>

**请求参数：**

“Content-Type“的详细描述请参见 [PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

**请求示例：**

将[创建Service](创建Service.md)创建的Service的port更新为8001。

```
Content-Type: application/merge-patch+json
```

```
{
    "spec": {
        "ports": [
            {
                "name": "service0",
                "protocol": "TCP",
                "port": 8001,
                "targetPort": 80
            }
        ]
    }
}
```

## 响应消息<a name="sab68cc958da442f79a8bdd2c90aae544"></a>

**响应参数：**

响应参数的详细描述请参见[表102](公共参数.md#zh-cn_topic_0079615000_ref458759328)。

**响应示例：**

```
{
  "kind": "Service",
  "apiVersion": "v1",
  "metadata": {
    "name": "redis",
    "namespace": "namespace-test",
    "selfLink": "/api/v1/namespaces/namespace-test/services/redis",
    "uid": "0a1f33ee-afe2-11e8-9d5d-c88d83be759f",
    "resourceVersion": "5446372",
    "creationTimestamp": "2018-09-04T01:30:00Z",
    "labels": {
      "app": "redis"
    },
    "enable": true
  },
  "spec": {
    "ports": [
      {
        "protocol": "TCP",
        "port": 8001,
        "targetPort": 8001
      }
    ],
    "selector": {
      "app": "redis"
    },
    "clusterIP": "10.247.160.133",
    "type": "ClusterIP",
    "sessionAffinity": "None"
  },
  "status": {
    "loadBalancer": {

    }
  }
}
```

## 状态码<a name="s3f10ef39263445cabc5b032a11c66233"></a>

[表3](#zh-cn_topic_0079614894_table62778039)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079614894_table62778039"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614894_row29754946"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p50518267203035"><a name="p50518267203035"></a><a name="p50518267203035"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0079614894_p2516162"><a name="zh-cn_topic_0079614894_p2516162"></a><a name="zh-cn_topic_0079614894_p2516162"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614894_row2482606"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614894_p66873365"><a name="zh-cn_topic_0079614894_p66873365"></a><a name="zh-cn_topic_0079614894_p66873365"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614894_p48033505"><a name="zh-cn_topic_0079614894_p48033505"></a><a name="zh-cn_topic_0079614894_p48033505"></a>This operation succeeds, and a Service resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

