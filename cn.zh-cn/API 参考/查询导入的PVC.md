# 查询导入的PVC<a name="cci_02_2022"></a>

## 功能介绍<a name="section54875957"></a>

查询指定命名空间下的PVC。

## URI<a name="section24121565"></a>

GET /api/v1/namespaces/\{namespace\}/extended-persistentvolumeclaims

**表 1**  Path参数

<a name="table16725372"></a>
<table><thead align="left"><tr id="row46809697"><th class="cellrowborder" valign="top" width="17.76%" id="mcps1.2.5.1.1"><p id="p33489078"><a name="p33489078"></a><a name="p33489078"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.14%" id="mcps1.2.5.1.2"><p id="p28260775"><a name="p28260775"></a><a name="p28260775"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.09%" id="mcps1.2.5.1.3"><p id="p980322612388"><a name="p980322612388"></a><a name="p980322612388"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.01%" id="mcps1.2.5.1.4"><p id="p7421470"><a name="p7421470"></a><a name="p7421470"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row64268160"><td class="cellrowborder" valign="top" width="17.76%" headers="mcps1.2.5.1.1 "><p id="p38338487"><a name="p38338487"></a><a name="p38338487"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="14.14%" headers="mcps1.2.5.1.2 "><p id="p18409771"><a name="p18409771"></a><a name="p18409771"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="17.09%" headers="mcps1.2.5.1.3 "><p id="p15803152673812"><a name="p15803152673812"></a><a name="p15803152673812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.01%" headers="mcps1.2.5.1.4 "><p id="p14796483"><a name="p14796483"></a><a name="p14796483"></a>命名空间。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table57664488"></a>
<table><thead align="left"><tr id="row28189627"><th class="cellrowborder" valign="top" width="17.630000000000003%" id="mcps1.2.5.1.1"><p id="p1658455"><a name="p1658455"></a><a name="p1658455"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.829999999999998%" id="mcps1.2.5.1.2"><p id="p9490272"><a name="p9490272"></a><a name="p9490272"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.400000000000002%" id="mcps1.2.5.1.3"><p id="p117163"><a name="p117163"></a><a name="p117163"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.13999999999999%" id="mcps1.2.5.1.4"><p id="p30514590"><a name="p30514590"></a><a name="p30514590"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row55762700"><td class="cellrowborder" valign="top" width="17.630000000000003%" headers="mcps1.2.5.1.1 "><p id="p20484818"><a name="p20484818"></a><a name="p20484818"></a>storageType</p>
</td>
<td class="cellrowborder" valign="top" width="14.829999999999998%" headers="mcps1.2.5.1.2 "><p id="p48948360"><a name="p48948360"></a><a name="p48948360"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="16.400000000000002%" headers="mcps1.2.5.1.3 "><p id="p48657561"><a name="p48657561"></a><a name="p48657561"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.13999999999999%" headers="mcps1.2.5.1.4 "><p id="p5394248"><a name="p5394248"></a><a name="p5394248"></a>Type of storage，目前支持：</p>
<a name="ul19102811391"></a><a name="ul19102811391"></a><ul id="ul19102811391"><li>bs: 云硬盘存储</li><li>nfs: 文件存储</li><li>efs:  极速文件存储</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section15767494"></a>

N/A

## 响应消息<a name="section7689721"></a>

**响应参数**

**表 3**  响应参数

<a name="table52727095"></a>
<table><thead align="left"><tr id="row34322009"><th class="cellrowborder" valign="top" width="19.72%" id="mcps1.2.4.1.1"><p id="p28619382"><a name="p28619382"></a><a name="p28619382"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.72%" id="mcps1.2.4.1.2"><p id="p36468595"><a name="p36468595"></a><a name="p36468595"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.559999999999995%" id="mcps1.2.4.1.3"><p id="p1166200"><a name="p1166200"></a><a name="p1166200"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row27353390"><td class="cellrowborder" valign="top" width="19.72%" headers="mcps1.2.4.1.1 "><p id="p1032124"><a name="p1032124"></a><a name="p1032124"></a>PersistentVolumeClaim</p>
</td>
<td class="cellrowborder" valign="top" width="24.72%" headers="mcps1.2.4.1.2 "><p id="p16493259"><a name="p16493259"></a><a name="p16493259"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="55.559999999999995%" headers="mcps1.2.4.1.3 "><p id="p60885635"><a name="p60885635"></a><a name="p60885635"></a>详情请参见<a href="数据结构.md#table37685299">表175</a>。</p>
</td>
</tr>
<tr id="row11099805"><td class="cellrowborder" valign="top" width="19.72%" headers="mcps1.2.4.1.1 "><p id="p26669028"><a name="p26669028"></a><a name="p26669028"></a>PersistentVolume</p>
</td>
<td class="cellrowborder" valign="top" width="24.72%" headers="mcps1.2.4.1.2 "><p id="p536765711525"><a name="p536765711525"></a><a name="p536765711525"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="55.559999999999995%" headers="mcps1.2.4.1.3 "><p id="p22689808"><a name="p22689808"></a><a name="p22689808"></a>详情请参见<a href="数据结构.md#table24845910">表184</a>。</p>
</td>
</tr>
<tr id="row2881685"><td class="cellrowborder" valign="top" width="19.72%" headers="mcps1.2.4.1.1 "><p id="p32089967"><a name="p32089967"></a><a name="p32089967"></a>StorageInfo</p>
</td>
<td class="cellrowborder" valign="top" width="24.72%" headers="mcps1.2.4.1.2 "><p id="p445425712528"><a name="p445425712528"></a><a name="p445425712528"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="55.559999999999995%" headers="mcps1.2.4.1.3 "><p id="p21772565"><a name="p21772565"></a><a name="p21772565"></a>详情请参见<a href="数据结构.md#table60569775">表199</a>。</p>
</td>
</tr>
</tbody>
</table>

