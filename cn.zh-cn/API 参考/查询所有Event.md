# 查询所有Event<a name="cci_02_3093"></a>

## 功能介绍<a name="zh-cn_topic_0091433726_section6726992"></a>

查询Namespace下所有Event的详细信息。

## URI<a name="zh-cn_topic_0091433726_section60542934"></a>

GET /api/v1/namespaces/\{namespace\}/events

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

<a name="zh-cn_topic_0091433726_d0e45403"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433726_row15382595"><th class="cellrowborder" valign="top" width="16.85%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433726_p65652297517"><a name="zh-cn_topic_0091433726_p65652297517"></a><a name="zh-cn_topic_0091433726_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.24%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433726_p165661629135114"><a name="zh-cn_topic_0091433726_p165661629135114"></a><a name="zh-cn_topic_0091433726_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="71.91%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433726_p14567629115114"><a name="zh-cn_topic_0091433726_p14567629115114"></a><a name="zh-cn_topic_0091433726_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433726_row50128196"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433726_p33852041"><a name="zh-cn_topic_0091433726_p33852041"></a><a name="zh-cn_topic_0091433726_p33852041"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433726_p57660778"><a name="zh-cn_topic_0091433726_p57660778"></a><a name="zh-cn_topic_0091433726_p57660778"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433726_p40011473"><a name="zh-cn_topic_0091433726_p40011473"></a><a name="zh-cn_topic_0091433726_p40011473"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row158155194316"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="p1223175554312"><a name="p1223175554312"></a><a name="p1223175554312"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="p9231755174312"><a name="p9231755174312"></a><a name="p9231755174312"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="p623175544310"><a name="p623175544310"></a><a name="p623175544310"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433726_row24558937"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433726_p43116865"><a name="zh-cn_topic_0091433726_p43116865"></a><a name="zh-cn_topic_0091433726_p43116865"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433726_p2805153"><a name="zh-cn_topic_0091433726_p2805153"></a><a name="zh-cn_topic_0091433726_p2805153"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433726_p31691062"><a name="zh-cn_topic_0091433726_p31691062"></a><a name="zh-cn_topic_0091433726_p31691062"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433726_row16784107"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433726_p17335461"><a name="zh-cn_topic_0091433726_p17335461"></a><a name="zh-cn_topic_0091433726_p17335461"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433726_p61995128"><a name="zh-cn_topic_0091433726_p61995128"></a><a name="zh-cn_topic_0091433726_p61995128"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433726_p55549451"><a name="zh-cn_topic_0091433726_p55549451"></a><a name="zh-cn_topic_0091433726_p55549451"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433726_row30183012"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433726_p28904890"><a name="zh-cn_topic_0091433726_p28904890"></a><a name="zh-cn_topic_0091433726_p28904890"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433726_p59594790"><a name="zh-cn_topic_0091433726_p59594790"></a><a name="zh-cn_topic_0091433726_p59594790"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433726_p62448653"><a name="zh-cn_topic_0091433726_p62448653"></a><a name="zh-cn_topic_0091433726_p62448653"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row1097911304447"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="p1097983010444"><a name="p1097983010444"></a><a name="p1097983010444"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="p59791130164411"><a name="p59791130164411"></a><a name="p59791130164411"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="p169792305443"><a name="p169792305443"></a><a name="p169792305443"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433726_row25166971"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433726_p25258793"><a name="zh-cn_topic_0091433726_p25258793"></a><a name="zh-cn_topic_0091433726_p25258793"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433726_p32696327"><a name="zh-cn_topic_0091433726_p32696327"></a><a name="zh-cn_topic_0091433726_p32696327"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433726_p31156797"><a name="zh-cn_topic_0091433726_p31156797"></a><a name="zh-cn_topic_0091433726_p31156797"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433726_row11975721"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433726_p30509335"><a name="zh-cn_topic_0091433726_p30509335"></a><a name="zh-cn_topic_0091433726_p30509335"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433726_p55337074"><a name="zh-cn_topic_0091433726_p55337074"></a><a name="zh-cn_topic_0091433726_p55337074"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433726_p53117985"><a name="zh-cn_topic_0091433726_p53117985"></a><a name="zh-cn_topic_0091433726_p53117985"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433726_row8299820"><td class="cellrowborder" valign="top" width="16.85%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433726_p1196789"><a name="zh-cn_topic_0091433726_p1196789"></a><a name="zh-cn_topic_0091433726_p1196789"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="11.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433726_p29831046"><a name="zh-cn_topic_0091433726_p29831046"></a><a name="zh-cn_topic_0091433726_p29831046"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433726_p395656"><a name="zh-cn_topic_0091433726_p395656"></a><a name="zh-cn_topic_0091433726_p395656"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433726_section8015500"></a>

N/A

## 响应消息<a name="zh-cn_topic_0091433726_section5030644"></a>

**响应参数：**

