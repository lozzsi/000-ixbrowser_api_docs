# 03 Copy Profile

---
title: "Copy Profile"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=680ec06c-e19a-4b8f-bf45-3da4c70bee9d"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Copy Profile

Update Time: 2024-09-09 00:12:01

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-copy*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Body Example request

```json
{
  "profile_id": 1640,  // Profile serial number
  "site_id": 11,       // Platform ID. For details, please refer to the Enumeration Variable Appendix
  "site_url": "http://baidu.com/",  // Specify the platform URL. Required when site_id is 21
  "name": "new_name",  // Profile Name
  "group_id": 177      // Group ID. The default group ID is 1
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile\_id* | `1640` | Yes | Integer | `Profile serial number` |
| *site\_id* | `11` | No | Integer | `Platform ID. For details, please refer to the Enumeration Variable Appendix` |
| *site\_url* | `http://baidu.com/` | No | String | `Specify the platform URL. Required when site_id is 21` |
| *name* | `new_name` | No | String | `Profile Name` |
| *group\_id* | `177` | No | Integer | `Group ID. The default group ID is 1` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1703759701
  },
  "data": 1639  // The serial number of the successfully copy browser profile
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1703759701` | Integer |  |
| *data* | `1639` | Integer | `The serial number of the successfully copy browser profile` |

#### Failed (200)

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `112005` | Integer | `Error Code (1000 1004 1007 2002 2004 2007 112xxx)` |
| *error.message* | `Group does not exist` | String | `Error Description` |
| *error.time* | `1703942086` | Integer |  |
| *data* |  | Array |  |