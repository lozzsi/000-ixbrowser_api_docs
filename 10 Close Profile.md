# 10 Close Profile

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=9809c35a-b870-4c16-9aef-acaefa2256c8"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Close Profile

Update Time：2024-09-09 00:13:55

The closed profile must be the profile opened through the API, otherwise the process cannot be found when closing.

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-close*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{
  "profile_id": 1442 //Profile serial number
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `188` | Yes | Integer | `Profile serial number` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success"
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |

#### Failed（200）

```json
{
  "error": {
    "code": 1009, //Error Code（1000 1009）
    "message": "Process not found" //Error Description
  },
  "data": null
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `1009` | Integer | `Error Code（1000 1009）` |
| *error.message* | `Process not found` | String | `Error Description` |
| *data* | `null` | Null |  |