# 删除PyTorchJob<a name="cci_02_3165"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

删除PyTorchJob。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

DELETE /apis/kubeflow.org/v1/namespaces/\{namespace\}/pytorchjobs/\{name\}

**表 1**  Path参数

|参数|是否必选|描述|
|--|--|--|
|name|Yes|name of the PyTorchJob|
|namespace|Yes|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|描述|
|--|--|--|
|dryRun|No|When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed|
|gracePeriodSeconds|No|The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.|
|orphanDependents|No|Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the “orphan” finalizer will be added to/removed from the object’s finalizers list. Either this field or PropagationPolicy may be set, but not both.|
|propagationPolicy|No|Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: ‘Orphan’ - orphan the dependents; ‘Background’ - allow the garbage collector to delete the dependents in the background; ‘Foreground’ - a cascading policy that deletes all dependents in the foreground.|
|pretty|No|If 'true’, then the output is pretty printed.|


## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

N/A

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数的详细描述请参见[表72](数据结构-0.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "Status",
    "apiVersion": "v1",
    "metadata": {},
    "status": "Success",
    "details": {
        "name": "pytorch-test",
        "group": "kubeflow.org",
        "kind": "pytorchjobs",
        "uid": "be7696f9-adfe-11e9-aaa4-340a9837e413"
    }
}
```

## 状态码<a name="zh-cn_topic_0083864910_section16509142112516"></a>

**表 3**  状态码

|状态码|描述|
|--|--|
|200|OK|
|202|Accepted|
|401|Unauthorized|
|500|Internal Error|
|403|Forbidden|


