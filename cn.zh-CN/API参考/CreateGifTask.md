# CreateGifTask {#doc_api_multimediaai_CreateGifTask .reference}

调用CreateGifTask提交视频GIF任务。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=multimediaai&api=CreateGifTask&type=RPC&version=2019-08-10)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateGifTask|系统规定参数。取值：CreateGifTask。

 |
|ApplicationId|String|是|ApplicationId|应用ID，需要在控制台先创建应用。

 |
|VideoName|String|是|testVideo|视频名称。

 |
|VideoUrl|String|是|http://XXX.mp4|视频地址。

 |
|RegionId|String|否|cn-beijing|VPC所在的地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|7CAB5D5A-575C-4E3D-A659-D1C9F6ABB012|请求唯一ID。

 |
|TaskId|Long|400010|任务id

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=CreateGifTask
&ApplicationId=ApplicationId
&VideoName=testVideo
&VideoUrl=http://XXX.mp4
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<CreateGifTaskResponse>
      <RequestId>7CAB5D5A-575C-4E3D-A659-D1C9F6ABB012</RequestId>
      <TaskId>400010</TaskId>
      <Code>OK</Code>
</CreateGifTaskResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"RequestId":"7CAB5D5A-575C-4E3D-A659-D1C9F6ABB012",
	"TaskId":400010,
	"Code":"OK"
}
```

## 错误码 { .section}

|HttpCode|错误码|错误信息|描述|
|--------|---|----|--|
|200|OK|Success|成功|
|500|InternalError|An error occurred while processing your request.|内部错误|
|404|InvalidApiNotFound|The specified API operation does not exist. Please check the URL and method.|API不存在，请检查url和method|
|400|InvalidParameter|The specified parameter %s is invalid.|参数非法，请检查参数%s|
|400|InvalidTimeStamp|The specified TimeStamp is invalid. Please check parameter %s.|时间格式非法，请检查参数%s|
|400|MissingParameter|You must specify the parameter %s.|缺少必要参数，请检查参数%s是否正确|
|404|ResourceNotFound|The requested resource does not exist. Please check the parameter %s.|请求资源不存在，请检查参数%s是否正确|
|500|ServiceUnavailable|An error occurred while processing your request.|内部服务不可用|
|500|UnknownError|An error occurred while processing your request.|未知错误|
|401|Unauthorized|You are not authorized to perform the operation.|该用户没有权限|
|406|ServiceNotSelected|The service is not activated.|未开启此服务|
|401|ServiceNotOpened|You have not purchased the service.|未购买此服务|
|401|BalanceNotEnough|The account balance is insufficient and you cannot perform the request.|余额不足，无法操作此请求|
|406|FaceImageCountLimit|The maximum number of face images is exceeded.|人脸数量达到限制|

访问[错误中心](https://error-center.aliyun.com/status/product/multimediaai)查看更多错误码。

