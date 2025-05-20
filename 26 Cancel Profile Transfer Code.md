# 26 Cancel Profile Transfer Code

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=56ce5439-23ea-4f3e-b6eb-1418e95540fe"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Cancel Profile Transfer Code

Update Time: 2024-09-09 00:20:23

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-transfer-cancel*
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
  "profile_id": 1606 //Profile serial number
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `1606` | Yes | Integer | `Profile serial number` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1697518178
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1697518178` | Integer |  |
| *data* |  | Array |  |

#### Failed (200)

```json
{
  "error": {
    "code": 1008, //Error Code (1000 1004 1007 1008 1011 1012 1013 1014 2001 109xxx)
    "message": "Your permissions are restricted", //Error Description
    "time": 1697518246
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `1008` | Integer | `Error Code (1000 1004 1007 1008 1011 1012 1013 1014 2001 109xxx)` |
| *error.message* | `Your permissions are restricted` | String | `Error Description` |
| *error.time* | `1697518246` | Integer |  |
| *data* |  | Array |  |