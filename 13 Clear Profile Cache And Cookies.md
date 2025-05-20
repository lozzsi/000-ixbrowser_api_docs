# 13 Clear Profile Cache And Cookies

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=e1495839-d026-49e2-9c16-05bca67988f7"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Clear Profile Cache And Cookies

Update Time: 2025-01-03 01:27:39

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-clear-cache-and-cookies*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| Parameter name | Example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{
  "profile_id": [1456, 1457] //Profile serial number
}
```

| Parameter name | Example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `161` | Yes | Array | `Profile serial number` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success"
  },
  "data": [1456, 1457] //Profile serial number that successfully cleared cache
}
```

| Parameter name | Example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *data* | `1456` | Array | `Profile serial number that successfully cleared cache` |

#### Failed (200)

```json
{
  "error": {
    "code": 2007, //Error Code (1000 1004 1008 2007)
    "message": "Profile does not exist" //Error Description
  },
  "data": null
}
```

| Parameter name | Example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2007` | Integer | `Error Code (1000 1004 1008 2007)` |
| *error.message* | `Profile does not exist` | String | `Error Description` |
| *data* | `null` | Null |  |