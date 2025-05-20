# 18 Update Profile Proxy Information - API Extraction

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=b0a5433e-90a2-44b4-b223-8b9ea72c713b"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Profile Proxy Information - API Extraction

Update Time: 2024-09-09 02:48:00

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-update-proxy-for-api-extraction*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String |  |

#### Body Example request

```json
{
  "profile_id": 161,
  "proxy_info": {
    "proxy_mode": 4, // API Extraction, specify proxy_mode=4
    "proxy_check_line": "global_line", // Proxy Detection Line Default:global_line proxy_mode is 2 or 4, effect when proxy_type is not direct
    "proxy_type": "socks5", // Proxy Type
    "proxy_service": "general", // Service provider general: general api
    "proxy_data_format_type": "txt", // Data format type Optional value: txt/json
    "proxy_data_txt_format": "ip:port", // TXT data format Default: ip:port For details, please refer to the enumeration variable appendix. It takes effect when the API extraction proxy data format type is txt.
    "proxy_data_json_format": {
      "ip": "ip", // Proxy IP mapping field Default: ip
      "port": "port", // Proxy Port mapping field Default: port
      "username": "username", // Proxy Username mapping field Default: username
      "password": "password" // Proxy Password mapping field Default: password
    }, // json data format mapping relationship
    "proxy_extraction_method": "invalid", // Extraction method invalid: extract a new IP when the IP is invalid every_type: extract a new IP every time the profile is opened
    "proxy_url": "" // Link extraction Required
  }
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `161` | Yes | Integer |  |
| *proxy_info* |  | Yes | Object |  |
| *proxy_info.proxy_mode* | `4` | Yes | Integer | `API Extraction, specify proxy_mode=4` |
| *proxy_info.proxy_check_line* | `global_line` | Yes | String | `Proxy Detection Line Default:global_line proxy_mode is 2 or 4, effect when proxy_type is not direct` |
| *proxy_info.proxy_type* | `socks5` | Yes | String | `Proxy Type` |
| *proxy_info.proxy_service* | `general` | Yes | String | `Service provider general: general api` |
| *proxy_info.proxy_data_format_type* | `txt` | Yes | String | `Data format type Optional value: txt/json` |
| *proxy_info.proxy_data_txt_format* | `ip:port` | No | String | `TXT data format Default: ip:port For details, please refer to the enumeration variable appendix. It takes effect when the API extraction proxy data format type is txt.` |
| *proxy_info.proxy_data_json_format* |  | No | Object | `json data format mapping relationship` |
| *proxy_info.proxy_data_json_format.ip* | `ip` | No | String | `Proxy IP mapping field Default: ip` |
| *proxy_info.proxy_data_json_format.port* | `port` | No | String | `Proxy Port mapping field Default: port` |
| *proxy_info.proxy_data_json_format.username* | `username` | No | String | `Proxy Username mapping field Default: username` |
| *proxy_info.proxy_data_json_format.password* | `password` | No | String | `Proxy Password mapping field Default: password` |
| *proxy_info.proxy_extraction_method* | `invalid` | Yes | String | `Extraction method invalid: extract a new IP when the IP is invalid every_type: extract a new IP every time the profile is opened` |
| *proxy_info.proxy_url* |  | Yes | String | `Link extraction Required` |

### Response example

#### Success (200)

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

#### Failed (200)

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2007` | Integer | `Error Code (1000 1008 2007 2009 2010)` |
| *error.message* | `Profile does not exist` | String | `Error Description` |
| *error.time* | `1694762291` | Integer |  |
| *data* |  | Array |  |