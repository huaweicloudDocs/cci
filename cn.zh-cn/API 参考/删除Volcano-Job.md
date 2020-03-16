# 删除Volcano Job<a name="cci_02_3137"></a>

## 功能介绍<a name="section19030251"></a>

删除Volcano Job。

## URI<a name="section37054533"></a>

DELETE /apis/batch.volcano.sh/v1alpha1/namespaces/\{namespace\}/jobs/\{name\}

**表 1**  Path参数

<a name="d0e45179"></a>
<table><thead align="left"><tr id="row64943380"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.318368163183685%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.273672632736734%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row61989525"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1834011925520"><a name="p1834011925520"></a><a name="p1834011925520"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1733951915512"><a name="p1733951915512"></a><a name="p1733951915512"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p143381019155512"><a name="p143381019155512"></a><a name="p143381019155512"></a>name of the Volcano Job</p>
</td>
</tr>
<tr id="row64568614216"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1445726823"><a name="p1445726823"></a><a name="p1445726823"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1844813188462"><a name="p1844813188462"></a><a name="p1844813188462"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1045718610211"><a name="p1045718610211"></a><a name="p1045718610211"></a>object name and auth scope, such as for teams and projects</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table11308949102120"></a>
<table><thead align="left"><tr id="row23131949192118"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p8316349122119"><a name="p8316349122119"></a><a name="p8316349122119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.318368163183685%" id="mcps1.2.4.1.2"><p id="p1231884913215"><a name="p1231884913215"></a><a name="p1231884913215"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.273672632736734%" id="mcps1.2.4.1.3"><p id="p2321124920215"><a name="p2321124920215"></a><a name="p2321124920215"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10334449142116"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p883818599545"><a name="p883818599545"></a><a name="p883818599545"></a>dryRun</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p6723919155117"><a name="p6723919155117"></a><a name="p6723919155117"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p19837859165418"><a name="p19837859165418"></a><a name="p19837859165418"></a>When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed</p>
</td>
</tr>
<tr id="row13340949102114"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1837105955414"><a name="p1837105955414"></a><a name="p1837105955414"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p672910198515"><a name="p672910198515"></a><a name="p672910198515"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1835159115412"><a name="p1835159115412"></a><a name="p1835159115412"></a>The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row1934684942112"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p7834175920549"><a name="p7834175920549"></a><a name="p7834175920549"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p57331819185117"><a name="p57331819185117"></a><a name="p57331819185117"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1083315596543"><a name="p1083315596543"></a><a name="p1083315596543"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the “orphan” finalizer will be added to/removed from the object’s finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row1235224982117"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p583285985414"><a name="p583285985414"></a><a name="p583285985414"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p6737181919511"><a name="p6737181919511"></a><a name="p6737181919511"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p11831185919540"><a name="p11831185919540"></a><a name="p11831185919540"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: ‘Orphan’ - orphan the dependents; ‘Background’ - allow the garbage collector to delete the dependents in the background; ‘Foreground’ - a cascading policy that deletes all dependents in the foreground.</p>
</td>
</tr>
<tr id="row6360204912217"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p78302591540"><a name="p78302591540"></a><a name="p78302591540"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p97401719185110"><a name="p97401719185110"></a><a name="p97401719185110"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p782915915547"><a name="p782915915547"></a><a name="p782915915547"></a>If 'true’, then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section65055348"></a>

N/A

## 响应消息<a name="section48627224"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例**：

```
{
    "kind": "Status",
    "apiVersion": "v1",
    "metadata": {},
    "status": "Success",
    "details": {
        "name": "openmpi-hello-3-com",
        "group": "batch.volcano.sh",
        "kind": "jobs",
        "uid": "1a32a8c4-97db-11e9-9d09-dc9914fb58e0"
    }
}
```

## 状态码<a name="section34991834"></a>

**表 3**  状态码

<a name="d0e45308"></a>
<table><thead align="left"><tr id="row6630185"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p174074"><a name="p174074"></a><a name="p174074"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p14100028"><a name="p14100028"></a><a name="p14100028"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1251606"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1367711985419"><a name="p1367711985419"></a><a name="p1367711985419"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1767541915544"><a name="p1767541915544"></a><a name="p1767541915544"></a>OK</p>
</td>
</tr>
<tr id="row230913431157"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1831019435514"><a name="p1831019435514"></a><a name="p1831019435514"></a>202</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p2031010435518"><a name="p2031010435518"></a><a name="p2031010435518"></a>Accepted</p>
</td>
</tr>
<tr id="row167323113611"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p273218112610"><a name="p273218112610"></a><a name="p273218112610"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p19732111364"><a name="p19732111364"></a><a name="p19732111364"></a>Unauthorized</p>
</td>
</tr>
<tr id="row12703150163313"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p107041043310"><a name="p107041043310"></a><a name="p107041043310"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p57047053313"><a name="p57047053313"></a><a name="p57047053313"></a>Internal Error</p>
</td>
</tr>
<tr id="row9831203210370"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1831173243713"><a name="p1831173243713"></a><a name="p1831173243713"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p158311832103714"><a name="p158311832103714"></a><a name="p158311832103714"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

