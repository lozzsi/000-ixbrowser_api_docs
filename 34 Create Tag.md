# 34 Create Tag

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=c0d1be5e-efd0-4a1e-ab8f-2d570f9a0175"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Create Tag

Update Time: 2024-09-09 00:22:58

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/tag-create*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{
  "title": "name" // Tag Name
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *title* | `name` | Yes | String | `Tag Name` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1694592419
  },
  "data": 185 // Tag ID
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1694592419` | Integer |  |
| *data* | `185` | Integer | `Tag ID` |

#### Failed (200)

```json
{
  "error": {
    "code": 113002, // Error Code (1000 1008 113xxx)
    "message": "标签名称已经存在", // Error Description
    "time": 1703941765
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `113002` | Integer | `Error Code (1000 1008 113xxx)` |
| *error.message* | `Tag name already exists` | String | `Error Description` |
| *error.time* | `1703941765` | Integer |  |
| *data* |  | Array |  |