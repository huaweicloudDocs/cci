# 创建Secret<a name="cci_02_3075"></a>

## 功能介绍<a name="s4e0a1c9701464caaa087bfb241e8faeb"></a>

创建Secret，Kubernetes提供了Secret来处理敏感信息。

## URI<a name="s3cae00f6e7914695ba88e44aa7a2a633"></a>

POST /api/v1/namespaces/\{namespace\}/secrets

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

<a name="zh-cn_topic_0079614900_table43659541"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614900_row65791910"><th class="cellrowborder" valign="top" width="12%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614900_p27544487"><a name="zh-cn_topic_0079614900_p27544487"></a><a name="zh-cn_topic_0079614900_p27544487"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.4.1.2"><p id="p4973534205955"><a name="p4973534205955"></a><a name="p4973534205955"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="76%" id="mcps1.2.4.1.3"><p id="p203075205955"><a name="p203075205955"></a><a name="p203075205955"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614900_row14572292"><td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614900_p39504966"><a name="zh-cn_topic_0079614900_p39504966"></a><a name="zh-cn_topic_0079614900_p39504966"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614900_p45785693"><a name="zh-cn_topic_0079614900_p45785693"></a><a name="zh-cn_topic_0079614900_p45785693"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614900_p17653681"><a name="zh-cn_topic_0079614900_p17653681"></a><a name="zh-cn_topic_0079614900_p17653681"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079614900_d0e9414"></a>

**请求参数：**

请求参数请参见[表123](数据结构.md#zh-cn_topic_0079614900_ref458786458)。

**请求示例：**

```
{
    "apiVersion": "v1",
    "kind": "Secret",
    "metadata": {
        "name": "secret-test"
    },
    "type": "Opaque",
    "data": {
        "key1": "MWYyZDFlMmU2N2Rm",
        "key2": "YWRtaW4="
    }
}
```

## 响应消息<a name="s08d56e5f4e57452da0a49400212440a4"></a>

**响应参数：**

响应参数的详细描述请参见[表123](数据结构.md#zh-cn_topic_0079614900_ref458786458)。

**响应示例：**

```
{
    "kind": "Secret",
    "apiVersion": "v1",
    "metadata": {
        "name": "secret-test",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/secrets/secret-test",
        "uid": "e6170b6d-aff6-11e8-8f17-c81fbe371a17",
        "resourceVersion": "5177770",
        "creationTimestamp": "2018-09-04T03:59:19Z",
        "enable": true
    },
    "data": {
        "key1": "MWYyZDFlMmU2N2Rm",
        "key2": "YWRtaW4="
    },
    "type": "Opaque"
}
```

## 状态码<a name="s50f1049a6a4d404c895cf636eb8f3bf1"></a>

[表3](#zh-cn_topic_0079614900_table46761928)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079614900_table46761928"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614900_row33254664"><th class="cellrowborder" valign="top" width="21%" id="mcps1.2.3.1.1"><p id="p55616028205955"><a name="p55616028205955"></a><a name="p55616028205955"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="79%" id="mcps1.2.3.1.2"><p id="p8604418205955"><a name="p8604418205955"></a><a name="p8604418205955"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row55054141495"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="p1150519141498"><a name="p1150519141498"></a><a name="p1150519141498"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="p153061316630"><a name="p153061316630"></a><a name="p153061316630"></a><span>Created</span></p>
</td>
</tr>
<tr id="row311644427"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="p101174412218"><a name="p101174412218"></a><a name="p101174412218"></a>202</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="p111644025"><a name="p111644025"></a><a name="p111644025"></a><span>Accepted</span></p>
</td>
</tr>
<tr id="row56253412217"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.3.1.1 "><p id="p1562524115217"><a name="p1562524115217"></a><a name="p1562524115217"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="79%" headers="mcps1.2.3.1.2 "><p id="p562519417215"><a name="p562519417215"></a><a name="p562519417215"></a>OK</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

