# 15 Update Profile Proxy Information - Purchased Residential Proxy

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=7bee7d1f-a72f-4aae-9485-86fd4baf0e7e"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Profile Proxy Information - Purchased Residential Proxy

Update Time：2024-09-09 00:15:23

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-update-proxy-for-purchased-traffic-package*
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
  "profile_id": 1575,
  "proxy_info": {
    "proxy_mode": 1, //Purchased Residential Proxy Specify proxy_mode=1
    "proxy_id": 6, //Residential Proxy ID
    "country": "us", //Country For details, please refer to the Country Appendix
    "city": "Ada", //City Can be queried in ixBrowser modification profilr-proxy configuration
    "gateway": "Default" //Residential Proxy default node. For details, please refer to the Enumeration Variable Appendix.
  }
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile\_id* | `1559` | Yes | Integer |  |
| *proxy\_info* |  | Yes | Object |  |
| *proxy\_info.proxy\_mode* | `1` | Yes | Integer | `Purchased Residential Proxy Specify proxy_mode=1` |
| *proxy\_info.proxy\_id* | `6` | Yes | Integer | `Residential Proxy ID` |
| *proxy\_info.country* |  | No | String | `Country For details, please refer to the Country Appendix` |
| *proxy\_info.city* |  | No | String | `City Can be queried in ixBrowser modification profilr-proxy configuration` |
| *proxy\_info.gateway* | `Default` | Yes | String | `Residential Proxy default node. For details, please refer to the Enumeration Variable Appendix.` |

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
| *error.code* | `2003` | Integer | `Error Code（1000 1008 2003 2007 2009 2010）` |
| *error.message* | `Residential Proxy does not exist` | String | `Error Description` |
| *error.time* | `1694587875` | Integer |  |
| *data* |  | Array |  |