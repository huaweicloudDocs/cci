# 删除所有Network<a name="cci_02_2014"></a>

## 功能介绍<a name="section1686113493165"></a>

删除指定namespace下的所有Network对象。

## URI<a name="section8403243161416"></a>

DELETE /apis/networking.cci.io/v1beta1/namespaces/\{namespace\}/networks

**表 1**  Path参数

<a name="zh-cn_topic_0079615000_table64523107"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615000_row55516030"><th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0079615000_p504568"><a name="zh-cn_topic_0079615000_p504568"></a><a name="zh-cn_topic_0079615000_p504568"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="8.080808080808081%" id="mcps1.2.5.1.2"><p id="p64287338205444"><a name="p64287338205444"></a><a name="p64287338205444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="8.080808080808081%" id="mcps1.2.5.1.3"><p id="p10603192911535"><a name="p10603192911535"></a><a name="p10603192911535"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="61.61616161616161%" id="mcps1.2.5.1.4"><p id="p39891894205444"><a name="p39891894205444"></a><a name="p39891894205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615000_row41865316"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615000_p35647420"><a name="zh-cn_topic_0079615000_p35647420"></a><a name="zh-cn_topic_0079615000_p35647420"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615000_p1759884"><a name="zh-cn_topic_0079615000_p1759884"></a><a name="zh-cn_topic_0079615000_p1759884"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p16603929145318"><a name="p16603929145318"></a><a name="p16603929145318"></a><span>String</span></p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table1389318443157"></a>
<table><thead align="left"><tr id="row16893044101510"><th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.2.5.1.1"><p id="p1989354431516"><a name="p1989354431516"></a><a name="p1989354431516"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="8.080808080808081%" id="mcps1.2.5.1.2"><p id="p1908644181512"><a name="p1908644181512"></a><a name="p1908644181512"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="8.080808080808081%" id="mcps1.2.5.1.3"><p id="p149081544151512"><a name="p149081544151512"></a><a name="p149081544151512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="61.61616161616161%" id="mcps1.2.5.1.4"><p id="p7908204415153"><a name="p7908204415153"></a><a name="p7908204415153"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row69086446155"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p59081544101513"><a name="p59081544101513"></a><a name="p59081544101513"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p390815444151"><a name="p390815444151"></a><a name="p390815444151"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p14908444131515"><a name="p14908444131515"></a><a name="p14908444131515"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p1908104418156"><a name="p1908104418156"></a><a name="p1908104418156"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row1390894417156"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p19908444141520"><a name="p19908444141520"></a><a name="p19908444141520"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p1190824413154"><a name="p1190824413154"></a><a name="p1190824413154"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p1592412443158"><a name="p1592412443158"></a><a name="p1592412443158"></a><span>String</span></p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p892424411157"><a name="p892424411157"></a><a name="p892424411157"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row192434410150"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p29241644171519"><a name="p29241644171519"></a><a name="p29241644171519"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p592464417158"><a name="p592464417158"></a><a name="p592464417158"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p8924174431518"><a name="p8924174431518"></a><a name="p8924174431518"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p10924124461513"><a name="p10924124461513"></a><a name="p10924124461513"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row1492474418152"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p69241644201512"><a name="p69241644201512"></a><a name="p69241644201512"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p1192419446152"><a name="p1192419446152"></a><a name="p1192419446152"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p2092454471519"><a name="p2092454471519"></a><a name="p2092454471519"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p59246444153"><a name="p59246444153"></a><a name="p59246444153"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row129244444152"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p1492404461519"><a name="p1492404461519"></a><a name="p1492404461519"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p29244442155"><a name="p29244442155"></a><a name="p29244442155"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p9924344111519"><a name="p9924344111519"></a><a name="p9924344111519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p12924194461519"><a name="p12924194461519"></a><a name="p12924194461519"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row292413445156"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p1594024417159"><a name="p1594024417159"></a><a name="p1594024417159"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p49401244111516"><a name="p49401244111516"></a><a name="p49401244111516"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p1294074411150"><a name="p1294074411150"></a><a name="p1294074411150"></a><span>Integer (int32)</span></p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p1794074431518"><a name="p1794074431518"></a><a name="p1794074431518"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row194054415154"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p1594024417153"><a name="p1594024417153"></a><a name="p1594024417153"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p11940104412159"><a name="p11940104412159"></a><a name="p11940104412159"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p109401044111513"><a name="p109401044111513"></a><a name="p109401044111513"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p15940194461510"><a name="p15940194461510"></a><a name="p15940194461510"></a><span>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion</span></p>
</td>
</tr>
<tr id="row99405448153"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p8940194411515"><a name="p8940194411515"></a><a name="p8940194411515"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p1094014481511"><a name="p1094014481511"></a><a name="p1094014481511"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p5940114410153"><a name="p5940114410153"></a><a name="p5940114410153"></a>Integer (int32)</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p794044421516"><a name="p794044421516"></a><a name="p794044421516"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.</p>
<p id="p179407445157"><a name="p179407445157"></a><a name="p179407445157"></a>The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row1894014448155"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p1194094417157"><a name="p1194094417157"></a><a name="p1194094417157"></a><span>continue</span></p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p139546441152"><a name="p139546441152"></a><a name="p139546441152"></a><span>false</span></p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p39541844171518"><a name="p39541844171518"></a><a name="p39541844171518"></a><span>String</span></p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p49541844201518"><a name="p49541844201518"></a><a name="p49541844201518"></a><span>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</span></p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s716a126cd0214f9eac118df493501969"></a>

N/A

## 响应消息<a name="s2203b49907514457834d6215429d3135"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "Status",
    "apiVersion": "v1",
    "metadata": {},
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
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615016_p11253479"><a name="zh-cn_topic_0079615016_p11253479"></a><a name="zh-cn_topic_0079615016_p11253479"></a>Delete a Service resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

