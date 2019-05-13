# 删除Secret<a name="cci_02_3078"></a>

## 功能介绍<a name="s33443b62a3884400b29be7af1a63ce43"></a>

删除Secret。

## URI<a name="sb59375acc1994f429f8cabd5b1bf4b80"></a>

DELETE /api/v1/namespaces/\{namespace\}/secrets/\{name\}

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the Secret.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079615047_table8667044"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615047_row41088586"><th class="cellrowborder" valign="top" width="21%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615047_p39841133"><a name="zh-cn_topic_0079615047_p39841133"></a><a name="zh-cn_topic_0079615047_p39841133"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.4.1.2"><p id="p9546513203257"><a name="p9546513203257"></a><a name="p9546513203257"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="65%" id="mcps1.2.4.1.3"><p id="p35070093203257"><a name="p35070093203257"></a><a name="p35070093203257"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615047_row29933900"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615047_p8726850"><a name="zh-cn_topic_0079615047_p8726850"></a><a name="zh-cn_topic_0079615047_p8726850"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615047_p35786256"><a name="zh-cn_topic_0079615047_p35786256"></a><a name="zh-cn_topic_0079615047_p35786256"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615047_p13005663"><a name="zh-cn_topic_0079615047_p13005663"></a><a name="zh-cn_topic_0079615047_p13005663"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row12459239101516"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p15459123941519"><a name="p15459123941519"></a><a name="p15459123941519"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.2 "><p id="p645983931516"><a name="p645983931516"></a><a name="p645983931516"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.4.1.3 "><p id="p04591839121512"><a name="p04591839121512"></a><a name="p04591839121512"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row94287341610"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p1842816321620"><a name="p1842816321620"></a><a name="p1842816321620"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.2 "><p id="p1942820331614"><a name="p1942820331614"></a><a name="p1942820331614"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.4.1.3 "><p id="p1942814313167"><a name="p1942814313167"></a><a name="p1942814313167"></a><strong id="b4118925171612"><a name="b4118925171612"></a><a name="b4118925171612"></a>Deprecated: please use the PropagationPolicy,</strong> this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row455611376163"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p7556837101617"><a name="p7556837101617"></a><a name="p7556837101617"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.2 "><p id="p355611372160"><a name="p355611372160"></a><a name="p355611372160"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.4.1.3 "><p id="p0618105441610"><a name="p0618105441610"></a><a name="p0618105441610"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both.</p>
<p id="p1993135741611"><a name="p1993135741611"></a><a name="p1993135741611"></a>The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
<p id="p128531859181612"><a name="p128531859181612"></a><a name="p128531859181612"></a>Acceptable values are:</p>
<p id="p119622191717"><a name="p119622191717"></a><a name="p119622191717"></a>'<strong id="b3134167121710"><a name="b3134167121710"></a><a name="b3134167121710"></a>Orphan</strong>' - orphan the dependents;</p>
<p id="p0711412178"><a name="p0711412178"></a><a name="p0711412178"></a>'<strong id="b59621295177"><a name="b59621295177"></a><a name="b59621295177"></a>Background</strong>' - allow the garbage collector to delete the dependents in the background;</p>
<p id="p12556153720168"><a name="p12556153720168"></a><a name="p12556153720168"></a>'<strong id="b138210125172"><a name="b138210125172"></a><a name="b138210125172"></a>Foreground</strong>' - a cascading policy that deletes all dependents in the foreground.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="see27f791d3ac4acfa5128d4b61126f2f"></a>

**请求参数：**

请求参数如[表65](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

```
{ 
   "kind": "DeleteOptions", 
   "apiVersion": "v1", 
   "gracePeriodSeconds": 10 
 }
```

## 响应消息<a name="s00e4933458e84b218d5369e1c39bfae6"></a>

**响应参数：**

响应参数的详细描述请参见[表73](数据结构.md#table37251757105918)。

**响应示例：**

```
{
  "kind": "Status",
  "apiVersion": "v1",
  "metadata": {

  },
  "status": "Success",
  "details": {
    "name": "secret-test",
    "kind": "secrets",
    "uid": "e6170b6d-aff6-11e8-8f17-c81fbe371a17"
  },
  "code": 200
}
```

## 状态码<a name="s25ccd5e4fb8949dd9dee7a70d15c0810"></a>

[表3](#zh-cn_topic_0079615047_table5659105)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615047_table5659105"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615047_row40139983"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p36672758203257"><a name="p36672758203257"></a><a name="p36672758203257"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p17703441203257"><a name="p17703441203257"></a><a name="p17703441203257"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615047_row4146549"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615047_p326206"><a name="zh-cn_topic_0079615047_p326206"></a><a name="zh-cn_topic_0079615047_p326206"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615047_p26422695"><a name="zh-cn_topic_0079615047_p26422695"></a><a name="zh-cn_topic_0079615047_p26422695"></a>Delete a secret resource objectre successfully.</p>
</td>
</tr>
</tbody>
</table>

