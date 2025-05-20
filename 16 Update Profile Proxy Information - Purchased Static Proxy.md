# 16 Update Profile Proxy Information - Purchased Static Proxy

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=1c509e5b-4e19-4438-ad2c-de3535492d43"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Profile Proxy Information - Purchased Static Proxy

Update Time：2024-09-09 00:15:44

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-update-proxy-to-purchased-mode*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Body Example request

```json
{
  "profile_id": 161,
  "proxy_info": {
    "proxy_mode": 3, //Purchased proxy, specify proxy_mode=3
    "proxy_id": 1 //Proxy ID
  }
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile\_id* | ``` 161 ``` | Yes | Integer |  |
| *proxy\_info* |  | Yes | Object |  |
| *proxy\_info.proxy\_mode* | ``` 3 ``` | Yes | Integer | ``` Purchased proxy, specify proxy_mode=3 ``` |
| *proxy\_info.proxy\_id* | ``` 1 ``` | Yes | Integer | ``` Proxy ID ``` |

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
| *error.code* | ``` 0 ``` | Integer |  |
| *error.message* | ``` success ``` | String |  |
| *error.time* | ``` 1691131803 ``` | Integer |  |
| *data* | ``` success ``` | String |  |

#### Failed（200）

```json
{
  "error": {
    "code": 2002, //Error Code（1000 1008 2002 2007 2009 2010）
    "message": "Proxy information does not exist", //Error Description
    "time": 1694587942
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ``` 2002 ``` | Integer | ``` Error Code（1000 1008 2002 2007 2009 2010） ``` |
| *error.message* | ``` Proxy information does not exist ``` | String | ``` Error Description ``` |
| *error.time* | ``` 1694587942 ``` | Integer |  |
| *data* |  | Array |  |