# 查询Network<a name="cci_02_2015"></a>

## 功能介绍<a name="section1686113493165"></a>

查询指定Network对象。

## URI<a name="section8403243161416"></a>

GET /apis/networking.cci.io/v1beta1/namespaces/\{namespace\}/networks/\{name\}

**表 1**  Path参数

<a name="zh-cn_topic_0079615000_table64523107"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615000_row55516030"><th class="cellrowborder" valign="top" width="18%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0079615000_p504568"><a name="zh-cn_topic_0079615000_p504568"></a><a name="zh-cn_topic_0079615000_p504568"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.2.5.1.2"><p id="p64287338205444"><a name="p64287338205444"></a><a name="p64287338205444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="p1891094219478"><a name="p1891094219478"></a><a name="p1891094219478"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="63%" id="mcps1.2.5.1.4"><p id="p39891894205444"><a name="p39891894205444"></a><a name="p39891894205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615000_row41865316"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615000_p35647420"><a name="zh-cn_topic_0079615000_p35647420"></a><a name="zh-cn_topic_0079615000_p35647420"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615000_p1759884"><a name="zh-cn_topic_0079615000_p1759884"></a><a name="zh-cn_topic_0079615000_p1759884"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p19910542114715"><a name="p19910542114715"></a><a name="p19910542114715"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="row544575442510"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.5.1.1 "><p id="p344535414251"><a name="p344535414251"></a><a name="p344535414251"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p844555492518"><a name="p844555492518"></a><a name="p844555492518"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p17910154210475"><a name="p17910154210475"></a><a name="p17910154210475"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p94451454182517"><a name="p94451454182517"></a><a name="p94451454182517"></a>要查询的Network名称。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table129281841141611"></a>
<table><thead align="left"><tr id="row14943164181616"><th class="cellrowborder" valign="top" width="18%" id="mcps1.2.5.1.1"><p id="p89431141121610"><a name="p89431141121610"></a><a name="p89431141121610"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.2.5.1.2"><p id="p209431141201618"><a name="p209431141201618"></a><a name="p209431141201618"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="p17943041131618"><a name="p17943041131618"></a><a name="p17943041131618"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="63%" id="mcps1.2.5.1.4"><p id="p1394334141617"><a name="p1394334141617"></a><a name="p1394334141617"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13943841171610"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.5.1.1 "><p id="p8943144116167"><a name="p8943144116167"></a><a name="p8943144116167"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p12943164161619"><a name="p12943164161619"></a><a name="p12943164161619"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p10943144111613"><a name="p10943144111613"></a><a name="p10943144111613"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p149432411161"><a name="p149432411161"></a><a name="p149432411161"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row20959124115162"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.5.1.1 "><p id="p7959141111610"><a name="p7959141111610"></a><a name="p7959141111610"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p9959841171617"><a name="p9959841171617"></a><a name="p9959841171617"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p7959144116160"><a name="p7959144116160"></a><a name="p7959144116160"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p14959204141618"><a name="p14959204141618"></a><a name="p14959204141618"></a>Should the export be exact. Exact export maintains cluster-specific fields like Namespace.</p>
</td>
</tr>
<tr id="row14959174141611"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.5.1.1 "><p id="p8959341141611"><a name="p8959341141611"></a><a name="p8959341141611"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p1995954110161"><a name="p1995954110161"></a><a name="p1995954110161"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p495904191616"><a name="p495904191616"></a><a name="p495904191616"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p1195914414163"><a name="p1195914414163"></a><a name="p1195914414163"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section947084713911"></a>

N/A

## 响应消息<a name="section61819725020"></a>

**响应参数**

响应参数的详细描述请参见[创建Network](创建Network.md)。

**响应示例**

```
{
    "kind": "Network",
    "apiVersion": "networking.cci.io/v1beta1",
    "metadata": {
        "name": "namespace-test-dc1-default-network",
        "namespace": "namespace-test",
        "selfLink": "/apis/networking.cci.io/v1beta1/namespaces/namespace-test/networks/namespace-test-dc1-default-network",
        "uid": "6fb85414-af6b-11e8-b6ef-f898ef6c78b4",
        "resourceVersion": "5016899",
        "creationTimestamp": "2018-09-03T11:21:00Z",
        "annotations": {
            "network.alpha.kubernetes.io/project-id": "51bf52609f2a49c68bfda3398817b376",
            "network.alpha.kubernetes.io/default-security-group": "19c5d024-aed5-4856-b958-c0f65ce70855",
            "network.alpha.kubernetes.io/domain-id": "aadb43c0b14c4cafbccfff483d075987"
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
```

## 状态码<a name="s50f1049a6a4d404c895cf636eb8f3bf1"></a>

**表 3**  状态码

<a name="zh-cn_topic_0079614900_table46761928"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614900_row33254664"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p55616028205955"><a name="p55616028205955"></a><a name="p55616028205955"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p8604418205955"><a name="p8604418205955"></a><a name="p8604418205955"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614900_row41084259"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p148891415121113"><a name="p148891415121113"></a><a name="p148891415121113"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614931_p42890904"><a name="zh-cn_topic_0079614931_p42890904"></a><a name="zh-cn_topic_0079614931_p42890904"></a>This operation succeeds, and a Network resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

