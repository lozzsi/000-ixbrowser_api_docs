# 19 Random Fingerprint Configuration

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=27c333ef-687b-41e7-92d5-f5a6100b4dcb"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Random Fingerprint Configuration

Update Time：2024-09-09 00:17:32

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-random-fingerprint-configuration*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Body Example request

```json
{
  "profile_id": 1442  //Profile serial number
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile\_id* | `1442` | Yes | Integer | `Profile serial number` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1694503767
  },
  "data": "success"
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1694503767` | Integer |  |
| *data* | `success` | String |  |

#### Failed（200）

```json
{
  "error": {
    "code": 1008,  //Error Code（1000 1008 1011 2007）
    "message": "Your permissions are restricted",  //Error Description
    "time": 1694503735
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `1008` | Integer | `Error Code（1000 1008 1011 2007）` |
| *error.message* | `Your permissions are restricted` | String | `Error Description` |
| *error.time* | `1694503735` | Integer |  |
| *data* |  | Array |  |