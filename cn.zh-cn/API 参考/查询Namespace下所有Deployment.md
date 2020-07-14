# 查询Namespace下所有Deployment<a name="cci_02_3025"></a>

## 功能介绍<a name="section51078739"></a>

查询Namespace下所有Deployment的详细信息。

## URI<a name="section57055467"></a>

GET /apis/apps/v1/namespaces/\{namespace\}/deployments

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

<a name="d0e36539"></a>
<table><thead align="left"><tr id="row2135501"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p459234765916"><a name="p459234765916"></a><a name="p459234765916"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.16%" id="mcps1.2.4.1.2"><p id="p1592144735919"><a name="p1592144735919"></a><a name="p1592144735919"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.62%" id="mcps1.2.4.1.3"><p id="p7592147185912"><a name="p7592147185912"></a><a name="p7592147185912"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row43367434"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p559254715917"><a name="p559254715917"></a><a name="p559254715917"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p17592447135915"><a name="p17592447135915"></a><a name="p17592447135915"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p1859234785912"><a name="p1859234785912"></a><a name="p1859234785912"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row49683219"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1059220472591"><a name="p1059220472591"></a><a name="p1059220472591"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p14592144716592"><a name="p14592144716592"></a><a name="p14592144716592"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p159254710598"><a name="p159254710598"></a><a name="p159254710598"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row54381628"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1359244755920"><a name="p1359244755920"></a><a name="p1359244755920"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p9592547135913"><a name="p9592547135913"></a><a name="p9592547135913"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p14592047105911"><a name="p14592047105911"></a><a name="p14592047105911"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row6210614"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1259214735917"><a name="p1259214735917"></a><a name="p1259214735917"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p145925473596"><a name="p145925473596"></a><a name="p145925473596"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p55922479592"><a name="p55922479592"></a><a name="p55922479592"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row43159710"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p13592154710597"><a name="p13592154710597"></a><a name="p13592154710597"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p7592174735918"><a name="p7592174735918"></a><a name="p7592174735918"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p9592104710591"><a name="p9592104710591"></a><a name="p9592104710591"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it is 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row61129466"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p15592124710598"><a name="p15592124710598"></a><a name="p15592124710598"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p5592247115910"><a name="p5592247115910"></a><a name="p5592247115910"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p15592154718592"><a name="p15592154718592"></a><a name="p15592154718592"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="row41189657"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p1959218479594"><a name="p1959218479594"></a><a name="p1959218479594"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p18592134713591"><a name="p18592134713591"></a><a name="p18592134713591"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p195931547115914"><a name="p195931547115914"></a><a name="p195931547115914"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
<tr id="row5181828184118"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p12111128154114"><a name="p12111128154114"></a><a name="p12111128154114"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p211192804116"><a name="p211192804116"></a><a name="p211192804116"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p1911428124116"><a name="p1911428124116"></a><a name="p1911428124116"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row1459693834112"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p3590123810415"><a name="p3590123810415"></a><a name="p3590123810415"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="16.16%" headers="mcps1.2.4.1.2 "><p id="p9590183804113"><a name="p9590183804113"></a><a name="p9590183804113"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.62%" headers="mcps1.2.4.1.3 "><p id="p19591123884111"><a name="p19591123884111"></a><a name="p19591123884111"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section43737161"></a>

N/A

## 响应消息<a name="section58090133"></a>

**响应参数：**

响应参数的详细描述请参见[表85](数据结构.md#table10664201816438)。

**响应示例**：

```
{
    "kind": "DeploymentList",
    "apiVersion": "apps/v1",
    "metadata": {
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/deployments",
        "resourceVersion": "5038849"
    },
    "items": [
        {
            "metadata": {
                "name": "deployment-test",
                "namespace": "namespace-test",
                "selfLink": "/apis/apps/v1/namespaces/namespace-test/deployments/deployment-test",
                "uid": "010506c7-af79-11e8-b6ef-f898ef6c78b4",
                "resourceVersion": "5036888",
                "generation": 1,
                "creationTimestamp": "2018-09-03T12:58:07Z",
                "labels": {
                    "app": "redis"
                },
                "annotations": {
                    "deployment.kubernetes.io/revision": "1"
                },
                "enable": true
            },
            "spec": {
                "replicas": 1,
                "selector": {
                    "matchLabels": {
                        "app": "redis"
                    }
                },
                "template": {
                    "metadata": {
                        "creationTimestamp": null,
                        "labels": {
                            "app": "redis"
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
                "strategy": {
                    "type": "RollingUpdate",
                    "rollingUpdate": {
                        "maxUnavailable": "25%",
                        "maxSurge": "25%"
                    }
                },
                "revisionHistoryLimit": 2,
                "progressDeadlineSeconds": 600
            },
            "status": {
                "observedGeneration": 1,
                "replicas": 1,
                "updatedReplicas": 1,
                "readyReplicas": 1,
                "availableReplicas": 1,
                "conditions": [
                    {
                        "type": "Available",
                        "status": "True",
                        "lastUpdateTime": "2018-09-03T12:58:12Z",
                        "lastTransitionTime": "2018-09-03T12:58:12Z",
                        "reason": "MinimumReplicasAvailable",
                        "message": "Deployment has minimum availability."
                    },
                    {
                        "type": "Progressing",
                        "status": "True",
                        "lastUpdateTime": "2018-09-03T12:58:12Z",
                        "lastTransitionTime": "2018-09-03T12:58:07Z",
                        "reason": "NewReplicaSetAvailable",
                        "message": "ReplicaSet \"deployment-test-57f7cff77c\" has successfully progressed."
                    }
                ]
            }
        }
    ]
}
```

## 状态码<a name="section53049152"></a>

[表3](#d0e36668)描述API的状态码。

**表 3**  状态码

<a name="d0e36668"></a>
<table><thead align="left"><tr id="row17031726"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p37392545"><a name="p37392545"></a><a name="p37392545"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p8897276"><a name="p8897276"></a><a name="p8897276"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49590760"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p57428620"><a name="p57428620"></a><a name="p57428620"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p21206673"><a name="p21206673"></a><a name="p21206673"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

