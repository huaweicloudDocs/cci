# 删除Deployment<a name="cci_02_0027"></a>

## 功能介绍<a name="zh-cn_topic_0091433673_section65321233"></a>

This API is used to delete a Deployment resource object.

## URI<a name="zh-cn_topic_0091433673_section51020189"></a>

DELETE /apis/apps/v1beta1/namespaces/\{namespace\}/deployments/\{name\}

[表1](#zh-cn_topic_0091433673_table2758112513516)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433673_table2758112513516"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433673_row65815647"><th class="cellrowborder" valign="top" width="17.348265173482652%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433673_p65652297517"><a name="zh-cn_topic_0091433673_p65652297517"></a><a name="zh-cn_topic_0091433673_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433673_p165661629135114"><a name="zh-cn_topic_0091433673_p165661629135114"></a><a name="zh-cn_topic_0091433673_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="66.32336766323368%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433673_p14567629115114"><a name="zh-cn_topic_0091433673_p14567629115114"></a><a name="zh-cn_topic_0091433673_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433673_row5608934"><td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433673_p51670535"><a name="zh-cn_topic_0091433673_p51670535"></a><a name="zh-cn_topic_0091433673_p51670535"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433673_p24563845"><a name="zh-cn_topic_0091433673_p24563845"></a><a name="zh-cn_topic_0091433673_p24563845"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433673_p43514439"><a name="zh-cn_topic_0091433673_p43514439"></a><a name="zh-cn_topic_0091433673_p43514439"></a>name of the Deployment</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433673_row56085638"><td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433673_p46642793"><a name="zh-cn_topic_0091433673_p46642793"></a><a name="zh-cn_topic_0091433673_p46642793"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433673_p19969926"><a name="zh-cn_topic_0091433673_p19969926"></a><a name="zh-cn_topic_0091433673_p19969926"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433673_row62561693"><td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433673_p34332366"><a name="zh-cn_topic_0091433673_p34332366"></a><a name="zh-cn_topic_0091433673_p34332366"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433673_p29458227"><a name="zh-cn_topic_0091433673_p29458227"></a><a name="zh-cn_topic_0091433673_p29458227"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433673_p37306164"><a name="zh-cn_topic_0091433673_p37306164"></a><a name="zh-cn_topic_0091433673_p37306164"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433673_row211163"><td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433673_p17104275"><a name="zh-cn_topic_0091433673_p17104275"></a><a name="zh-cn_topic_0091433673_p17104275"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433673_p43269019"><a name="zh-cn_topic_0091433673_p43269019"></a><a name="zh-cn_topic_0091433673_p43269019"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433673_p15129627"><a name="zh-cn_topic_0091433673_p15129627"></a><a name="zh-cn_topic_0091433673_p15129627"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433673_row1948920"><td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433673_p23644832"><a name="zh-cn_topic_0091433673_p23644832"></a><a name="zh-cn_topic_0091433673_p23644832"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433673_p36183253"><a name="zh-cn_topic_0091433673_p36183253"></a><a name="zh-cn_topic_0091433673_p36183253"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433673_p45162366"><a name="zh-cn_topic_0091433673_p45162366"></a><a name="zh-cn_topic_0091433673_p45162366"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433673_row3808114"><td class="cellrowborder" valign="top" width="17.348265173482652%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433673_p40021797"><a name="zh-cn_topic_0091433673_p40021797"></a><a name="zh-cn_topic_0091433673_p40021797"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433673_p20540096"><a name="zh-cn_topic_0091433673_p20540096"></a><a name="zh-cn_topic_0091433673_p20540096"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66.32336766323368%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433673_p53135084"><a name="zh-cn_topic_0091433673_p53135084"></a><a name="zh-cn_topic_0091433673_p53135084"></a></p>
<p id="zh-cn_topic_0091433673_p8453712"><a name="zh-cn_topic_0091433673_p8453712"></a><a name="zh-cn_topic_0091433673_p8453712"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433673_section56528519"></a>

**请求参数：**

请求参数如[表65](公共参数.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

-   只删除Deployment（对应ReplicSet和Pod不删除）

    ```
    {
        "Kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Orphan"
    }
    ```

-   前台级联删除（按照Pod-\>ReplicaSet-\>Deployment的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Foreground"
    }
    ```

-   后台级联删除（按照Deployment-\>ReplicaSet-\>Pod的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Background"
    }
    ```


## 响应消息<a name="zh-cn_topic_0091433673_section38994624"></a>

**响应参数：**

响应参数的详细描述请参见[表52](公共响应参数（OLD-VERSIONS）.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "Status", 
    "apiVersion": "v1", 
    "metadata": {}, 
    "status": "Success", 
    "details": {
        "name": "deployment-test", 
        "group": "extensions", 
        "kind": "deployments", 
        "uid": "ed89a51c-2728-11e8-b891-84a9c46e8c8b"
    }, 
    "code": 200
}
```

## 状态码<a name="zh-cn_topic_0091433673_section15407297"></a>

[表2](#zh-cn_topic_0091433673_d0e35248)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433673_d0e35248"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433673_row25883953"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433673_p16225480"><a name="zh-cn_topic_0091433673_p16225480"></a><a name="zh-cn_topic_0091433673_p16225480"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433673_p39195466"><a name="zh-cn_topic_0091433673_p39195466"></a><a name="zh-cn_topic_0091433673_p39195466"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433673_row20716193"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433673_p290101"><a name="zh-cn_topic_0091433673_p290101"></a><a name="zh-cn_topic_0091433673_p290101"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433673_p23498221"><a name="zh-cn_topic_0091433673_p23498221"></a><a name="zh-cn_topic_0091433673_p23498221"></a>Delete a Deployments resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

