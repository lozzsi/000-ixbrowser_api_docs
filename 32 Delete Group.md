# 32 Delete Group

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=10eb43c7-03a2-4cd6-90d9-3de30ade8473"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Delete Group

Update Time：2024-09-09 00:22:22

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/group-delete*
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
  "id": 182 //Group ID
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *id* | `173` | Yes | Integer | `Group ID` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1676455329
  },
  "data": 0
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1676455329` | Integer |  |
| *data* | `0` | Integer |  |

#### Failed（200）

```json
{
  "error": {
    "code": 107002, //Error Code（1000 1008 107xxx）
    "message": "Group does not exist", //Error Description
    "time": 1693982688
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `107002` | Integer | `Error Code（1000 1008 107xxx）` |
| *error.message* | `Group does not exist` | String | `Error Description` |
| *error.time* | `1693982688` | Integer |  |
| *data* |  | Array |  |