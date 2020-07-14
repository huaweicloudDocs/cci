# 查询所有Service<a name="cci_02_3053"></a>

## 功能介绍<a name="scd7c5d26006f4f2fa18d7944090a515a"></a>

查询Namespace下所有Service的详细信息。

## URI<a name="sf266bb0aca594ae0bfe7c7952d99b504"></a>

GET /api/v1/namespaces/\{namespace\}/services

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

<a name="zh-cn_topic_0079614912_table30173457"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614912_row62631706"><th class="cellrowborder" valign="top" width="24.3%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614912_p40003440"><a name="zh-cn_topic_0079614912_p40003440"></a><a name="zh-cn_topic_0079614912_p40003440"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.13%" id="mcps1.2.4.1.2"><p id="p55041445195410"><a name="p55041445195410"></a><a name="p55041445195410"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.57%" id="mcps1.2.4.1.3"><p id="p29172047195410"><a name="p29172047195410"></a><a name="p29172047195410"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614912_row51438757"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p5789773"><a name="zh-cn_topic_0079614912_p5789773"></a><a name="zh-cn_topic_0079614912_p5789773"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p66318445"><a name="zh-cn_topic_0079614912_p66318445"></a><a name="zh-cn_topic_0079614912_p66318445"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p3084974"><a name="zh-cn_topic_0079614912_p3084974"></a><a name="zh-cn_topic_0079614912_p3084974"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614912_row27764770"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p34353911"><a name="zh-cn_topic_0079614912_p34353911"></a><a name="zh-cn_topic_0079614912_p34353911"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p31203392"><a name="zh-cn_topic_0079614912_p31203392"></a><a name="zh-cn_topic_0079614912_p31203392"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p44446822"><a name="zh-cn_topic_0079614912_p44446822"></a><a name="zh-cn_topic_0079614912_p44446822"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614912_row64477079"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p55260882"><a name="zh-cn_topic_0079614912_p55260882"></a><a name="zh-cn_topic_0079614912_p55260882"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p46946462"><a name="zh-cn_topic_0079614912_p46946462"></a><a name="zh-cn_topic_0079614912_p46946462"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p44567074"><a name="zh-cn_topic_0079614912_p44567074"></a><a name="zh-cn_topic_0079614912_p44567074"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614912_row65559353"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p8707397"><a name="zh-cn_topic_0079614912_p8707397"></a><a name="zh-cn_topic_0079614912_p8707397"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p34210590"><a name="zh-cn_topic_0079614912_p34210590"></a><a name="zh-cn_topic_0079614912_p34210590"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p19594411"><a name="zh-cn_topic_0079614912_p19594411"></a><a name="zh-cn_topic_0079614912_p19594411"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614912_row42131977"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p57246976"><a name="zh-cn_topic_0079614912_p57246976"></a><a name="zh-cn_topic_0079614912_p57246976"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p6493471"><a name="zh-cn_topic_0079614912_p6493471"></a><a name="zh-cn_topic_0079614912_p6493471"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p56209167"><a name="zh-cn_topic_0079614912_p56209167"></a><a name="zh-cn_topic_0079614912_p56209167"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614912_row36120461"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p40076217"><a name="zh-cn_topic_0079614912_p40076217"></a><a name="zh-cn_topic_0079614912_p40076217"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p24948105"><a name="zh-cn_topic_0079614912_p24948105"></a><a name="zh-cn_topic_0079614912_p24948105"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p7530597"><a name="zh-cn_topic_0079614912_p7530597"></a><a name="zh-cn_topic_0079614912_p7530597"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079614912_row666516"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p53987822"><a name="zh-cn_topic_0079614912_p53987822"></a><a name="zh-cn_topic_0079614912_p53987822"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614912_p10937481"><a name="zh-cn_topic_0079614912_p10937481"></a><a name="zh-cn_topic_0079614912_p10937481"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p13520781"><a name="zh-cn_topic_0079614912_p13520781"></a><a name="zh-cn_topic_0079614912_p13520781"></a>Object name and auth scope, such as for teams and projects.</p>
</td>
</tr>
<tr id="r8a408c32e95a4e11a0f37c7e8c496ae9"><td class="cellrowborder" valign="top" width="24.3%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614912_p62023147538"><a name="zh-cn_topic_0079614912_p62023147538"></a><a name="zh-cn_topic_0079614912_p62023147538"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.13%" headers="mcps1.2.4.1.2 "><p id="afed04ce8ed5b4563a1682d61a3792448"><a name="afed04ce8ed5b4563a1682d61a3792448"></a><a name="afed04ce8ed5b4563a1682d61a3792448"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.57%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614912_p120261435313"><a name="zh-cn_topic_0079614912_p120261435313"></a><a name="zh-cn_topic_0079614912_p120261435313"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="sfa72efcb12544146a6d0110ec99bdde9"></a>

