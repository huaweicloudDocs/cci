# 列出APIVersions<a name="getCoreAPIVersions"></a>

## 功能介绍

get available API versions

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=getCoreAPIVersions)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

GET /api

## 请求参数

**表 1**  请求Header参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|X-Auth-Token|是|String|用户Token。通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。|


## 响应参数

**状态码： 200**

**表 2**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|serverAddressByClientCIDRs|Array of io.k8s.apimachinery.pkg.apis.meta.v1.ServerAddressByClientCIDR_v2 objects|a map of client CIDR to server address that is serving this group. This is to help clients reach servers in the most network-efficient way possible. Clients can use the appropriate server address as per the CIDR that they match. In case of multiple matches, clients should use the longest matching CIDR. The server returns only those CIDRs that it thinks that the client can match. For example: the master will return an internal IP CIDR only, if the client reaches the server using an internal IP. Server looks at X-Forwarded-For header or X-Real-Ip header or request.RemoteAddr (in that order) to get the client IP.|
|versions|Array of strings|versions are the api versions that are available.|


**表 3**  io.k8s.apimachinery.pkg.apis.meta.v1.ServerAddressByClientCIDR\_v2

|参数|参数类型|描述|
|--|--|--|
|clientCIDR|String|The CIDR with which clients can match their IP to figure out the server address that they should use.|
|serverAddress|String|Address of this server, suitable for a client that matches the above CIDR. This can be a hostname, hostname:port, IP or IP:port.|


## 请求示例

无

## 响应示例

**状态码： 200**

OK

```
{
  "kind" : "APIVersions",
  "serverAddressByClientCIDRs" : [ {
    "clientCIDR" : "0.0.0.0/0",
    "serverAddress" : "https://cci.cn-east-3.myhuaweicloud.com"
  } ],
  "versions" : [ "v1" ]
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


