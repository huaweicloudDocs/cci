# 列出Namespace<a name="cci_02_3095"></a>

## 功能介绍<a name="s26b600951f5a4b5bbf0ef7cd492640a1"></a>

该API用于获取集群中该用户当前项目下所有Namespace的详细信息。

## URI<a name="sec2fa5f295114052960ed7b3e11ad998"></a>

GET /api/v1/namespaces

[表1](#zh-cn_topic_0079614949_table47826462)  描述该API的参数。

**表 1**  参数描述

<a name="zh-cn_topic_0079614949_table47826462"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614949_row657479"><th class="cellrowborder" valign="top" width="18.55%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614949_p53255854"><a name="zh-cn_topic_0079614949_p53255854"></a><a name="zh-cn_topic_0079614949_p53255854"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="8.74%" id="mcps1.2.4.1.2"><p id="p50544370201922"><a name="p50544370201922"></a><a name="p50544370201922"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="72.71%" id="mcps1.2.4.1.3"><p id="p453306201922"><a name="p453306201922"></a><a name="p453306201922"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614949_row53778287"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p61073976"><a name="zh-cn_topic_0079614949_p61073976"></a><a name="zh-cn_topic_0079614949_p61073976"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p48045022"><a name="zh-cn_topic_0079614949_p48045022"></a><a name="zh-cn_topic_0079614949_p48045022"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p66441544"><a name="zh-cn_topic_0079614949_p66441544"></a><a name="zh-cn_topic_0079614949_p66441544"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row184781327710"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="p44809321575"><a name="p44809321575"></a><a name="p44809321575"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="p20480193211716"><a name="p20480193211716"></a><a name="p20480193211716"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="p1048011323713"><a name="p1048011323713"></a><a name="p1048011323713"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row61102986"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p50394838"><a name="zh-cn_topic_0079614949_p50394838"></a><a name="zh-cn_topic_0079614949_p50394838"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p55450074"><a name="zh-cn_topic_0079614949_p55450074"></a><a name="zh-cn_topic_0079614949_p55450074"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p62271039"><a name="zh-cn_topic_0079614949_p62271039"></a><a name="zh-cn_topic_0079614949_p62271039"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row23568445"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p29995926"><a name="zh-cn_topic_0079614949_p29995926"></a><a name="zh-cn_topic_0079614949_p29995926"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p13750947"><a name="zh-cn_topic_0079614949_p13750947"></a><a name="zh-cn_topic_0079614949_p13750947"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p40084941"><a name="zh-cn_topic_0079614949_p40084941"></a><a name="zh-cn_topic_0079614949_p40084941"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row221012217818"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="p121092217814"><a name="p121092217814"></a><a name="p121092217814"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="p1221022220819"><a name="p1221022220819"></a><a name="p1221022220819"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="p1621019228818"><a name="p1621019228818"></a><a name="p1621019228818"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the `continue` field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="rdcad1860dfda4c83abbd4181730c1300"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="a44c2e37fd9134f74b7f6eea74afc35eb"><a name="a44c2e37fd9134f74b7f6eea74afc35eb"></a><a name="a44c2e37fd9134f74b7f6eea74afc35eb"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p171421421023"><a name="zh-cn_topic_0079614949_p171421421023"></a><a name="zh-cn_topic_0079614949_p171421421023"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p161421242927"><a name="zh-cn_topic_0079614949_p161421242927"></a><a name="zh-cn_topic_0079614949_p161421242927"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row25220152"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p29566423"><a name="zh-cn_topic_0079614949_p29566423"></a><a name="zh-cn_topic_0079614949_p29566423"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p46070087"><a name="zh-cn_topic_0079614949_p46070087"></a><a name="zh-cn_topic_0079614949_p46070087"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p40689584"><a name="zh-cn_topic_0079614949_p40689584"></a><a name="zh-cn_topic_0079614949_p40689584"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row30661937"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p588929"><a name="zh-cn_topic_0079614949_p588929"></a><a name="zh-cn_topic_0079614949_p588929"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p47703261"><a name="zh-cn_topic_0079614949_p47703261"></a><a name="zh-cn_topic_0079614949_p47703261"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p38758958"><a name="zh-cn_topic_0079614949_p38758958"></a><a name="zh-cn_topic_0079614949_p38758958"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row13286310"><td class="cellrowborder" valign="top" width="18.55%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p2449345"><a name="zh-cn_topic_0079614949_p2449345"></a><a name="zh-cn_topic_0079614949_p2449345"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="8.74%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p64179269"><a name="zh-cn_topic_0079614949_p64179269"></a><a name="zh-cn_topic_0079614949_p64179269"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="72.71%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p31138264"><a name="zh-cn_topic_0079614949_p31138264"></a><a name="zh-cn_topic_0079614949_p31138264"></a>Timeout for the list/watch call.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079614949_section138844"></a>

N/A

## 响应消息<a name="s593cd0719e504a2a8f6dd2e4b6200d8e"></a>

**响应参数：**

响应参数如[表2](#zh-cn_topic_0079614949_table27784979)所示。

**表 2**  参数描述

<a name="zh-cn_topic_0079614949_table27784979"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614949_row52925796"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614949_p59131099"><a name="zh-cn_topic_0079614949_p59131099"></a><a name="zh-cn_topic_0079614949_p59131099"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.2"><p id="p32885365201922"><a name="p32885365201922"></a><a name="p32885365201922"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45%" id="mcps1.2.4.1.3"><p id="p46468891201922"><a name="p46468891201922"></a><a name="p46468891201922"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614949_row25741004"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p4646565"><a name="zh-cn_topic_0079614949_p4646565"></a><a name="zh-cn_topic_0079614949_p4646565"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p40827483"><a name="zh-cn_topic_0079614949_p40827483"></a><a name="zh-cn_topic_0079614949_p40827483"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p18691797"><a name="zh-cn_topic_0079614949_p18691797"></a><a name="zh-cn_topic_0079614949_p18691797"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row34008447"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p3220827"><a name="zh-cn_topic_0079614949_p3220827"></a><a name="zh-cn_topic_0079614949_p3220827"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p59560431"><a name="zh-cn_topic_0079614949_p59560431"></a><a name="zh-cn_topic_0079614949_p59560431"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p59665636"><a name="zh-cn_topic_0079614949_p59665636"></a><a name="zh-cn_topic_0079614949_p59665636"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row119818"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p9705331"><a name="zh-cn_topic_0079614949_p9705331"></a><a name="zh-cn_topic_0079614949_p9705331"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614930_p47105906"><a name="zh-cn_topic_0079614930_p47105906"></a><a name="zh-cn_topic_0079614930_p47105906"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p57477322"><a name="zh-cn_topic_0079614949_p57477322"></a><a name="zh-cn_topic_0079614949_p57477322"></a>详情请参见<a href="#zh-cn_topic_0079614949_table48738220">表3</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row47533853"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p25036876"><a name="zh-cn_topic_0079614949_p25036876"></a><a name="zh-cn_topic_0079614949_p25036876"></a>items</p>
</td>
<td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.2 "><p id="p11435165712107"><a name="p11435165712107"></a><a name="p11435165712107"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p61373038"><a name="zh-cn_topic_0079614949_p61373038"></a><a name="zh-cn_topic_0079614949_p61373038"></a>Items is the list of Namespace objects in the list. 详情请参见<a href="创建Namespace.md#zh-cn_topic_0079615062_ref458759029">表2</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  metadata字段数据结构说明

<a name="zh-cn_topic_0079614949_table48738220"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614949_row41599065"><th class="cellrowborder" valign="top" width="25.06%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614949_p14081115"><a name="zh-cn_topic_0079614949_p14081115"></a><a name="zh-cn_topic_0079614949_p14081115"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.14%" id="mcps1.2.4.1.2"><p id="p49677728201922"><a name="p49677728201922"></a><a name="p49677728201922"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.800000000000004%" id="mcps1.2.4.1.3"><p id="p64473071201922"><a name="p64473071201922"></a><a name="p64473071201922"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614949_row39937165"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p13684913"><a name="zh-cn_topic_0079614949_p13684913"></a><a name="zh-cn_topic_0079614949_p13684913"></a>selfLink</p>
</td>
<td class="cellrowborder" valign="top" width="30.14%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p34736162"><a name="zh-cn_topic_0079614949_p34736162"></a><a name="zh-cn_topic_0079614949_p34736162"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.800000000000004%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p62165703"><a name="zh-cn_topic_0079614949_p62165703"></a><a name="zh-cn_topic_0079614949_p62165703"></a>SelfLink is a URL representing this object. Populated by the system. Read-only.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614949_row22620416"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614949_p20314447"><a name="zh-cn_topic_0079614949_p20314447"></a><a name="zh-cn_topic_0079614949_p20314447"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="30.14%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614949_p34857543"><a name="zh-cn_topic_0079614949_p34857543"></a><a name="zh-cn_topic_0079614949_p34857543"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.800000000000004%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614949_p4888719"><a name="zh-cn_topic_0079614949_p4888719"></a><a name="zh-cn_topic_0079614949_p4888719"></a>String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only.</p>
</td>
</tr>
</tbody>
</table>

**响应示例：**

```
{
    "kind": "NamespaceList",
    "apiVersion": "v1",
    "metadata": {
        "selfLink": "/api/v1/namespaces",
        "resourceVersion": "594181"
    },
    "items": [
        {
            "metadata": {
                "name": "default",
                "selfLink": "/api/v1/namespaces/default",
                "uid": "90dd5244-5881-11e7-b5d7-fa163e08a2fd",
                "resourceVersion": "6",
                "creationTimestamp": "2017-06-24T02:05:16Z"
            },
            "spec": {
                "finalizers": [
                    "kubernetes"
                ]
            },
            "status": {
                "phase": "Active"
            }
        },
        {
            "metadata": {
                "name": "kube-system",
                "selfLink": "/api/v1/namespaces/kube-system",
                "uid": "9178fce6-5881-11e7-b5d7-fa163e08a2fd",
                "resourceVersion": "25",
                "creationTimestamp": "2017-06-24T02:05:17Z"
            },
            "spec": {
                "finalizers": [
                    "kubernetes"
                ]
            },
            "status": {
                "phase": "Active"
            }
        }
    ]
}
```

## 状态码<a name="sa8b2c48c82c44c2f8337034f7aef2c27"></a>

[表4](#zh-cn_topic_0079614949_table35990804)描述API的状态码。

**表 4**  状态码

<a name="zh-cn_topic_0079614949_table35990804"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614949_row5174319"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p21487463201922"><a name="p21487463201922"></a><a name="p21487463201922"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p62762933201922"><a name="p62762933201922"></a><a name="p62762933201922"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614949_row59587228"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614949_p61836145"><a name="zh-cn_topic_0079614949_p61836145"></a><a name="zh-cn_topic_0079614949_p61836145"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614949_p42671863"><a name="zh-cn_topic_0079614949_p42671863"></a><a name="zh-cn_topic_0079614949_p42671863"></a>This operation succeeds, and a group of Namespace resource objects is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

