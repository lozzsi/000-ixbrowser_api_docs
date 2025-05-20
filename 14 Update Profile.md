# 14 Update Profile

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=22ee227e-5f94-4eaa-85f4-6072c81133c9"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Profile

Update Time：2025-04-29 21:29:09

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-update*
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
  "profile_id": 1600, //Profile serial number
  "new_profile_id": 1589, //New profile serial number (this parameter will update the old profile serial number)
  "site_id": 2, //Platform ID For details, please refer to the Enumeration Variable Appendix.
  "site_url": "https://amazon.com", //Specified Platform URL
  "color": "#CC9966", //Profile Color
  "name": "name1", //Profile Name
  "note": "", //Profile Notes
  "group_id": 12, //Group ID
  "tag": "", //Tag name (If there are multiple tags, please sendin array format)
  "username": "user", //Platform login username
  "password": "123456", //Platform login password
  "tfa_secret": "", //2FA Key
  "cookie": "", //Cookie json format
  "proxy_config": {
    "proxy_mode": 2, //Proxy Method For details, please refer to the Enumeration Variable Appendix
    "proxy_check_line": "global_line", //Proxy Detection Line Default:global_line proxy_mode is 2 or 4, effect when proxy_type is not direct
    "proxy_id": "", //Proxy ID Required when proxy_mode is not 2
    "proxy_type": "direct", //Proxy Type For details, please refer to the Enumeration Variable Appendix
    "proxy_ip": "", //Proxy IP proxy_mode is 2, required when proxy_type is not direct
    "proxy_port": "", //Proxy Port proxy_mode is 2, required when proxy_type is not direct
    "proxy_user": "", //Proxy Account
    "proxy_password": "", //Proxy Password
    "ip_detection": "1", //Whether to obtain the latest IP's country, time zone, coordinates, etc. every time (not required for non-dynamic IP) 0: Off 1: On Default: 0
    "traffic_package_ip_policy": false, //IP Policy false: keep the IP unchanged (5~60 minutes) true: get a new IP every time you open the profile Default: false takes effect when proxy_mode is 1
    "proxy_service": "general", //Service provider general: general api It takes effect when proxy_mode is 4
    "proxy_data_format_type": "txt", //Data format type Optional value: txt/json
    "proxy_data_txt_format": "ip:port", //TXT data format For details, please refer to the enumeration variable appendix. The API extraction proxy data format type is effective when it is txt.
    "proxy_data_json_format": {
      "ip": "ip", //Proxy IP Mapping Field
      "port": "port", //Proxy Port Mapping Field
      "username": "username", //Proxy Account Mapping Field
      "password": "password" //Proxy Password Mapping Field
    }, //json data format mapping relationship
    "proxy_extraction_method": "invalid", //Extraction method invalid: extract a new IP when the IP expires every_type: extract a new IP every time the profile is opened, effective when proxy_mode is 4
    "proxy_url": "", //Link extraction It takes effect when proxy_mode is 4
    "use_system_proxy": "1", //Enable system proxy 1:follow global settings 2:Enable 3:Close
    "enable_bypass": "0", //Bypass List 0:Close 1:Open
    "bypass_list": "" //The domains that do not go through the proxy, separate by newlines
  }, //Proxy information configuration
  "fingerprint_config": {
    "hardware_concurrency": "4", //CPU Parameter
    "device_memory": "8", //Memory Parameters
    "ua_type": 1, //System Type 1: PC 2: Mobile Phone
    "platform": "Windows", //When system's ua_type is 1, it only supports Windows/Macos. When ua_type is 2, it only supports Android/IOS
    "br_version": "", //Browser Version For details, please refer to the Enumeration Variable Appendix
    "ua_info": "Mozilla/5.0 (Windows NT 6.2; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.0.0 Safari/537.36", //UA Details
    "hide_debug_panel": "1", //Hidedebug panel 1:Open 2:Close (effective when ua_type is 2)
    "kernel_version": "0", //Kernel version 0: automatch 102:102 kernel 114:114 kernel 121:121kernel
    "language_type": "1", //Language type 1: Generated based on access IP 2: Customized
    "language": "cn", //Language For details, please refer to the Enumeration Variable Appendix
    "timezone_type": "1", //Time zone type 1: Generated based on access IP 2: Customized
    "timezone": "Asia/Shanghai", //Time zone For details, please refer to the Enumeration Variable Appendix
    "location": "1", //Geolocation type 1: Ask 2: Allow 3: Disable
    "location_type": "1", //Whether to open geolocation 0: Customized 1: Generated based on access IP
    "longitude": 25.7247, //Longitude
    "latitude": 119.3712, //Latitude
    "accuracy": 1000, //Default Accuracy
    "resolving_power_type": "1", //Resolution type 1: Follow device 2: Custom Default: 1 (Customization is not supported when the system type is mobile)
    "resolving_power": "1920,1080", //Resolution
    "fonts_type": "1", //Font 1: System default 2: Custom Default: 1
    "fonts": [], //Font List Please refer to the Font Appendix for details.
    "webrtc": "3", //WebRTC 1: Replace 2: True 3: Disable
    "webgl_image": "1", //WebGL image 0: off 1: random
    "canvas_type": "1", //Canvas 0: Close 1: Random
    "webgl_data_type": "1", //WebGL Metadata 1: Random 2: Custom
    "webgl_factory": "", //Vendor Please refer to the WebGL Metadata Appendix for details.
    "webgl_info": "ANGLE (AMD, ATI Radeon HD 4200 Direct3D9Ex vs_3_0 ps_3_0, atiumd64.dll-8.14.10.678)", //Renderer Please refer to the WebGL Metadata Appendix for details.
    "webgpu_data_type": "2", //WebGPU 0: Disable 1: True 2: Based on WEbGL
    "audio_context": "1", //AudioContext 0: Close 1: Random
    "media_equipment": "1", //Media Device 0: off 1: random
    "javascript_memory_type": "0", //JavaScript Memory Restrictions 0:Default 1:Maximum
    "client_rects": "1", //Noise 0: Off 1: Random
    "speech_voices": "1", //SpeechVoices 0: Off 1: Random
    "device_name_source": "1", //Device name source 0: Each browser uses the device name of the current computer 1: Random
    "track": "1", //Do Not Track 0:off 1:default 2:on
    "allow_scan_ports": "0", //Port Scan Protection 0: off 1: on
    "allow_scan_ports_content": "", //The port scan protection list uses an integer, ranging from 1 to 65535. Multiple ports are separated by commas (half-width), example: 4000,4001
    "cloudflare_challenge_bypassing": "0" //Cloudflare Verification Optimization 0: off 1: on
  }, //Fingerprint Configuration
  "preference_config": {
    "cookies_backup": "1", //Cloud backup cookie 0: Off 1: On
    "indexed_db_backup": "0", //Synchronize Indexed DB 0: Disable 1: Enable (valid when cloud backup cookie is enabled)
    "local_storage_backup": "0", //Synchronize Local Storage 0: Off 1: On (effective when cloud backup cookie is turned on)
    "extension_data_backup": "0", //Synchronize extension data 0: Off 1: On (effective when cloud backup cookie is turned on)
    "extra_tab_source": "0", //Tag management 0: Open a specific URL each time 1: Open the tabs from the profile was last closed Default: 0 (Doesn't support opening the tabs from the profile was last closed under cloud backup cookie closed status)
    "open_url": "", //Open the specified URL and split it by line
    "block_image": "0", //Block Image 0: Close 1: Open Default: 0
    "block_audio": "0", //Block Audio 0: Close 1: Open Default: 0
    "block_password_pages": "0", //Disable Password Saving Box 0: off 1: on
    "block_restore_pages": "1", //Prohibit restoring pages pop-up  0: Close 1: Open
    "block_popup_blocking": "1", //Disable Pop-up Interception  0: Close 1: Open
    "load_profile_info_page": "1", //Load profile information page 0: Close 1: Open
    "show_password": "0", //Show Password  0: Close 1: Open
    "load_bookmarks": "0", //Load Imported Bookmarks  0: Close 1: Open
    "show_bookmarks_bar": "0" //Show Bookmarks Bar 0: off 1: on
  } //Preference Settings
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile\_id* | `1600` | Yes | Integer | `Profile serial number` |
| *new\_profile\_id* | `1589` | No | Integer | `New profile serial number (this parameter will update the old profile serial number)` |
| *site\_id* | `2` | No | Integer | `Platform ID For details, please refer to the Enumeration Variable Appendix.` |
| *site\_url* | `https://amazon.com` | No | String | `Specified Platform URL` |
| *color* | `#CC9966` | No | String | `Profile Color` |
| *name* | `name1` | No | String | `Profile Name` |
| *note* |  | No | String | `Profile Notes` |
| *group\_id* | `12` | No | Integer | `Group ID` |
| *tag* |  | No | String | `Tag name (If there are multiple tags, please sendin array format)` |
| *username* | `user` | No | String | `Platform login username` |
| *password* | `123456` | No | String | `Platform login password` |
| *tfa\_secret* |  | No | String | `2FA Key` |
| *cookie* |  | No | String | `Cookie json format` |
| *proxy\_config* |  | No | Object | `Proxy information configuration` |
| *proxy\_config.proxy\_mode* | `2` | No | Integer | `Proxy Method For details, please refer to the Enumeration Variable Appendix` |
| *proxy\_config.proxy\_check\_line* | `global_line` | No | String | `Proxy Detection Line Default:global_line proxy_mode is 2 or 4, effect when proxy_type is not direct` |
| *proxy\_config.proxy\_id* |  | No | String | `Proxy ID Required when proxy_mode is not 2` |
| *proxy\_config.proxy\_type* | `direct` | No | String | `Proxy Type For details, please refer to the Enumeration Variable Appendix` |
| *proxy\_config.proxy\_ip* |  | No | String | `Proxy IP proxy_mode is 2, required when proxy_type is not direct` |
| *proxy\_config.proxy\_port* |  | No | String | `Proxy Port proxy_mode is 2, required when proxy_type is not direct` |
| *proxy\_config.proxy\_user* |  | No | String | `Proxy Account` |
| *proxy\_config.proxy\_password* |  | No | String | `Proxy Password` |
| *proxy\_config.ip\_detection* | `1` | No | String | `Whether to obtain the latest IP's country, time zone, coordinates, etc. every time (not required for non-dynamic IP) 0: Off 1: On Default: 0` |
| *proxy\_config.traffic\_package\_ip\_policy* | `false` | No | Boolean | `IP Policy false: keep the IP unchanged (5~60 minutes) true: get a new IP every time you open the profile Default: false takes effect when proxy_mode is 1` |
| *proxy\_config.proxy\_service* | `general` | No | String | `Service provider general: general api It takes effect when proxy_mode is 4` |
| *proxy\_config.proxy\_data\_format\_type* | `txt` | No | String | `Data format type Optional value: txt/json` |
| *proxy\_config.proxy\_data\_txt\_format* | `ip:port` | No | String | `TXT data format For details, please refer to the enumeration variable appendix. The API extraction proxy data format type is effective when it is txt.` |
| *proxy\_config.proxy\_data\_json\_format* |  | No | Object | `json data format mapping relationship` |
| *proxy\_config.proxy\_data\_json\_format.ip* | `ip` | No | String | `Proxy IP Mapping Field` |
| *proxy\_config.proxy\_data\_json\_format.port* | `port` | No | String | `Proxy Port Mapping Field` |
| *proxy\_config.proxy\_data\_json\_format.username* | `username` | No | String | `Proxy Account Mapping Field` |
| *proxy\_config.proxy\_data\_json\_format.password* | `password` | No | String | `Proxy Password Mapping Field` |
| *proxy\_config.proxy\_extraction\_method* | `invalid` | No | String | `Extraction method invalid: extract a new IP when the IP expires every_type: extract a new IP every time the profile is opened, effective when proxy_mode is 4` |
| *proxy\_config.proxy\_url* |  | No | String | `Link extraction It takes effect when proxy_mode is 4` |
| *proxy\_config.use\_system\_proxy* | `1` | No | String | `Enable system proxy 1:follow global settings 2:Enable 3:Close` |
| *proxy\_config.enable\_bypass* | `0` | No | String | `Bypass List 0:Close 1:Open` |
| *proxy\_config.bypass\_list* |  | No | String | `The domains that do not go through the proxy, separate by newlines` |
| *fingerprint\_config* |  | No | Object | `Fingerprint Configuration` |
| *fingerprint\_config.hardware\_concurrency* | `4` | No | String | `CPU Parameter` |
| *fingerprint\_config.device\_memory* | `8` | No | String | `Memory Parameters` |
| *fingerprint\_config.ua\_type* | `1` | No | Integer | `System Type 1: PC 2: Mobile Phone` |
| *fingerprint\_config.platform* | `Windows` | No | String | `When system's ua_type is 1, it only supports Windows/Macos. When ua_type is 2, it only supports Android/IOS` |
| *fingerprint\_config.br\_version* |  | No | String | `Browser Version For details, please refer to the Enumeration Variable Appendix` |
| *fingerprint\_config.ua\_info* | `Mozilla/5.0 (Windows NT 6.2; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.0.0 Safari/537.36` | No | String | `UA Details` |
| *fingerprint\_config.hide\_debug\_panel* | `1` | No | String | `Hidedebug panel 1:Open 2:Close (effective when ua_type is 2)` |
| *fingerprint\_config.kernel\_version* | `0` | No | String | `Kernel version 0: automatch 102:102 kernel 114:114 kernel 121:121kernel` |
| *fingerprint\_config.language\_type* | `1` | No | String | `Language type 1: Generated based on access IP 2: Customized` |
| *fingerprint\_config.language* | `cn` | No | String | `Language For details, please refer to the Enumeration Variable Appendix` |
| *fingerprint\_config.timezone\_type* | `1` | No | String | `Time zone type 1: Generated based on access IP 2: Customized` |
| *fingerprint\_config.timezone* | `Asia/Shanghai` | No | String | `Time zone For details, please refer to the Enumeration Variable Appendix` |
| *fingerprint\_config.location* | `1` | No | String | `Geolocation type 1: Ask 2: Allow 3: Disable` |
| *fingerprint\_config.location\_type* | `1` | No | String | `Whether to open geolocation 0: Customized 1: Generated based on access IP` |
| *fingerprint\_config.longitude* | `25.7247` | No | Number | `Longitude` |
| *fingerprint\_config.latitude* | `119.3712` | No | Number | `Latitude` |
| *fingerprint\_config.accuracy* | `1000` | No | Integer | `Default Accuracy` |
| *fingerprint\_config.resolving\_power\_type* | `1` | No | String | `Resolution type 1: Follow device 2: Custom Default: 1 (Customization is not supported when the system type is mobile)` |
| *fingerprint\_config.resolving\_power* | `1920,1080` | No | String | `Resolution` |
| *fingerprint\_config.fonts\_type* | `1` | No | String | `Font 1: System default 2: Custom Default: 1` |
| *fingerprint\_config.fonts* |  | No | Array | `Font List Please refer to the Font Appendix for details.` |
| *fingerprint\_config.webrtc* | `3` | No | String | `WebRTC 1: Replace 2: True 3: Disable` |
| *fingerprint\_config.webgl\_image* | `1` | No | String | `WebGL image 0: off 1: random` |
| *fingerprint\_config.canvas\_type* | `1` | No | String | `Canvas 0: Close 1: Random` |
| *fingerprint\_config.webgl\_data\_type* | `1` | No | String | `WebGL Metadata 1: Random 2: Custom` |
| *fingerprint\_config.webgl\_factory* |  | No | String | `Vendor Please refer to the WebGL Metadata Appendix for details.` |
| *fingerprint\_config.webgl\_info* | `ANGLE (AMD, ATI Radeon HD 4200 Direct3D9Ex vs_3_0 ps_3_0, atiumd64.dll-8.14.10.678)` | No | String | `Renderer Please refer to the WebGL Metadata Appendix for details.` |
| *fingerprint\_config.webgpu\_data\_type* | `2` | No | String | `WebGPU 0: Disable 1: True 2: Based on WEbGL` |
| *fingerprint\_config.audio\_context* | `1` | No | String | `AudioContext 0: Close 1: Random` |
| *fingerprint\_config.media\_equipment* | `1` | No | String | `Media Device 0: off 1: random` |
| *fingerprint\_config.javascript\_memory\_type* | `0` | No | String | `JavaScript Memory Restrictions 0:Default 1:Maximum` |
| *fingerprint\_config.client\_rects* | `1` | No | String | `Noise 0: Off 1: Random` |
| *fingerprint\_config.speech\_voices* | `1` | No | String | `SpeechVoices 0: Off 1: Random` |
| *fingerprint\_config.device\_name\_source* | `1` | No | String | `Device name source 0: Each browser uses the device name of the current computer 1: Random` |
| *fingerprint\_config.track* | `1` | No | String | `Do Not Track 0:off 1:default 2:on` |
| *fingerprint\_config.allow\_scan\_ports* | `0` | No | String | `Port Scan Protection 0: off 1: on` |
| *fingerprint\_config.allow\_scan\_ports\_content* |  | No | String | `The port scan protection list uses an integer, ranging from 1 to 65535. Multiple ports are separated by commas (half-width), example: 4000,4001` |
| *fingerprint\_config.cloudflare\_challenge\_bypassing* | `0` | No | String | `Cloudflare Verification Optimization 0: off 1: on` |
| *preference\_config* |  | No | Object | `Preference Settings` |
| *preference\_config.cookies\_backup* | `1` | No | String | `Cloud backup cookie 0: Off 1: On` |
| *preference\_config.indexed\_db\_backup* | `0` | No | String | `Synchronize Indexed DB 0: Disable 1: Enable (valid when cloud backup cookie is enabled)` |
| *preference\_config.local\_storage\_backup* | `0` | No | String | `Synchronize Local Storage 0: Off 1: On (effective when cloud backup cookie is turned on)` |
| *preference\_config.extension\_data\_backup* | `0` | No | String | `Synchronize extension data 0: Off 1: On (effective when cloud backup cookie is turned on)` |
| *preference\_config.extra\_tab\_source* | `0` | No | String | `Tag management 0: Open a specific URL each time 1: Open the tabs from the profile was last closed Default: 0 (Doesn't support opening the tabs from the profile was last closed under cloud backup cookie closed status)` |
| *preference\_config.open\_url* |  | No | String | `Open the specified URL and split it by line` |
| *preference\_config.block\_image* | `0` | No | String | `Block Image 0: Close 1: Open Default: 0` |
| *preference\_config.block\_audio* | `0` | No | String | `Block Audio 0: Close 1: Open Default: 0` |
| *preference\_config.block\_password\_pages* | `0` | Yes | String | `Disable Password Saving Box 0: off 1: on` |
| *preference\_config.block\_restore\_pages* | `1` | No | String | `Prohibit restoring pages pop-up  0: Close 1: Open` |
| *preference\_config.block\_popup\_blocking* | `1` | No | String | `Disable Pop-up Interception  0: Close 1: Open` |
| *preference\_config.load\_profile\_info\_page* | `1` | No | String | `Load profile information page 0: Close 1: Open` |
| *preference\_config.show\_password* | `0` | No | String | `Show Password  0: Close 1: Open` |
| *preference\_config.load\_bookmarks* | `0` | No | String | `Load Imported Bookmarks  0: Close 1: Open` |
| *preference\_config.show\_bookmarks\_bar* | `0` | Yes | String | `Show Bookmarks Bar 0: off 1: on` |

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
| *error.code* | `102009` | Integer | `Error Code（1000 1004 1007 2002 2004 2007 102xxx)` |
| *error.message* | `Group does not exist` | String | `Error Description` |
| *error.time* | `1694587776` | Integer |  |
| *data* |  | Array |  |