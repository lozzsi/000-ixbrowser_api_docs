# 01 Get Profile List

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=e40f5b74-d87d-47f3-92d6-3e3f0c59947b"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get Profile List

Update Time: 2025-03-17 04:00:44

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-list*
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
  "profile_id": 0,  // Profile serial number
  "name": "",       // Profile Name
  "group_id": 0,    // Group ID
  "tag_id": 0,      // Tag ID
  "page": 1,        // Number of pages Default: 1
  "limit": 10       // Number of returns per page Default: 10
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `0` | No | Integer | `Profile serial number` |
| *name* |  | No | String | `Profile Name` |
| *group_id* | `0` | No | Integer | `Group ID` |
| *tag_id* | `0` | No | Integer | `Tag ID` |
| *page* | `1` | No | Integer | `Number of pages Default: 1` |
| *limit* | `10` | No | Integer | `Number of returns per page Default: 10` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1694943505
  },
  "data": {
    "total": 214,  // Quantity
    "data": [
      {
        "profile_id": 1267,  // Profile Serial Number
        "site_url": "chrome://newtab",  // Platform URL
        "name": "test",  // Profile Name
        "note": "",  // Notes
        "color": "#CC9966",  // Icon color of profile
        "username": "",  // Username
        "password": "",  // Password
        "last_open_time": 1733361693,  // Last Opened Time
        "group_id": 1,  // Group ID
        "group_name": "Default",  // Group name
        "tag_id": "",  // Tag ID
        "tag_name": "",  // Tag name
        "proxy_mode": 2,  // Proxy Method
        "proxy_id": 16881522,  // Proxy ID
        "proxy_type": "socks5",  // Proxy Type
        "proxy_ip": "",  // Proxy IP
        "proxy_port": "",  // Proxy Port
        "real_ip": "",  // Real IP
        "cache_path": "d6fe3f95eeab65617f025343bee057ef"  // Profile Cache Catalog
      },
      {
        "profile_id": 1266,  // Profile Serial Number
        "site_url": "chrome://newtab",  // Platform URL
        "name": "test",  // Profile Name
        "note": "",  // Notes
        "color": "#90EE90",  // Icon color of profile
        "username": "",  // Username
        "password": "",  // Password
        "last_open_time": 1733198288,  // Last Opened Time
        "group_id": 1,  // Group ID
        "group_name": "Default",  // Group name
        "tag_id": "",  // Tag ID
        "tag_name": "",  // Tag name
        "proxy_mode": 4,  // Proxy Method
        "proxy_type": "socks5",  // Proxy Type
        "real_ip": "",  // Real IP
        "proxy_url": "",
        "cache_path": "4c4a40904dfa2bbbc284b4e656a95ede"  // Profile Cache Catalog
      },
      {
        "profile_id": 1265,  // Profile Serial Number
        "site_url": "chrome://newtab",  // Platform URL
        "name": "test",  // Profile Name
        "note": "111111111111",  // Notes
        "color": "#FFD700",  // Icon color of profile
        "username": "",  // Username
        "password": "",  // Password
        "last_open_time": 1732938121,  // Last Opened Time
        "group_id": 137604,  // Group ID
        "group_name": "1111111",  // Group name
        "tag_id": "14152",  // Tag ID
        "tag_name": "test",  // Tag name
        "proxy_mode": 2,  // Proxy Method
        "proxy_type": "direct",  // Proxy Type
        "real_ip": "",  // Real IP
        "cache_path": "7b8e72e39d418ba878d2bd284c56dbc1"  // Profile Cache Catalog
      },
      {
        "profile_id": 1264,  // Profile Serial Number
        "site_url": "chrome://newtab",  // Platform URL
        "name": "test",  // Profile Name
        "note": "",  // Notes
        "color": "#C71585",  // Icon color of profile
        "username": "",  // Username
        "password": "",  // Password
        "last_open_time": 1733209698,  // Last Opened Time
        "group_id": 1,  // Group ID
        "group_name": "Default",  // Group name
        "tag_id": "",  // Tag ID
        "tag_name": "",  // Tag name
        "proxy_mode": 1,  // Proxy Method
        "proxy_id": 64,  // Proxy ID
        "real_ip": "",  // Real IP
        "cache_path": "a88b5a4e66f02d062ab7a48b7cd8c7df"  // Profile Cache Catalog
      },
      {
        "profile_id": 1263,  // Profile Serial Number
        "site_url": "chrome://newtab",  // Platform URL
        "name": "test",  // Profile Name
        "note": "",  // Notes
        "color": "#FFD700",  // Icon color of profile
        "username": "",  // Username
        "password": "",  // Password
        "last_open_time": 1733209696,  // Last Opened Time
        "group_id": 1,  // Group ID
        "group_name": "Default",  // Group name
        "tag_id": "",  // Tag ID
        "tag_name": "",  // Tag name
        "proxy_mode": 2,  // Proxy Method
        "proxy_type": "direct",  // Proxy Type
        "real_ip": "",  // Real IP
        "cache_path": "8582b39ab00538f2f034082518f9aad0"  // Profile Cache Catalog
      }
    ]  // Profile Information
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1694943505` | Integer |  |
| *data* |  | Object |  |
| *data.total* | `214` | Integer | `Quantity` |
| *data.data* |  | Array | `Profile Information` |
| *data.data.profile_id* | `1267` | Integer | `Profile Serial Number` |
| *data.data.site_url* | `chrome://newtab` | String | `Platform URL` |
| *data.data.name* | `test` | String | `Profile Name` |
| *data.data.note* |  | String | `Notes` |
| *data.data.color* | `#CC9966` | String | `Icon color of profile` |
| *data.data.username* |  | String | `Username` |
| *data.data.password* |  | String | `Password` |
| *data.data.last_open_time* | `1733361693` | Integer | `Last Opened Time` |
| *data.data.group_id* | `1` | Integer | `Group ID` |
| *data.data.group_name* | `Default` | String | `Group name` |
| *data.data.tag_id* |  | String | `Tag ID` |
| *data.data.tag_name* |  | String | `Tag name` |
| *data.data.proxy_mode* | `2` | Integer | `Proxy Method` |
| *data.data.proxy_id* | `16881522` | Integer | `Proxy ID` |
| *data.data.proxy_type* | `socks5` | String | `Proxy Type` |
| *data.data.proxy_ip* |  | String | `Proxy IP` |
| *data.data.proxy_port* |  | String | `Proxy Port` |
| *data.data.real_ip* |  | String | `Real IP` |
| *data.data.cache_path* |  | String | `Profile Cache Catalog` |

#### Failed (200)

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `1008` | Integer | `Error Code (1000 1004 1007 1008)` |
| *error.message* | `Your permissions are restricted` | String | `Error Description` |
| *error.time* | `1694489921` | Integer |  |
| *data* |  | Array |  |