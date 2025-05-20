# 07 Customize the layout for the profiles already opened

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=03592e93-7974-45b7-9fe1-61dd76918bdd"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Customize the layout for the profiles already opened

Update Time：2025-04-30 00:14:04

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-opened-list-arrange-tile*
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
  "screen": 0, // Monitor 0: Primary Screen 1: Extended Screen 1 2: Extended Screen 2 ... Default: 0
  "layout": 1, // Layout 1: Grid 2: Overlapped Default: 1
  "adaptive": 1, // Auto-arrange profiles based on monitor resolution 1: Enable 0: Disable Default: 1
  "starting_position_x": 10, // Profile Horizontal Starting Position Default: 10 (Effective when adaptive is 0)
  "starting_position_y": 10, // Profile Vertical Starting Position Default: 10 (Effective when adaptive is 0)
  "profile_size_width": 500, // Profile Width Default: 500 (Effective when adaptive is 0)
  "profile_size_hight": 500, // Profile Height Default: 500 (Effective when adaptive is 0)
  "profile_spacing_horizontal": 10, // Profile Horizontal Spacing Default: 10 (Effective when adaptive is 0 and layout is 1)
  "profile_spacing_vertical": 10, // Profile Vertical Spacing Default: 10 (Effective when adaptive is 0 and layout is 1)
  "profile_deviaton_x": 50, // Profile Horizontal Offset Default: 50 (Effective when adaptive is 0 and layout is 2)
  "profile_deviaton_y": 50, // Profile Vertical Offset Default: 50 (Effective when adaptive is 0 and layout is 2)
  "per_line_number_of_profiles": 3 // Number of Profiles per Row Default: 3 (Effective when adaptive is 0 and layout is 1)
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *screen* | ```0``` | No | Integer | ```Monitor 0: Primary Screen 1: Extended Screen 1 2: Extended Screen 2 ... Default: 0``` |
| *layout* | ```1``` | No | Integer | ```Layout 1: Grid 2: Overlapped Default: 1``` |
| *adaptive* | ```1``` | No | Integer | ```Auto-arrange profiles based on monitor resolution 1: Enable 0: Disable Default: 1``` |
| *starting_position_x* | ```10``` | No | Integer | ```Profile Horizontal Starting Position Default: 10 (Effective when adaptive is 0)``` |
| *starting_position_y* | ```10``` | No | Integer | ```Profile Vertical Starting Position Default: 10 (Effective when adaptive is 0)``` |
| *profile_size_width* | ```500``` | No | Integer | ```Profile Width Default: 500 (Effective when adaptive is 0)``` |
| *profile_size_hight* | ```500``` | No | Integer | ```Profile Height Default: 500 (Effective when adaptive is 0)``` |
| *profile_spacing_horizontal* | ```10``` | No | Integer | ```Profile Horizontal Spacing Default: 10 (Effective when adaptive is 0 and layout is 1)``` |
| *profile_spacing_vertical* | ```10``` | No | Integer | ```Profile Vertical Spacing Default: 10 (Effective when adaptive is 0 and layout is 1)``` |
| *profile_deviaton_x* | ```50``` | No | Integer | ```Profile Horizontal Offset Default: 50 (Effective when adaptive is 0 and layout is 2)``` |
| *profile_deviaton_y* | ```50``` | No | Integer | ```Profile Vertical Offset Default: 50 (Effective when adaptive is 0 and layout is 2)``` |
| *per_line_number_of_profiles* | ```3``` | No | Integer | ```Number of Profiles per Row Default: 3 (Effective when adaptive is 0 and layout is 1)``` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success"
  },
  "data": null
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```0``` | Integer |  |
| *error.message* | ```success``` | String |  |
| *data* | ```null``` | Null |  |