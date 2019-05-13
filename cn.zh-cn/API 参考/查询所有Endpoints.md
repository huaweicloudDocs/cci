# 查询所有Endpoints<a name="cci_02_3126"></a>

## 功能介绍<a name="s929c7f68195e496187ed769a50539e04"></a>

查询Namespace下所有Endpoints

## URI<a name="s3de16f9dad264ecd9bc63f9ea6344f66"></a>

GET /api/v1/namespaces/\{namespace\}/endpoints

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

## 请求消息<a name="sef5c2e860abe4851bf5e58fb868633d9"></a>

N/A

## 响应消息<a name="sd91f7b136258433a922cbc821ade2d1f"></a>

**响应参数：**

响应参数的详细描述请参见[表139](数据结构.md#table219774262719)。

**响应示例：**

```
{
    "kind": "EndpointsList",
    "apiVersion": "v1",
    "metadata": {
        "selfLink": "/api/v1/namespaces/default/endpoints",
        "resourceVersion": "598704"
    },
    "items": [
        {
            "metadata": {
                "name": "kubernetes",
                "namespace": "default",
                "selfLink": "/api/v1/namespaces/default/endpoints/kubernetes",
                "uid": "64593b5d-f83d-11e7-9c3c-fa163eb8ad1a",
                "resourceVersion": "49",
                "creationTimestamp": "2018-01-13T08:40:21Z",
                "enable": true
            },
            "subsets": [
                {
                    "addresses": [
                        {
                            "ip": "192.168.0.64"
                        }
                    ],
                    "ports": [
                        {
                            "name": "https",
                            "port": 5444,
                            "protocol": "TCP"
                        }
                    ]
                }
            ]
        }
    ]
}
```

## 状态码<a name="s1736c40a8a6e4e3dab0ee276f7614231"></a>

**表 3**  状态码

<a name="zh-cn_topic_0079615068_table769899"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615068_row22998005"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p11007541201651"><a name="p11007541201651"></a><a name="p11007541201651"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p19195629201651"><a name="p19195629201651"></a><a name="p19195629201651"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615068_row15320653"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615068_p33013406"><a name="zh-cn_topic_0079615068_p33013406"></a><a name="zh-cn_topic_0079615068_p33013406"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615068_p56840268"><a name="zh-cn_topic_0079615068_p56840268"></a><a name="zh-cn_topic_0079615068_p56840268"></a>This operation succeeds, and a group of Endpoint resource objects is returned.</p>
</td>
</tr>
</tbody>
</table>

