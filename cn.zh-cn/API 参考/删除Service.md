# 删除Service<a name="cci_02_3049"></a>

## 功能介绍<a name="se5309007813b47538be7080cd63898e3"></a>

删除Service。

## URI<a name="s6d0d073ca7cd41c79bd61a816536f9a2"></a>

DELETE /api/v1/namespaces/\{namespace\}/services/\{name\}

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

<a name="zh-cn_topic_0079615016_table17955773"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615016_row34849842"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615016_p4264914"><a name="zh-cn_topic_0079615016_p4264914"></a><a name="zh-cn_topic_0079615016_p4264914"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p47001612205713"><a name="p47001612205713"></a><a name="p47001612205713"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p49034188205713"><a name="p49034188205713"></a><a name="p49034188205713"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615016_row15472413"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615016_p45305951"><a name="zh-cn_topic_0079615016_p45305951"></a><a name="zh-cn_topic_0079615016_p45305951"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615016_p45903438"><a name="zh-cn_topic_0079615016_p45903438"></a><a name="zh-cn_topic_0079615016_p45903438"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615016_p27190993"><a name="zh-cn_topic_0079615016_p27190993"></a><a name="zh-cn_topic_0079615016_p27190993"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s716a126cd0214f9eac118df493501969"></a>

N/A

## 响应消息<a name="s2203b49907514457834d6215429d3135"></a>

**响应参数：**

响应参数的详细描述请参见[表73](公共参数.md#table37251757105918)。

**响应示例：**

```
{
  "kind": "Status",
  "apiVersion": "v1",
  "metadata": {

  },
  "status": "Success",
  "code": 200
}
```

## 状态码<a name="s10d425dd6e6d43a394ec0cd15cf7b233"></a>

[表3](#zh-cn_topic_0079615016_ref458764468)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615016_ref458764468"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615016_row40325647"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p25374999205713"><a name="p25374999205713"></a><a name="p25374999205713"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p42109061205713"><a name="p42109061205713"></a><a name="p42109061205713"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615016_row23578293"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615016_p30793598"><a name="zh-cn_topic_0079615016_p30793598"></a><a name="zh-cn_topic_0079615016_p30793598"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615016_p11253479"><a name="zh-cn_topic_0079615016_p11253479"></a><a name="zh-cn_topic_0079615016_p11253479"></a>Delete a Service resource objectre successfully.</p>
</td>
</tr>
</tbody>
</table>

