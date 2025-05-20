# 11 Close Profiles in Batches

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=e4f8cc8e-43a1-4f2e-9c50-a8477fea55b0"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Close Profiles in Batches

Update Time: 2024-09-09 00:14:11

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-close-in-batches*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| Parameter name | Example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String | `application/json` |

#### Body Example request

```json
{
  "profile_id": ["161", "162"] // Profile serial number
}
```

| Parameter name | Example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `161` | Yes | Array | `Profile serial number` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success"
  },
  "data": ["161"] // The serial number of the profile that was successfully closed
}
```

| Parameter name | Example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *data* | `161` | Array | `The serial number of the profile that was successfully closed` |

#### Failed (200)

```json
{
  "error": {
    "code": 1009, // Error Code (1000 1009)
    "message": "Process not found" // Error Description
  },
  "data": null
}
```

| Parameter name | Example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `1009` | Integer | `Error Code (1000 1009)` |
| *error.message* | `Process not found` | String | `Error Description` |
| *data* | `null` | Null |  |