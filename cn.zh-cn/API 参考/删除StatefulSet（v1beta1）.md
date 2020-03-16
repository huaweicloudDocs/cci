# 删除StatefulSet<a name="cci_02_0036"></a>

## 功能介绍<a name="zh-cn_topic_0091433688_section31372179"></a>

This API is used to delete a StatefulSet resource object.

## URI<a name="zh-cn_topic_0091433688_section13914160"></a>

DELETE /apis/apps/v1beta1/namespaces/\{namespace\}/statefulsets/\{name\}

[表1](#zh-cn_topic_0091433688_d0e38270)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433688_d0e38270"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433688_row14143522"><th class="cellrowborder" valign="top" width="21.21%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433688_p65652297517"><a name="zh-cn_topic_0091433688_p65652297517"></a><a name="zh-cn_topic_0091433688_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433688_p165661629135114"><a name="zh-cn_topic_0091433688_p165661629135114"></a><a name="zh-cn_topic_0091433688_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="62.629999999999995%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433688_p14567629115114"><a name="zh-cn_topic_0091433688_p14567629115114"></a><a name="zh-cn_topic_0091433688_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433688_row49796945"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433688_p7020714"><a name="zh-cn_topic_0091433688_p7020714"></a><a name="zh-cn_topic_0091433688_p7020714"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433688_p31806923"><a name="zh-cn_topic_0091433688_p31806923"></a><a name="zh-cn_topic_0091433688_p31806923"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433688_p26223965"><a name="zh-cn_topic_0091433688_p26223965"></a><a name="zh-cn_topic_0091433688_p26223965"></a>Name of the StatefulSet.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433688_row34689095"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433688_p58353349"><a name="zh-cn_topic_0091433688_p58353349"></a><a name="zh-cn_topic_0091433688_p58353349"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433688_p29000839"><a name="zh-cn_topic_0091433688_p29000839"></a><a name="zh-cn_topic_0091433688_p29000839"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433688_row2320041"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433688_p53705670"><a name="zh-cn_topic_0091433688_p53705670"></a><a name="zh-cn_topic_0091433688_p53705670"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433688_p55192003"><a name="zh-cn_topic_0091433688_p55192003"></a><a name="zh-cn_topic_0091433688_p55192003"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433688_p41367240"><a name="zh-cn_topic_0091433688_p41367240"></a><a name="zh-cn_topic_0091433688_p41367240"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433688_row36760846"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433688_p24838515"><a name="zh-cn_topic_0091433688_p24838515"></a><a name="zh-cn_topic_0091433688_p24838515"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433688_p65762676"><a name="zh-cn_topic_0091433688_p65762676"></a><a name="zh-cn_topic_0091433688_p65762676"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433688_p25176571"><a name="zh-cn_topic_0091433688_p25176571"></a><a name="zh-cn_topic_0091433688_p25176571"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433688_row25262547"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433688_p33000411"><a name="zh-cn_topic_0091433688_p33000411"></a><a name="zh-cn_topic_0091433688_p33000411"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433688_p55787611"><a name="zh-cn_topic_0091433688_p55787611"></a><a name="zh-cn_topic_0091433688_p55787611"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433688_p22502652"><a name="zh-cn_topic_0091433688_p22502652"></a><a name="zh-cn_topic_0091433688_p22502652"></a>Deprecated: Use the PropagationPolicy. This field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433688_row1197280"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433688_p29870869"><a name="zh-cn_topic_0091433688_p29870869"></a><a name="zh-cn_topic_0091433688_p29870869"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433688_p3621310"><a name="zh-cn_topic_0091433688_p3621310"></a><a name="zh-cn_topic_0091433688_p3621310"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433688_p22689637"><a name="zh-cn_topic_0091433688_p22689637"></a><a name="zh-cn_topic_0091433688_p22689637"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433688_section58118584"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

-   只删除StatefulSet（对应Pod不删除）

    ```
    {
        "Kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Orphan"
    }
    ```

-   前台级联删除（按照Pod-\>StatefulSet的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Foreground"
    }
    ```

-   后台级联删除（按照StatefulSet-\>Pod的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Background"
    }
    ```


## 响应消息<a name="zh-cn_topic_0091433688_section53305210"></a>

**响应参数：**

响应参数的详细描述请参见[表52](响应数据结构（OLD-VERSIONS）.md#table37251757105918)。

响应示例：

```
{
    "kind": "Status", 
    "apiVersion": "v1", 
    "metadata": {}, 
    "status": "Success", 
    "details": {
        "name": "statefulset-test", 
        "group": "apps", 
        "kind": "statefulsets", 
        "uid": "ee0ef0d0-2728-11e8-8930-84a9c46e8ca3"
    }, 
    "code": 200
}
```

## 状态码<a name="zh-cn_topic_0091433688_section9984849"></a>

[表2](#zh-cn_topic_0091433688_d0e38393)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433688_d0e38393"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433688_row39018542"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433688_p6385371"><a name="zh-cn_topic_0091433688_p6385371"></a><a name="zh-cn_topic_0091433688_p6385371"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433688_p47453032"><a name="zh-cn_topic_0091433688_p47453032"></a><a name="zh-cn_topic_0091433688_p47453032"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433688_row18490365"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433688_p21324611"><a name="zh-cn_topic_0091433688_p21324611"></a><a name="zh-cn_topic_0091433688_p21324611"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433688_p49571937"><a name="zh-cn_topic_0091433688_p49571937"></a><a name="zh-cn_topic_0091433688_p49571937"></a>Delete a StatefulSet resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

