# 47 Switch Access Gateway

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=9c033221-2e96-4d85-86b7-4a3e013122b0"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Switch Access Gateway

Update Time：2024-09-18 21:51:11

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/gateway-switch*
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
  "id": "1" //Gateway ID: obtained by getting the gateway list
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *id* | `1` | Yes | String | `Gateway ID: obtained by getting the gateway list` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success"
  },
  "data": null
}
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
    "code": 118002, //Error Code（1000 118001 118002）
    "message": "gateway does not exist" //Error Description
  },
  "data": null
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `118002` | Integer | `Error Code（1000 118001 118002）` |
| *error.message* | `gateway does not exist` | String | `Error Description` |
| *data* | `null` | Null |  |