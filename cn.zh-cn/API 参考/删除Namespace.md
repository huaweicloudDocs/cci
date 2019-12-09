# 删除Namespace<a name="cci_02_3003"></a>

## 功能介绍<a name="sd3cfd7eb5e604cbfacc39f3d39217286"></a>

删除一个Namespace。

## URI<a name="sb360ead1682b4a91886de13dec66f5c4"></a>

DELETE /api/v1/namespaces/\{name\}

**表 1**  Path参数

<a name="table1696332124519"></a>
<table><thead align="left"><tr id="row11961332194516"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.3.1.1"><p id="p396032144518"><a name="p396032144518"></a><a name="p396032144518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="76%" id="mcps1.2.3.1.2"><p id="p18962325454"><a name="p18962325454"></a><a name="p18962325454"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9960327457"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1496113214456"><a name="p1496113214456"></a><a name="p1496113214456"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p796193274515"><a name="p796193274515"></a><a name="p796193274515"></a>Name of the Namespace.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079615060_table31198475"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615060_row10758903"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615060_p66164776"><a name="zh-cn_topic_0079615060_p66164776"></a><a name="zh-cn_topic_0079615060_p66164776"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23%" id="mcps1.2.4.1.2"><p id="p2285494921117"><a name="p2285494921117"></a><a name="p2285494921117"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="44%" id="mcps1.2.4.1.3"><p id="p3931158921117"><a name="p3931158921117"></a><a name="p3931158921117"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615060_row46130559"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615060_p45587811"><a name="zh-cn_topic_0079615060_p45587811"></a><a name="zh-cn_topic_0079615060_p45587811"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615060_p1625174"><a name="zh-cn_topic_0079615060_p1625174"></a><a name="zh-cn_topic_0079615060_p1625174"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615060_p64530307"><a name="zh-cn_topic_0079615060_p64530307"></a><a name="zh-cn_topic_0079615060_p64530307"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="rb4b98780ec4947749cd70a13580cbd2a"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615060_p427182983911"><a name="zh-cn_topic_0079615060_p427182983911"></a><a name="zh-cn_topic_0079615060_p427182983911"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615060_p827162911396"><a name="zh-cn_topic_0079615060_p827162911396"></a><a name="zh-cn_topic_0079615060_p827162911396"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.2.4.1.3 "><p id="a694bff5476754aee8d6cfe59c3b1825d"><a name="a694bff5476754aee8d6cfe59c3b1825d"></a><a name="a694bff5476754aee8d6cfe59c3b1825d"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="r0ac2448870d94693b737e1401fe3c64c"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="a331c14c2f28e4c8a901952fe930ad5c5"><a name="a331c14c2f28e4c8a901952fe930ad5c5"></a><a name="a331c14c2f28e4c8a901952fe930ad5c5"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="a301f889a07ba4c4ab3bd4314bae0df0e"><a name="a301f889a07ba4c4ab3bd4314bae0df0e"></a><a name="a301f889a07ba4c4ab3bd4314bae0df0e"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615060_p157076445396"><a name="zh-cn_topic_0079615060_p157076445396"></a><a name="zh-cn_topic_0079615060_p157076445396"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="r60cb73a9905946e18477437d9bd30d97"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615060_p447118462392"><a name="zh-cn_topic_0079615060_p447118462392"></a><a name="zh-cn_topic_0079615060_p447118462392"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="a318694aa068f4384a683351e4ef97d16"><a name="a318694aa068f4384a683351e4ef97d16"></a><a name="a318694aa068f4384a683351e4ef97d16"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.2.4.1.3 "><p id="ae473bba629a542729271da7f9a71f051"><a name="ae473bba629a542729271da7f9a71f051"></a><a name="ae473bba629a542729271da7f9a71f051"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s868ed9032ac544a8908766b83229eba1"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

```
{
    "kind": "DeleteOptions",
    "apiVersion": "v1",
    "gracePeriodSeconds": 10
}
```

## 响应消息<a name="s40c3210a927d4400b708d17d3f0a3cbe"></a>

N/A

## 状态码<a name="s379564af9d9b4e6c915ee4629fc129e5"></a>

[表3](#zh-cn_topic_0079615060_table44048571)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615060_table44048571"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615060_row48163256"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p4561445121117"><a name="p4561445121117"></a><a name="p4561445121117"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p378306821117"><a name="p378306821117"></a><a name="p378306821117"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615060_row4281684"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615060_p11272110"><a name="zh-cn_topic_0079615060_p11272110"></a><a name="zh-cn_topic_0079615060_p11272110"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615060_p40625737"><a name="zh-cn_topic_0079615060_p40625737"></a><a name="zh-cn_topic_0079615060_p40625737"></a>Delete a Namespace resource objectre successfully.</p>
</td>
</tr>
</tbody>
</table>

