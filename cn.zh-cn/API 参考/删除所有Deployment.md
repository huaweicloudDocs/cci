# 删除所有Deployment<a name="cci_02_3021"></a>

## 功能介绍<a name="section58759520"></a>

删除Namespace下所有Deployment。

## URI<a name="section59073635"></a>

DELETE /apis/apps/v1/namespaces/\{namespace\}/deployments

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

<a name="d0e35322"></a>
<table><thead align="left"><tr id="row32289194"><th class="cellrowborder" valign="top" width="22.45%" id="mcps1.2.4.1.1"><p id="p1219420112592"><a name="p1219420112592"></a><a name="p1219420112592"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.33%" id="mcps1.2.4.1.2"><p id="p17194151113591"><a name="p17194151113591"></a><a name="p17194151113591"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.22%" id="mcps1.2.4.1.3"><p id="p3194121115596"><a name="p3194121115596"></a><a name="p3194121115596"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row47634511"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p519491110591"><a name="p519491110591"></a><a name="p519491110591"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p6194161175912"><a name="p6194161175912"></a><a name="p6194161175912"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p519418117593"><a name="p519418117593"></a><a name="p519418117593"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row1161053"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p1119412114598"><a name="p1119412114598"></a><a name="p1119412114598"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p1419461145915"><a name="p1419461145915"></a><a name="p1419461145915"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p151947119590"><a name="p151947119590"></a><a name="p151947119590"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row23813312"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p8195211125918"><a name="p8195211125918"></a><a name="p8195211125918"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p419514115597"><a name="p419514115597"></a><a name="p419514115597"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p1719512117596"><a name="p1719512117596"></a><a name="p1719512117596"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row57732278"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p13195311115914"><a name="p13195311115914"></a><a name="p13195311115914"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p131952011115915"><a name="p131952011115915"></a><a name="p131952011115915"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p1819519111598"><a name="p1819519111598"></a><a name="p1819519111598"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row64753968"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p11195811155918"><a name="p11195811155918"></a><a name="p11195811155918"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p1719571125915"><a name="p1719571125915"></a><a name="p1719571125915"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p71954112595"><a name="p71954112595"></a><a name="p71954112595"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row25799037"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p14195121110593"><a name="p14195121110593"></a><a name="p14195121110593"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p3196151125919"><a name="p3196151125919"></a><a name="p3196151125919"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p81961311185913"><a name="p81961311185913"></a><a name="p81961311185913"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row43057396"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p31961211135915"><a name="p31961211135915"></a><a name="p31961211135915"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p111962114599"><a name="p111962114599"></a><a name="p111962114599"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p18196191155912"><a name="p18196191155912"></a><a name="p18196191155912"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
<tr id="row164372344353"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p44344342352"><a name="p44344342352"></a><a name="p44344342352"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p124346346359"><a name="p124346346359"></a><a name="p124346346359"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p1243443410355"><a name="p1243443410355"></a><a name="p1243443410355"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row102037522358"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="p11197152183510"><a name="p11197152183510"></a><a name="p11197152183510"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p18198185212357"><a name="p18198185212357"></a><a name="p18198185212357"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="p11198252103514"><a name="p11198252103514"></a><a name="p11198252103514"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section61900675"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

-   只删除Deployment（对应ReplicSet和Pod不删除）

    ```
    {
        "Kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Orphan"
    }
    ```

-   前台级联删除（按照Pod-\>ReplicaSet-\>Deployment的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Foreground"
    }
    ```

-   后台级联删除（按照Deployment-\>ReplicaSet-\>Pod的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Background"
    }
    ```


## 响应消息<a name="section20235168"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "DeploymentList",
    "apiVersion": "apps/v1",
    "metadata": {
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/deployments",
        "resourceVersion": "5039958"
    },
    "items": null
}
```

## 状态码<a name="section47898787"></a>

[表3](#d0e35450)描述API的状态码。

**表 3**  状态码

<a name="d0e35450"></a>
<table><thead align="left"><tr id="row7535426"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p6389758"><a name="p6389758"></a><a name="p6389758"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p47808350"><a name="p47808350"></a><a name="p47808350"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row47271114"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3755051"><a name="p3755051"></a><a name="p3755051"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p28437418"><a name="p28437418"></a><a name="p28437418"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

