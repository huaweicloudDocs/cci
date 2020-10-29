# 删除Network<a name="cci_02_2016"></a>

## 功能介绍<a name="section1686113493165"></a>

删除一个指定Network对象。

## URI<a name="section8403243161416"></a>

DELETE /apis/networking.cci.io/v1beta1/namespaces/\{namespace\}/networks/\{name\}

**表 1**  Path参数

<a name="table14116182419179"></a>
<table><thead align="left"><tr id="row151161124131713"><th class="cellrowborder" valign="top" width="18%" id="mcps1.2.5.1.1"><p id="p7116102411175"><a name="p7116102411175"></a><a name="p7116102411175"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9%" id="mcps1.2.5.1.2"><p id="p1311614248179"><a name="p1311614248179"></a><a name="p1311614248179"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="p1891094219478"><a name="p1891094219478"></a><a name="p1891094219478"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="63%" id="mcps1.2.5.1.4"><p id="p1913212418176"><a name="p1913212418176"></a><a name="p1913212418176"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9132424201715"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.5.1.1 "><p id="p10132124141712"><a name="p10132124141712"></a><a name="p10132124141712"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p91321024201717"><a name="p91321024201717"></a><a name="p91321024201717"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p19910542114715"><a name="p19910542114715"></a><a name="p19910542114715"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p141322024151712"><a name="p141322024151712"></a><a name="p141322024151712"></a>命名空间。</p>
</td>
</tr>
<tr id="row713232412177"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.5.1.1 "><p id="p17132152417178"><a name="p17132152417178"></a><a name="p17132152417178"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="9%" headers="mcps1.2.5.1.2 "><p id="p713272417176"><a name="p713272417176"></a><a name="p713272417176"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="p17910154210475"><a name="p17910154210475"></a><a name="p17910154210475"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63%" headers="mcps1.2.5.1.4 "><p id="p6132102411170"><a name="p6132102411170"></a><a name="p6132102411170"></a>要删除的Network名称。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079615000_table64523107"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615000_row55516030"><th class="cellrowborder" valign="top" width="21.782178217821784%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0079615000_p504568"><a name="zh-cn_topic_0079615000_p504568"></a><a name="zh-cn_topic_0079615000_p504568"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.900990099009901%" id="mcps1.2.5.1.2"><p id="p64287338205444"><a name="p64287338205444"></a><a name="p64287338205444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="12.871287128712872%" id="mcps1.2.5.1.3"><p id="p18478185523915"><a name="p18478185523915"></a><a name="p18478185523915"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.44554455445545%" id="mcps1.2.5.1.4"><p id="p39891894205444"><a name="p39891894205444"></a><a name="p39891894205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615000_row48602122"><td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615000_p44457847"><a name="zh-cn_topic_0079615000_p44457847"></a><a name="zh-cn_topic_0079615000_p44457847"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="9.900990099009901%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615000_p44315844"><a name="zh-cn_topic_0079615000_p44315844"></a><a name="zh-cn_topic_0079615000_p44315844"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="12.871287128712872%" headers="mcps1.2.5.1.3 "><p id="p047811555392"><a name="p047811555392"></a><a name="p047811555392"></a><span>String</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.44554455445545%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615000_p32813593"><a name="zh-cn_topic_0079615000_p32813593"></a><a name="zh-cn_topic_0079615000_p32813593"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row14243172612403"><td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.2.5.1.1 "><p id="p42431526144010"><a name="p42431526144010"></a><a name="p42431526144010"></a><span>propagationPolicy</span></p>
</td>
<td class="cellrowborder" valign="top" width="9.900990099009901%" headers="mcps1.2.5.1.2 "><p id="p1624362616401"><a name="p1624362616401"></a><a name="p1624362616401"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="12.871287128712872%" headers="mcps1.2.5.1.3 "><p id="p10243182694014"><a name="p10243182694014"></a><a name="p10243182694014"></a><span>String</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.44554455445545%" headers="mcps1.2.5.1.4 "><p id="p6243426154012"><a name="p6243426154012"></a><a name="p6243426154012"></a><span>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: </span><em id="i1852514174019"><a name="i1852514174019"></a><a name="i1852514174019"></a>Orphan</em><span>- orphan the dependents; </span><em id="i1852564114017"><a name="i1852564114017"></a><a name="i1852564114017"></a>Background</em><span> - allow the garbage collector to delete the dependents in the background; </span><em id="i10525174134013"><a name="i10525174134013"></a><a name="i10525174134013"></a>Foreground</em><span> - a cascading policy that deletes all dependents in the foreground.</span></p>
</td>
</tr>
<tr id="row9618126114019"><td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.2.5.1.1 "><p id="p176181226114017"><a name="p176181226114017"></a><a name="p176181226114017"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="9.900990099009901%" headers="mcps1.2.5.1.2 "><p id="p106181266407"><a name="p106181266407"></a><a name="p106181266407"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="12.871287128712872%" headers="mcps1.2.5.1.3 "><p id="p1461822617404"><a name="p1461822617404"></a><a name="p1461822617404"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="55.44554455445545%" headers="mcps1.2.5.1.4 "><p id="p1961815263404"><a name="p1961815263404"></a><a name="p1961815263404"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object’s finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row1172064412"><td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.2.5.1.1 "><p id="p272967414"><a name="p272967414"></a><a name="p272967414"></a><span>gracePeriodSeconds</span></p>
</td>
<td class="cellrowborder" valign="top" width="9.900990099009901%" headers="mcps1.2.5.1.2 "><p id="p2723617414"><a name="p2723617414"></a><a name="p2723617414"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="12.871287128712872%" headers="mcps1.2.5.1.3 "><p id="p77226114115"><a name="p77226114115"></a><a name="p77226114115"></a><span>integer (int32)</span></p>
</td>
<td class="cellrowborder" valign="top" width="55.44554455445545%" headers="mcps1.2.5.1.4 "><p id="p8727684117"><a name="p8727684117"></a><a name="p8727684117"></a><span>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</span></p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section56528519"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

```
{
    "Kind": "DeleteOptions",
    "apiVersion": "v1",
    "gracePeriodSeconds": 0
}
```

## 响应消息<a name="section38994624"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "Status",
    "apiVersion": "v1",
    "metadata": {},
    "status": "Success",
    "details": {
        "name": "network-12130306",
        "group": "networking.cci.io",
        "kind": "networks",
        "uid": "27072a31-dfb3-11e7-9c19-fa163e2d897b"
    },
    "code": 200
}
```

## 状态码<a name="section15407297"></a>

[表3](#d0e35248)描述API的状态码。

**表 3**  状态码

<a name="d0e35248"></a>
<table><thead align="left"><tr id="row25883953"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p16225480"><a name="p16225480"></a><a name="p16225480"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p39195466"><a name="p39195466"></a><a name="p39195466"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row20716193"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p290101"><a name="p290101"></a><a name="p290101"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p23498221"><a name="p23498221"></a><a name="p23498221"></a>Delete a Network resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

