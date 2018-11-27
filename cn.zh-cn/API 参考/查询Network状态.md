# 查询Network状态<a name="cci_02_2017"></a>

## 功能描述<a name="section1686113493165"></a>

查询一个指定Network对象的状态。

## URI<a name="section8403243161416"></a>

GET /apis/networking.cci.io/v1beta1/namespaces/\{namespace\}/networks/\{name\}/status

**表 1**  Path参数

<a name="zh-cn_topic_0079615000_table64523107"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615000_row55516030"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615000_p504568"><a name="zh-cn_topic_0079615000_p504568"></a><a name="zh-cn_topic_0079615000_p504568"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.999999999999996%" id="mcps1.2.4.1.2"><p id="p64287338205444"><a name="p64287338205444"></a><a name="p64287338205444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47%" id="mcps1.2.4.1.3"><p id="p39891894205444"><a name="p39891894205444"></a><a name="p39891894205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615000_row41865316"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615000_p35647420"><a name="zh-cn_topic_0079615000_p35647420"></a><a name="zh-cn_topic_0079615000_p35647420"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615000_p1759884"><a name="zh-cn_topic_0079615000_p1759884"></a><a name="zh-cn_topic_0079615000_p1759884"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="row544575442510"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.4.1.1 "><p id="p344535414251"><a name="p344535414251"></a><a name="p344535414251"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p844555492518"><a name="p844555492518"></a><a name="p844555492518"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.4.1.3 "><p id="p94451454182517"><a name="p94451454182517"></a><a name="p94451454182517"></a>要查询的Network名称。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table209971615188"></a>
<table><thead align="left"><tr id="row79971112186"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.4.1.1"><p id="p0997618189"><a name="p0997618189"></a><a name="p0997618189"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.999999999999996%" id="mcps1.2.4.1.2"><p id="p19977141817"><a name="p19977141817"></a><a name="p19977141817"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47%" id="mcps1.2.4.1.3"><p id="p19997019182"><a name="p19997019182"></a><a name="p19997019182"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1299711201810"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.4.1.1 "><p id="p312112131810"><a name="p312112131810"></a><a name="p312112131810"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p912122185"><a name="p912122185"></a><a name="p912122185"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.4.1.3 "><p id="p1412162131811"><a name="p1412162131811"></a><a name="p1412162131811"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section947084713911"></a>

N/A

## 响应消息<a name="section61819725020"></a>

**响应参数**

响应参数的详细描述请参见[表3](创建Network.md#table34052983203655)。

**响应示例**

```
{
	"kind": "Network",
	"apiVersion": "networking.cci.io/v1beta1",
	"metadata": {
		"name": "test-network",
		"namespace": "test-ns",
		"selfLink": "/apis/networking.cci.io/v1beta1/namespaces/test-ns/networks/test-network",
		"uid": "f03452ac-a4ea-11e8-8500-c81fbe371a17",
		"resourceVersion": "2025736",
		"creationTimestamp": "2018-08-21T02:35:59Z",
		"annotations": {
			"network.alpha.kubernetes.io/default-security-group": "security-group-id",
			"network.alpha.kubernetes.io/domain-id": "domain-id",
			"network.alpha.kubernetes.io/project-id": "project-id",
			"network.alpha.kubernetes.io/type": "underlay_neutron"
		},
		"enable": true
	},
	"spec": {
		"availableZone": "cnnorth1a",
		"cidr": "192.168.0.0/24",
		"attachedVPC": "vpc-id",
		"networkID": "network-id",
		"networkType": "underlay_neutron",
		"subnetID": "subnet-id"
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
<tbody><tr id="zh-cn_topic_0079614900_row41084259"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p16829188175413"><a name="p16829188175413"></a><a name="p16829188175413"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p168295885414"><a name="p168295885414"></a><a name="p168295885414"></a>This operation succeeds, and a Network resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

