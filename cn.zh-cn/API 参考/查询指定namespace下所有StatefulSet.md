# 查询指定namespace下所有StatefulSet<a name="cci_02_3034"></a>

## 功能介绍<a name="section55184758"></a>

查询Namespace下所有StatefulSet的详细信息。

## URI<a name="section26900781"></a>

GET /apis/apps/v1/namespaces/\{namespace\}/statefulsets

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
</tbody>
</table>

**表 2**  Query参数

<a name="d0e39332"></a>
<table><thead align="left"><tr id="row16249415"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p102391234191410"><a name="p102391234191410"></a><a name="p102391234191410"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.4.1.2"><p id="p1864653711143"><a name="p1864653711143"></a><a name="p1864653711143"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.26367363263674%" id="mcps1.2.4.1.3"><p id="p122391934161412"><a name="p122391934161412"></a><a name="p122391934161412"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row33792834"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p73544013613"><a name="p73544013613"></a><a name="p73544013613"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p143541201969"><a name="p143541201969"></a><a name="p143541201969"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p20354190866"><a name="p20354190866"></a><a name="p20354190866"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row60416185"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p9354701961"><a name="p9354701961"></a><a name="p9354701961"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p1835413017617"><a name="p1835413017617"></a><a name="p1835413017617"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p1435417016617"><a name="p1435417016617"></a><a name="p1435417016617"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row54868012"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1735460567"><a name="p1735460567"></a><a name="p1735460567"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p173543018614"><a name="p173543018614"></a><a name="p173543018614"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p113541802068"><a name="p113541802068"></a><a name="p113541802068"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row11887742"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p63542009616"><a name="p63542009616"></a><a name="p63542009616"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p173541006613"><a name="p173541006613"></a><a name="p173541006613"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p20354401867"><a name="p20354401867"></a><a name="p20354401867"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row45811103"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p6354801564"><a name="p6354801564"></a><a name="p6354801564"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p83541108616"><a name="p83541108616"></a><a name="p83541108616"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p123541904617"><a name="p123541904617"></a><a name="p123541904617"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="row27682122"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1335410016619"><a name="p1335410016619"></a><a name="p1335410016619"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p19354140463"><a name="p19354140463"></a><a name="p19354140463"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p1535480265"><a name="p1535480265"></a><a name="p1535480265"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row30622110"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1635413015619"><a name="p1635413015619"></a><a name="p1635413015619"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p935416015619"><a name="p935416015619"></a><a name="p935416015619"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p5354102066"><a name="p5354102066"></a><a name="p5354102066"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
<tr id="row46062658"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p3354110762"><a name="p3354110762"></a><a name="p3354110762"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p13544010612"><a name="p13544010612"></a><a name="p13544010612"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p7354401562"><a name="p7354401562"></a><a name="p7354401562"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
<tr id="row1821717410617"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p7220341464"><a name="p7220341464"></a><a name="p7220341464"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.4.1.2 "><p id="p3220114112619"><a name="p3220114112619"></a><a name="p3220114112619"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.26367363263674%" headers="mcps1.2.4.1.3 "><p id="p0220104114617"><a name="p0220104114617"></a><a name="p0220104114617"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section40780438"></a>

N/A

## 响应消息<a name="section31479628"></a>

**响应参数：**

响应参数的详细描述请参见[表96](数据结构.md#table185396462518)。

**响应示例：**

```
{
    "kind": "StatefulSetList",
    "apiVersion": "apps/v1",
    "metadata": {
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/statefulsets",
        "resourceVersion": "5215730"
    },
    "items": [
        {
            "metadata": {
                "name": "statefulset-test",
                "namespace": "namespace-test",
                "selfLink": "/apis/apps/v1/namespaces/namespace-test/statefulsets/statefulset-test",
                "uid": "f4a35f35-b011-11e8-b6ef-f898ef6c78b4",
                "resourceVersion": "5209881",
                "generation": 1,
                "creationTimestamp": "2018-09-04T07:13:00Z",
                "labels": {
                    "app": "statefulset-test"
                },
                "enable": true
            },
            "spec": {
                "replicas": 3,
                "selector": {
                    "matchLabels": {
                        "app": "statefulset-test"
                    }
                },
                "template": {
                    "metadata": {
                        "creationTimestamp": null,
                        "labels": {
                            "app": "statefulset-test"
                        },
                        "annotations": {
                            "cri.cci.io/container-type": "secure-container"
                        },
                        "enable": true
                    },
                    "spec": {
                        "containers": [
                            {
                                "name": "container-0",
                                "image": "redis",
                                "resources": {
                                    "limits": {
                                        "cpu": "500m",
                                        "memory": "1Gi"
                                    },
                                    "requests": {
                                        "cpu": "500m",
                                        "memory": "1Gi"
                                    }
                                },
                                "terminationMessagePath": "/dev/termination-log",
                                "terminationMessagePolicy": "File",
                                "imagePullPolicy": "IfNotPresent"
                            }
                        ],
                        "restartPolicy": "Always",
                        "terminationGracePeriodSeconds": 30,
                        "dnsPolicy": "ClusterFirst",
                        "securityContext": {},
                        "imagePullSecrets": [
                            {
                                "name": "imagepull-secret"
                            }
                        ],
                        "schedulerName": "default-scheduler"
                    }
                },
                "serviceName": "",
                "podManagementPolicy": "OrderedReady",
                "updateStrategy": {
                    "type": "OnDelete"
                },
                "revisionHistoryLimit": 10
            },
            "status": {
                "observedGeneration": 1,
                "replicas": 3,
                "readyReplicas": 2,
                "currentReplicas": 3,
                "currentRevision": "statefulset-test-f986b645b",
                "updateRevision": "statefulset-test-f986b645b",
                "collisionCount": 0
            }
        }
    ]
}
```

## 状态码<a name="section14881199"></a>

[表3](#d0e39461)描述API的状态码。

**表 3**  状态码

<a name="d0e39461"></a>
<table><thead align="left"><tr id="row5459157"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p39538597"><a name="p39538597"></a><a name="p39538597"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p48509806"><a name="p48509806"></a><a name="p48509806"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row36980183"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p42604808"><a name="p42604808"></a><a name="p42604808"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p28437418"><a name="p28437418"></a><a name="p28437418"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

