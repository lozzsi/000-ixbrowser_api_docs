# 39 Create Custom Proxy

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=0586d3a8-d747-4651-b0da-d6bedd99e59f"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Create Custom Proxy

Update Time：2025-04-29 21:32:45

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/proxy-create*
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
  "proxy_type": "socks5",    // Proxy type http/https/scoks5/ssh
  "proxy_ip": "127.0.0.1",   // Proxy IP
  "proxy_port": "57425",     // Proxy Port
  "proxy_user": "",          // Proxy Account
  "proxy_password": "",      // Proxy Password
  "tag": "",                 // Tag name (If there are multiple tags, please send in array format)
  "note": ""                 // Proxy Notes
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *proxy_type* | `socks5` | Yes | String | `Proxy type http/https/scoks5/ssh` |
| *proxy_ip* | `127.0.0.1` | Yes | String | `Proxy IP` |
| *proxy_port* | `57425` | Yes | String | `Proxy Port` |
| *proxy_user* |  | Yes | String | `Proxy Account` |
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
    "time": 1694597422
  },
  "data": 24441  // Proxy ID
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1694597422` | Integer |  |
| *data* | `24441` | Integer | `Proxy ID` |

#### Failed（200）

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `103005` | Integer | `Error Code（1000 1004 1007 1008 1011 103xxx ）` |
| *error.message* | `Failed to add proxy, the proxy already exists` | String | `Error Description` |
| *error.time* | `1694597826` | Integer |  |
| *data* |  | Array |  |