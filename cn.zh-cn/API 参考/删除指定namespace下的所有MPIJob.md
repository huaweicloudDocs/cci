# 删除指定namespace下的所有MPIJob<a name="cci_02_3174"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

删除命名空间下的所有MPIJob。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

DELETE /apis/kubeflow.org/v1alpha2/namespaces/\{namespace\}/mpijobs

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
<tbody><tr id="zh-cn_topic_0083864910_row1670122004014"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="p11646446263"><a name="p11646446263"></a><a name="p11646446263"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="p06461461167"><a name="p06461461167"></a><a name="p06461461167"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="p664617461468"><a name="p664617461468"></a><a name="p664617461468"></a>object name and auth scope, such as for teams and projects</p>
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
<tbody><tr id="row10334449142116"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p883818599545"><a name="p883818599545"></a><a name="p883818599545"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p13471678575"><a name="p13471678575"></a><a name="p13471678575"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p19837859165418"><a name="p19837859165418"></a><a name="p19837859165418"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row13340949102114"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1837105955414"><a name="p1837105955414"></a><a name="p1837105955414"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p14763715718"><a name="p14763715718"></a><a name="p14763715718"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1835159115412"><a name="p1835159115412"></a><a name="p1835159115412"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row1934684942112"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p7834175920549"><a name="p7834175920549"></a><a name="p7834175920549"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p18481137175716"><a name="p18481137175716"></a><a name="p18481137175716"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1083315596543"><a name="p1083315596543"></a><a name="p1083315596543"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.</p>
<p id="p131881042183711"><a name="p131881042183711"></a><a name="p131881042183711"></a>The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row1235224982117"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p583285985414"><a name="p583285985414"></a><a name="p583285985414"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p15851394571"><a name="p15851394571"></a><a name="p15851394571"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p11831185919540"><a name="p11831185919540"></a><a name="p11831185919540"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it’s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row6360204912217"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p78302591540"><a name="p78302591540"></a><a name="p78302591540"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p7591159165710"><a name="p7591159165710"></a><a name="p7591159165710"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p782915915547"><a name="p782915915547"></a><a name="p782915915547"></a>Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.</p>
</td>
</tr>
<tr id="row0370549162119"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p128281598548"><a name="p128281598548"></a><a name="p128281598548"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p35952935711"><a name="p35952935711"></a><a name="p35952935711"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p682665918549"><a name="p682665918549"></a><a name="p682665918549"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表174](数据结构.md#table160054115535)。

**响应示例：**

```
{
	"apiVersion": "kubeflow.org/v1alpha2",
	"items": [{
		"apiVersion": "kubeflow.org/v1alpha2",
		"kind": "MPIJob",
		"metadata": {
			"creationTimestamp": "2019-07-29T03:05:59Z",
			"generation": 1,
			"name": "mpi-test",
			"namespace": "kube-test",
			"resourceVersion": "75603660",
			"selfLink": "/apis/kubeflow.org/v1alpha2/namespaces/kube-test/mpijobs/mpi-test",
			"uid": "ca55275f-b1ad-11e9-b7c9-340a9837e2a7"
		},
		"spec": {
			"cleanPodPolicy": "All",
			"mpiReplicaSpecs": {
				"Launcher": {
					"replicas": 1,
					"template": {
						"spec": {
							"containers": [{
								"args": ["-c", "mpirun --allow-run-as-root python mxnet_mnist.py --batch-size 32 --no-cuda --epoch 1"],
								"command": ["/bin/bash"],
								"image": "100.79.1.215:20202/paas_cci_w00427225/horovod-mxnet:mnist",
								"name": "mpi",
								"resources": {
									"limits": {
										"cpu": 1,
										"memory": "2Gi"
									},
									"requests": {
										"cpu": 1,
										"memory": "2Gi"
									}
								}
							}],
							"imagePullSecrets": [{
								"name": "imagepull-secret"
							}]
						}
					}
				},
				"Worker": {
					"replicas": 2,
					"template": {
						"spec": {
							"containers": [{
								"image": "100.79.1.215:20202/paas_cci_w00427225/horovod-mxnet:mnist",
								"name": "mpi",
								"resources": {
									"limits": {
										"cpu": 1,
										"memory": "2Gi"
									},
									"requests": {
										"cpu": 1,
										"memory": "2Gi"
									}
								}
							}],
							"imagePullSecrets": [{
								"name": "imagepull-secret"
							}]
						}
					}
				}
			},
			"slotsPerWorker": 1
		},
		"status": {
			"completionTime": "2019-07-29T03:09:37Z",
			"conditions": [{
				"lastTransitionTime": "2019-07-29T03:05:59Z",
				"lastUpdateTime": "2019-07-29T03:05:59Z",
				"message": "MPIJob kube-test/mpi-test is created.",
				"reason": "MPIJobCreated",
				"status": "True",
				"type": "Created"
			}, {
				"lastTransitionTime": "2019-07-29T03:06:24Z",
				"lastUpdateTime": "2019-07-29T03:06:24Z",
				"message": "MPIJob kube-test/mpi-test is running.",
				"reason": "MPIJobRunning",
				"status": "False",
				"type": "Running"
			}, {
				"lastTransitionTime": "2019-07-29T03:09:37Z",
				"lastUpdateTime": "2019-07-29T03:09:37Z",
				"message": "MPIJob kube-test/mpi-test successfully completed.",
				"reason": "MPIJobSucceeded",
				"status": "True",
				"type": "Succeeded"
			}],
			"replicaStatuses": {
				"Launcher": {
					"succeeded": 1
				},
				"Worker": {}
			},
			"startTime": "2019-07-29T03:05:59Z"
		}
	}],
	"kind": "MPIJobList",
	"metadata": {
		"continue": "",
		"resourceVersion": "75604440",
		"selfLink": "/apis/kubeflow.org/v1alpha2/namespaces/kube-test/mpijobs"
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
<tbody><tr id="zh-cn_topic_0083864910_row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p208151253142014"><a name="p208151253142014"></a><a name="p208151253142014"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9815175310205"><a name="p9815175310205"></a><a name="p9815175310205"></a>OK</p>
</td>
</tr>
<tr id="row19701448172017"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p11815353142016"><a name="p11815353142016"></a><a name="p11815353142016"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p281545315203"><a name="p281545315203"></a><a name="p281545315203"></a>Unauthorized</p>
</td>
</tr>
<tr id="row12724251122018"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1481545318202"><a name="p1481545318202"></a><a name="p1481545318202"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1981614536200"><a name="p1981614536200"></a><a name="p1981614536200"></a>Internal error</p>
</td>
</tr>
</tbody>
</table>

