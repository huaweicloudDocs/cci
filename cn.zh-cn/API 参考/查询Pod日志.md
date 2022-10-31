# 查询Pod日志<a name="readCoreV1NamespacedPodLog"></a>

## 功能介绍

查询Pod的日志。

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=readCoreV1NamespacedPodLog)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

GET /api/v1/namespaces/\{namespace\}/pods/\{name\}/log

**表 1**  路径参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|是|String|name of the Pod|
|namespace|是|String|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|container|否|String|The container for which to stream logs. Defaults to only container if there is one container in the pod.|
|follow|否|Boolean|Follow the log stream of the pod. Defaults to false.|
|limitBytes|否|Integer|If set, the number of bytes to read from the server before terminating the log output. This may not display a complete final line of logging, and may return slightly more or slightly less than the specified limit.|
|pretty|否|String|If 'true', then the output is pretty printed.|
|previous|否|Boolean|Return previous terminated container logs. Defaults to false.|
|sinceSeconds|否|Integer|A relative time in seconds before the current time from which to show logs. If this value precedes the time a pod was started, only logs since the pod start will be returned. If this value is in the future, no logs will be returned. Only one of sinceSeconds or sinceTime may be specified.|
|tailLines|否|Integer|If set, the number of lines from the end of the logs to show. If not specified, logs are shown from the creation of the container or sinceSeconds or sinceTime|
|timestamps|否|Boolean|If true, add an RFC3339 or RFC3339Nano timestamp at the beginning of every line of log output. Defaults to false.|


## 请求参数

**表 3**  请求Header参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|X-Auth-Token|是|String|用户Token。通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。|


## 响应参数

无

## 请求示例

无

## 响应示例

无

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


