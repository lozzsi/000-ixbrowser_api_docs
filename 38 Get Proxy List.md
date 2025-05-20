# Get Proxy List

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=ae7b60e2-3bdc-4631-809a-d678eae82343"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get Proxy List

Update Time：2025-04-29 21:30:49

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/proxy-list*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{
  "page": 1, // Number of pages Default: 1
  "limit": 10, // Number of returns per page Default: 10
  "type": 2, // Proxy type 0: All 1: Custom agent 2: Purchased proxy Default: 0
  "proxy_ip": "", // Proxy IP
  "tag_id": 0 // Proxy Tag ID
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *page* | `1` | No | Integer | `Number of pages Default: 1` |
| *limit* | `10` | No | Integer | `Number of returns per page Default: 10` |
| *type* | `1` | No | Integer | `Proxy type 0: All 1: Custom agent 2: Purchased proxy Default: 0` |
| *proxy\_ip* |  | No | String | `Proxy IP` |
| *tag\_id* |  | No | Integer | `Proxy Tag ID` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1693399093
  },
  "data": {
    "total": 1, // Quantity
    "data": [
      {
        "id": 24320, // Proxy IP
        "proxy_type": "ssh", // Proxy Type
        "proxy_ip": "127.0.0.1", // Proxy IP
        "proxy_port": "22", // Proxy Port
        "proxy_user": "", // Proxy Account
        "proxy_password": "", // Proxy Password
        "note": "", // Notes
        "type": 1, // 1: Custom Proxy 2: Purchased Proxy
        "tag_id": "117 118", // Tag ID
        "tag_name": "tag1 tag2",
        "query": "", // IP
        "country": "", // Country
        "timezone": "", // Time Zone
        "city": "", // City
        "activeWindow": 2 // Active Profile
      }
    ] // Proxy Information
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1693399093` | Integer |  |
| *data* |  | Object |  |
| *data.total* | `1` | Integer | `Quantity` |
| *data.data* |  | Array | `Proxy Information` |
| *data.data.id* | `24320` | Integer | `Proxy IP` |
| *data.data.proxy\_type* | `ssh` | String | `Proxy Type` |
| *data.data.proxy\_ip* | `127.0.0.1` | String | `Proxy IP` |
| *data.data.proxy\_port* | `22` | String | `Proxy Port` |
| *data.data.proxy\_user* |  | String | `Proxy Account` |
| *data.data.proxy\_password* |  | String | `Proxy Password` |
| *data.data.note* |  | String | `Notes` |
| *data.data.type* | `1` | Integer | `1: Custom Proxy 2: Purchased Proxy` |
| *data.data.tag\_id* | `1 45 146` | String | `Tag ID` |
| *data.data.query* |  | String | `IP` |
| *data.data.country* |  | String | `Country` |
| *data.data.timezone* |  | String | `Time Zone` |
| *data.data.city* |  | String | `City` |
| *data.data.activeWindow* | `2` | Integer | `Active Profile` |