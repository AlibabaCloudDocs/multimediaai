# GetTaskResult

调用GetTaskResult查新任务结果。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=multimediaai&api=GetTaskResult&type=RPC&version=2019-08-10)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GetTaskResult|系统规定参数。取值：GetTaskResult。 |
|TaskId|Long|是|1|任务ID。 |
|RegionId|String|否|cn-beijing|地域ID。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|75d919f1-feb6-40a4-9676-5ea4ebd3a010|请求唯一ID，具有唯一性。 |
|Result|Struct| |返回任务结果对象。 |
|AnalysisUseTime|Long|30|视频分析时间，单位秒。 |
|ApplicationId|String|applicationId|应用ID。 |
|ErrorCode|String|1000| |
|ErrorMessage|String|Download fail| |
|ErrorName|String|Download fail|错误名称 |
|ErrorReason|String|Download fail| |
|ProcessResultUrl|String|http://XXX.oss-cn-beijing.aliyuncs.com/processResult/xxxx.txt?Expires=1571392620&OSSAccessKeyId=LTAIHxxxxxxxQ2&Signature=9NTfu2jNuS45RRUCamiBLDQEtKg%3D|视频结果地址。 |
|VideoName|String|videoName|视频名称。 |
|VideoUrl|String|http://...|视频Url。 |
|Status|Integer|2|任务状态，0:提交中，1:执行中 2:执行成功，3:执行失败 。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=GetTaskResult
&TaskId=1
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<Status>2</Status>
<RequestId>75d919f1-feb6-40a4-9676-5ea4ebd3a010</RequestId>
<Result>
    <VideoName>videoName</VideoName>
    <AnalysisUseTime>30</AnalysisUseTime>
    <ApplicationId>applicationId</ApplicationId>
    <ProcessResultUrl>http://XXX.oss-cn-beijing.aliyuncs.com/processResult/xxxx.txt?Expires=1571392620&amp;OSSAccessKeyId=LTAIHxxxxxxxQ2&amp;Signature=9NTfu2jNuS45RRUCamiBLDQEtKg%3D</ProcessResultUrl>
    <VideoUrl>http://...</VideoUrl>
</Result>
```

`JSON` 格式

```
{
    "Status": 2,
    "RequestId": "75d919f1-feb6-40a4-9676-5ea4ebd3a010",
    "Result": {
        "VideoName": "videoName",
        "AnalysisUseTime": 30,
        "ApplicationId": "applicationId",
        "ProcessResultUrl": "http://XXX.oss-cn-beijing.aliyuncs.com/processResult/xxxx.txt?Expires=1571392620&amp;OSSAccessKeyId=LTAIHxxxxxxxQ2&amp;Signature=9NTfu2jNuS45RRUCamiBLDQEtKg%3D",
        "VideoUrl": "http://..."
    }
}
```

## 错误码

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
|406|ApplicationCountLimit|The maximum number of applications is exceeded.|应用数量达到限制|
|406|FileUploadCountLimit|The maximum number of file upload is exceeded.|上传文件数量达到限制|
|406|FileContentInvalid|The specified file content is invalid.|文件内容格式不正确|
|406|ExistParameter|The specified parameter %s exists.|参数%s已存在|
|406|ExistTemplateRelationship|The associated template already exists.|存在关联模板|
|400|InvalidParameterLengthLimit|The maximum length of %s is exceeded.|字段%s最大长度限制|
|403|Forbidden|The beta version has expired.|公测已到期|

访问[错误中心](https://error-center.aliyun.com/status/product/multimediaai)查看更多错误码。

