# 创建Service<a name="cci_02_3048"></a>

## 功能介绍<a name="s6b7bf0e53f9c495eb9b89e73dc6bae80"></a>

创建一个Service。

## URI<a name="s5d6abc7988cb426db0a9a10aa1e612b6"></a>

POST /api/v1/namespaces/\{namespace\}/services

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

<a name="zh-cn_topic_0079615000_table64523107"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615000_row55516030"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615000_p504568"><a name="zh-cn_topic_0079615000_p504568"></a><a name="zh-cn_topic_0079615000_p504568"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p64287338205444"><a name="p64287338205444"></a><a name="p64287338205444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p39891894205444"><a name="p39891894205444"></a><a name="p39891894205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615000_row48602122"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615000_p44457847"><a name="zh-cn_topic_0079615000_p44457847"></a><a name="zh-cn_topic_0079615000_p44457847"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615000_p44315844"><a name="zh-cn_topic_0079615000_p44315844"></a><a name="zh-cn_topic_0079615000_p44315844"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p32813593"><a name="zh-cn_topic_0079615000_p32813593"></a><a name="zh-cn_topic_0079615000_p32813593"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079615000_ref458763557"></a>

**请求参数：**

请求参数参见[表101](数据结构.md#zh-cn_topic_0079615000_ref458759328)。

**请求示例：**

ClusterIP类型示例。

```
{
    "apiVersion": "v1",
    "kind": "Service",
    "metadata": {
        "name": "redis",
        "labels": {
            "app": "redis"
        }
    },
    "spec": {
        "selector": {
            "app": "redis"
        },
        "ports": [
            {
                "name": "service0",
                "targetPort": 80,
                "port": 8080,
                "protocol": "TCP"
            }
        ],
        "type": "ClusterIP"
    }
}
```

LoadBalancer类型示例。

LoadBalancer类型Service需要在metadata.annotations自定中添加elb实例ID（kubernetes.io/elb.id）、项目ID（tenant.kubernetes.io/project-id）和账号ID（tenant.kubernetes.io/domain-id）

```
{
    "apiVersion": "v1",
    "kind": "Service",
    "metadata": {
        "name": "nginx",
        "annotations": {
           "kubernetes.io/elb.id": "77e6246c-a091-xxxx-xxxx-789baa571280",
            "tenant.kubernetes.io/project-id": "a9cab8xxxxxxxxxxxxxxxx41c0aeb",
            "tenant.kubernetes.io/domain-id": "65382xxxxxxxxxxxxxxxxxe684b"
        }
    },
    "spec": {
        "selector": {
            "app": "nginx"
        },
        "ports": [
            {
                "name": "service0",
                "targetPort": 80,
                "port": 8080,
                "protocol": "TCP"
            }
        ],
        "type": "LoadBalancer"
    }
}
```

## 响应消息<a name="s6d1491fd7cac4a0fa401c80bcb2778d1"></a>

**响应参数：**

响应参数的详细描述请参见[表101](数据结构.md#zh-cn_topic_0079615000_ref458759328)。

**响应示例：**

```
{
    "kind": "Service",
    "apiVersion": "v1",
    "metadata": {
        "name": "redis",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/services/redis",
        "uid": "d6a1ce79-afdb-11e8-b6ef-f898ef6c78b4",
        "resourceVersion": "5146412",
        "creationTimestamp": "2018-09-04T00:45:36Z",
        "labels": {
            "app": "redis"
        },
        "enable": true
    },
    "spec": {
        "ports": [
            {
                "name": "service0",
                "protocol": "TCP",
                "port": 8080,
                "targetPort": 80
            }
        ],
        "selector": {
            "app": "redis"
        },
        "clusterIP": "10.247.212.210",
        "type": "ClusterIP",
        "sessionAffinity": "None"
    },
    "status": {
        "loadBalancer": {}
    }
}
```

## 状态码<a name="s98b5155925e944f0b008c4f34c95225b"></a>

[表3](#zh-cn_topic_0079615000_table33742049)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615000_table33742049"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615000_row19948981"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p59593538205444"><a name="p59593538205444"></a><a name="p59593538205444"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p62347282205444"><a name="p62347282205444"></a><a name="p62347282205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615000_row49645340"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615000_p61849578"><a name="zh-cn_topic_0079615000_p61849578"></a><a name="zh-cn_topic_0079615000_p61849578"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615000_p43759888"><a name="zh-cn_topic_0079615000_p43759888"></a><a name="zh-cn_topic_0079615000_p43759888"></a>The request has been fulfilled, resulting in the creation of a new resource.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

