# 41 Delete Custom Proxy

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=eecba46a-c03a-417b-97a8-80aaeea3bfb1"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Delete Custom Proxy

Update Time：2024-09-09 00:25:10

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/proxy-delete*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String |  |

#### Body Example request

```json
{
  "id": 2444 //Proxy ID
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *id* | `24330` | Yes | Integer | `Proxy ID` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1693464615
  },
  "data": 1
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1693464615` | Integer |  |
| *data* | `1` | Integer |  |

#### Failed（200）

```json
{
  "error": {
    "code": 2002, //Error Code（1000 1008 108xxx）
    "message": "Proxy information does not exist", //Error Description
    "time": 1694599218
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2002` | Integer | `Error Code（1000 1008 108xxx）` |
| *error.message* | `Proxy information does not exist` | String | `Error Description` |
| *error.time* | `1694599218` | Integer |  |
| *data* |  | Array |  |