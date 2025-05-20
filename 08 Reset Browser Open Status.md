# 08 Reset Browser Open Status

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=6be0c221-8c8d-43cf-859b-8a3b2fb902ae"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Reset Browser Open Status

Update Time：2024-09-18 21:49:40

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-open-state-reset*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{"profile_id": 11971}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `1197` | Yes | Integer | `Profile serial number` |

### Response example

#### Success（200）

```json
{"error": {"code": 0,"message": "success"},"data": null}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *data* | `null` | Null |  |

#### Failed（200）

```json
{
  "error": {
    "code": 2007,
    "message": "Profile does not exist"
  },
  "data": null
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2007` | Integer | `Error Code（1000 1004 1008 2001）` |
| *error.message* | `Profile does not exist` | String | `Error Description` |
| *data* | `null` | Null |  |