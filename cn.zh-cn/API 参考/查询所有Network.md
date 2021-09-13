# 查询所有Network<a name="cci_02_2013"></a>

## 功能介绍<a name="section1686113493165"></a>

查询指定namespace下的所有Network对象。

## URI<a name="section8403243161416"></a>

GET /apis/networking.cci.io/v1beta1/namespaces/\{namespace\}/networks

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
<tbody><tr id="zh-cn_topic_0079615000_row48602122"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615000_p44457847"><a name="zh-cn_topic_0079615000_p44457847"></a><a name="zh-cn_topic_0079615000_p44457847"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615000_p44315844"><a name="zh-cn_topic_0079615000_p44315844"></a><a name="zh-cn_topic_0079615000_p44315844"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p19603192912532"><a name="p19603192912532"></a><a name="p19603192912532"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615000_p32813593"><a name="zh-cn_topic_0079615000_p32813593"></a><a name="zh-cn_topic_0079615000_p32813593"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row384544205011"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p23101228"><a name="p23101228"></a><a name="p23101228"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p59260195"><a name="p59260195"></a><a name="p59260195"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p1960315294535"><a name="p1960315294535"></a><a name="p1960315294535"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p35346519"><a name="p35346519"></a><a name="p35346519"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row1484444195013"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p64917804"><a name="p64917804"></a><a name="p64917804"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p23850806"><a name="p23850806"></a><a name="p23850806"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p360352965319"><a name="p360352965319"></a><a name="p360352965319"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p6042403"><a name="p6042403"></a><a name="p6042403"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row48414441505"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p42835719"><a name="p42835719"></a><a name="p42835719"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p47141219"><a name="p47141219"></a><a name="p47141219"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p760314292536"><a name="p760314292536"></a><a name="p760314292536"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p60342391"><a name="p60342391"></a><a name="p60342391"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row1884174405016"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p6275621"><a name="p6275621"></a><a name="p6275621"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p38563284"><a name="p38563284"></a><a name="p38563284"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p1360316297538"><a name="p1360316297538"></a><a name="p1360316297538"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p36618324"><a name="p36618324"></a><a name="p36618324"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row186984435014"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p52539702"><a name="p52539702"></a><a name="p52539702"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p27857430"><a name="p27857430"></a><a name="p27857430"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p1860320295536"><a name="p1860320295536"></a><a name="p1860320295536"></a>Integer (int32)</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p41859330"><a name="p41859330"></a><a name="p41859330"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row10691744155020"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p48027907"><a name="p48027907"></a><a name="p48027907"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p65055278"><a name="p65055278"></a><a name="p65055278"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p46031229135317"><a name="p46031229135317"></a><a name="p46031229135317"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p958515298529"><a name="p958515298529"></a><a name="p958515298529"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion</p>
</td>
</tr>
<tr id="row174784403522"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p1547812404524"><a name="p1547812404524"></a><a name="p1547812404524"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p1747813407524"><a name="p1747813407524"></a><a name="p1747813407524"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p1260362913535"><a name="p1260362913535"></a><a name="p1260362913535"></a>Integer (int32)</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p1251516531"><a name="p1251516531"></a><a name="p1251516531"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.</p>
<p id="p92514555315"><a name="p92514555315"></a><a name="p92514555315"></a>The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row1677516408524"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.2.5.1.1 "><p id="p67755406525"><a name="p67755406525"></a><a name="p67755406525"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.2 "><p id="p16775340115210"><a name="p16775340115210"></a><a name="p16775340115210"></a>false</p>
</td>
<td class="cellrowborder" valign="top" width="8.080808080808081%" headers="mcps1.2.5.1.3 "><p id="p1160382916535"><a name="p1160382916535"></a><a name="p1160382916535"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="61.61616161616161%" headers="mcps1.2.5.1.4 "><p id="p67751440145212"><a name="p67751440145212"></a><a name="p67751440145212"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section43737161"></a>

N/A

## 响应消息<a name="section58090133"></a>

**响应参数：**

响应参数的详细描述请参见[表3](创建Network.md#table34052983203655)

**响应示例**：

```
{
    "kind": "NetworkList",
    "apiVersion": "networking.cci.io/v1beta1",
    "metadata": {
        "selfLink": "/apis/networking.cci.io/v1beta1/namespaces/namespace-test/networks",
        "resourceVersion": "5016953"
    },
    "items": [
        {
            "metadata": {
                "name": "namespace-test-dc1-default-network",
                "namespace": "namespace-test",
                "selfLink": "/apis/networking.cci.io/v1beta1/namespaces/namespace-test/networks/namespace-test-dc1-default-network",
                "uid": "6fb85414-af6b-11e8-b6ef-f898ef6c78b4",
                "resourceVersion": "5016899",
                "creationTimestamp": "2018-09-03T11:21:00Z",
                "annotations": {
                    "network.alpha.kubernetes.io/default-security-group": "19c5d024-aed5-4856-b958-c0f65ce70855",
                    "network.alpha.kubernetes.io/domain-id": "aadb43c0b14c4cafbccfff483d075987",
                    "network.alpha.kubernetes.io/project-id": "51bf52609f2a49c68bfda3398817b376"
                },
                "enable": true
            },
            "spec": {
                "cidr": "192.168.244.0/23",
                "attachedVPC": "0d4080e5-546a-46c4-86fe-f3e26d685177",
                "networkType": "underlay_neutron",
                "physicalNetwork": "phy_net0",
                "networkID": "0022e356-f730-4226-802e-9cdaa6e7da17",
                "subnetID": "1ffd839d-e534-4fa8-a59d-42356335bf74",
                "availableZone": "cn-north-1a"
            },
            "status": {
                "state": "Active"
            }
        }
    ]
}
```

## 状态码<a name="section53049152"></a>

描述API的状态码。

**表 3**  状态码

<a name="d0e36668"></a>
<table><thead align="left"><tr id="row17031726"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p37392545"><a name="p37392545"></a><a name="p37392545"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p8897276"><a name="p8897276"></a><a name="p8897276"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49590760"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p57428620"><a name="p57428620"></a><a name="p57428620"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p21206673"><a name="p21206673"></a><a name="p21206673"></a>This operation succeeds, and a NetworkList resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

