# 24 Empty Recycle Bin

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=0c100e0a-c324-46ba-86a7-108c66fdfbb7"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Empty Recycle Bin

Update Time：2024-09-09 00:19:45

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/empty-recycle-bin*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *page* | `1` | No | Integer | `Number of pages Default: 1` |
| *limit* | `10` | No | Integer | `Number of returns per page Default: 10` |
| *group_id* | `0` | No | Integer | `Group ID` |
| *tag_id* | `0` | Yes | Integer | `Tag ID` |
| *name* |  | No | String | `Profile Name` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1714037494
  },
  "data": 5
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1714037494` | Integer |  |
| *data* | `5` | Integer |  |

#### Failed（200）

```json
{
  "error": {
    "code": 117001, //Error Code (1004 1007 1008 117001)
    "message": "Failed to empty recycle bin", //Error Description
    "time": 1714033795
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `117001` | Integer | `Error Code (1004 1007 1008 117001)` |
| *error.message* | `Failed to empty recycle bin` | String | `Error Description` |
| *error.time* | `1714033795` | Integer |  |
| *data* |  | Array |  |