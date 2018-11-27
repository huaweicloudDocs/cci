# 创建Ingress<a name="cci_02_3056"></a>

## 功能介绍<a name="section53754776"></a>

创建Ingress。

如果在创建Ingress资源对象和Deployment/StatefuleSet资源对象后，要在CCI界面，工作负载详情页面中，“访问方式“页签下显示对应的Ingress资源，则需要给创建的Ingress资源对象添加labels标签，并且设置对应的selector。

设置请求消息体中的“metadata.labels“参数键值如下：

```
labels:
    app: appname
```

设置请求消息体中的“spec.selector“参数键值如下：

```
selector:
    app: appname 
```

其中：

-   lables参数下“app“参数所键入的“appname“为显示在CCI工作负载界面上的工作负载名称，其值与Deployment/StatefuleSet的“metadata.name“中所添加的内容一致。
-   selector参数下“app“的值与需要关联的Deployment的“spec.selector“保持一致。

## URI<a name="section14030938"></a>

POST /apis/extensions/v1beta1/namespaces/\{namespace\}/ingresses

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

<a name="d0e42906"></a>
<table><thead align="left"><tr id="row10640301"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.169999999999998%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17811636"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p33456451"><a name="p33456451"></a><a name="p33456451"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p25618043"><a name="p25618043"></a><a name="p25618043"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p61795587"><a name="p61795587"></a><a name="p61795587"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section18662134312520"></a>

**请求参数：**

请求参数请参见[表111](公共参数.md#d0e42951)。

**表 3**  创建Ingress时必填的annotations字段数据结构说明

<a name="table1219043217326"></a>
<table><thead align="left"><tr id="row1019023212325"><th class="cellrowborder" valign="top" width="31.683168316831683%" id="mcps1.2.5.1.1"><p id="p11909326324"><a name="p11909326324"></a><a name="p11909326324"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.891089108910892%" id="mcps1.2.5.1.2"><p id="p171901532153212"><a name="p171901532153212"></a><a name="p171901532153212"></a>是否必须</p>
</th>
<th class="cellrowborder" valign="top" width="12.871287128712872%" id="mcps1.2.5.1.3"><p id="p219015321324"><a name="p219015321324"></a><a name="p219015321324"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.554455445544555%" id="mcps1.2.5.1.4"><p id="p8872152412914"><a name="p8872152412914"></a><a name="p8872152412914"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10190183223213"><td class="cellrowborder" valign="top" width="31.683168316831683%" headers="mcps1.2.5.1.1 "><p id="p3190103273218"><a name="p3190103273218"></a><a name="p3190103273218"></a>kubernetes.io/elb.id</p>
</td>
<td class="cellrowborder" valign="top" width="10.891089108910892%" headers="mcps1.2.5.1.2 "><p id="p16465204161912"><a name="p16465204161912"></a><a name="p16465204161912"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="12.871287128712872%" headers="mcps1.2.5.1.3 "><p id="p787663812220"><a name="p787663812220"></a><a name="p787663812220"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.554455445544555%" headers="mcps1.2.5.1.4 "><p id="p19440125812308"><a name="p19440125812308"></a><a name="p19440125812308"></a>ELB实例的ID。</p>
</td>
</tr>
<tr id="row11190183213217"><td class="cellrowborder" valign="top" width="31.683168316831683%" headers="mcps1.2.5.1.1 "><p id="p1480352318318"><a name="p1480352318318"></a><a name="p1480352318318"></a>kubernetes.io/elb.ip</p>
</td>
<td class="cellrowborder" valign="top" width="10.891089108910892%" headers="mcps1.2.5.1.2 "><p id="p1037844716197"><a name="p1037844716197"></a><a name="p1037844716197"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="12.871287128712872%" headers="mcps1.2.5.1.3 "><p id="p574619495197"><a name="p574619495197"></a><a name="p574619495197"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.554455445544555%" headers="mcps1.2.5.1.4 "><p id="p1787717112314"><a name="p1787717112314"></a><a name="p1787717112314"></a>ELB实例的IP。</p>
</td>
</tr>
<tr id="row1367415418314"><td class="cellrowborder" valign="top" width="31.683168316831683%" headers="mcps1.2.5.1.1 "><p id="p2674841314"><a name="p2674841314"></a><a name="p2674841314"></a>kubernetes.io/elb.port</p>
</td>
<td class="cellrowborder" valign="top" width="10.891089108910892%" headers="mcps1.2.5.1.2 "><p id="p444433216314"><a name="p444433216314"></a><a name="p444433216314"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="12.871287128712872%" headers="mcps1.2.5.1.3 "><p id="p114441632163115"><a name="p114441632163115"></a><a name="p114441632163115"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.554455445544555%" headers="mcps1.2.5.1.4 "><p id="p2674174193117"><a name="p2674174193117"></a><a name="p2674174193117"></a>ELB实例的端口。</p>
</td>
</tr>
</tbody>
</table>

**请求示例：**

```
{
    "apiVersion": "extensions/v1beta1",
    "kind": "Ingress",
    "metadata": {
        "name": "redis",
        "labels": {
            "app": "redis",
            "isExternal": "true",
            "zone": "data"
        },
        "annotations": {
            "kubernetes.io/elb.id": "2d48d034-6046-48db-8bb2-53c67e8148b5",
            "kubernetes.io/elb.ip": "192.168.137.182",
            "kubernetes.io/elb.port": "6071"
        }
    },
    "spec": {
        "rules": [
            {
                "http": {
                    "paths": [
                        {
                            "path": "/",
                            "backend": {
                                "serviceName": "redis",
                                "servicePort": 8080
                            }
                        }
                    ]
                }
            }
        ]
    }
}
```

## 响应消息<a name="section42255610417"></a>

**响应参数：**

响应参数的详细描述请参见[表111](公共参数.md#d0e42951)。

**响应示例：**

```
{
  "kind": "Ingress",
  "apiVersion": "extensions/v1beta1",
  "metadata": {
    "name": "redis",
    "namespace": "namespace-test",
    "selfLink": "/apis/extensions/v1beta1/namespaces/namespace-test/ingresses/redis",
    "uid": "7f86c310-afe8-11e8-b6ef-f898ef6c78b4",
    "resourceVersion": "5161127",
    "generation": 1,
    "creationTimestamp": "2018-09-04T02:16:14Z",
    "labels": {
      "app": "redis",
      "isExternal": "true",
      "zone": "data"
    },
    "annotations": {
      "kubernetes.io/elb.id": "2d48d034-6046-48db-8bb2-53c67e8148b5",
      "kubernetes.io/elb.ip": "192.168.137.182",
      "kubernetes.io/elb.port": "6071"
    },
    "enable": true
  },
  "spec": {
    "rules": [
      {
        "http": {
          "paths": [
            {
              "path": "/",
              "backend": {
                "serviceName": "redis",
                "servicePort": 8080
              }
            }
          ]
        }
      }
    ]
  },
  "status": {
    "loadBalancer": {

    }
  }
}
```

## 状态码<a name="section7688181432015"></a>

[表4](#d0e43055)描述API的状态码。

**表 4**  状态码

<a name="d0e43055"></a>
<table><thead align="left"><tr id="row20813512"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p8172937"><a name="p8172937"></a><a name="p8172937"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p58028199"><a name="p58028199"></a><a name="p58028199"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2663689"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p14432280"><a name="p14432280"></a><a name="p14432280"></a>202</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p28164027"><a name="p28164027"></a><a name="p28164027"></a>Accepted</p>
</td>
</tr>
</tbody>
</table>

