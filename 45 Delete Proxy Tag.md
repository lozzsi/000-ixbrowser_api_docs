# 45 Delete Proxy Tag

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=be733487-5472-42ad-8970-540902357476"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Delete Proxy Tag

Update Time：2025-04-29 21:46:37

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/proxy-tag-delete*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{"id": 182} //Tag ID
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
    "code": 121002, //Error Code（1000 1008 121xxx）
    "message": "Tag does not exist", //Error Description
    "time": 1703941988
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `121002` | Integer | `Error Code（1000 1008 121xxx）` |
| *error.message* | `Tag does not exist` | String | `Error Description` |
| *error.time* | `1703941988` | Integer |  |
| *data* |  | Array |  |