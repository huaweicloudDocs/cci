# 替换Service<a name="cci_02_3052"></a>

## 功能介绍<a name="s7f16b6de4e854b61a40ec42af83c7a24"></a>

替换Service。

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

## URI<a name="sd473d9d2d140486eb450698f18eb16e1"></a>

PUT /api/v1/namespaces/\{namespace\}/services/\{name\}

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

<a name="zh-cn_topic_0079615066_table59996030"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615066_row4196075"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615066_p4337788"><a name="zh-cn_topic_0079615066_p4337788"></a><a name="zh-cn_topic_0079615066_p4337788"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p45173014195352"><a name="p45173014195352"></a><a name="p45173014195352"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0079615066_p6069154"><a name="zh-cn_topic_0079615066_p6069154"></a><a name="zh-cn_topic_0079615066_p6069154"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615066_row21839497"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615066_p24168795"><a name="zh-cn_topic_0079615066_p24168795"></a><a name="zh-cn_topic_0079615066_p24168795"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615066_p11515394"><a name="zh-cn_topic_0079615066_p11515394"></a><a name="zh-cn_topic_0079615066_p11515394"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615066_p60331750"><a name="zh-cn_topic_0079615066_p60331750"></a><a name="zh-cn_topic_0079615066_p60331750"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079615066_ref458765758"></a>

**响应参数：**

请求参数的详细描述请参见[表102](数据结构.md#zh-cn_topic_0079615000_ref458759328)。

**请求示例：**

将[创建Service](创建Service.md)创建的Service的port替换为8080。

```
{
  "kind": "Service",
  "apiVersion": "v1",
  "metadata": {
    "name": "redis",
    "namespace": "namespace-test",
    "selfLink": "/api/v1/namespaces/namespace-test/services/redis",
    "uid": "0a1f33ee-afe2-11e8-9d5d-c88d83be759f",
    "resourceVersion": "5153408",
    "creationTimestamp": "2018-09-04T01:30:00Z",
    "labels": {
      "app": "redis"
    },
    "enable": true
  },
  "spec": {
    "ports": [
      {
        "name": "service0",
        "protocol": "TCP",
        "port": 8000,
        "targetPort": 80
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

## 响应消息<a name="s45b51f911829442cae934355300a440d"></a>

**响应参数：**

响应参数的详细描述请参见[表102](数据结构.md#zh-cn_topic_0079615000_ref458759328)。

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
    "resourceVersion": "5446752",
    "creationTimestamp": "2018-09-04T01:30:00Z",
    "labels": {
      "app": "redis"
    },
    "enable": true
  },
  "spec": {
    "ports": [
      {
        "name": "service0",
        "protocol": "TCP",
        "port": 8001,
        "targetPort": 80
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

## 状态码<a name="s5ba1a0225c3c4dd8948fdd7a6c393876"></a>

[表3](#zh-cn_topic_0079615066_table3093358)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615066_table3093358"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615066_row66569734"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p53137435195352"><a name="p53137435195352"></a><a name="p53137435195352"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0079615066_p19540130"><a name="zh-cn_topic_0079615066_p19540130"></a><a name="zh-cn_topic_0079615066_p19540130"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615066_row39246670"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615066_p24863727"><a name="zh-cn_topic_0079615066_p24863727"></a><a name="zh-cn_topic_0079615066_p24863727"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615066_p696045"><a name="zh-cn_topic_0079615066_p696045"></a><a name="zh-cn_topic_0079615066_p696045"></a>This operation succeeds, and a Service resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

