# 删除所有Secret<a name="cci_02_3079"></a>

## 功能介绍<a name="section44856736"></a>

删除Namespace下所有Secret。

## URI<a name="section1057444"></a>

DELETE /api/v1/namespaces/\{namespace\}/secrets

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

<a name="d0e14442"></a>
<table><thead align="left"><tr id="row49778871"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.1"><p id="p5556711"><a name="p5556711"></a><a name="p5556711"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11%" id="mcps1.2.4.1.2"><p id="p47440419"><a name="p47440419"></a><a name="p47440419"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="70%" id="mcps1.2.4.1.3"><p id="p17468756"><a name="p17468756"></a><a name="p17468756"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row50676091"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p11122696"><a name="p11122696"></a><a name="p11122696"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p28523165"><a name="p28523165"></a><a name="p28523165"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p28675043"><a name="p28675043"></a><a name="p28675043"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row37921129111715"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p679211299178"><a name="p679211299178"></a><a name="p679211299178"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p87927295175"><a name="p87927295175"></a><a name="p87927295175"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p379222911716"><a name="p379222911716"></a><a name="p379222911716"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
<tr id="row56748800"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p33250065"><a name="p33250065"></a><a name="p33250065"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p8900776"><a name="p8900776"></a><a name="p8900776"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p49874218"><a name="p49874218"></a><a name="p49874218"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row46214784"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p52410000"><a name="p52410000"></a><a name="p52410000"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p17351617"><a name="p17351617"></a><a name="p17351617"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p63303738"><a name="p63303738"></a><a name="p63303738"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row32862738"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p44636107"><a name="p44636107"></a><a name="p44636107"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p58754913"><a name="p58754913"></a><a name="p58754913"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p61527483"><a name="p61527483"></a><a name="p61527483"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row485591015188"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p2855510151815"><a name="p2855510151815"></a><a name="p2855510151815"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p1385591014181"><a name="p1385591014181"></a><a name="p1385591014181"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p885521018181"><a name="p885521018181"></a><a name="p885521018181"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row16876437"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p24814161"><a name="p24814161"></a><a name="p24814161"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p63790021"><a name="p63790021"></a><a name="p63790021"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p66718106"><a name="p66718106"></a><a name="p66718106"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row63592048"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p50682297"><a name="p50682297"></a><a name="p50682297"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p11625398"><a name="p11625398"></a><a name="p11625398"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p2133200"><a name="p2133200"></a><a name="p2133200"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row19198803"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.1 "><p id="p11599202"><a name="p11599202"></a><a name="p11599202"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="p11330"><a name="p11330"></a><a name="p11330"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.4.1.3 "><p id="p917787"><a name="p917787"></a><a name="p917787"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section9517004"></a>

N/A

## 响应消息<a name="section18544176"></a>

**响应参数**：

响应参数的详细描述请参见[表73](数据结构.md#table37251757105918)。

**响应示例：**

```

```

## 状态码<a name="section32679856"></a>

[表3](#d0e14569)描述API的状态码。

**表 3**  状态码

<a name="d0e14569"></a>
<table><thead align="left"><tr id="row25575097"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p58316938"><a name="p58316938"></a><a name="p58316938"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p26051532"><a name="p26051532"></a><a name="p26051532"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row29799334"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p64935873"><a name="p64935873"></a><a name="p64935873"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p28437418"><a name="p28437418"></a><a name="p28437418"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

