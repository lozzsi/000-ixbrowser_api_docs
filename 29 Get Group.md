# 29 Get Group

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=1be85610-dbff-4abe-899e-622f7bbbb80e"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get Group

Update Time: 2024-09-09 00:21:27

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/group-list*
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
  "page": 1, // Number of pages Default: 1
  "limit": 10, // Number of returns per page Default: 10
  "title": "" // Group Name
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *page* | `1` | No | Integer | `Number of pages Default: 1` |
| *limit* | `10` | No | Integer | `Number of returns per page Default: 10` |
| *title* |  | No | String | `Group Name` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1676454936
  },
  "data": {
    "total": 1, // Quantity
    "data": [
      {
        "title": "Facebook1", // Group Name
        "id": 169 // Group ID
      }
    ] // Group Information
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1676454936` | Integer |  |
| *data* |  | Object |  |
| *data.total* | `1` | Integer | `Quantity` |
| *data.data* |  | Array | `Group Information` |
| *data.data.title* | `Facebook1` | String | `Group Name` |
| *data.data.id* | `169` | Integer | `Group ID` |