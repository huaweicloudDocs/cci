# 删除所有StatefulSet<a name="cci_02_0037"></a>

## 功能介绍<a name="zh-cn_topic_0091433689_section11422692"></a>

This API is used to delete collection of StatefulSet.

该接口不支持级联删除创建StatefulSet时同步创建的Pod等资源。

## URI<a name="zh-cn_topic_0091433689_section35695364"></a>

DELETE /apis/apps/v1beta1/namespaces/\{namespace\}/statefulsets

[表1](#zh-cn_topic_0091433689_d0e38460)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433689_d0e38460"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433689_row36648893"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433689_p65652297517"><a name="zh-cn_topic_0091433689_p65652297517"></a><a name="zh-cn_topic_0091433689_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.15%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433689_p165661629135114"><a name="zh-cn_topic_0091433689_p165661629135114"></a><a name="zh-cn_topic_0091433689_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="62.629999999999995%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433689_p14567629115114"><a name="zh-cn_topic_0091433689_p14567629115114"></a><a name="zh-cn_topic_0091433689_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433689_row44947838"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p16896290"><a name="zh-cn_topic_0091433689_p16896290"></a><a name="zh-cn_topic_0091433689_p16896290"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p26422250"><a name="zh-cn_topic_0091433689_p26422250"></a><a name="zh-cn_topic_0091433689_p26422250"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row1576761"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p60608844"><a name="zh-cn_topic_0091433689_p60608844"></a><a name="zh-cn_topic_0091433689_p60608844"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p10369311"><a name="zh-cn_topic_0091433689_p10369311"></a><a name="zh-cn_topic_0091433689_p10369311"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p34607834"><a name="zh-cn_topic_0091433689_p34607834"></a><a name="zh-cn_topic_0091433689_p34607834"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row43035054"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p63287386"><a name="zh-cn_topic_0091433689_p63287386"></a><a name="zh-cn_topic_0091433689_p63287386"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p26004609"><a name="zh-cn_topic_0091433689_p26004609"></a><a name="zh-cn_topic_0091433689_p26004609"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p25998605"><a name="zh-cn_topic_0091433689_p25998605"></a><a name="zh-cn_topic_0091433689_p25998605"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row32660861"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p28284059"><a name="zh-cn_topic_0091433689_p28284059"></a><a name="zh-cn_topic_0091433689_p28284059"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p9307409"><a name="zh-cn_topic_0091433689_p9307409"></a><a name="zh-cn_topic_0091433689_p9307409"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p15702664"><a name="zh-cn_topic_0091433689_p15702664"></a><a name="zh-cn_topic_0091433689_p15702664"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row7106251"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p38735462"><a name="zh-cn_topic_0091433689_p38735462"></a><a name="zh-cn_topic_0091433689_p38735462"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p50564693"><a name="zh-cn_topic_0091433689_p50564693"></a><a name="zh-cn_topic_0091433689_p50564693"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p2099457"><a name="zh-cn_topic_0091433689_p2099457"></a><a name="zh-cn_topic_0091433689_p2099457"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row18895113"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p54109146"><a name="zh-cn_topic_0091433689_p54109146"></a><a name="zh-cn_topic_0091433689_p54109146"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p20764700"><a name="zh-cn_topic_0091433689_p20764700"></a><a name="zh-cn_topic_0091433689_p20764700"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p4219126"><a name="zh-cn_topic_0091433689_p4219126"></a><a name="zh-cn_topic_0091433689_p4219126"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row37972140"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p55844510"><a name="zh-cn_topic_0091433689_p55844510"></a><a name="zh-cn_topic_0091433689_p55844510"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p27111485"><a name="zh-cn_topic_0091433689_p27111485"></a><a name="zh-cn_topic_0091433689_p27111485"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p48546672"><a name="zh-cn_topic_0091433689_p48546672"></a><a name="zh-cn_topic_0091433689_p48546672"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row34266869"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p24152994"><a name="zh-cn_topic_0091433689_p24152994"></a><a name="zh-cn_topic_0091433689_p24152994"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p10235479"><a name="zh-cn_topic_0091433689_p10235479"></a><a name="zh-cn_topic_0091433689_p10235479"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p23767485"><a name="zh-cn_topic_0091433689_p23767485"></a><a name="zh-cn_topic_0091433689_p23767485"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row12580778"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p12410075"><a name="zh-cn_topic_0091433689_p12410075"></a><a name="zh-cn_topic_0091433689_p12410075"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p65692050"><a name="zh-cn_topic_0091433689_p65692050"></a><a name="zh-cn_topic_0091433689_p65692050"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p19455796"><a name="zh-cn_topic_0091433689_p19455796"></a><a name="zh-cn_topic_0091433689_p19455796"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433689_row40884442"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433689_p23305482"><a name="zh-cn_topic_0091433689_p23305482"></a><a name="zh-cn_topic_0091433689_p23305482"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433689_p8695899"><a name="zh-cn_topic_0091433689_p8695899"></a><a name="zh-cn_topic_0091433689_p8695899"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.629999999999995%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433689_p33279220"><a name="zh-cn_topic_0091433689_p33279220"></a><a name="zh-cn_topic_0091433689_p33279220"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433689_section52822821"></a>

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


## 响应消息<a name="zh-cn_topic_0091433689_section5643344"></a>

**响应参数：**

响应参数的详细描述请参见[表52](响应数据结构（废弃）.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "StatefulSet",
    "apiVersion": "apps/v1beta1",
    "metadata": {
        "name": "state--12130306",
        "namespace": "ns-12130306-s",
        "selfLink": "/apis/apps/v1beta1/namespaces/ns-12130306-s/statefulsets/state--12130306",
        "uid": "dc139fbd-dfb3-11e7-9c19-fa163e2d897b",
        "resourceVersion": "418993",
        "generation": 2,
        "creationTimestamp": "2017-12-13T03:15:24Z",
        "deletionTimestamp": "2017-12-13T03:15:24Z",
        "deletionGracePeriodSeconds": 0,
        "labels": {
            "app": "mysql-0"
        },
        "finalizers": [
            "orphan"
        ],
        "enable": true
    },
    "spec": {
        "replicas": 1,
        "selector": {
            "matchLabels": {
                "app": "cci"
            }
        },
        "template": {
            "metadata": {
                "creationTimestamp": null,
                "labels": {
                    "app": "cci"
                },
                "enable": true
            },
            "spec": {
                "containers": [
                    {
                        "name": "rccon-12130306",
                        "image": "redis:v1",
                        "resources": {},
                        "terminationMessagePath": "/dev/termination-log",
                        "terminationMessagePolicy": "File",
                        "imagePullPolicy": "Always"
                    }
                ],
                "restartPolicy": "Always",                                
                "dnsPolicy": "ClusterFirst",
                "securityContext": {},
                "schedulerName": "default-scheduler"
            }
        },
        "serviceName": "sc-12130306-s-0",
        "podManagementPolicy": "OrderedReady",
        "updateStrategy": {
            "type": "OnDelete"
        },
        "revisionHistoryLimit": 10
    },
    "status": {
        "observedGeneration": 1,
        "replicas": 1,
        "currentReplicas": 1,
        "currentRevision": "state--12130306-1800136863",
        "updateRevision": "state--12130306-1800136863"
    }
}
```

## 状态码<a name="zh-cn_topic_0091433689_section50790103"></a>

[表2](#zh-cn_topic_0091433689_d0e38608)描述API的状态码。

**表 2**  状态码

<a name="zh-cn_topic_0091433689_d0e38608"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433689_row19701069"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433689_p52282775"><a name="zh-cn_topic_0091433689_p52282775"></a><a name="zh-cn_topic_0091433689_p52282775"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433689_p7046373"><a name="zh-cn_topic_0091433689_p7046373"></a><a name="zh-cn_topic_0091433689_p7046373"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433689_row33885344"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433689_p60358319"><a name="zh-cn_topic_0091433689_p60358319"></a><a name="zh-cn_topic_0091433689_p60358319"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p192181717161119"><a name="p192181717161119"></a><a name="p192181717161119"></a>OK</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

