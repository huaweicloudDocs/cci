# 查询指定namespace下所有Job<a name="cci_02_3043"></a>

## 功能介绍<a name="section51751064"></a>

查询Namespace下所有Job的详细信息。

## URI<a name="section63106395"></a>

GET /apis/batch/v1/namespaces/\{namespace\}/jobs

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

<a name="d0e42130"></a>
<table><thead align="left"><tr id="row60594871"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="26%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="41%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row40994086"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p32186706"><a name="p32186706"></a><a name="p32186706"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.2 "><p id="p56986361"><a name="p56986361"></a><a name="p56986361"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="41%" headers="mcps1.2.4.1.3 "><p id="p52492549"><a name="p52492549"></a><a name="p52492549"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row2670901"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p15016403"><a name="p15016403"></a><a name="p15016403"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.2 "><p id="p8369097"><a name="p8369097"></a><a name="p8369097"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="41%" headers="mcps1.2.4.1.3 "><p id="p6808256"><a name="p6808256"></a><a name="p6808256"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="row61274307"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p64271838"><a name="p64271838"></a><a name="p64271838"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.2 "><p id="p38636365"><a name="p38636365"></a><a name="p38636365"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="41%" headers="mcps1.2.4.1.3 "><p id="p42537849"><a name="p42537849"></a><a name="p42537849"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="row47296321"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p5796754"><a name="p5796754"></a><a name="p5796754"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.2 "><p id="p66883924"><a name="p66883924"></a><a name="p66883924"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="41%" headers="mcps1.2.4.1.3 "><p id="p37345572"><a name="p37345572"></a><a name="p37345572"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="row565833"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p45832525"><a name="p45832525"></a><a name="p45832525"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.2 "><p id="p21447008"><a name="p21447008"></a><a name="p21447008"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="41%" headers="mcps1.2.4.1.3 "><p id="p59486125"><a name="p59486125"></a><a name="p59486125"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
<tr id="row65613080"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p13059244"><a name="p13059244"></a><a name="p13059244"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.2 "><p id="p51165837"><a name="p51165837"></a><a name="p51165837"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="41%" headers="mcps1.2.4.1.3 "><p id="p50792098"><a name="p50792098"></a><a name="p50792098"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="row54475699"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p50455538"><a name="p50455538"></a><a name="p50455538"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.2 "><p id="p60366810"><a name="p60366810"></a><a name="p60366810"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="41%" headers="mcps1.2.4.1.3 "><p id="p57873426"><a name="p57873426"></a><a name="p57873426"></a>Timeout for the list/watch call.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section31086645"></a>

N/A

## 响应消息<a name="section11344351"></a>

**响应参数：**

响应参数的详细描述请参见[表68](公共参数.md#zh-cn_topic_0079614930_table6622802)。

**响应示例：**

```
{
  "kind": "JobList",
  "apiVersion": "batch/v1",
  "metadata": {
    "selfLink": "/apis/batch/v1/namespaces/namespace-test/jobs",
    "resourceVersion": "5391600"
  },
  "items": [
    {
      "metadata": {
        "name": "pi",
        "namespace": "namespace-test",
        "selfLink": "/apis/batch/v1/namespaces/namespace-test/jobs/pi",
        "uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
        "resourceVersion": "5391205",
        "creationTimestamp": "2018-09-05T01:10:59Z",
        "labels": {
          "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
          "job-name": "pi"
        },
        "enable": true
      },
      "spec": {
        "parallelism": 1,
        "completions": 1,
        "backoffLimit": 6,
        "selector": {
          "matchLabels": {
            "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4"
          }
        },
        "template": {
          "metadata": {
            "name": "pi",
            "creationTimestamp": null,
            "labels": {
              "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
              "job-name": "pi"
            },
            "annotations": {
              "cri.cci.io/container-type": "secure-container"
            },
            "enable": true
          },
          "spec": {
            "containers": [
              {
                "name": "pi",
                "image": "perl",
                "command": [
                  "perl",
                  "-Mbignum=bpi",
                  "-wle",
                  "print bpi(2000)"
                ],
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
                "imagePullPolicy": "Always"
              }
            ],
            "restartPolicy": "Never",
            "terminationGracePeriodSeconds": 30,
            "dnsPolicy": "ClusterFirst",
            "securityContext": {

            },
            "imagePullSecrets": [
              {
                "name": "imagepull-secret"
              }
            ],
            "schedulerName": "default-scheduler"
          }
        }
      },
      "status": {
        "startTime": "2018-09-05T01:10:59Z",
        "active": 1
      }
    }
  ]
}
```

## 状态码<a name="section34990298"></a>

[表3](#d0e42261)描述API的状态码。

**表 3**  状态码

<a name="d0e42261"></a>
<table><thead align="left"><tr id="row59414131"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p47815306"><a name="p47815306"></a><a name="p47815306"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p47834569"><a name="p47834569"></a><a name="p47834569"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49394905"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p41564386"><a name="p41564386"></a><a name="p41564386"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p11272075"><a name="p11272075"></a><a name="p11272075"></a>This operation succeeds, and a group of Job resource objects is returned.</p>
</td>
</tr>
</tbody>
</table>

