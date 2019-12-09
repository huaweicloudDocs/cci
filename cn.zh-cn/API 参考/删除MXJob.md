# 删除MXJob<a name="cci_02_3155"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

删除MXJob。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

DELETE /apis/kubeflow.org/v1/namespaces/\{namespace\}/mxjobs/\{name\}

**表 1**  Path参数

<a name="zh-cn_topic_0083864910_table167042013408"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row2067022020405"><th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0083864910_p65652297517"><a name="zh-cn_topic_0083864910_p65652297517"></a><a name="zh-cn_topic_0083864910_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.772277227722775%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0083864910_p165661629135114"><a name="zh-cn_topic_0083864910_p165661629135114"></a><a name="zh-cn_topic_0083864910_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.4059405940594%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0083864910_p14567629115114"><a name="zh-cn_topic_0083864910_p14567629115114"></a><a name="zh-cn_topic_0083864910_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row1670122004014"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p54235140273"><a name="p54235140273"></a><a name="p54235140273"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p204291838165515"><a name="p204291838165515"></a><a name="p204291838165515"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p34231146275"><a name="p34231146275"></a><a name="p34231146275"></a>name of the MXJob</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row136701220114011"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p1342415144273"><a name="p1342415144273"></a><a name="p1342415144273"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p64321638135514"><a name="p64321638135514"></a><a name="p64321638135514"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p164241014112713"><a name="p164241014112713"></a><a name="p164241014112713"></a>object name and auth scope, such as for teams and projects</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table20890193762714"></a>
<table><thead align="left"><tr id="row198912378271"><th class="cellrowborder" valign="top" width="21.542154215421544%" id="mcps1.2.4.1.1"><p id="p591823113285"><a name="p591823113285"></a><a name="p591823113285"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.02150215021502%" id="mcps1.2.4.1.2"><p id="p2091893102818"><a name="p2091893102818"></a><a name="p2091893102818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.43634363436343%" id="mcps1.2.4.1.3"><p id="p189181631142812"><a name="p189181631142812"></a><a name="p189181631142812"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row158911379278"><td class="cellrowborder" valign="top" width="21.542154215421544%" headers="mcps1.2.4.1.1 "><p id="p1886014491287"><a name="p1886014491287"></a><a name="p1886014491287"></a>dryRun</p>
</td>
<td class="cellrowborder" valign="top" width="15.02150215021502%" headers="mcps1.2.4.1.2 "><p id="p1761745614524"><a name="p1761745614524"></a><a name="p1761745614524"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.43634363436343%" headers="mcps1.2.4.1.3 "><p id="p98605492284"><a name="p98605492284"></a><a name="p98605492284"></a>When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed</p>
</td>
</tr>
<tr id="row1891737172714"><td class="cellrowborder" valign="top" width="21.542154215421544%" headers="mcps1.2.4.1.1 "><p id="p88601949102813"><a name="p88601949102813"></a><a name="p88601949102813"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="15.02150215021502%" headers="mcps1.2.4.1.2 "><p id="p196201056165210"><a name="p196201056165210"></a><a name="p196201056165210"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.43634363436343%" headers="mcps1.2.4.1.3 "><p id="p1860184915286"><a name="p1860184915286"></a><a name="p1860184915286"></a>The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row28911377279"><td class="cellrowborder" valign="top" width="21.542154215421544%" headers="mcps1.2.4.1.1 "><p id="p68601349132816"><a name="p68601349132816"></a><a name="p68601349132816"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="15.02150215021502%" headers="mcps1.2.4.1.2 "><p id="p956495811520"><a name="p956495811520"></a><a name="p956495811520"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.43634363436343%" headers="mcps1.2.4.1.3 "><p id="p486014497280"><a name="p486014497280"></a><a name="p486014497280"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the “orphan” finalizer will be added to/removed from the object’s finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row1389163762710"><td class="cellrowborder" valign="top" width="21.542154215421544%" headers="mcps1.2.4.1.1 "><p id="p12860249112810"><a name="p12860249112810"></a><a name="p12860249112810"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="15.02150215021502%" headers="mcps1.2.4.1.2 "><p id="p25691358165216"><a name="p25691358165216"></a><a name="p25691358165216"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.43634363436343%" headers="mcps1.2.4.1.3 "><p id="p1386084922816"><a name="p1386084922816"></a><a name="p1386084922816"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: ‘Orphan’ - orphan the dependents; ‘Background’ - allow the garbage collector to delete the dependents in the background; ‘Foreground’ - a cascading policy that deletes all dependents in the foreground.</p>
</td>
</tr>
<tr id="row1189163717273"><td class="cellrowborder" valign="top" width="21.542154215421544%" headers="mcps1.2.4.1.1 "><p id="p1586015497285"><a name="p1586015497285"></a><a name="p1586015497285"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="15.02150215021502%" headers="mcps1.2.4.1.2 "><p id="p657395885213"><a name="p657395885213"></a><a name="p657395885213"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.43634363436343%" headers="mcps1.2.4.1.3 "><p id="p386016496281"><a name="p386016496281"></a><a name="p386016496281"></a>If 'true’, then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "Status",
    "apiVersion": "v1",
    "metadata": {},
    "status": "Success",
    "details": {
        "name": "mxnet-job",
        "group": "kubeflow.org",
        "kind": "mxjobs",
        "uid": "fac6dcd2-adee-11e9-8041-340a9837e2a7"
    }
}
```

## 状态码<a name="zh-cn_topic_0083864910_section16509142112516"></a>

**表 3**  状态码

<a name="zh-cn_topic_0083864910_table6957182913514"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row12961162965119"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0083864910_p189627299518"><a name="zh-cn_topic_0083864910_p189627299518"></a><a name="zh-cn_topic_0083864910_p189627299518"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0083864910_p1596342917515"><a name="zh-cn_topic_0083864910_p1596342917515"></a><a name="zh-cn_topic_0083864910_p1596342917515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p586645143113"><a name="p586645143113"></a><a name="p586645143113"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p6866205113316"><a name="p6866205113316"></a><a name="p6866205113316"></a>OK</p>
</td>
</tr>
<tr id="row0499135010312"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p286625193115"><a name="p286625193115"></a><a name="p286625193115"></a>202</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9866651153110"><a name="p9866651153110"></a><a name="p9866651153110"></a>Accepted</p>
</td>
</tr>
<tr id="row3472154410294"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1866165116317"><a name="p1866165116317"></a><a name="p1866165116317"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1286612515312"><a name="p1286612515312"></a><a name="p1286612515312"></a>Unauthorized</p>
</td>
</tr>
<tr id="row645473822914"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1786615110316"><a name="p1786615110316"></a><a name="p1786615110316"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p13866175114316"><a name="p13866175114316"></a><a name="p13866175114316"></a>Internal Error</p>
</td>
</tr>
<tr id="row1137716489314"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p486612511315"><a name="p486612511315"></a><a name="p486612511315"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p16866451163110"><a name="p16866451163110"></a><a name="p16866451163110"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

