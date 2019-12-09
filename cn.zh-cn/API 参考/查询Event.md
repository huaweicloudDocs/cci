# 查询Event<a name="cci_02_3092"></a>

## 功能介绍<a name="section6726992"></a>

查询Event详细信息。

## URI<a name="section60542934"></a>

GET /api/v1/namespaces/\{namespace\}/events/\{name\}

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

<a name="d0e45403"></a>
<table><thead align="left"><tr id="row15382595"><th class="cellrowborder" valign="top" width="16.851685168516852%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.11101110111011%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="73.03730373037303%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row50128196"><td class="cellrowborder" valign="top" width="16.851685168516852%" headers="mcps1.2.4.1.1 "><p id="p33852041"><a name="p33852041"></a><a name="p33852041"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="10.11101110111011%" headers="mcps1.2.4.1.2 "><p id="p57660778"><a name="p57660778"></a><a name="p57660778"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="73.03730373037303%" headers="mcps1.2.4.1.3 "><p id="p40011473"><a name="p40011473"></a><a name="p40011473"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row24558937"><td class="cellrowborder" valign="top" width="16.851685168516852%" headers="mcps1.2.4.1.1 "><p id="p43116865"><a name="p43116865"></a><a name="p43116865"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="10.11101110111011%" headers="mcps1.2.4.1.2 "><p id="p2805153"><a name="p2805153"></a><a name="p2805153"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="73.03730373037303%" headers="mcps1.2.4.1.3 "><p id="p8957179144314"><a name="p8957179144314"></a><a name="p8957179144314"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="row16784107"><td class="cellrowborder" valign="top" width="16.851685168516852%" headers="mcps1.2.4.1.1 "><p id="p17335461"><a name="p17335461"></a><a name="p17335461"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="10.11101110111011%" headers="mcps1.2.4.1.2 "><p id="p61995128"><a name="p61995128"></a><a name="p61995128"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="73.03730373037303%" headers="mcps1.2.4.1.3 "><p id="p12754151974311"><a name="p12754151974311"></a><a name="p12754151974311"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8015500"></a>

N/A

## 响应消息<a name="section5030644"></a>

**响应参数：**

响应参数请参见[表127](数据结构.md#table134439518556)。

**响应示例**：

```
{
    "kind": "Event",
    "apiVersion": "v1",
    "metadata": {
        "name": "deployment-test-57f7cff77c-5x5tw.1550e534d2d8a5ef",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/events/deployment-test-57f7cff77c-5x5tw.1550e534d2d8a5ef",
        "uid": "0122b5b2-af79-11e8-8f17-c81fbe371a17",
        "resourceVersion": "760533",
        "creationTimestamp": "2018-09-03T12:58:07Z",
        "enable": true
    },
    "involvedObject": {
        "kind": "Pod",
        "namespace": "namespace-test",
        "name": "deployment-test-57f7cff77c-5x5tw",
        "uid": "010fec39-af79-11e8-8f17-c81fbe371a17",
        "apiVersion": "v1",
        "resourceVersion": "5036865"
    },
    "reason": "Scheduled",
    "message": "Successfully assigned deployment-test-57f7cff77c-5x5tw to c0dd6256-195a-e811-90a2-10c17294fcbc",
    "source": {
        "component": "default-scheduler"
    },
    "firstTimestamp": "2018-09-03T12:58:07Z",
    "lastTimestamp": "2018-09-03T12:58:07Z",
    "count": 1,
    "type": "Normal",
    "eventTime": null,
    "reportingComponent": "",
    "reportingInstance": ""
}
```

## 状态码<a name="section45275797"></a>

[表3](#d0e45532)描述API的状态码。

**表 3**  状态码

<a name="d0e45532"></a>
<table><thead align="left"><tr id="row18260744"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p2725313"><a name="p2725313"></a><a name="p2725313"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p19423770"><a name="p19423770"></a><a name="p19423770"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row29821499"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p66731213"><a name="p66731213"></a><a name="p66731213"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p36519159"><a name="p36519159"></a><a name="p36519159"></a>This operation succeeds, and an Event resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

