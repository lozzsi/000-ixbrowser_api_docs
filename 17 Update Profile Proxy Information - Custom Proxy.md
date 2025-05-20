# 17 Update Profile Proxy Information - Custom Proxy

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=2f75e82f-536c-4456-93ba-d893b85ec711"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Profile Proxy Information - Custom Proxy

Update Time：2024-09-09 00:16:01

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-update-proxy-for-custom-proxy*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Body Example request

```json
{
  "profile_id": 161,
  "proxy_info": {
    "proxy_mode": 2, //Custom proxy, specify proxy_mode=2
    "proxy_check_line": "global_line", //Proxy Detection Line Default:global_line proxy_mode is 2 or 4, effect when proxy_type is not direct
    "proxy_type": "socks5", //Proxy Type  direct/socks5/http/ssh
    "proxy_ip": "127.0.0.1", //Proxy IP   Required when proxy_type is not direct
    "proxy_port": "51095", //Proxy Port   Required when proxy_type is not direct
    "proxy_user": "", //Proxy Account
    "proxy_password": "" //Proxy Password
  }
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile\_id* | `161` | Yes | Integer |  |
| *proxy\_info* |  | Yes | Object |  |
| *proxy\_info.proxy\_mode* | `2` | Yes | Integer | `Custom proxy, specify proxy_mode=2` |
| *proxy\_info.proxy\_check\_line* | `global_line` | No | String | `Proxy Detection Line Default:global_line proxy_mode is 2 or 4, effect when proxy_type is not direct` |
| *proxy\_info.proxy\_type* | `socks5` | Yes | String | `Proxy Type  direct/socks5/http/ssh` |
| *proxy\_info.proxy\_ip* | `127.0.0.1` | No | String | `Proxy IP   Required when proxy_type is not direct` |
| *proxy\_info.proxy\_port* | `51095` | No | String | `Proxy Port   Required when proxy_type is not direct` |
| *proxy\_info.proxy\_user* |  | No | String | `Proxy Account` |
| *proxy\_info.proxy\_password* |  | No | String | `Proxy Password` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1691131803
  },
  "data": "success"
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1691131803` | Integer |  |
| *data* | `success` | String |  |

#### Failed（200）

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2007` | Integer | `Error Code（1000 1008 2007 2009 2010）` |
| *error.message* | `Profile does not exist` | String | `Error Description` |
| *error.time* | `1694762291` | Integer |  |
| *data* |  | Array |  |