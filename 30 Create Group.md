# 30 Create Group

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=75ed3dd1-5546-4e20-9119-d8b85a20c8e0"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Create Group

Update Time: 2024-09-09 00:21:47

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/group-create*
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
  "title": "name", // Group Name
  "sort": 0 // Sort
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *title* | ```name``` | Yes | String | ```Group Name``` |
| *sort* | ```0``` | Yes | Integer | ```Sort``` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1694592419
  },
  "data": 185 // Group ID
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```0``` | Integer |  |
| *error.message* | ```success``` | String |  |
| *error.time* | ```1694592419``` | Integer |  |
| *data* | ```185``` | Integer | ```Group ID``` |

#### Failed (200)

```json
{
  "error": {
    "code": 105003, // Error Code (1000 1008 105xxx)
    "message": "Group sorting cannot be empty", // Error Description
    "time": 1694592123
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```105003``` | Integer | ```Error Code (1000 1008 105xxx)``` |
| *error.message* | ```Group sorting cannot be empty``` | String | ```Error Description``` |
| *error.time* | ```1694592123``` | Integer |  |
| *data* |  | Array |  |