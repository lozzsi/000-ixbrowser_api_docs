# 04 Open Profile

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=c642de2b-092a-45ed-878a-c353049938fe"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Open Profile

Update Time：2024-09-09 00:13:12

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-open*
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
    "profile_id": 1557, //Profile serial number
    "args": ["--disable-extension-welcome-page"], //Enable parameters. Example "args": ["--disable-extensions", "--blink-settings=imagesEnabled=false" ] For more parameters, please refer to: https://peter.sh/experiments/chromium-command-line-switches（ You can try to use more parameters, but there is no guarantee that they will all work)
    "load_extensions": true, //Whether to enable the extension
    "load_profile_info_page": false, //Whether to load the profile information page
    "cookies_backup": true, //Cloud backup cookie false: off true: on
    "cookie": "" //cookie json Format
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `1442` | Yes | Integer | `Profile serial number` |
| *args* | `--disable-extension-welcome-page` | No | Array | `Enable parameters. Example "args": ["--disable-extensions", "--blink-settings=imagesEnabled=false" ] For more parameters, please refer to: https://peter.sh/experiments/chromium-command-line-switches（ You can try to use more parameters, but there is no guarantee that they will all work)` |
| *load_extensions* | `true` | No | Boolean | `Whether to enable the extension` |
| *load_profile_info_page* | `false` | No | Boolean | `Whether to load the profile information page` |
| *cookies_backup* | `true` | No | Boolean | `Cloud backup cookie false: off true: on` |
| *cookie* |  | No | String | `cookie json Format` |

### Response example

#### Success（200）

```json
{
    "error": {
        "code": 0,
        "message": "success"
    },
    "data": {
        "debugging_address": "127.0.0.1:27109", //Remote debugging address
        "debugging_port": 27109, //Remote debugging port
        "profile_id": 1557, //Profile serial number
        "pid": 32384, //Process ID
        "ws": "ws://127.0.0.1:27109/devtools/browser/f58e0350-e025-4bc7-9253-8113c99d2266", //WS Address
        "gateway": "Current Node:US【Transit in US】...", //The default node opened by the Residential traffic package, and the custom proxy is not displayed
        "webdriver": "E:\\\\FreeBrower\\\\Brower\\\\resources\\\\chrome\\\\webdriver\\\\114\\\\chromedriver.exe" //The kernel of the currently opened environment returns the corresponding kernel webdriver driver path
    }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *data* |  | Object |  |
| *data.debugging_address* | `127.0.0.1:27109` | String | `Remote debugging address` |
| *data.debugging_port* | `27109` | Integer | `Remote debugging port` |
| *data.profile_id* | `1557` | Integer | `Profile serial number` |
| *data.pid* | `32384` | Integer | `Process ID` |
| *data.ws* | `ws://127.0.0.1:27109/devtools/browser/f58e0350-e025-4bc7-9253-8113c99d2266` | String | `WS Address` |
| *data.gateway* | `Current Node:US【Transit in US】...` | String | `The default node opened by the Residential traffic package, and the custom proxy is not displayed` |
| *data.webdriver* | `E:\\FreeBrower\\Brower\\resources\\chrome\\webdriver\\114\\chromedriver.exe` | String | `The kernel of the currently opened environment returns the corresponding kernel webdriver driver path` |

#### Failed（200）

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2007` | Integer | `Error Code（1000 1003 1004 1007 1008 2001 2002 2003 2007 2008）` |
| *error.message* | `Profile does not exist` | String | `Error Description` |
| *data* | `null` | Null |  |