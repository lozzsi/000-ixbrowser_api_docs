# 36 Delete Tag

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=8d8a902f-0117-425e-976b-ac8e47d21c58"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Delete Tag

Update Time：2025-04-30 00:27:01

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/tag-delete*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{"id": 182}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *id* | `182` | Yes | Integer | `Tag ID` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1676455329
  },
  "data": 0
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1676455329` | Integer |  |
| *data* | `0` | Integer |  |

#### Failed（200）

```json
{
  "error": {
    "code": 115002,
    "message": "Tag does not exist",
    "time": 1703941988
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `115002` | Integer | `Error Code（1000 1008 115xxx）` |
| *error.message* | `Tag does not exist` | String | `Error Description` |
| *error.time* | `1703941988` | Integer |  |
| *data* |  | Array |  |