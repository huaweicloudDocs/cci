# 查询Pod日志<a name="cci_02_3016"></a>

## 功能介绍<a name="s71ad64c953904f0985921f05a66305f4"></a>

查询Pod的日志。

## URI<a name="sf5f1071056e347eb9822c210cfa0b051"></a>

GET /api/v1/namespaces/\{namespace\}/pods/\{name\}/log

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
<tr id="row115455519446"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p15341161164510"><a name="p15341161164510"></a><a name="p15341161164510"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p1234131114458"><a name="p1234131114458"></a><a name="p1234131114458"></a>Name of the Pod.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079614904_table61950116"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614904_row42466880"><th class="cellrowborder" valign="top" width="24.702470247024703%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614904_p17265247"><a name="zh-cn_topic_0079614904_p17265247"></a><a name="zh-cn_topic_0079614904_p17265247"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.25212521252125%" id="mcps1.2.4.1.2"><p id="p25470926205834"><a name="p25470926205834"></a><a name="p25470926205834"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="54.045404540454044%" id="mcps1.2.4.1.3"><p id="p49879135205834"><a name="p49879135205834"></a><a name="p49879135205834"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614904_row1125057"><td class="cellrowborder" valign="top" width="24.702470247024703%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614904_p24020754"><a name="zh-cn_topic_0079614904_p24020754"></a><a name="zh-cn_topic_0079614904_p24020754"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="21.25212521252125%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614904_p66632916"><a name="zh-cn_topic_0079614904_p66632916"></a><a name="zh-cn_topic_0079614904_p66632916"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="54.045404540454044%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614904_p28557102"><a name="zh-cn_topic_0079614904_p28557102"></a><a name="zh-cn_topic_0079614904_p28557102"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="r94dded79cd6b4b48a4f5f012fcdfd007"><td class="cellrowborder" valign="top" width="24.702470247024703%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614904_p865375652118"><a name="zh-cn_topic_0079614904_p865375652118"></a><a name="zh-cn_topic_0079614904_p865375652118"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="21.25212521252125%" headers="mcps1.2.4.1.2 "><p id="a5bdb3bb6b715429cb36a6898c2e06f45"><a name="a5bdb3bb6b715429cb36a6898c2e06f45"></a><a name="a5bdb3bb6b715429cb36a6898c2e06f45"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="54.045404540454044%" headers="mcps1.2.4.1.3 "><p id="a025c81775dbc47b7bf3cd51960572a98"><a name="a025c81775dbc47b7bf3cd51960572a98"></a><a name="a025c81775dbc47b7bf3cd51960572a98"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="r3e5af34ff36848cb9e42855c1d173081"><td class="cellrowborder" valign="top" width="24.702470247024703%" headers="mcps1.2.4.1.1 "><p id="a194412d25ff14c699f54d9d578dc145f"><a name="a194412d25ff14c699f54d9d578dc145f"></a><a name="a194412d25ff14c699f54d9d578dc145f"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="21.25212521252125%" headers="mcps1.2.4.1.2 "><p id="af85e4b0765f84fa29ebaf6149f3d014f"><a name="af85e4b0765f84fa29ebaf6149f3d014f"></a><a name="af85e4b0765f84fa29ebaf6149f3d014f"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="54.045404540454044%" headers="mcps1.2.4.1.3 "><p id="a5cc1c775e2d5462589fffa4ec954aa30"><a name="a5cc1c775e2d5462589fffa4ec954aa30"></a><a name="a5cc1c775e2d5462589fffa4ec954aa30"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="sae909138a6384d598a5abdab965f3b5f"></a>

N/A

## 响应消息<a name="sfbfa68773c254ab2aa9a05ac4c2968bd"></a>

**响应示例：**

Pod打印消息为Helloworld：

```
Tue Sep  3 03:15:25 UTC 2019
Helloworld
Tue Sep  3 03:15:26 UTC 2019
Helloworld
Tue Sep  3 03:15:27 UTC 2019
Helloworld
```

## 状态码<a name="s4baae12d06434a838dd91d75626b67a1"></a>

**表 3**  状态码

<a name="zh-cn_topic_0079614904_table20680137"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614904_row35122812"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p38215036205834"><a name="p38215036205834"></a><a name="p38215036205834"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p8410240205834"><a name="p8410240205834"></a><a name="p8410240205834"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614904_row43124371"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614904_p3413175"><a name="zh-cn_topic_0079614904_p3413175"></a><a name="zh-cn_topic_0079614904_p3413175"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614904_p8031722"><a name="zh-cn_topic_0079614904_p8031722"></a><a name="zh-cn_topic_0079614904_p8031722"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

