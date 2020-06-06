# 获取ClusterRole列表<a name="cci_02_3186"></a>

## 功能介绍<a name="section8861359184518"></a>

This API is used to list or watch objects of kind ClusterRole

## URL<a name="section47133333463"></a>

GET /apis/rbac.authorization.k8s.io/v1/clusterroles

[参数解释](#d0e42906)描述该API的参数。

**表 1**  参数解释

<a name="d0e42906"></a>
<table><thead align="left"><tr id="row10640301"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.169999999999998%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17811636"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p33456451"><a name="p33456451"></a><a name="p33456451"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p25618043"><a name="p25618043"></a><a name="p25618043"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p61795587"><a name="p61795587"></a><a name="p61795587"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row26391471649"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p14640471145"><a name="p14640471145"></a><a name="p14640471145"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p064011716413"><a name="p064011716413"></a><a name="p064011716413"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p11437414145"><a name="p11437414145"></a><a name="p11437414145"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
<tr id="row98891214131413"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p388971421419"><a name="p388971421419"></a><a name="p388971421419"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p4889131431416"><a name="p4889131431416"></a><a name="p4889131431416"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p16889514181418"><a name="p16889514181418"></a><a name="p16889514181418"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row1340582313149"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1140572321416"><a name="p1140572321416"></a><a name="p1140572321416"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p18405423201414"><a name="p18405423201414"></a><a name="p18405423201414"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p15405102321410"><a name="p15405102321410"></a><a name="p15405102321410"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row1540512320146"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p164059236141"><a name="p164059236141"></a><a name="p164059236141"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p18405172319146"><a name="p18405172319146"></a><a name="p18405172319146"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p6405112331410"><a name="p6405112331410"></a><a name="p6405112331410"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row1352892919147"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p125284299145"><a name="p125284299145"></a><a name="p125284299145"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p125281429131419"><a name="p125281429131419"></a><a name="p125281429131419"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p19528122919142"><a name="p19528122919142"></a><a name="p19528122919142"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row1940582351420"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1940572318143"><a name="p1940572318143"></a><a name="p1940572318143"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p12405112318140"><a name="p12405112318140"></a><a name="p12405112318140"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p18405923171410"><a name="p18405923171410"></a><a name="p18405923171410"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row646235915314"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p164621259105310"><a name="p164621259105310"></a><a name="p164621259105310"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p114621959175318"><a name="p114621959175318"></a><a name="p114621959175318"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p846255916536"><a name="p846255916536"></a><a name="p846255916536"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row3929191015548"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p593021020541"><a name="p593021020541"></a><a name="p593021020541"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p1793014101543"><a name="p1793014101543"></a><a name="p1793014101543"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p69301210205419"><a name="p69301210205419"></a><a name="p69301210205419"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section18662134312520"></a>

**请求参数**

**表 2**  请求Header参数说明

<a name="table165001054142614"></a>
<table><thead align="left"><tr id="row55001954122614"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p115009545264"><a name="p115009545264"></a><a name="p115009545264"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.2"><p id="p175001547265"><a name="p175001547265"></a><a name="p175001547265"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61%" id="mcps1.2.4.1.3"><p id="p16500154162611"><a name="p16500154162611"></a><a name="p16500154162611"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row199801811203412"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p69808112344"><a name="p69808112344"></a><a name="p69808112344"></a>X-CCI-Namespace</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.2 "><p id="p3980111103414"><a name="p3980111103414"></a><a name="p3980111103414"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61%" headers="mcps1.2.4.1.3 "><p id="p4234331132917"><a name="p4234331132917"></a><a name="p4234331132917"></a>当前用户任一Namespace的名称。</p>
</td>
</tr>
</tbody>
</table>

**请求示例**

N/A

## 响应消息<a name="section726119112252"></a>

**响应参数：**

响应参数的详细描述请参见[表2 响应参数](获取指定的ClusterRole.md#table1154814995615)。

**响应示例：**

```
{
    "kind" : "ClusterRoleList",
    "apiVersion" : "rbac.authorization.k8s.io/v1",
    "metadata" : {
        "selfLink" : "/apis/rbac.authorization.k8s.io/v1/clusterroles",
        "resourceVersion" : "4622"
    },
    "items" : [ {
        "metadata" : {
            "name" : "secret-reader",
            "selfLink" : "/apis/rbac.authorization.k8s.io/v1/clusterroles/secret-reader",
            "uid" : "8d358854-f1e7-11e8-b449-fa163ec24e06",
            "resourceVersion" : "4619",
            "creationTimestamp" : "2018-11-27T01:55:44Z"
        },
        "rules" : [ {
            "verbs" : [ "get", "watch", "list" ],
            "apiGroups" : [ "" ],
            "resources" : [ "secrets" ]
        } ]
    } ]
}
```

## 状态码<a name="section534515230266"></a>

[状态码](#d0e43055)描述API的状态码。

**表 3**  状态码

<a name="d0e43055"></a>
<table><thead align="left"><tr id="row20813512"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p8172937"><a name="p8172937"></a><a name="p8172937"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p58028199"><a name="p58028199"></a><a name="p58028199"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2663689"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p14432280"><a name="p14432280"></a><a name="p14432280"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p0978454104816"><a name="p0978454104816"></a><a name="p0978454104816"></a>OK</p>
</td>
</tr>
</tbody>
</table>

异常状态码请参见[状态码](状态码.md)。

