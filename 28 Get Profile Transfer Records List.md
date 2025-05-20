# 28 Get Profile Transfer Records List

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=dfb38fa3-3bad-459c-9571-4f2242e2c749"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get Profile Transfer Records List

Update Time：2024-09-09 00:20:56

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-transfer-record-list*
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
  "type": 2,  // Type 1:Transfer Records 2:Receive Records  Default：1
  "title": "", // Profile Name
  "page": 1,   // Number of pages Default: 1
  "limit": 10  // Number of returns per page Default: 10
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *type* | `2` | No | Integer | `Type 1:Transfer Records 2:Receive Records  Default：1` |
| *title* |  | No | String | `Profile Name` |
| *page* | `1` | No | Integer | `Number of pages Default: 1` |
| *limit* | `10` | No | Integer | `Number of returns per page Default: 10` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1699352194
  },
  "data": {
    "data": [
      {
        "id": 7,
        "transfer_code": "18895312-39361749",  // Transfer Code
        "transfer_proxy": 1,  // Transfer Proxy  0:Don't Transfer 1:Transfer
        "transfer_proxy_mode": 2,  // Option of Tranansfering Proxy 1:Proxy Sharing 2:Proxy Transfer
        "transfer_note": 1,  // Transfer Notes  0:Don't Transfer 1:Transfer
        "color": "#FF8C00",  // Profile Color
        "name": "asdfa111",  // Profile Name
        "note": "1111111111",  // Profile Notes
        "username": "li****5@126.com",  // Transfer User
        "reception_username": "35****8318@qq.com",  // Receive User
        "created_at": 1698607152,  // Transfer Time
        "receipt_time": 1698607183  // Receive Time
      },
      {
        "id": 6,
        "transfer_code": "62528043-51752649",  // Transfer Code
        "transfer_proxy": 1,  // Transfer Proxy  0:Don't Transfer 1:Transfer
        "transfer_proxy_mode": 2,  // Option of Tranansfering Proxy 1:Proxy Sharing 2:Proxy Transfer
        "transfer_note": 1,  // Transfer Notes  0:Don't Transfer 1:Transfer
        "color": "#CC9966",  // Profile Color
        "name": "name1",  // Profile Name
        "note": "",  // Profile Notes
        "username": "li****5@126.com",  // Transfer User
        "reception_username": "35****8318@qq.com",  // Receive User
        "created_at": 1698605594,  // Transfer Time
        "receipt_time": 1698605627  // Receive Time
      }
    ],
    "total": 2
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1699352194` | Integer |  |
| *data* |  | Object |  |
| *data.data* |  | Array |  |
| *data.data.id* | `7` | Integer |  |
| *data.data.transfer_code* | `18895312-39361749` | String | `Transfer Code` |
| *data.data.transfer_proxy* | `1` | Integer | `Transfer Proxy  0:Don't Transfer 1:Transfer` |
| *data.data.transfer_proxy_mode* | `2` | Integer | `Option of Tranansfering Proxy 1:Proxy Sharing 2:Proxy Transfer` |
| *data.data.transfer_note* | `1` | Integer | `Transfer Notes  0:Don't Transfer 1:Transfer` |
| *data.data.color* | `#FF8C00` | String | `Profile Color` |
| *data.data.name* | `asdfa111` | String | `Profile Name` |
| *data.data.note* | `1111111111` | String | `Profile Notes` |
| *data.data.username* | `li****5@126.com` | String | `Transfer User` |
| *data.data.reception_username* | `35****8318@qq.com` | String | `Receive User` |
| *data.data.created_at* | `1698607152` | Integer | `Transfer Time` |
| *data.data.receipt_time* | `1698607183` | Integer | `Receive Time` |
| *data.total* | `2` | Integer |  |