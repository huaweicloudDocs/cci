# 创建Deployment回滚（v1beta1）<a name="cci_02_0026"></a>

## 功能介绍<a name="zh-cn_topic_0091433672_section41398477"></a>

This API is used to create rollback of a Deployment Rollback

## URI<a name="zh-cn_topic_0091433672_section37041974"></a>

POST /apis/apps/v1beta1/namespaces/\{namespace\}/deployments/\{name\}/rollback

[表1](#zh-cn_topic_0091433672_d0e34843)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433672_d0e34843"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433672_row27299130"><th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433672_p65652297517"><a name="zh-cn_topic_0091433672_p65652297517"></a><a name="zh-cn_topic_0091433672_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433672_p165661629135114"><a name="zh-cn_topic_0091433672_p165661629135114"></a><a name="zh-cn_topic_0091433672_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="67.67999999999999%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433672_p14567629115114"><a name="zh-cn_topic_0091433672_p14567629115114"></a><a name="zh-cn_topic_0091433672_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433672_row41719447"><td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433672_p23832023"><a name="zh-cn_topic_0091433672_p23832023"></a><a name="zh-cn_topic_0091433672_p23832023"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433672_p51345720"><a name="zh-cn_topic_0091433672_p51345720"></a><a name="zh-cn_topic_0091433672_p51345720"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="67.67999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433672_p65362657"><a name="zh-cn_topic_0091433672_p65362657"></a><a name="zh-cn_topic_0091433672_p65362657"></a>Name of the Deployment Rollback.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433672_row51393009"><td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433672_p2084186"><a name="zh-cn_topic_0091433672_p2084186"></a><a name="zh-cn_topic_0091433672_p2084186"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433672_p34601376"><a name="zh-cn_topic_0091433672_p34601376"></a><a name="zh-cn_topic_0091433672_p34601376"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="67.67999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433672_row58579196"><td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433672_p47294440"><a name="zh-cn_topic_0091433672_p47294440"></a><a name="zh-cn_topic_0091433672_p47294440"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433672_p5644428"><a name="zh-cn_topic_0091433672_p5644428"></a><a name="zh-cn_topic_0091433672_p5644428"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="67.67999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433672_p54545553"><a name="zh-cn_topic_0091433672_p54545553"></a><a name="zh-cn_topic_0091433672_p54545553"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433672_section64942310"></a>

**请求参数：**

**表 2**  Request parameters

<a name="zh-cn_topic_0091433672_table10173552218"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433672_row31887193"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433672_p32725858"><a name="zh-cn_topic_0091433672_p32725858"></a><a name="zh-cn_topic_0091433672_p32725858"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433672_p33548811"><a name="zh-cn_topic_0091433672_p33548811"></a><a name="zh-cn_topic_0091433672_p33548811"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="22%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433672_p33099132"><a name="zh-cn_topic_0091433672_p33099132"></a><a name="zh-cn_topic_0091433672_p33099132"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="43%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433672_p63784030"><a name="zh-cn_topic_0091433672_p63784030"></a><a name="zh-cn_topic_0091433672_p63784030"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433672_row66232792"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433672_p63255955"><a name="zh-cn_topic_0091433672_p63255955"></a><a name="zh-cn_topic_0091433672_p63255955"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433672_p23458743"><a name="zh-cn_topic_0091433672_p23458743"></a><a name="zh-cn_topic_0091433672_p23458743"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433672_p21109994"><a name="zh-cn_topic_0091433672_p21109994"></a><a name="zh-cn_topic_0091433672_p21109994"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433672_p32187991"><a name="zh-cn_topic_0091433672_p32187991"></a><a name="zh-cn_topic_0091433672_p32187991"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433672_row21256466"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433672_p44052166"><a name="zh-cn_topic_0091433672_p44052166"></a><a name="zh-cn_topic_0091433672_p44052166"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433672_p11455687"><a name="zh-cn_topic_0091433672_p11455687"></a><a name="zh-cn_topic_0091433672_p11455687"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433672_p55495420"><a name="zh-cn_topic_0091433672_p55495420"></a><a name="zh-cn_topic_0091433672_p55495420"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433672_p65944013"><a name="zh-cn_topic_0091433672_p65944013"></a><a name="zh-cn_topic_0091433672_p65944013"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433672_row56625212"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433672_p23239492"><a name="zh-cn_topic_0091433672_p23239492"></a><a name="zh-cn_topic_0091433672_p23239492"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433672_p3350684"><a name="zh-cn_topic_0091433672_p3350684"></a><a name="zh-cn_topic_0091433672_p3350684"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433672_p2969964"><a name="zh-cn_topic_0091433672_p2969964"></a><a name="zh-cn_topic_0091433672_p2969964"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433672_p39240541"><a name="zh-cn_topic_0091433672_p39240541"></a><a name="zh-cn_topic_0091433672_p39240541"></a>Required: This must match the Name of a deployment.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433672_row17620553"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433672_p17978702"><a name="zh-cn_topic_0091433672_p17978702"></a><a name="zh-cn_topic_0091433672_p17978702"></a>rollbackTo</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433672_p46988743"><a name="zh-cn_topic_0091433672_p46988743"></a><a name="zh-cn_topic_0091433672_p46988743"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433672_p47991837"><a name="zh-cn_topic_0091433672_p47991837"></a><a name="zh-cn_topic_0091433672_p47991837"></a><a href="#cci_02_0026__zh-cn_topic_0091433672_table3169229152410">表3</a></p>
</td>
<td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433672_p22331121"><a name="zh-cn_topic_0091433672_p22331121"></a><a name="zh-cn_topic_0091433672_p22331121"></a>The config of this deployment rollback.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433672_row66762365"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433672_p39042521"><a name="zh-cn_topic_0091433672_p39042521"></a><a name="zh-cn_topic_0091433672_p39042521"></a>updatedAnnotations</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433672_p8327600"><a name="zh-cn_topic_0091433672_p8327600"></a><a name="zh-cn_topic_0091433672_p8327600"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433672_p3447020"><a name="zh-cn_topic_0091433672_p3447020"></a><a name="zh-cn_topic_0091433672_p3447020"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433672_p10773237"><a name="zh-cn_topic_0091433672_p10773237"></a><a name="zh-cn_topic_0091433672_p10773237"></a>The annotations to be updated to a deployment</p>
</td>
</tr>
</tbody>
</table>

**表 3**  rollbackTo字段数据结构说明

<a name="zh-cn_topic_0091433672_table3169229152410"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433672_row49859166"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433672_p12060663"><a name="zh-cn_topic_0091433672_p12060663"></a><a name="zh-cn_topic_0091433672_p12060663"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433672_p37389616"><a name="zh-cn_topic_0091433672_p37389616"></a><a name="zh-cn_topic_0091433672_p37389616"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433672_p8660017"><a name="zh-cn_topic_0091433672_p8660017"></a><a name="zh-cn_topic_0091433672_p8660017"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433672_p30372771"><a name="zh-cn_topic_0091433672_p30372771"></a><a name="zh-cn_topic_0091433672_p30372771"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433672_row44275373"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433672_p29535480"><a name="zh-cn_topic_0091433672_p29535480"></a><a name="zh-cn_topic_0091433672_p29535480"></a>revision</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433672_p43563692"><a name="zh-cn_topic_0091433672_p43563692"></a><a name="zh-cn_topic_0091433672_p43563692"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433672_p38998127"><a name="zh-cn_topic_0091433672_p38998127"></a><a name="zh-cn_topic_0091433672_p38998127"></a>integer</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433672_p4731756"><a name="zh-cn_topic_0091433672_p4731756"></a><a name="zh-cn_topic_0091433672_p4731756"></a>The revision to rollback to. If set to 0, rollback to the last revision.</p>
</td>
</tr>
</tbody>
</table>

**请求示例：**

```
{
    "kind": "DeploymentRollback", 
    "apiVersion": "apps/v1beta1", 
    "name": "deployment-test", 
    "rollbackTo": {
        "revision": 0
    }
}
```

## 响应消息<a name="zh-cn_topic_0091433672_section47609878"></a>

**响应参数：**

响应参数的详细描述请参见[表2](#zh-cn_topic_0091433672_table10173552218)

**响应示例：**

```
{
    "kind": "Status", 
    "apiVersion": "v1", 
    "metadata": {}, 
    "status": "Success", 
    "message": "rollback request for deployment \"deployment-test\" succeeded", 
    "code": 201
}
```

## 状态码<a name="zh-cn_topic_0091433672_section25835719"></a>

[表4](#zh-cn_topic_0091433672_d0e35052)描述API的状态码。

**表 4**  状态码

<a name="zh-cn_topic_0091433672_d0e35052"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433672_row49033913"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433672_p12324050"><a name="zh-cn_topic_0091433672_p12324050"></a><a name="zh-cn_topic_0091433672_p12324050"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433672_p58723999"><a name="zh-cn_topic_0091433672_p58723999"></a><a name="zh-cn_topic_0091433672_p58723999"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433672_row59023497"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433672_p16173943"><a name="zh-cn_topic_0091433672_p16173943"></a><a name="zh-cn_topic_0091433672_p16173943"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433672_p35021010"><a name="zh-cn_topic_0091433672_p35021010"></a><a name="zh-cn_topic_0091433672_p35021010"></a>The request has been fulfilled, resulting in the creation of a new resource.</p>
</td>
</tr>
</tbody>
</table>

