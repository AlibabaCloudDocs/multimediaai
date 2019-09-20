# GetTaskResult {#doc_api_multimediaai_GetTaskResult .reference}

调用GetTaskResult查新任务结果。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=multimediaai&api=GetTaskResult&type=RPC&version=2019-08-10)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetTaskResult|系统规定参数。取值：GetTaskResult。

 |
|TaskId|Long|是|1|任务ID。

 |
|RegionId|String|否|cn-beijing|VPC所在地域ID。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|75d919f1-feb6-40a4-9676-5ea4ebd3a010|请求唯一id

 |
|Result| | |返回任务结果对象

 |
|AnalysisUseTime|Long|30|视频分析时间，单位秒

 |
|ApplicationId|String|applicationId|应用id

 |
|ProcessResultUrl|String|http://XXX.oss-cn-beijing.aliyuncs.com/processResult/xxxx.txt?Expires=1571392620&OSSAccessKeyId=LTAIHWpn3Px9nfQ2&Signature=9NTfu2jNuS45RRUCamiBLDQEtKg%3D|视频结果地址

 |
|VideoName|String|videoName|视频名称

 |
|Status|Integer|2|任务状态，0:提交中，1:执行中 2:执行成功，3:执行失败

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=GetTaskResult
&TaskId=1
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<GetTaskResultResponse>
      <Result>
            <ProcessResultUrl>
            		      <ProcessResultUrl>http://XXXx.oss-cn-beijing.aliyuncs.com/processResult/xxxx.txt?Expires=1571392620&amp;OSSAccessKeyId=LTAIHWpn3Px9nfQ2&amp;Signature=9NTfu2jNuS45RRUCamiBLDQEtKg%3D</ProcessResultUrl>
            </ProcessResultUrl>
            <VideoName>400099</VideoName>
            <ApplicationId>1913287818704742</ApplicationId>
      </Result>
      <Status>2</Status>
      <RequestId>fa1976da-e6c6-472c-bdc8-09d42eb11884</RequestId>
</GetTaskResultResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"Status":2,
	"Result":{
		"ProcessResultUrl":"http://XXXx.oss-cn-beijing.aliyuncs.com/processResult/xxxx.txt?Expires=1571392620&OSSAccessKeyId=LTAIHWpn3Px9nfQ2&Signature=9NTfu2jNuS45RRUCamiBLDQEtKg%3D",
		"VideoName":"400099",
		"ApplicationId":"XXXXXXXX"
	},
	"RequestId":"75d919f1-feb6-40a4-9676-5ea4ebd3a010",
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

