# 44 Update Proxy Tag

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=4f78271f-9902-4781-ae10-23efcd02356b"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Proxy Tag

Update Time：2025-04-29 21:45:29

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/proxy-tag-update*
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
  "title": "test", // Tag Name
  "id": 14 // Tag ID
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *title* | `name` | Yes | String | `Tag Name` |
| *id* | `173` | Yes | Integer | `Tag ID` |

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
    "code": 120003, // Error Code（1000 1008 120xxx）
    "message": "Tag does not exist", // Error Description
    "time": 1694592471
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `120003` | Integer | `Error Code（1000 1008 120xxx）` |
| *error.message* | `Tag does not exist` | String | `Error Description` |
| *error.time* | `1694592471` | Integer |  |
| *data* |  | Array |  |