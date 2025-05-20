# 06 Retrieve profiles opened via the local API

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=c2683363-2ea3-40d3-bc86-bc6c71db9ebb"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Retrieve profiles opened via the local API

Update Time：2025-04-30 00:29:30

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/native-client-profile-opened-list*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | ```application/json``` | Yes | String | ```application/json``` |

#### Body Example request

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
      "debugging_address": "127.0.0.1:28545", //Remote debugging address
      "debugging_port": 28545, //Remote debugging port
      "profile_id": 2073, //Profile serial number
      "pid": 11380, //Process ID
      "open_time": "2025-04-30 14:25:47", //Opened Time
      "ws": "ws://127.0.0.1:28545/devtools/browser/5cb87d78-7da2-4c4f-a319-6f96e776cda7", //WS Address
      "webdriver": "C:\\Users\\Administrator\\AppData\\Roaming\\ixBrowser-Resources\\chrome\\134-0001\\chromedriver.exe" //The kernel of the currently opened environment returns the corresponding kernel webdriver driver path
    }
  ]
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```0``` | Integer |  |
| *error.message* | ```success``` | String |  |
| *data* |  | Array |  |
| *data.debugging\_address* | ```127.0.0.1:28545``` | String | ```Remote debugging address``` |
| *data.debugging\_port* | ```28545``` | Integer | ```Remote debugging port``` |
| *data.profile\_id* | ```2073``` | Integer | ```Profile serial number``` |
| *data.pid* | ```11380``` | Integer | ```Process ID``` |
| *data.open\_time* | ```2025-04-30 14:25:47``` | String | ```Opened Time``` |
| *data.ws* | ```ws://127.0.0.1:28545/devtools/browser/5cb87d78-7da2-4c4f-a319-6f96e776cda7``` | String | ```WS Address``` |
| *data.webdriver* | ```C:\\Users\\Administrator\\AppData\\Roaming\\ixBrowser-Resources\\chrome\\134-0001\\chromedriver.exe``` | String | ```The kernel of the currently opened environment returns the corresponding kernel webdriver driver path``` |

#### Failed（200）

```json
{
  "error": {
    "code": 2007, //Error Code（1000 1003 1004 1007 1008 2001 2002 2003 2007 2008）
    "message": "Profile does not exist" //Error Description
  },
  "data": null
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ```2007``` | Integer | ```Error Code（1000 1003 1004 1007 1008 2001 2002 2003 2007 2008）``` |
| *error.message* | ```Profile does not exist``` | String | ```Error Description``` |
| *data* | ```null``` | Null |  |