响应参数如[表133](数据结构.md#table2908120115216)所示。

**表 3**  EventSource字段数据结构说明

<a name="table94641515173415"></a>
<table><thead align="left"><tr id="row9476131511345"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p11480151553412"><a name="p11480151553412"></a><a name="p11480151553412"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="p848751511346"><a name="p848751511346"></a><a name="p848751511346"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="61.62%" id="mcps1.2.4.1.3"><p id="p194941315153411"><a name="p194941315153411"></a><a name="p194941315153411"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15497141515348"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p17502161593411"><a name="p17502161593411"></a><a name="p17502161593411"></a>component</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p13505115103418"><a name="p13505115103418"></a><a name="p13505115103418"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p16306820173518"><a name="p16306820173518"></a><a name="p16306820173518"></a>Component from which the event is generated.</p>
</td>
</tr>
<tr id="row25101115143414"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p17515715183418"><a name="p17515715183418"></a><a name="p17515715183418"></a>host</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p2518171512342"><a name="p2518171512342"></a><a name="p2518171512342"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p8324143113358"><a name="p8324143113358"></a><a name="p8324143113358"></a>Node name on which the event is generated.</p>
</td>
</tr>
</tbody>
</table>

**响应示例：**

```
{
  "kind": "EventList",
  "apiVersion": "v1",
  "metadata": {
    "selfLink": "/api/v1/namespaces/namespace-test/events",
    "resourceVersion": "764693"
  },
  "items": [
    {
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
    },
    {
      "metadata": {
        "name": "deployment-test-57f7cff77c-5x5tw.1550e534d3105acd",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/events/deployment-test-57f7cff77c-5x5tw.1550e534d3105acd",
        "uid": "0123faea-af79-11e8-8f17-c81fbe371a17",
        "resourceVersion": "760542",
        "creationTimestamp": "2018-09-03T12:58:07Z",
        "enable": true
      },
      "involvedObject": {
        "kind": "Pod",
        "namespace": "namespace-test",
        "name": "deployment-test-57f7cff77c-5x5tw",
        "uid": "010fec39-af79-11e8-8f17-c81fbe371a17",
        "apiVersion": "v1",
        "resourceVersion": "5036870"
      },
      "reason": "SuccessfulMountVolume",
      "message": "Successfully mounted volumes for pod \"deployment-test-57f7cff77c-5x5tw_namespace-test(010fec39-af79-11e8-8f17-c81fbe371a17)\"",
      "source": {
        "component": "kubelet",
        "host": "c0dd6256-195a-e811-90a2-10c17294fcbc"
      },
      "firstTimestamp": "2018-09-03T12:58:07Z",
      "lastTimestamp": "2018-09-03T12:58:12Z",
      "count": 2,
      "type": "Normal",
      "eventTime": null,
      "reportingComponent": "",
      "reportingInstance": ""
    },
    {
      "metadata": {
        "name": "deployment-test-57f7cff77c-5x5tw.1550e5354a5915e0",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/events/deployment-test-57f7cff77c-5x5tw.1550e5354a5915e0",
        "uid": "025554a4-af79-11e8-8f17-c81fbe371a17",
        "resourceVersion": "760536",
        "creationTimestamp": "2018-09-03T12:58:09Z",
        "enable": true
      },
      "involvedObject": {
        "kind": "Pod",
        "namespace": "namespace-test",
        "name": "deployment-test-57f7cff77c-5x5tw",
        "uid": "010fec39-af79-11e8-8f17-c81fbe371a17",
        "apiVersion": "v1",
        "resourceVersion": "5036870",
        "fieldPath": "spec.containers{container-0}"
      },
      "reason": "Pulling",
      "message": "pulling image \"100.125.5.235:20202/cci_z00425431/redis:V1\"",
      "source": {
        "component": "kubelet",
        "host": "c0dd6256-195a-e811-90a2-10c17294fcbc"
      },
      "firstTimestamp": "2018-09-03T12:58:09Z",
      "lastTimestamp": "2018-09-03T12:58:09Z",
      "count": 1,
      "type": "Normal",
      "eventTime": null,
      "reportingComponent": "",
      "reportingInstance": ""
    }
  ]
}
```

## 状态码<a name="zh-cn_topic_0091433726_section45275797"></a>

[表4](#zh-cn_topic_0091433726_d0e45532)描述API的状态码。

**表 4**  状态码

<a name="zh-cn_topic_0091433726_d0e45532"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433726_row18260744"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433726_p2725313"><a name="zh-cn_topic_0091433726_p2725313"></a><a name="zh-cn_topic_0091433726_p2725313"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433726_p19423770"><a name="zh-cn_topic_0091433726_p19423770"></a><a name="zh-cn_topic_0091433726_p19423770"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433726_row29821499"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433726_p66731213"><a name="zh-cn_topic_0091433726_p66731213"></a><a name="zh-cn_topic_0091433726_p66731213"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433726_p36519159"><a name="zh-cn_topic_0091433726_p36519159"></a><a name="zh-cn_topic_0091433726_p36519159"></a>This operation succeeds, and an Event resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

