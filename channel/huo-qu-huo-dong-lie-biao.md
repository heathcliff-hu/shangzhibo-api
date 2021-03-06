## 获取活动列表

### 接口

请求地址

```
GET api/activity
```

### 授权

请求 header

```
Authorization: Bearer <accessToken>
Content-Type: application/json
```

注：请将上方的`<accessToken>`替换为分配给您的秘钥串。关于如何获取 accessToken ，请咨询杨经理（18968187008）、彭经理（15167172618）。

### 参数

| 参数 | 参数类型 | 是否必填 | 描述 |
| :--- | :--- | :--- | :--- |
| status | string | 是 | 活动状态，分别为“可用”（enabled）、“已结束”（disabled）、“已禁用”（forbidden） 和”已归档“（deleted） |
| page | integer | 是 | 页码 |
| pageSize | integer | 是 | 每页几条 |

### 请求样例

```
/activity?status=enabled
```

### 响应参数

| 参数 | 类型 | 描述 | 示例 |
| :--- | :--- | :--- | :--- |
| page | string | 页码 | 2 |
| pageSize | string | 一页显示几条 | 10 |
| total | string | 总条数 | 100 |
| id | string | 活动 ID | 8050309 |
| name | string | 活动名称 | 分享禁用测试活动 |
| status | string | 活动状态 | enabled |

### 响应示例

```
{
    "pager": {
        "page": 1,
        "pageSize": 10,
        "total": 16
    },
    "items": [
        {
            "id": "2837888",
            "name": "创想人工智能峰会-深圳站",
            "categoryId": 1,
            "status": "disabled",
            "agentId": 101691,
            "startedAt": "2018-01-29T06:58:26.000Z",
            "endedAt": "2018-01-29T10:58:26.000Z",
            "pushDomain": "push.shangzhibo.tv",
            "pullDomain": "play.shangzhibo.tv",
            "isPushing": false,
            "createdAt": "2018-01-29T05:58:28.000Z",
            "updatedAt": "2018-01-29T11:09:35.000Z",
            "app": "r1g3-d43BM",
            "stream": "Hkb3WOE2BM?auth_key=1548741508-0-0-95d0d2627a7c91d28499ba89137dfb19",
            "isPrologueEnabled": true,
            "isEpilogueEnabled": true,
            "isBackupRecordEnabled": false,
            "isLiveEnabled": true,
            "fake": {
                "baseCount": 0,
                "increaseMin": 1,
                "increaseMax": 1
            },
            "isFakeEnabled": false,
            "isFilterAllEnabled": false,
            "filterIpList": {},
            "filterSidList": {},
            "filterUserList": {},
            "isRobotEnabled": false,
            "robot": {
                "initialCount": 10,
                "incrementCount": 1
            },
            "expired": false,
            "maxConcurrentUser": -1,
            "maxPushingTime": -1
        }
    ]
}
```



