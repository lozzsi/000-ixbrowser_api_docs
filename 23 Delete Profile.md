# 23 Delete Profile

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=224d3325-7605-4176-bc74-a0693bfd66a1"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Delete Profile

Update Time: 2024-09-09 00:19:22

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-delete*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | ```application/json``` | Yes | String | ```application/json``` |

#### Body Example request

```json
{
  "profile_id": 161  //Profile serial number
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | ```161``` | Yes | Integer | ```Profile serial number``` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1676454333
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```0``` | Integer |  |
| *error.message* | ```success``` | String |  |
| *error.time* | ```1676454333``` | Integer |  |
| *data* |  | Array |  |

#### Failed (200)

```json
{
  "error": {
    "code": 2007,  //Error Code (1000 1004 1008 2001)
    "message": "Profile does not exist"  //Error Description
  },
  "data": null
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```2007``` | Integer | ```Error Code (1000 1004 1008 2001)``` |
| *error.message* | ```Profile does not exist``` | String | ```Error Description``` |
| *data* | ```null``` | Null |  |