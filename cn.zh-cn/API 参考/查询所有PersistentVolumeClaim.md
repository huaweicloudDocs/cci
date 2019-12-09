# 查询所有PersistentVolumeClaim<a name="cci_02_3088"></a>

## 功能介绍<a name="s56cf46cd1088494ba3345c1672a9b59a"></a>

查询Namespace下的所有PersistentVolumeClaim。

## URI<a name="s31d720a41bf84b65b5d3417e08ffcadb"></a>

GET /api/v1/namespaces/\{namespace\}/persistentvolumeclaims

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

<a name="t11883f44ee8e465e93615fe19d7d4f59"></a>
<table><thead align="left"><tr id="rad26db413d7d42108494dad8eb868789"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.4.1.1"><p id="a43f8f66ef278415a82e2ca2a7084290b"><a name="a43f8f66ef278415a82e2ca2a7084290b"></a><a name="a43f8f66ef278415a82e2ca2a7084290b"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12%" id="mcps1.2.4.1.2"><p id="p27344536201625"><a name="p27344536201625"></a><a name="p27344536201625"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="66%" id="mcps1.2.4.1.3"><p id="p314980201625"><a name="p314980201625"></a><a name="p314980201625"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r0f899f4f8ea54f2fa893c3e0cf87630c"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="a59bb22f28087453ca02324478ffbeacb"><a name="a59bb22f28087453ca02324478ffbeacb"></a><a name="a59bb22f28087453ca02324478ffbeacb"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="a2efc413ffd07407c95e92b4e6d9a897e"><a name="a2efc413ffd07407c95e92b4e6d9a897e"></a><a name="a2efc413ffd07407c95e92b4e6d9a897e"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="a0a7b2841e1c7435eb425115739a1ce01"><a name="a0a7b2841e1c7435eb425115739a1ce01"></a><a name="a0a7b2841e1c7435eb425115739a1ce01"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row198282232194"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p282892316198"><a name="p282892316198"></a><a name="p282892316198"></a>continue</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="p882818232194"><a name="p882818232194"></a><a name="p882818232194"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="p582852391916"><a name="p582852391916"></a><a name="p582852391916"></a>The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server, the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported if watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.</p>
</td>
</tr>
<tr id="r7e813ae72466493da1ae3476c4217a9a"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="aa9c64e4ab78b4acd88c66b1e801ca35a"><a name="aa9c64e4ab78b4acd88c66b1e801ca35a"></a><a name="aa9c64e4ab78b4acd88c66b1e801ca35a"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="a0d4037ffde7e416fa83b9299a1a4a87a"><a name="a0d4037ffde7e416fa83b9299a1a4a87a"></a><a name="a0d4037ffde7e416fa83b9299a1a4a87a"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="a276f514c7e054fe594be37cb743f5173"><a name="a276f514c7e054fe594be37cb743f5173"></a><a name="a276f514c7e054fe594be37cb743f5173"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="r3a7c2bd394cc4b38a62660d120d35a61"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614896_p628523492519"><a name="zh-cn_topic_0079614896_p628523492519"></a><a name="zh-cn_topic_0079614896_p628523492519"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="aab3047b805ad4854aeefd8db47cf4d99"><a name="aab3047b805ad4854aeefd8db47cf4d99"></a><a name="aab3047b805ad4854aeefd8db47cf4d99"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="a163adfe9b2884ce09f91ddc74ec8c32a"><a name="a163adfe9b2884ce09f91ddc74ec8c32a"></a><a name="a163adfe9b2884ce09f91ddc74ec8c32a"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="r3e03b3ed19724be4b39fe666ed7011f5"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="a43a73c63fa9546e080760e7e88d5ecf2"><a name="a43a73c63fa9546e080760e7e88d5ecf2"></a><a name="a43a73c63fa9546e080760e7e88d5ecf2"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="abe9b1918c28c44a09ba2c13b3fdfac83"><a name="abe9b1918c28c44a09ba2c13b3fdfac83"></a><a name="abe9b1918c28c44a09ba2c13b3fdfac83"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="ac0386b9e9729419d808bfc1e4da82d9c"><a name="ac0386b9e9729419d808bfc1e4da82d9c"></a><a name="ac0386b9e9729419d808bfc1e4da82d9c"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row18767185011196"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="p1476714506193"><a name="p1476714506193"></a><a name="p1476714506193"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="p16767195011920"><a name="p16767195011920"></a><a name="p16767195011920"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="p15767145017195"><a name="p15767145017195"></a><a name="p15767145017195"></a>limit is a maximum number of responses to return for a list call. If more items exist, the server will set the continue field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true. The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.</p>
</td>
</tr>
<tr id="rb24b664f262244d8817205f6426fc18d"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="ab92f7219f16340be9ae9a42c2702afc7"><a name="ab92f7219f16340be9ae9a42c2702afc7"></a><a name="ab92f7219f16340be9ae9a42c2702afc7"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="a09235cc3ced749dcbb2940e0d05fb814"><a name="a09235cc3ced749dcbb2940e0d05fb814"></a><a name="a09235cc3ced749dcbb2940e0d05fb814"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="a5267faf2beb54f448afd8d0566d2e815"><a name="a5267faf2beb54f448afd8d0566d2e815"></a><a name="a5267faf2beb54f448afd8d0566d2e815"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="r905443bc04e941289138dc2173e87bc7"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="acce97a3e928a45deb3f0d61bcd998746"><a name="acce97a3e928a45deb3f0d61bcd998746"></a><a name="acce97a3e928a45deb3f0d61bcd998746"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="a4b9e930dbbf940d297016f43b9858f87"><a name="a4b9e930dbbf940d297016f43b9858f87"></a><a name="a4b9e930dbbf940d297016f43b9858f87"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="a8e45bcc0a7704befb090dc6e70c7c134"><a name="a8e45bcc0a7704befb090dc6e70c7c134"></a><a name="a8e45bcc0a7704befb090dc6e70c7c134"></a>Timeout for the list/watch call.</p>
</td>
</tr>
<tr id="r76de6a58993848c7953e1d93a68eb6ac"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.1 "><p id="ad538da99548e4303a160e21d889620a2"><a name="ad538da99548e4303a160e21d889620a2"></a><a name="ad538da99548e4303a160e21d889620a2"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="12%" headers="mcps1.2.4.1.2 "><p id="a064e1d3de451400dbb80b180df98254e"><a name="a064e1d3de451400dbb80b180df98254e"></a><a name="a064e1d3de451400dbb80b180df98254e"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="66%" headers="mcps1.2.4.1.3 "><p id="ab64449bf39f74dfc8a50ec513c46f5bf"><a name="ab64449bf39f74dfc8a50ec513c46f5bf"></a><a name="ab64449bf39f74dfc8a50ec513c46f5bf"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s1aaade19a5f2449c8f90fc400cb59e0a"></a>

