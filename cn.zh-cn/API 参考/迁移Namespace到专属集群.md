# 迁移Namespace到专属集群<a name="cci_02_3210"></a>

## 功能介绍<a name="sd3cfd7eb5e604cbfacc39f3d39217286"></a>

将共享集群的Namespace迁移到专属集群。共享集群是普通租户通用的资源池，包含一些共用的节点，按照负载的资源使用量和运行时长收费；专属集群是用户按照包年包月方式购买的节点，这些节点只有他自己能使用。

用户购买新的专属集群时，调用该接口可将原先创建的共享集群的Namespace迁移到对应类型专属集群中。Namespace迁移到专属集群后，新创建的Pod将直接运行在专属集群中，迁移时已经运行在共享集群中的Pod不会自动迁移，如有需要，请自行迁移。

## URI<a name="sb360ead1682b4a91886de13dec66f5c4"></a>

PUT /cci/v1/namespaces/\{name\}/todedicated

**表 1**  Path参数

<a name="table1696332124519"></a>
<table><thead align="left"><tr id="row11961332194516"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.3.1.1"><p id="p396032144518"><a name="p396032144518"></a><a name="p396032144518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="76%" id="mcps1.2.3.1.2"><p id="p18962325454"><a name="p18962325454"></a><a name="p18962325454"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9960327457"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1496113214456"><a name="p1496113214456"></a><a name="p1496113214456"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p796193274515"><a name="p796193274515"></a><a name="p796193274515"></a>Name of the Namespace.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="d0e36967"></a>
<table><thead align="left"><tr id="row62299817"><th class="cellrowborder" valign="top" width="24.507549245075495%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.327967203279673%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.164483551644835%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10278610"><td class="cellrowborder" valign="top" width="24.507549245075495%" headers="mcps1.2.4.1.1 "><p id="p27261059"><a name="p27261059"></a><a name="p27261059"></a>allowed_on_shared_node</p>
</td>
<td class="cellrowborder" valign="top" width="20.327967203279673%" headers="mcps1.2.4.1.2 "><p id="p60662202"><a name="p60662202"></a><a name="p60662202"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="55.164483551644835%" headers="mcps1.2.4.1.3 "><p id="p0893191113155"><a name="p0893191113155"></a><a name="p0893191113155"></a>用于指定是否开启弹性调度，可设置为true或false。默认取值为false，不开启时不需要指定该参数值。</p>
<p id="p2034614315202"><a name="p2034614315202"></a><a name="p2034614315202"></a>弹性调度：指当专属资源用尽时，可自动弹性创建CCI按需实例。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s868ed9032ac544a8908766b83229eba1"></a>

N/A

## 响应消息<a name="s40c3210a927d4400b708d17d3f0a3cbe"></a>

N/A

## 状态码<a name="s379564af9d9b4e6c915ee4629fc129e5"></a>

[表3](#zh-cn_topic_0079615060_table44048571)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615060_table44048571"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615060_row48163256"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p4561445121117"><a name="p4561445121117"></a><a name="p4561445121117"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p378306821117"><a name="p378306821117"></a><a name="p378306821117"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615060_row4281684"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615060_p11272110"><a name="zh-cn_topic_0079615060_p11272110"></a><a name="zh-cn_topic_0079615060_p11272110"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615060_p40625737"><a name="zh-cn_topic_0079615060_p40625737"></a><a name="zh-cn_topic_0079615060_p40625737"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

