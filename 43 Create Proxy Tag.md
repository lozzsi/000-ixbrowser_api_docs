# 43 Create Proxy Tag

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=5fcb1874-4afb-4af4-becc-e275ce282371"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Create Proxy Tag

Update Time：2025-04-29 21:36:58

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/proxy-tag-create*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{"title": "name"}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *title* | `name` | Yes | String | `Tag Name` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1694592419
  },
  "data": 185
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1694592419` | Integer |  |
| *data* | `185` | Integer | `Tag ID` |

#### Failed（200）

```json
{
  "error": {
    "code": 119001,
    "message": "Tag name cannot be empty",
    "time": 1703941765
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `119001` | Integer | `Error Code（1000 1007 1008 119xxx）` |
| *error.message* | `Tag name already exists` | String | `Error Description` |
| *error.time* | `1703941765` | Integer |  |
| *data* |  | Array |  |