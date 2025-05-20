# 40 Update Custom Proxy

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=ae7ed992-c55b-477d-8663-6e8f63ddf723"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Custom Proxy

Update Time：2025-04-29 21:31:52

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/proxy-update*
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
  "id": 24330, // Proxy ID
  "proxy_type": "socks5", // Proxy type http/https/scoks5/ssh
  "proxy_ip": "127.0.0.2", // Proxy IP
  "proxy_port": "57425", // Proxy Port
  "proxy_user": "", // Proxy Account
  "proxy_password": "", // Proxy Password
  "tag": "", // Tag name (If there are multiple tags, please send in array format)
  "note": "" // Proxy Notes
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *id* | `24330` | Yes | Integer | `Proxy ID` |
| *proxy_type* | `socks5` | No | String | `Proxy type http/https/scoks5/ssh` |
| *proxy_ip* | `127.0.0.2` | No | String | `Proxy IP` |
| *proxy_port* | `57425` | No | String | `Proxy Port` |
| *proxy_user* |  | No | String | `Proxy Account` |
| *proxy_password* |  | No | String | `Proxy Password` |
| *tag* |  | No | String | `Tag name (If there are multiple tags, please send in array format)` |
| *note* |  | No | String | `Proxy Notes` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1693464163
  },
  "data": 1
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1693464163` | Integer |  |
| *data* | `1` | Integer |  |

#### Failed（200）

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2002` | Integer | `Error Code（1000 1004 1008 1011 2002 104xxx）` |
| *error.message* | `Proxy information does not exist` | String | `Error Description` |
| *error.time* | `1694598121` | Integer |  |
| *data* |  | Array |  |