**响应示例**

```
[
    {
        "persistentVolumeClaim": {
            "metadata": {
                "name": "cci-evs-jxzqegxe-k1z3",
                "namespace": "test-namespace",
                "selfLink": "/api/v1/namespaces/csms/persistentvolumeclaims/cci-evs-jxzqegxe-k1z3",
                "uid": "e82c1574-a46d-11e9-be8a-b44326d0c915",
                "resourceVersion": "65003551",
                "creationTimestamp": "2019-07-12T06:25:56Z",
                "annotations": {
                    "pv.kubernetes.io/bind-completed": "yes",
                    "pv.kubernetes.io/bound-by-controller": "yes",
                    "volume.beta.kubernetes.io/storage-provisioner": "flexvolume-huawei.com/fuxivol"
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
                "volumeName": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "storageClassName": "sata"
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
        },
        "persistentVolume": {
            "metadata": {
                "name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "selfLink": "/api/v1/persistentvolumes/pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "uid": "eb0a0ca1-a46d-11e9-be8a-b44326d0c915",
                "resourceVersion": "65003549",
                "creationTimestamp": "2019-07-12T06:26:01Z",
                "labels": {
                    "tenant.kubernetes.io/domain-id": "f0c61dbd65974140956ed37a91ea860f",
                    "tenant.kubernetes.io/project-id": "cdb4249297a44665a63eec4f27ad09bf"
                },
                "annotations": {
                    "kubernetes.io/createdby": "huawei.com/fuxivol-dynamic-provisioner",
                    "pv.kubernetes.io/bound-by-controller": "yes",
                    "pv.kubernetes.io/namespace": "test-namespace",
                    "pv.kubernetes.io/provisioned-by": "flexvolume-huawei.com/fuxivol",
                    "tenant.kubernetes.io/domain-id": "f0c61dbd65974140956ed37a91ea860f",
                    "tenant.kubernetes.io/project-id": "cdb4249297a44665a63eec4f27ad09bf"
                },
                "finalizers": [
                    "kubernetes.io/pv-protection"
                ]
            },
            "spec": {
                "capacity": {
                    "storage": "10Gi"
                },
                "flexVolume": {
                    "driver": "huawei.com/fuxivol",
                    "fsType": "ext4",
                    "options": {
                        "fsType": "ext4",
                        "volumeID": "06e10708-6412-4190-8496-f9531fb5fd0c"
                    }
                },
                "accessModes": [
                    "ReadWriteMany"
                ],
                "claimRef": {
                    "kind": "PersistentVolumeClaim",
                    "namespace": "test-namespace",
                    "name": "cci-evs-jxzqegxe-k1z3",
                    "uid": "e82c1574-a46d-11e9-be8a-b44326d0c915",
                    "apiVersion": "v1",
                    "resourceVersion": "65003516"
                },
                "persistentVolumeReclaimPolicy": "Delete",
                "storageClassName": "sata"
            },
            "status": {
                "phase": "Bound"
            }
        },
        "storageInfo": {
            "kind": "Volume",
            "apiVersion": "paas/v1beta1",
            "metadata": {
                "name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "creationTimestamp": "2019-07-12T06:25:56Z",
                "labels": {
                    "__system__volume_name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                    "hw:passthrough": "true",
                    "kubernetes.io/namespace": "test-namespace",
                    "tenant.kubernetes.io/domain-id": "f0c61dbd65974140956ed37a91ea860f",
                    "tenant.kubernetes.io/project-id": "cdb4249297a44665a63eec4f27ad09bf"
                }
            },
            "spec": {
                "name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "size": 10,
                "inresourcepool": false,
                "availability_zone": "cn-north-1a",
                "volume_type": "sata",
                "multiattach": true,
                "access": {
                    "": {
                        "access_type": "",
                        "access_to": "",
                        "access_level": "",
                        "id": "",
                        "state": ""
                    }
                },
                "vpc_id": ""
            },
            "status": {
                "id": "06e10708-6412-4190-8496-f9531fb5fd0c",
                "status": "available",
                "created_at": "2019-07-12T06:25:56Z",
                "attachments": null,
                "app_info": null
            }
        }
    }
]
```

## 状态码<a name="section2098632"></a>

**表 4**  状态码

<a name="table51313205"></a>
<table><thead align="left"><tr id="row28244554"><th class="cellrowborder" valign="top" width="33.25%" id="mcps1.2.3.1.1"><p id="p6107551"><a name="p6107551"></a><a name="p6107551"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="66.75%" id="mcps1.2.3.1.2"><p id="p24949608"><a name="p24949608"></a><a name="p24949608"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row7652366"><td class="cellrowborder" valign="top" width="33.25%" headers="mcps1.2.3.1.1 "><p id="p15861880"><a name="p15861880"></a><a name="p15861880"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="66.75%" headers="mcps1.2.3.1.2 "><p id="p9743886"><a name="p9743886"></a><a name="p9743886"></a>查询成功，并返回结果。</p>
</td>
</tr>
</tbody>
</table>

