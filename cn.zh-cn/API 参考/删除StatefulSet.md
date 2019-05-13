# 删除StatefulSet<a name="cci_02_3029"></a>

## 功能介绍<a name="section31372179"></a>

删除StatefulSet。

## URI<a name="section13914160"></a>

DELETE /apis/apps/v1/namespaces/\{namespace\}/statefulsets/\{name\}

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
<tr id="row13794857171116"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p5984165818113"><a name="p5984165818113"></a><a name="p5984165818113"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the StatefulSet.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="d0e38270"></a>
<table><thead align="left"><tr id="row14143522"><th class="cellrowborder" valign="top" width="21.21%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="62.629999999999995%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2320041"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="p53705670"><a name="p53705670"></a><a name="p53705670"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p55192003"><a name="p55192003"></a><a name="p55192003"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="p41367240"><a name="p41367240"></a><a name="p41367240"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row36760846"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="p24838515"><a name="p24838515"></a><a name="p24838515"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p65762676"><a name="p65762676"></a><a name="p65762676"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="p25176571"><a name="p25176571"></a><a name="p25176571"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row25262547"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="p33000411"><a name="p33000411"></a><a name="p33000411"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p55787611"><a name="p55787611"></a><a name="p55787611"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="p22502652"><a name="p22502652"></a><a name="p22502652"></a>Deprecated: Use the PropagationPolicy. This field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row1197280"><td class="cellrowborder" valign="top" width="21.21%" headers="mcps1.2.4.1.1 "><p id="p29870869"><a name="p29870869"></a><a name="p29870869"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p3621310"><a name="p3621310"></a><a name="p3621310"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="p168541140142815"><a name="p168541140142815"></a><a name="p168541140142815"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
<p id="p14884542142816"><a name="p14884542142816"></a><a name="p14884542142816"></a>Acceptable values are:</p>
<p id="p1360412456287"><a name="p1360412456287"></a><a name="p1360412456287"></a>'<strong id="b114631449152819"><a name="b114631449152819"></a><a name="b114631449152819"></a>Orphan</strong>' - orphan the dependents;</p>
<p id="p2044017414610"><a name="p2044017414610"></a><a name="p2044017414610"></a>'<strong id="b5198652192820"><a name="b5198652192820"></a><a name="b5198652192820"></a>Background</strong>' - allow the garbage collector to delete the dependents in the background; '<strong id="b310155592813"><a name="b310155592813"></a><a name="b310155592813"></a>Foreground</strong>' - a cascading policy that deletes all dependents in the foreground.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section58118584"></a>

**请求参数：**

请求参数如[表65](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

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


## 响应消息<a name="section53305210"></a>

**响应参数：**

响应参数的详细描述请参见[表73](数据结构.md#table37251757105918)。

**响应示例**：

```
{
  "kind": "Status",
  "apiVersion": "v1",
  "metadata": {

  },
  "status": "Success",
  "details": {
    "name": "statefulset-test",
    "group": "apps",
    "kind": "statefulsets",
    "uid": "5eb82b50-b028-11e8-9d5d-c88d83be759f"
  },
  "code": 200
}
```

## 状态码<a name="section9984849"></a>

[表3](#d0e38393)描述API的状态码。

**表 3**  状态码

<a name="d0e38393"></a>
<table><thead align="left"><tr id="row39018542"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p6385371"><a name="p6385371"></a><a name="p6385371"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p47453032"><a name="p47453032"></a><a name="p47453032"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row18490365"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p21324611"><a name="p21324611"></a><a name="p21324611"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p49571937"><a name="p49571937"></a><a name="p49571937"></a>Delete a StatefulSet resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

