# 查询Volcano Job详情<a name="cci_02_3135"></a>

## 功能介绍<a name="section19030251"></a>

查询Volcano Job的详细信息。

## URI<a name="section37054533"></a>

GET /apis/batch.volcano.sh/v1alpha1/namespaces/\{namespace\}/jobs/\{name\}

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
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1767753014503"><a name="p1767753014503"></a><a name="p1767753014503"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p143381019155512"><a name="p143381019155512"></a><a name="p143381019155512"></a>name of the Volcano Job</p>
</td>
</tr>
<tr id="row454191484115"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p2541201454120"><a name="p2541201454120"></a><a name="p2541201454120"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p6676530155020"><a name="p6676530155020"></a><a name="p6676530155020"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p165414146415"><a name="p165414146415"></a><a name="p165414146415"></a>object name and auth scope, such as for teams and projects</p>
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
<tbody><tr id="row10334449142116"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p883818599545"><a name="p883818599545"></a><a name="p883818599545"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p283845919544"><a name="p283845919544"></a><a name="p283845919544"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p19837859165418"><a name="p19837859165418"></a><a name="p19837859165418"></a>If 'true’, then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section65055348"></a>

N/A

## 响应消息<a name="section48627224"></a>

**响应参数：**

响应参数的详细描述请参考[表144](数据结构.md#table1251082312812)。

**响应示例**：

```
{
    "apiVersion": "batch.volcano.sh/v1alpha1",
    "kind": "Job",
    "metadata": {
        "creationTimestamp": "2019-06-26T06:24:50Z",
        "generation": 1,
        "name": "openmpi-hello-3-com",
        "namespace": "cci-namespace-42263891",
        "resourceVersion": "7681358",
        "selfLink": "/apis/batch.volcano.sh/v1alpha1/namespaces/cci-namespace-42263891/jobs/openmpi-hello-3-com",
        "uid": "1a32a8c4-97db-11e9-9d09-dc9914fb58e0"
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
                                "image": "*.*.*.*:20202/swr/openmpi-hello:3.28",
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
                                "image": "*.*.*.*:20202/swr/openmpi-hello:3.28",
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
            "lastTransitionTime": "2019-06-26T06:24:51Z",
            "phase": "Inqueue"
        }
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
<tr id="row15507142154318"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1850718294311"><a name="p1850718294311"></a><a name="p1850718294311"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1350717216431"><a name="p1350717216431"></a><a name="p1350717216431"></a>Unauthorized</p>
</td>
</tr>
<tr id="row17577150123115"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1657775011315"><a name="p1657775011315"></a><a name="p1657775011315"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p15577750123113"><a name="p15577750123113"></a><a name="p15577750123113"></a>Not found</p>
</td>
</tr>
<tr id="row193281855173118"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5328175573120"><a name="p5328175573120"></a><a name="p5328175573120"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p183291755193118"><a name="p183291755193118"></a><a name="p183291755193118"></a>Internal error</p>
</td>
</tr>
<tr id="row206596258383"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p10659425153815"><a name="p10659425153815"></a><a name="p10659425153815"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p19659825203817"><a name="p19659825203817"></a><a name="p19659825203817"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

