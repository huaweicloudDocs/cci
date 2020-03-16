# 删除namespace下的所有Volcano Job<a name="cci_02_3134"></a>

## 功能介绍<a name="section19030251"></a>

删除命名空间下的所有Volcano Job。

## URI<a name="section37054533"></a>

DELETE /apis/batch.volcano.sh/v1alpha1/namespaces/\{namespace\}/jobs

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
<tbody><tr id="row61989525"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1834011925520"><a name="p1834011925520"></a><a name="p1834011925520"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1733951915512"><a name="p1733951915512"></a><a name="p1733951915512"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p143381019155512"><a name="p143381019155512"></a><a name="p143381019155512"></a>object name and auth scope, such as for teams and projects</p>
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
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p94378133507"><a name="p94378133507"></a><a name="p94378133507"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p19837859165418"><a name="p19837859165418"></a><a name="p19837859165418"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row13340949102114"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1837105955414"><a name="p1837105955414"></a><a name="p1837105955414"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p9446161317501"><a name="p9446161317501"></a><a name="p9446161317501"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1835159115412"><a name="p1835159115412"></a><a name="p1835159115412"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row1934684942112"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p7834175920549"><a name="p7834175920549"></a><a name="p7834175920549"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p8834105912542"><a name="p8834105912542"></a><a name="p8834105912542"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1083315596543"><a name="p1083315596543"></a><a name="p1083315596543"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.</p>
<p id="p131881042183711"><a name="p131881042183711"></a><a name="p131881042183711"></a>The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="row1235224982117"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p583285985414"><a name="p583285985414"></a><a name="p583285985414"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p7294112117508"><a name="p7294112117508"></a><a name="p7294112117508"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p11831185919540"><a name="p11831185919540"></a><a name="p11831185919540"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it’s 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.</p>
</td>
</tr>
<tr id="row6360204912217"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p78302591540"><a name="p78302591540"></a><a name="p78302591540"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p8300321165020"><a name="p8300321165020"></a><a name="p8300321165020"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p782915915547"><a name="p782915915547"></a><a name="p782915915547"></a>Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.</p>
</td>
</tr>
<tr id="row0370549162119"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p128281598548"><a name="p128281598548"></a><a name="p128281598548"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1330672115508"><a name="p1330672115508"></a><a name="p1330672115508"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p682665918549"><a name="p682665918549"></a><a name="p682665918549"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section65055348"></a>

N/A

## 响应消息<a name="section48627224"></a>

**响应参数：**

响应参数的详细描述请参考[表145](数据结构.md#table1251082312812)。

**响应示例**：

```
{
    "apiVersion": "batch.volcano.sh/v1alpha1",
    "items": [
        {
            "apiVersion": "batch.volcano.sh/v1alpha1",
            "kind": "Job",
            "metadata": {
                "creationTimestamp": "2019-06-26T03:16:26Z",
                "generation": 1,
                "labels": {
                    "app": "patchlabel"
                },
                "name": "openmpi-hello-2-com",
                "namespace": "cci-namespace-42263891",
                "resourceVersion": "7695210",
                "selfLink": "/apis/batch.volcano.sh/v1alpha1/namespaces/cci-namespace-42263891/jobs/openmpi-hello-2-com",
                "uid": "c84d86f0-97c0-11e9-9d09-dc9914fb58e0"
            },
            "spec": {
                "minAvailable": 1,
                "plugins": {
                    "env": [],
                    "ssh": [],
                    "svc": []
                },
                "queue": "default",
                "schedulerName": "volcano",
                "tasks": [
                    {
                        "name": "mpimaster",
                        "policies": [
                            {
                                "action": "CompleteJob",
                                "event": "TaskCompleted"
                            }
                        ],
                        "replicas": 1,
                        "template": {
                            "spec": {
                                "containers": [
                                    {
                                        "command": [
                                            "/bin/sh",
                                            "-c",
                                            "MPI_HOST=`cat /etc/volcano/mpiworker.host | tr \"\\n\" \",\"`;\nmkdir -p /var/run/sshd; /usr/sbin/sshd;\nmpiexec --allow-run-as-root --host ${MPI_HOST} -np 2 mpi_hello_world 003e /home/re\n"
                                        ],
                                        "image": "*.*.*.*:20202/l00427178/openmpi-hello:3.28",
                                        "name": "mpimaster",
                                        "ports": [
                                            {
                                                "containerPort": 22,
                                                "name": "mpijob-port"
                                            }
                                        ],
                                        "resources": {
                                            "limits": {
                                                "cpu": "250m",
                                                "memory": "1Gi"
                                            },
                                            "requests": {
                                                "cpu": "250m",
                                                "memory": "1Gi"
                                            }
                                        },
                                        "workingDir": "/home"
                                    }
                                ],
                                "imagePullSecrets": [
                                    {
                                        "name": "default-secret"
                                    }
                                ],
                                "restartPolicy": "OnFailure"
                            }
                        }
                    },
                    {
                        "name": "mpiworker",
                        "replicas": 2,
                        "template": {
                            "spec": {
                                "containers": [
                                    {
                                        "command": [
                                            "/bin/sh",
                                            "-c",
                                            "mkdir -p /var/run/sshd; /usr/sbin/sshd -D;\n"
                                        ],
                                        "image": "*.*.*.*:20202/l00427178/openmpi-hello:3.28",
                                        "name": "mpiworker",
                                        "ports": [
                                            {
                                                "containerPort": 22,
                                                "name": "mpijob-port"
                                            }
                                        ],
                                        "resources": {
                                            "limits": {
                                                "cpu": "250m",
                                                "memory": "1Gi"
                                            },
                                            "requests": {
                                                "cpu": "250m",
                                                "memory": "1Gi"
                                            }
                                        },
                                        "workingDir": "/home"
                                    }
                                ],
                                "imagePullSecrets": [
                                    {
                                        "name": "default-secret"
                                    }
                                ],
                                "restartPolicy": "OnFailure"
                            }
                        }
                    }
                ]
            },
            "status": {
                "controlledResources": {
                    "plugin-env": "env",
                    "plugin-ssh": "ssh",
                    "plugin-svc": "svc"
                },
                "minAvailable": 1,
                "pending": 3,
                "state": {
                    "lastTransitionTime": "2019-06-26T03:16:27Z",
                    "phase": "Inqueue"
                }
            }
        }
    ],
    "kind": "JobList",
    "metadata": {
        "continue": "",
        "resourceVersion": "7732232",
        "selfLink": "/apis/batch.volcano.sh/v1alpha1/namespaces/cci-namespace-42263891/jobs"
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
<tr id="row1238272133915"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p133821021133910"><a name="p133821021133910"></a><a name="p133821021133910"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p538272183910"><a name="p538272183910"></a><a name="p538272183910"></a>Unauthorized</p>
</td>
</tr>
<tr id="row112512534292"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p114411511294"><a name="p114411511294"></a><a name="p114411511294"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8144175192919"><a name="p8144175192919"></a><a name="p8144175192919"></a>Internal error</p>
</td>
</tr>
</tbody>
</table>

