# 31 Update Group

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=18652acf-bc87-4f96-aed1-969e5e2d2d43"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Group

Update Time：2024-09-09 00:22:07

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/group-update*
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
  "title": "测试分组123", // Group Name
  "id": 1835 // Group ID
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *title* | `name` | Yes | String | `Group Name` |
| *id* | `173` | Yes | Integer | `Group ID` |
| *sort* | `0` | No | Integer | `Sort` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1676455195
  },
  "data": 1
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1676455195` | Integer |  |
| *data* | `0` | Integer |  |

#### Failed（200）

```json
{
  "error": {
    "code": 106003, // Error Code（1000 1008 106xxx）
    "message": "Group does not exist", // Error Description
    "time": 1694592471
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `106003` | Integer | `Error Code（1000 1008 106xxx）` |
| *error.message* | `Group does not exist` | String | `Error Description` |
| *error.time* | `1694592471` | Integer |  |
| *data* |  | Array |  |