# ListTasks

获取任务列表

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=multimediaai&api=ListTasks&type=RPC&version=2019-08-10)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|ListTasks|系统规定参数。取值：ListTasks。 |
|PageNumber|Integer|是|1|页数 |
|PageSize|Integer|是|10|每页大小 |
|RegionId|String|否|cn-beijing|区域 |
|Status|Integer|否|2|状态0：等待中 1：执行中 2：成功 3：失败 |
|ApplicationName|String|否|应用名称|应用名 |
|TaskId|Long|否|4235611|任务ID |
|ServiceType|Integer|否|1|类型 1：结构化分析 2：静态封面 3：动态封面 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|PageNumber|Integer|1|页码 |
|PageSize|Integer|10|页面大小 |
|RequestId|String|abc-123|请求ID |
|Tasks|Array of Task| |任务 |
|ApplicationId|String|abc123|应用id |
|ApplicationName|String|应用名称|应用名 |
|CreateTime|String|2021-01-01|创建时间 |
|ErrorCode|String|400|错误码 |
|ErrorMessage|String|The service is not activated.|错误信息 |
|ErrorName|String|ServiceNotSelected|错误名称 |
|ErrorReason|String|The service is not activated.|错误原因 |
|ProcessResultUrl|String|http://xxx.xxx.xx|结果地址 |
|ProcessingDuration|Long|1000|处理耗时 |
|Status|Integer|2|任务状态 |
|TaskId|Long|43567811|任务ID |
|Template|Struct| |模板信息 |
|Id|String|176|模板ID |
|Name|String|模板名字|模板名称 |
|VideoName|String|视频名称|视频名称 |
|VideoUrl|String|http://xxx.xxx.xxx|视频地址 |
|TotalCount|Long|100000|总数 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=ListTasks
&PageNumber=1
&PageSize=10
&<公共请求参数>
```

正常返回示例

`XML`格式

```
<TotalCount/>
<Tasks>
    <ErrorName/>
    <Status/>
    <ApplicationName/>
    <TaskId/>
    <VideoName/>
    <ProcessingDuration/>
    <CreateTime/>
    <ErrorReason/>
    <ErrorCode/>
    <ErrorMessage/>
    <ApplicationId/>
    <ProcessResultUrl/>
    <VideoUrl/>
    <Template>
        <Id/>
        <Name/>
    </Template>
</Tasks>
<PageSize/>
<RequestId/>
<PageNumber/>
```

`JSON`格式

```
{
    "TotalCount": "",
    "Tasks": {
        "ErrorName": "",
        "Status": "",
        "ApplicationName": "",
        "TaskId": "",
        "VideoName": "",
        "ProcessingDuration": "",
        "CreateTime": "",
        "ErrorReason": "",
        "ErrorCode": "",
        "ErrorMessage": "",
        "ApplicationId": "",
        "ProcessResultUrl": "",
        "VideoUrl": "",
        "Template": {
            "Id": "",
            "Name": ""
        }
    },
    "PageSize": "",
    "RequestId": "",
    "PageNumber": ""
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