N/A

## 响应消息<a name="se1ddbf9e5de0401e83a36b0530ef7b5d"></a>

**响应参数：**

响应参数参见[表126](数据结构.md#t48c604ca9f9f44e59b88ea85d6d7fd4b)。

**响应示例：**

```
{
    "kind": "PersistentVolumeClaimList",
    "apiVersion": "v1",
    "metadata": {
        "selfLink": "/api/v1/namespaces/namespace-test/persistentvolumeclaims",
        "resourceVersion": "6456754"
    },
    "items": [
        {
            "metadata": {
                "name": "pvc-test",
                "namespace": "test-namespace",
                "selfLink": "/api/v1/namespaces/namespace-test/persistentvolumeclaims/pvc-test",
                "uid": "19a355cc-b26e-11e8-b205-c88d83be759f",
                "resourceVersion": "5915795",
                "creationTimestamp": "2018-09-07T07:17:38Z",
                "annotations": {
                    "volume.beta.kubernetes.io/storage-class": "sata",
                    "volume.beta.kubernetes.io/storage-provisioner": "flexvolume-huawei.com/fuxivol",
                    "pv.kubernetes.io/bind-completed": "yes",
                    "pv.kubernetes.io/bound-by-controller": "yes"
                },
                "finalizers": [
                    "kubernetes.io/pvc-protection"
                ],
                "enable": true
            },
            "spec": {
                "accessModes": [
                    "ReadWriteMany"
                ],
                "resources": {
                    "requests": {
                        "storage": "10Gi"
                    }
                },
                "volumeName": "pvc-19a355cc-b26e-11e8-b205-c88d83be759f"
            },
            "status": {
                "phase": "Bound",
                "accessModes": [
                    "ReadWriteMany"
                ],
                "capacity": {
                    "storage": "10Gi"
                }
            }
        }
    ]
}
```

## 状态码<a name="s78ba216a41044b28a40ef9cc720c3838"></a>

[表3](#t16e97f6b7a8c4f54a023a2eb0d459bfb)描述API的状态码。

**表 3**  状态码

<a name="t16e97f6b7a8c4f54a023a2eb0d459bfb"></a>
<table><thead align="left"><tr id="r4f0d60352a9a4527ae0d6caf73953e40"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p4700061320177"><a name="p4700061320177"></a><a name="p4700061320177"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p4895330420177"><a name="p4895330420177"></a><a name="p4895330420177"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="rd9aa5e820c1a41fb820be5720e536e37"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="aae13f204c7664dddb863191193f3e1de"><a name="aae13f204c7664dddb863191193f3e1de"></a><a name="aae13f204c7664dddb863191193f3e1de"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="a1ba62f4c05ff40d999386b5968f2ac45"><a name="a1ba62f4c05ff40d999386b5968f2ac45"></a><a name="a1ba62f4c05ff40d999386b5968f2ac45"></a>This operation succeeds, and a group of PersistentVolumeClaim resource objects is returned.</p>
</td>
</tr>
</tbody>
</table>

