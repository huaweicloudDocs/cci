# 查询PersistentVolumeClaim<a name="cci_02_3087"></a>

## 功能介绍<a name="s0766f38d8a9142d895e93cfb7d977c17"></a>

查询PersistentVolumeClaim。

## URI<a name="s6c83b7ac5f8848cdad6aa0f72beb7b0c"></a>

GET /api/v1/namespaces/\{namespace\}/persistentvolumeclaims/\{name\}

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
<tr id="row13794857171116"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p5984165818113"><a name="p5984165818113"></a><a name="p5984165818113"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the PersistentVolumeClaim.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="t905c776ecca443388ba20364de9fe4b1"></a>
<table><thead align="left"><tr id="re4448348c64e428fb5c1d1cddd8fa39d"><th class="cellrowborder" valign="top" width="21.5%" id="mcps1.2.4.1.1"><p id="a6b56275af4254aa8afbfddfdb98e7a4c"><a name="a6b56275af4254aa8afbfddfdb98e7a4c"></a><a name="a6b56275af4254aa8afbfddfdb98e7a4c"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.98%" id="mcps1.2.4.1.2"><p id="p20093560201657"><a name="p20093560201657"></a><a name="p20093560201657"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.519999999999996%" id="mcps1.2.4.1.3"><p id="p16965695201657"><a name="p16965695201657"></a><a name="p16965695201657"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r688017883dba445cac8b473c7e48d335"><td class="cellrowborder" valign="top" width="21.5%" headers="mcps1.2.4.1.1 "><p id="af59efb8fedcd4850bb55e382f01d2076"><a name="af59efb8fedcd4850bb55e382f01d2076"></a><a name="af59efb8fedcd4850bb55e382f01d2076"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.98%" headers="mcps1.2.4.1.2 "><p id="abfc66d6f8cd84571845c8d2be8aa5e3d"><a name="abfc66d6f8cd84571845c8d2be8aa5e3d"></a><a name="abfc66d6f8cd84571845c8d2be8aa5e3d"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.519999999999996%" headers="mcps1.2.4.1.3 "><p id="a2d2478fd5ac14c0da905226a4da988ea"><a name="a2d2478fd5ac14c0da905226a4da988ea"></a><a name="a2d2478fd5ac14c0da905226a4da988ea"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="rf253f01f49ba458f93f6fecf95ac33a5"><td class="cellrowborder" valign="top" width="21.5%" headers="mcps1.2.4.1.1 "><p id="a67e7df0587bc4b31a91a8ab83426dd31"><a name="a67e7df0587bc4b31a91a8ab83426dd31"></a><a name="a67e7df0587bc4b31a91a8ab83426dd31"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="16.98%" headers="mcps1.2.4.1.2 "><p id="a0e21efd5a6ea49ea807b87a72f5e325c"><a name="a0e21efd5a6ea49ea807b87a72f5e325c"></a><a name="a0e21efd5a6ea49ea807b87a72f5e325c"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.519999999999996%" headers="mcps1.2.4.1.3 "><p id="a84b651f574804bf5b0dcb09fb4f1b17d"><a name="a84b651f574804bf5b0dcb09fb4f1b17d"></a><a name="a84b651f574804bf5b0dcb09fb4f1b17d"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="rb4021dd42289434f8263c1328e171814"><td class="cellrowborder" valign="top" width="21.5%" headers="mcps1.2.4.1.1 "><p id="af2440c7693cb4fc19c8e702de5b4f12e"><a name="af2440c7693cb4fc19c8e702de5b4f12e"></a><a name="af2440c7693cb4fc19c8e702de5b4f12e"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="16.98%" headers="mcps1.2.4.1.2 "><p id="a1646fa4fc6ea42979982ad943bf25902"><a name="a1646fa4fc6ea42979982ad943bf25902"></a><a name="a1646fa4fc6ea42979982ad943bf25902"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="61.519999999999996%" headers="mcps1.2.4.1.3 "><p id="ad0fb8de0f1bc4250a089d1456477089d"><a name="ad0fb8de0f1bc4250a089d1456477089d"></a><a name="ad0fb8de0f1bc4250a089d1456477089d"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="sbbfee804cd1441feb02c5b1256f37066"></a>

N/A

## 响应消息<a name="s2c230500e1d545709e0e50812a3d2236"></a>

**响应参数：**

响应参数请参见：[表93](公共参数.md#t7aa9de1153e9466cbfcaa9af17a24772)

**响应示例：**

```
{
  "kind": "PersistentVolumeClaim",
  "apiVersion": "v1",
  "metadata": {
    "name": "pvc-test",
    "namespace": "namespace-test",
    "selfLink": "/api/v1/namespaces/namespace-test/persistentvolumeclaims/pvc-test",
    "uid": "19a355cc-b26e-11e8-b205-c88d83be759f",
    "resourceVersion": "5915795",
    "creationTimestamp": "2018-09-07T07:17:38Z",
    "annotations": {
      "pv.kubernetes.io/bound-by-controller": "yes",
      "volume.beta.kubernetes.io/storage-class": "sata",
      "volume.beta.kubernetes.io/storage-provisioner": "flexvolume-huawei.com/fuxivol",
      "pv.kubernetes.io/bind-completed": "yes"
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
        "storage": "1Gi"
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
      "storage": "1Gi"
    }
  }
}
```

## 状态码<a name="s5e327306549c4e9883cffd48fd3dd116"></a>

[表3](#t50192f4902814904a2a6aaba297e2318)描述API的状态码。

**表 3**  状态码

<a name="t50192f4902814904a2a6aaba297e2318"></a>
<table><thead align="left"><tr id="rec68d1eaab554ce189b1adad4d5f7042"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p16246668201657"><a name="p16246668201657"></a><a name="p16246668201657"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p40911755201657"><a name="p40911755201657"></a><a name="p40911755201657"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="rbcf728b6557a4c4badd2e6ce50865ee5"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="a14d7eb271a044aac83b27ebeb7378432"><a name="a14d7eb271a044aac83b27ebeb7378432"></a><a name="a14d7eb271a044aac83b27ebeb7378432"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="a89d3305a10044770b67608656d17fa5c"><a name="a89d3305a10044770b67608656d17fa5c"></a><a name="a89d3305a10044770b67608656d17fa5c"></a>This operation succeeds, and a PersistentVolumeClaim resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

