# 46 Get Gateway List

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=5554550c-2f27-4f2a-b7f1-804f6152c71d"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get Gateway List

Update Time：2024-09-18 21:50:52

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/gateway-list*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String |  |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success"
  },
  "data": [
    {
      "id": "1", // Gateway ID
      "name": "Line1" // Gateway Name
    },
    {
      "id": "2", // Gateway ID
      "name": "Line2" // Gateway Name
    }
  ]
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *data* |  | Array |  |
| *data.id* | `1` | String | `Gateway ID` |
| *data.name* | `Line1` | String | `Gateway Name` |