# 25 Create Profile Transfer Code

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=936ec18e-1ce7-4433-8d19-e72b894c0791"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Create Profile Transfer Code

Update Time：2024-09-09 00:20:03

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-transfer-code-create*
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
  "profile_id": 1441, // Profile serial number
  "transfer_proxy": 1, // Transfer Proxy  0:Don't Transfer 1:Transfer  Default:0  (The proxy does not take effect when it is in traffic packet or direct connection mode)
  "transfer_proxy_mode": 1, // Options of Transfering Proxy 1:Proxy Sharing 2:Proxy Transfer  Default:1 (It takes effect when transferring proxy and the proxy bound with the profile is a purchased proxy)
  "transfer_note": 1, // Transfer Notes  0:Don't Transfer 1:Transfer  Default:0
  "password": "123456" // Login Password
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | ```1441``` | Yes | Integer | ```Profile serial number``` |
| *transfer_proxy* | ```1``` | No | Integer | ```Transfer Proxy  0:Don't Transfer 1:Transfer  Default:0  (The proxy does not take effect when it is in traffic packet or direct connection mode)``` |
| *transfer_proxy_mode* | ```1``` | No | Integer | ```Options of Transfering Proxy 1:Proxy Sharing 2:Proxy Transfer  Default:1 (It takes effect when transferring proxy and the proxy bound with the profile is a purchased proxy)``` |
| *transfer_note* | ```1``` | No | Integer | ```Transfer Notes  0:Don't Transfer 1:Transfer  Default:0``` |
| *password* | ```123456``` | Yes | String | ```Login Password``` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1697183482
  },
  "data": {
    "transfer_code": "43186757-63164567" // Transfer Code
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```0``` | Integer |  |
| *error.message* | ```success``` | String |  |
| *error.time* | ```1697183482``` | Integer |  |
| *data* |  | Object |  |
| *data.transfer_code* | ```43186757-63164567``` | String | ```Transfer Code``` |

#### Failed（200）

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```1013``` | Integer | ```Error Code (1000 1004 1007 1008 1011 1012 1013 1014 2001 109xxx)``` |
| *error.message* | ```Wrong Password``` | String | ```Error Description``` |
| *error.time* | ```1697183584``` | Integer |  |
| *data* |  | Array |  |