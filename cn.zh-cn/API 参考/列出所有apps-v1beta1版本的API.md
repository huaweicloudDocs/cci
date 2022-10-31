# 列出所有apps/v1beta1版本的API<a name="getAppsV1beta1APIResources"></a>

## 功能介绍

get available resources

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=getAppsV1beta1APIResources)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

GET /apis/apps/v1beta1

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
|groupVersion|String|groupVersion is the group and version this APIResourceList is for.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|resources|Array of io.k8s.apimachinery.pkg.apis.meta.v1.APIResource_v2 objects|resources contains the name of the resources and if they are namespaced.|


**表 3**  io.k8s.apimachinery.pkg.apis.meta.v1.APIResource\_v2

|参数|参数类型|描述|
|--|--|--|
|categories|Array of strings|categories is a list of the grouped resources this resource belongs to (e.g. 'all')|
|group|String|group is the preferred group of the resource.  Empty implies the group of the containing resource list. For subresources, this may have a different value, for example: Scale".|
|kind|String|kind is the kind for the resource (e.g. 'Foo' is the kind for a resource 'foo')|
|name|String|name is the plural name of the resource.|
|namespaced|Boolean|namespaced indicates if a resource is namespaced or not.|
|shortNames|Array of strings|shortNames is a list of suggested short names of the resource.|
|singularName|String|singularName is the singular name of the resource. This allows clients to handle plural and singular opaquely. The singularName is more correct for reporting status on a single item and both singular and plural are allowed from the kubectl CLI interface.|
|verbs|Array of strings|verbs is a list of supported kube verbs (this includes get, list, watch, create, update, patch, delete, deletecollection, and proxy)|
|version|String|version is the preferred version of the resource.  Empty implies the version of the containing resource list For subresources, this may have a different value, for example: v1 (while inside a v1beta1 version of the core resource's group)".|


## 请求示例

无

## 响应示例

**状态码： 200**

OK

```
{
  "apiVersion" : "v1",
  "groupVersion" : "apps/v1beta1",
  "kind" : "APIResourceList",
  "resources" : [ {
    "categories" : [ "all" ],
    "kind" : "Deployment",
    "name" : "deployments",
    "namespaced" : true,
    "shortNames" : [ "deploy" ],
    "singularName" : "",
    "verbs" : [ "create", "delete", "deletecollection", "get", "list", "patch", "update", "watch" ]
  }, {
    "kind" : "DeploymentRollback",
    "name" : "deployments/rollback",
    "namespaced" : true,
    "singularName" : "",
    "verbs" : [ "create" ]
  }, {
    "kind" : "Deployment",
    "name" : "deployments/status",
    "namespaced" : true,
    "singularName" : "",
    "verbs" : [ "get", "patch", "update" ]
  }, {
    "categories" : [ "all" ],
    "kind" : "StatefulSet",
    "name" : "statefulsets",
    "namespaced" : true,
    "shortNames" : [ "sts" ],
    "singularName" : "",
    "verbs" : [ "create", "delete", "deletecollection", "get", "list", "patch", "update", "watch" ]
  }, {
    "kind" : "StatefulSet",
    "name" : "statefulsets/status",
    "namespaced" : true,
    "singularName" : "",
    "verbs" : [ "get", "patch", "update" ]
  } ]
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


