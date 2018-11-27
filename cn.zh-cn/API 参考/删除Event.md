# 删除Event<a name="cci_02_3094"></a>

## 功能描述<a name="section1686113493165"></a>

删除Event。

## URI<a name="section8403243161416"></a>

DELETE /api/v1/namespaces/\{namespace\}/events/\{name\}

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the event.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079615000_table64523107"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615000_row55516030"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615000_p504568"><a name="zh-cn_topic_0079615000_p504568"></a><a name="zh-cn_topic_0079615000_p504568"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.4.1.2"><p id="p64287338205444"><a name="p64287338205444"></a><a name="p64287338205444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="68%" id="mcps1.2.4.1.3"><p id="p39891894205444"><a name="p39891894205444"></a><a name="p39891894205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615000_row48602122"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615000_p44457847"><a name="zh-cn_topic_0079615000_p44457847"></a><a name="zh-cn_topic_0079615000_p44457847"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615000_p44315844"><a name="zh-cn_topic_0079615000_p44315844"></a><a name="zh-cn_topic_0079615000_p44315844"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p32813593"><a name="zh-cn_topic_0079615000_p32813593"></a><a name="zh-cn_topic_0079615000_p32813593"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row1221215134810"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p11224155482"><a name="p11224155482"></a><a name="p11224155482"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="p11221415194810"><a name="p11221415194810"></a><a name="p11221415194810"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.4.1.3 "><p id="p132214159487"><a name="p132214159487"></a><a name="p132214159487"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row2365142013487"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p236582084810"><a name="p236582084810"></a><a name="p236582084810"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="p1136592054810"><a name="p1136592054810"></a><a name="p1136592054810"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.4.1.3 "><p id="p18365172011486"><a name="p18365172011486"></a><a name="p18365172011486"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row1615923164812"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p16151123204818"><a name="p16151123204818"></a><a name="p16151123204818"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="p2615132312481"><a name="p2615132312481"></a><a name="p2615132312481"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="68%" headers="mcps1.2.4.1.3 "><p id="p20615523144820"><a name="p20615523144820"></a><a name="p20615523144820"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: 'Orphan' - orphan the dependents; 'Background' - allow the garbage collector to delete the dependents in the background; 'Foreground' - a cascading policy that deletes all dependents in the foreground.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section947084713911"></a>

**请求参数：**

请求参数如[表65](公共参数.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

```
{ 
   "kind": "DeleteOptions", 
   "apiVersion": "v1", 
   "gracePeriodSeconds": 0 
 }
```

## 响应消息<a name="section61819725020"></a>

**响应参数**

响应参数的详细描述请参见[表73](公共参数.md#table37251757105918)。

**响应示例**

```

```

## 状态码<a name="s50f1049a6a4d404c895cf636eb8f3bf1"></a>

**表 3**  状态码

<a name="zh-cn_topic_0079614900_table46761928"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614900_row33254664"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p55616028205955"><a name="p55616028205955"></a><a name="p55616028205955"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p8604418205955"><a name="p8604418205955"></a><a name="p8604418205955"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614900_row41084259"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p148891415121113"><a name="p148891415121113"></a><a name="p148891415121113"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1788991571115"><a name="p1788991571115"></a><a name="p1788991571115"></a>OK</p>
</td>
</tr>
</tbody>
</table>

