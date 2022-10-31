# 删除Job<a name="deleteBatchV1NamespacedJob"></a>

## 功能介绍

删除Job。

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=deleteBatchV1NamespacedJob)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

DELETE /apis/batch/v1/namespaces/\{namespace\}/jobs/\{name\}

**表 1**  路径参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|是|String|name of the Job|
|namespace|是|String|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|gracePeriodSeconds|否|Integer|The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.|
|orphanDependents|否|Boolean|Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.|
|propagationPolicy|否|String|Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: 'Orphan' - orphan the dependents; 'Background' - allow the garbage collector to delete the dependents in the background; 'Foreground' - a cascading policy that deletes all dependents in the foreground.|
|pretty|否|String|If 'true', then the output is pretty printed.|


## 请求参数

**表 3**  请求Header参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|X-Auth-Token|是|String|用户Token。通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。|
|Content-Type|是|String|消息体的类型（格式），默认取值为“application/json”缺省值：**application/json**|


**表 4**  请求Body参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|否|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|gracePeriodSeconds|否|Long|The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.|
|kind|否|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|orphanDependents|否|Boolean|Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.|
|preconditions|否|io.k8s.apimachinery.pkg.apis.meta.v1.Preconditions object|Must be fulfilled before a deletion is carried out. If not possible, a 409 Conflict status will be returned.|
|propagationPolicy|否|String|Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: 'Orphan' - orphan the dependents; 'Background' - allow the garbage collector to delete the dependents in the background; 'Foreground' - a cascading policy that deletes all dependents in the foreground.|


**表 5**  io.k8s.apimachinery.pkg.apis.meta.v1.Preconditions

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|uid|否|String|Specifies the target UID.|


## 响应参数

**状态码： 200**

**表 6**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails_v3 object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|String|A human-readable description of the status of this operation.|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta_v2 object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 7**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 8**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 9**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


## 请求示例

-   只删除Job（对应Pod不删除）：

    ```
    {
      "apiVersion" : "v1",
      "gracePeriodSeconds" : 0,
      "kind" : "DeleteOptions",
      "propagationPolicy" : "Orphan"
    }
    ```

-   前台级联删除（按照Pod-\>Job的顺序进行删除）

    ```
    {
      "apiVersion" : "v1",
      "kind" : "DeleteOptions",
      "propagationPolicy" : "Foreground"
    }
    ```

-   后台级联删除（按照Job-\>Pod的顺序进行删除）

    ```
    {
      "apiVersion" : "v1",
      "kind" : "DeleteOptions",
      "propagationPolicy" : "Background"
    }
    ```


## 响应示例

**状态码： 200**

OK

```
{
  "apiVersion" : "batch/v1",
  "kind" : "Job",
  "metadata" : {
    "creationTimestamp" : "2018-09-05T01:10:59Z",
    "deletionGracePeriodSeconds" : 0,
    "deletionTimestamp" : "2018-09-05T03:27:34Z",
    "enable" : true,
    "finalizers" : [ "orphan" ],
    "labels" : {
      "app" : "test2",
      "controller-uid" : "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
      "job-name" : "pi"
    },
    "name" : "pi",
    "namespace" : "namespace-test",
    "resourceVersion" : "5415127",
    "selfLink" : "/apis/batch/v1/namespaces/namespace-test/jobs/pi",
    "uid" : "8c923079-b0a8-11e8-8bcb-f898ef6c78b4"
  },
  "spec" : {
    "backoffLimit" : 6,
    "completions" : 1,
    "parallelism" : 1,
    "selector" : {
      "matchLabels" : {
        "controller-uid" : "8c923079-b0a8-11e8-8bcb-f898ef6c78b4"
      }
    },
    "template" : {
      "metadata" : {
        "annotations" : {
          "cri.cci.io/container-type" : "secure-container"
        },
        "creationTimestamp" : null,
        "enable" : true,
        "labels" : {
          "controller-uid" : "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
          "job-name" : "pi"
        },
        "name" : "pi"
      },
      "spec" : {
        "containers" : [ {
          "command" : [ "perl", "-Mbignum=bpi", "-wle", "print bpi(2000)" ],
          "image" : "perl",
          "imagePullPolicy" : "Always",
          "name" : "pi",
          "resources" : {
            "limits" : {
              "cpu" : "500m",
              "memory" : "1Gi"
            },
            "requests" : {
              "cpu" : "500m",
              "memory" : "1Gi"
            }
          },
          "terminationMessagePath" : "/dev/termination-log",
          "terminationMessagePolicy" : "File"
        } ],
        "dnsPolicy" : "ClusterFirst",
        "imagePullSecrets" : [ {
          "name" : "imagepull-secret"
        } ],
        "restartPolicy" : "Never",
        "schedulerName" : "default-scheduler",
        "securityContext" : { }
      }
    }
  },
  "status" : {
    "active" : 1,
    "startTime" : "2018-09-05T01:10:59Z"
  }
}
```

## 状态码

|状态码|描述|
|--|--|
|200|OK|
|400|BadRequest|
|401|Unauthorized|
|403|Forbidden|
|404|NotFound|
|405|MethodNotAllowed|
|406|NotAcceptable|
|409|Conflict|
|415|UnsupportedMediaType|
|422|Invalid|
|429|TooManyRequests|
|500|InternalError|
|503|ServiceUnavailable|
|504|ServerTimeout|


