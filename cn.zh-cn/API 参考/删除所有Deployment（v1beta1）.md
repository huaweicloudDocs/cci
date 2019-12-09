# 删除所有Deployment<a name="cci_02_0028"></a>

## 功能介绍<a name="zh-cn_topic_0091433674_section58759520"></a>

This API is used to delete collection of Deployment.

## URI<a name="zh-cn_topic_0091433674_section59073635"></a>

DELETE /apis/apps/v1beta1/namespaces/\{namespace\}/deployments

[表1](#zh-cn_topic_0091433674_d0e35322)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433674_d0e35322"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433674_row32289194"><th class="cellrowborder" valign="top" width="22.45%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433674_p65652297517"><a name="zh-cn_topic_0091433674_p65652297517"></a><a name="zh-cn_topic_0091433674_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.33%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433674_p165661629135114"><a name="zh-cn_topic_0091433674_p165661629135114"></a><a name="zh-cn_topic_0091433674_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.22%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433674_p14567629115114"><a name="zh-cn_topic_0091433674_p14567629115114"></a><a name="zh-cn_topic_0091433674_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433674_row60766168"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p23112558"><a name="zh-cn_topic_0091433674_p23112558"></a><a name="zh-cn_topic_0091433674_p23112558"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p60177946"><a name="zh-cn_topic_0091433674_p60177946"></a><a name="zh-cn_topic_0091433674_p60177946"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433674_row47634511"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p33190205"><a name="zh-cn_topic_0091433674_p33190205"></a><a name="zh-cn_topic_0091433674_p33190205"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p4052059"><a name="zh-cn_topic_0091433674_p4052059"></a><a name="zh-cn_topic_0091433674_p4052059"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433674_p59781329"><a name="zh-cn_topic_0091433674_p59781329"></a><a name="zh-cn_topic_0091433674_p59781329"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433674_row1161053"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p26936459"><a name="zh-cn_topic_0091433674_p26936459"></a><a name="zh-cn_topic_0091433674_p26936459"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p34369574"><a name="zh-cn_topic_0091433674_p34369574"></a><a name="zh-cn_topic_0091433674_p34369574"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433674_p32472085"><a name="zh-cn_topic_0091433674_p32472085"></a><a name="zh-cn_topic_0091433674_p32472085"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433674_row23813312"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p49830089"><a name="zh-cn_topic_0091433674_p49830089"></a><a name="zh-cn_topic_0091433674_p49830089"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p9705370"><a name="zh-cn_topic_0091433674_p9705370"></a><a name="zh-cn_topic_0091433674_p9705370"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433674_p47937500"><a name="zh-cn_topic_0091433674_p47937500"></a><a name="zh-cn_topic_0091433674_p47937500"></a></p>
<p id="zh-cn_topic_0091433674_p28784318"><a name="zh-cn_topic_0091433674_p28784318"></a><a name="zh-cn_topic_0091433674_p28784318"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433674_row57732278"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p45802961"><a name="zh-cn_topic_0091433674_p45802961"></a><a name="zh-cn_topic_0091433674_p45802961"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p19052373"><a name="zh-cn_topic_0091433674_p19052373"></a><a name="zh-cn_topic_0091433674_p19052373"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433674_p66847208"><a name="zh-cn_topic_0091433674_p66847208"></a><a name="zh-cn_topic_0091433674_p66847208"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433674_row64753968"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p10580064"><a name="zh-cn_topic_0091433674_p10580064"></a><a name="zh-cn_topic_0091433674_p10580064"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p51678836"><a name="zh-cn_topic_0091433674_p51678836"></a><a name="zh-cn_topic_0091433674_p51678836"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433674_p25236181"><a name="zh-cn_topic_0091433674_p25236181"></a><a name="zh-cn_topic_0091433674_p25236181"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433674_row25799037"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p9347259"><a name="zh-cn_topic_0091433674_p9347259"></a><a name="zh-cn_topic_0091433674_p9347259"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p18930554"><a name="zh-cn_topic_0091433674_p18930554"></a><a name="zh-cn_topic_0091433674_p18930554"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433674_p56979938"><a name="zh-cn_topic_0091433674_p56979938"></a><a name="zh-cn_topic_0091433674_p56979938"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433674_row43057396"><td class="cellrowborder" valign="top" width="22.45%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433674_p65097067"><a name="zh-cn_topic_0091433674_p65097067"></a><a name="zh-cn_topic_0091433674_p65097067"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433674_p38371103"><a name="zh-cn_topic_0091433674_p38371103"></a><a name="zh-cn_topic_0091433674_p38371103"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.22%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433674_p21051639"><a name="zh-cn_topic_0091433674_p21051639"></a><a name="zh-cn_topic_0091433674_p21051639"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433674_section61900675"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

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


## 响应消息<a name="zh-cn_topic_0091433674_section20235168"></a>

**响应参数：**

响应参数的详细描述请参见[表52](响应数据结构（OLD-VERSIONS）.md#table37251757105918)。

**响应示例：**

```
{
    "message": "Authorization information is wrong", 
    "request_id": "392eb3cb829b13e530a55bd215303582"
}
```

## 状态码<a name="zh-cn_topic_0091433674_section47898787"></a>

[表2](#zh-cn_topic_0091433674_d0e35450)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433674_d0e35450"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433674_row7535426"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433674_p6389758"><a name="zh-cn_topic_0091433674_p6389758"></a><a name="zh-cn_topic_0091433674_p6389758"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433674_p47808350"><a name="zh-cn_topic_0091433674_p47808350"></a><a name="zh-cn_topic_0091433674_p47808350"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433674_row47271114"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433674_p3755051"><a name="zh-cn_topic_0091433674_p3755051"></a><a name="zh-cn_topic_0091433674_p3755051"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433681_p21206673"><a name="zh-cn_topic_0091433681_p21206673"></a><a name="zh-cn_topic_0091433681_p21206673"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