N/A

## 响应消息<a name="sadda659ddfa046368c5c736891a5c24d"></a>

**响应参数：**

响应参数如[表109](数据结构.md#zh-cn_topic_0079614912_ref458774242)所示。

**响应示例：**

```
{
    "kind": "ServiceList",
    "apiVersion": "v1",
    "metadata": {
        "selfLink": "/api/v1/namespaces/namespace-test/services",
        "resourceVersion": "5147871"
    },
    "items": [
        {
            "metadata": {
                "name": "kube-dns",
                "namespace": "namespace-test",
                "selfLink": "/api/v1/namespaces/namespace-test/services/kube-dns",
                "uid": "6d356f18-af6b-11e8-b6ef-f898ef6c78b4",
                "resourceVersion": "5016792",
                "creationTimestamp": "2018-09-03T11:20:56Z",
                "labels": {
                    "addonmanager.kubernetes.io/mode": "Reconcile",
                    "app": "kube-dns",
                    "kubernetes.io/cluster-service": "true",
                    "kubernetes.io/name": "KubeDNS"
                },
                "enable": true
            },
            "spec": {
                "ports": [
                    {
                        "name": "dns",
                        "protocol": "UDP",
                        "port": 53,
                        "targetPort": 5353
                    },
                    {
                        "name": "dns-tcp",
                        "protocol": "TCP",
                        "port": 53,
                        "targetPort": 5353
                    }
                ],
                "selector": {
                    "app": "kube-dns"
                },
                "clusterIP": "10.247.189.43",
                "type": "ClusterIP",
                "sessionAffinity": "None"
            },
            "status": {
                "loadBalancer": {}
            }
        },
        {
            "metadata": {
                "name": "redis",
                "namespace": "namespace-test",
                "selfLink": "/api/v1/namespaces/namespace-test/services/redis",
                "uid": "d6a1ce79-afdb-11e8-b6ef-f898ef6c78b4",
                "resourceVersion": "5146412",
                "creationTimestamp": "2018-09-04T00:45:36Z",
                "labels": {
                    "app": "redis"
                },
                "enable": true
            },
            "spec": {
                "ports": [
                    {
                        "name": "service0",
                        "protocol": "TCP",
                        "port": 8080,
                        "targetPort": 80
                    }
                ],
                "selector": {
                    "app": "redis"
                },
                "clusterIP": "10.247.212.210",
                "type": "ClusterIP",
                "sessionAffinity": "None"
            },
            "status": {
                "loadBalancer": {}
            }
        }
    ]
}
```

## 状态码<a name="sb209ebbf78944af4b92248c35b3aecfc"></a>

[表3](#zh-cn_topic_0079614912_table28130990)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079614912_table28130990"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614912_row58140769"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p51917783195410"><a name="p51917783195410"></a><a name="p51917783195410"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p44590880195410"><a name="p44590880195410"></a><a name="p44590880195410"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614912_row58604130"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614912_p49314056"><a name="zh-cn_topic_0079614912_p49314056"></a><a name="zh-cn_topic_0079614912_p49314056"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614912_p35015599"><a name="zh-cn_topic_0079614912_p35015599"></a><a name="zh-cn_topic_0079614912_p35015599"></a>This operation succeeds, and a group of Service resource objects is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

