# 27 Import Profile via Transfer Code

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=bcc57ade-9e76-486d-a1f3-cea9537417bc"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Import Profile via Transfer Code

Update Time: 2024-09-09 00:20:42

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-transfer-code-import*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{
  "transfer_code": "76686828-89727101", // Transfer Code
  "group_id": 1, // The group ID assigned to the profile. If the ID is not uploaded, the profile will be assigned to the default group
  "proxy_config": {
    "proxy_mode": 2, // Proxy Method. For details, please refer to the enumeration variable appendix
    "proxy_id": "", // Proxy ID. Required when proxy_mode is not 2
    "proxy_type": "direct", // Proxy Type. For details, please refer to the enumeration variable appendix
    "proxy_ip": "", // Proxy IP. Required when proxy_mode is 2, and the proxy_type is not in direct mode
    "proxy_port": "", // Proxy Port. Required when proxy_mode is 2, and the proxy_type is not in direct mode
    "proxy_user": "", // Proxy Account
    "proxy_password": "", // Proxy Password
    "traffic_package_ip_policy": false, // IP Policy false:Keep the IP unchanged (5~60 minutes) true:Get a new IP when everytime open the profile It takes effect when proxy_mode is 1
    "enable_bypass": "0", // Bypass List 0:Close 1:Open
    "bypass_list": "*.example1.com\nwww.example2.com" // The domains that do not go through the proxy, separate by newlines
  } // Proxy Information Configuration
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *transfer_code* | `76686828-89727101` | Yes | String | `Transfer Code` |
| *group_id* | `1` | No | Integer | `The group ID assigned to the profile. If the ID is not uploaded, the profile will be assigned to the default group` |
| *proxy_config* |  | No | Object | `Proxy Information Configuration` |
| *proxy_config.proxy_mode* | `2` | No | Integer | `Proxy Method. For details, please refer to the enumeration variable appendix` |
| *proxy_config.proxy_id* |  | No | String | `Proxy ID. Required when proxy_mode is not 2` |
| *proxy_config.proxy_type* | `direct` | No | String | `Proxy Type. For details, please refer to the enumeration variable appendix` |
| *proxy_config.proxy_ip* |  | No | String | `Proxy IP. Required when proxy_mode is 2, and the proxy_type is not in direct mode` |
| *proxy_config.proxy_port* |  | No | String | `Proxy Port. Required when proxy_mode is 2, and the proxy_type is not in direct mode` |
| *proxy_config.proxy_user* |  | No | String | `Proxy Account` |
| *proxy_config.proxy_password* |  | No | String | `Proxy Password` |
| *proxy_config.traffic_package_ip_policy* | `false` | No | Boolean | `IP Policy false:Keep the IP unchanged (5~60 minutes) true:Get a new IP when everytime open the profile It takes effect when proxy_mode is 1` |
| *proxy_config.enable_bypass* | `0` | Yes | String | `Bypass List 0:Close 1:Open` |
| *proxy_config.bypass_list* | `*.example1.com\nwww.example2.com` | Yes | String | `The domains that do not go through the proxy, separate by newlines` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1697184642
  },
  "data": {
    "profile_id": 1 // Profile serial number
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1697184642` | Integer |  |
| *data* |  | Object |  |
| *data.profile_id* | `1` | Integer | `Profile serial number` |

#### Failed (404)

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `110002` | Integer | `Error Code (1000 1004 1007 1008 1011 1014 110xxx)` |
| *error.message* | `The transfer code is wrong` | String | `Error Description` |
| *error.time* | `1697184375` | Integer |  |
| *data* |  | Array |  |