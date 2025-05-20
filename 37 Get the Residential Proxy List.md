# 37 Get the Residential Proxy List

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=ef250223-4e16-49c3-8ade-330b4f43fbb7"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get the Residential Proxy List

Update Time：2024-09-09 00:23:59

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/traffic-package-list*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | ```application/json``` | Yes | String | ```application/json``` |

#### Body Example request

```json
{
  "page": 1, // Number of pages Default: 1
  "limit": 10 // Number of returns per page Default: 10
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *page* | ```1``` | No | Integer | ```Number of pages Default: 1``` |
| *limit* | ```10``` | No | Integer | ```Number of returns per page Default: 10``` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1694943843
  },
  "data": {
    "total": 1, // Quantity
    "data": [
      {
        "id": 6, // Residential Proxy ID
        "limit_flow": "1024.00", // Total Traffic (M)
        "used_flow": "11.65", // Traffic Used（M）
        "supply_name": "Cost-effective traffic provider" // Supplier
      }
    ] // Residential Proxy Information
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```0``` | Integer |  |
| *error.message* | ```success``` | String |  |
| *error.time* | ```1694943843``` | Integer |  |
| *data* |  | Object |  |
| *data.total* | ```1``` | Integer | ```Quantity``` |
| *data.data* |  | Array | ```Residential Proxy Information``` |
| *data.data.id* | ```6``` | Integer | ```Residential Proxy ID``` |
| *data.data.limit\_flow* | ```1024.00``` | String | ```Total Traffic (M)``` |
| *data.data.used\_flow* | ```11.65``` | String | ```Traffic Used（M）``` |
| *data.data.supply\_name* | ```Cost-effective traffic provider``` | String | ```Supplier``` |

#### Failed（200）

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```1008``` | Integer | ```Error Code（1007 1008）``` |
| *error.message* | ```Your permissions are restricted``` | String | ```Error Description``` |
| *error.time* | ```1694592896``` | Integer |  |
| *data* |  | Array |  |