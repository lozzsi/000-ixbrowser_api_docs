# 20 Update Profile Groups in Batches

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=709ca708-b9f1-4279-937f-769bfe7b6f7f"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Profile Groups in Batches

Update Time：2024-09-09 00:17:54

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-update-groups-in-batches*
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
  "group_id": 171,  // Group ID
  "profile_id": [170]  // Profile serial number
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *group_id* | `1` | Yes | Integer | `Group ID` |
| *profile_id* | `161` | Yes | Array | `Profile serial number` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1676454536
  },
  "data": "success"  // The serial number of the successfully modified profile
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1676454536` | Integer |  |
| *data* | `success` | String | `The serial number of the successfully modified profile` |

#### Failed（200）

```json
{
  "error": {
    "code": 1008,  // Error Code（1000 1004 1008 1011 2001 2007）
    "message": "Your permissions are restricted"  // Error Description
  },
  "data": null
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `1008` | Integer | `Error Code（1000 1004 1008 1011 2001 2007）` |
| *error.message* | `Your permissions are restricted` | String | `Error Description` |
| *data* | `null` | Null |  |