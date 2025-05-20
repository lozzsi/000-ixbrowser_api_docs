# 05 Get Opened Profile

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=53d03e34-497c-4e9c-8144-083dff16f7d2"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get Opened Profile

Update Time: 2024-09-19 00:22:51

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-opened-list*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| Parameter name | Example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

*(No content provided in the original document)*

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1725863281
  },
  "data": [
    {
      "profile_id": 1196, //Profile Serial Number
      "last_opened_user": "test@qq.com", //Last Opened User
      "last_opened_time": "2024-09-09 14:27:56" //Last Opened Time
    },
    {
      "profile_id": 1197, //Profile Serial Number
      "last_opened_user": "test@qq.com", //Last Opened User
      "last_opened_time": "2024-09-09 14:27:56" //Last Opened Time
    }
  ]
}
```

| Parameter name | Example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1725863281` | Integer |  |
| *data* |  | Array |  |
| *data.profile_id* | `1196` | Integer | `Profile Serial Number` |
| *data.last_opened_user* | `350248318@qq.com` | String | `Last Opened User` |
| *data.last_opened_time* | `2024-09-09 14:27:56` | String | `Last Opened Time` |