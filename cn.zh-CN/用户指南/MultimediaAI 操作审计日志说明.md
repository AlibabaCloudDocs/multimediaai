MultimediaAI 操作审计日志说明 
==========================================



阿里云 MultimediaAI 已与 阿里云 ActionTrail 集成，您可以在 ActionTrail 中查看和检索用户行为日志，同时通过ActrionTrail 将日志投递到日志服务 LogStore 或指定的 OSS Bucket 中，满足实时审计、问题回溯分析等需要。



**ActionTrail 中记录的 MultimediaAI 操作日志** 

MultimediaAI 的操作审计日志主要包含的是 API 事件，其中 OpenAPI 事件在 ActionTrail 中记录的 eventType 取值为 ApiCall，其含义可以参考 [MultimediaAI 的 API 说明](https://help.aliyun.com/document_detail/139446.html?spm=a2c4g.11186623.6.562.7905213bmI6vR4)。



**MultimediaAI 的日志样例** 

    {
      "eventId": "25084769-F769-4614-A1A1-8DEE56E3F8CC",
      "eventVersion": 1,
      "responseElements": {
        "TaskId": 10051344,
        "RequestId": "25084769-f769-4614-a1a1-8dee56e3f8cc"
      },
      "eventSource": "multimediaai.cn-hangzhou.aliyuncs.com",
      "requestParameters": {
        "charset": "UTF-8",
        "AcsHost": "multimediaai.cn-hangzhou.aliyuncs.com",
        "AcsProduct": "multimediaai",
        "RequestId": "25084769-F769-4614-A1A1-8DEE56E3F8CC",
        "VideoName": "2278518_74.mp4",
        "AcceptLanguage": "zh-CN",
        "RegionId": "cn-hangzhou",
        "HostId": "multimediaai.cn-hangzhou.aliyuncs.com",
        "ApplicationId": "d79cca0e686843e9",
        "TemplateId": 689,
        "VideoUrl": "https://shotaction.oss-cn-zhangjiakou.aliyuncs.com/seg_dir/2278518_74.mp4"
      },
      "sourceIpAddress": "42.120.72.93",
      "userAgent": "pre-multimediaai.console.aliyun.com",
      "eventType": "ApiCall",
      "referencedResources": {
        "ACS::MultimediaAI::Application": [
          "d79cca0e686843e9"
        ],
        "ACS::MultimediaAI::Task": [
          "10051344"
        ]
      },
      "userIdentity": {
        "sessionContext": {
          "attributes": {
            "mfaAuthenticated": "false"
          }
        },
        "accountId": "1679287699149642",
        "principalId": "1679287699149642",
        "type": "root-account",
        "userName": "root"
      },
      "serviceName": "MultimediaAI",
      "additionalEventData": {
        "Scheme": "http"
      },
      "apiVersion": "2019-08-10",
      "requestId": "25084769-F769-4614-A1A1-8DEE56E3F8CC",
      "eventTime": "2021-02-05T08:31:49Z",
      "isGlobal": false,
      "acsRegion": "cn-hangzhou",
      "eventName": "CreateLabelTask"
    }



