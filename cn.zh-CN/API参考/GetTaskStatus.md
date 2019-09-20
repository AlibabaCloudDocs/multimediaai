# GetTaskStatus {#doc_api_multimediaai_GetTaskStatus .reference}

调用GetTaskStatus查询任务执行状态

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=multimediaai&api=GetTaskStatus&type=RPC&version=2019-08-10)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetTaskStatus|系统规定参数。取值：GetTaskStatus。

 |
|TaskId|Long|是|1|应用id

 |
|RegionId|String|否|cn-beijing|VPC所在的区域id

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|cc53a4b3-8002-4717-a1d8-208be4492834|请求唯一id

 |
|Status|Integer|2|任务状态：

 -   0：提交中
-   1：执行中
-   2：执行成功
-   3：执行失败

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=GetTaskStatus
&TaskId=1
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<GetTaskStatusResponse>
      <Status>2</Status>
      <RequestId>cc53a4b3-8002-4717-a1d8-208be4492834</RequestId>
</GetTaskStatusResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Status":2,
	"RequestId":"cc53a4b3-8002-4717-a1d8-208be4492834"
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

