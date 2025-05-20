# 09 Open Profile with Random Fingerprint Configuration

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=7dc3642e-81bc-4f5c-883f-23b26f3fd7f4"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Open Profile with Random Fingerprint Configuration

Update Time：2025-04-29 21:25:09

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-open-with-random-fingerprint*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Body Example request

```json
{
  "profile_id": 1576, // Profile serial number
  "args": ["--disable-extension-welcome-page"], // Enable parameters. Example "args": ["--disable-extensions", "--blink-settings=imagesEnabled=false" ] For more parameters, please refer to: https://peter.sh/experiments/chromium-command-line-switches（ You can try to use more parameters, but there is no guarantee that they will all work)
  "load_profile_info_page": true, // Whether to load the profile information page
  "cookie": "", // cookie json Format
  "proxy_config": {
    "proxy_mode": "2", // Proxy Method For details, please refer to the Enumeration Variable Appendix.
    "proxy_check_line": "global_line",
    "proxy_id": 6, // Proxy ID Required when proxy_mode is not 2
    "country": "US", // Country Enabled when proxy_mode=1, please refer to the National Appendix for details
    "city": "", // City Enabled when proxy_mode=1, which can be queried in the ixBrowser modification profile - proxy configuration.
    "gateway": "Default", // Residential Proxy Enabled when proxy_mode=1, for details, please refer to the Enumeration Variable Appendix.
    "proxy_type": "socks5", // Proxy Method Required when proxy_mode=2, for details, please refer to the Enumeration Variable Appendix.
    "proxy_ip": "127.156.1.31", // Proxy IP  proxy_mode is 2, required when proxy_type is not direct
    "proxy_port": "1234", // Proxy Port proxy_mode is 2, required when proxy_type is not direct
    "proxy_user": "", // Proxy Account
    "proxy_password": "", // Proxy Password
    "proxy_service": "general", // Service provider general: general api default: effective when general proxy_mode is 4
    "proxy_data_format_type": "txt", // Data format type Optional value: txt/json
    "proxy_data_txt_format": "ip:port", // TXT data format Default: ip:port For details, please refer to the enumeration variable appendix. It takes effect when the API extraction proxy data format type is txt.
    "proxy_data_json_format": {
      "ip": "ip", // Proxy IP mapping field Default: ip
      "port": "port", // Proxy Port mapping field Default: port
      "username": "username", // Proxy Username mapping field Default: username
      "password": "password" // Proxy Password mapping field Default: password
    }, // json data format mapping relationship
    "proxy_url": "", // Link extraction Required when proxy_mode is 4
    "use_system_proxy": "1", // Enable system proxy 1:follow global settings 2:Enable 3:Close
    "enable_bypass": "0", // Bypass List 0:Close 1:Open Default：0
    "bypass_list": "" // The domains that do not go through the proxy, separate by newlines
  }, // Proxy Information
  "fingerprint_config": {
    "hardware_concurrency": "4", // CPU Parameter
    "device_memory": "8", // Memory Parameters
    "ua_type": 1, // System Type 1: PC 2: Mobile Phone
    "platform": "Windows", // When system's ua_type is 1, it only supports Windows/Macos. When ua_type is 2, it only supports Android/IOS
    "br_version": "", // Browser Version For details, please refer to the Enumeration Variable Appendix
    "ua_info": "Mozilla/5.0 (Windows NT 6.2; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.0.0 Safari/537.36", // UA Details
    "hide_debug_panel": "1", // Hidedebug panel 1:Open 2:Close (effective when ua_type is 2)
    "kernel_version": "0", // Kernel version 0: automatch 102:102 kernel 114:114 kernel 121:121kernel
    "language_type": "1", // Language type 1: Generated based on access IP 2: Customized
    "language": "cn", // Language For details, please refer to the Enumeration Variable Appendix
    "timezone_type": "1", // Time zone type 1: Generated based on access IP 2: Customized
    "timezone": "Asia/Shanghai", // Time zone For details, please refer to the Enumeration Variable Appendix
    "location": "1", // Geolocation type 1: Ask 2: Allow 3: Disable
    "location_type": "1", // Whether to open geolocation 0: Customized 1: Generated based on access IP
    "longitude": 25.7247, // Longitude
    "latitude": 119.3712, // Latitude
    "accuracy": 1000, // Default Accuracy
    "resolving_power_type": "1", // Resolution type 1: Follow device 2: Custom Default: 1 (Customization is not supported when the system type is mobile)
    "resolving_power": "1920,1080", // Resolution
    "fonts_type": "1", // Font 1: System default 2: Custom Default: 1
    "fonts": [], // Font List Please refer to the Font Appendix for details.
    "webrtc": "3", // WebRTC 1: Replace 2: True 3: Disable
    "webgl_image": "1", // WebGL image 0: off 1: random
    "canvas_type": "1", // Canvas 0: Close 1: Random
    "webgl_data_type": "1", // WebGL Metadata 1: Random 2: Custom 3:Close
    "webgl_factory": "", // Vendor Please refer to the WebGL Metadata Appendix for details.
    "webgl_info": "ANGLE (AMD, ATI Radeon HD 4200 Direct3D9Ex vs_3_0 ps_3_0, atiumd64.dll-8.14.10.678)", // Renderer Please refer to the WebGL Metadata Appendix for details.
    "webgpu_data_type": "2", // WebGPU 0:禁用 1:真实 2:基于WebGL
    "audio_context": "1", // AudioContext 0: Close 1: Random
    "media_equipment": "1", // Media Device 0: off 1: random
    "javascript_memory_type": "0", // JavaScript 内存限制 0:默认 1:最大
    "client_rects": "1", // Noise 0: Off 1: Random
    "speech_voices": "1", // SpeechVoices 0: Off 1: Random
    "device_name_source": "1", // Device name source 0: Each browser uses the device name of the current computer 1: Random
    "track": "1", // Do Not Track 0:off 1:default 2:on
    "allow_scan_ports": "0", // Port Scan Protection 0: off 1: on
    "allow_scan_ports_content": "", // The port scan protection list uses an integer, ranging from 1 to 65535. Multiple ports are separated by commas (half-width), example: 4000,4001
    "cloudflare_challenge_bypassing": "0" // Cloudflare Verification Optimization 0: off 1: on
  } // Fingerprint Configuration
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile\_id* | ``` 1576 ``` | Yes | Integer | ``` Profile serial number ``` |
| *args* | ``` --disable-extension-welcome-page ``` | No | Array | ``` Enable parameters. Example "args": ["--disable-extensions", "--blink-settings=imagesEnabled=false" ] For more parameters, please refer to: https://peter.sh/experiments/chromium-command-line-switches（ You can try to use more parameters, but there is no guarantee that they will all work) ``` |
| *load\_profile\_info\_page* | ``` true ``` | No | Boolean | ``` Whether to load the profile information page ``` |
| *cookie* |  | No | String | ``` cookie  json Format ``` |
| *proxy\_config* |  | No | Object | ``` Proxy Information ``` |
| *proxy\_config.proxy\_mode* | ``` 2 ``` | Yes | String | ``` Proxy Method For details, please refer to the Enumeration Variable Appendix. ``` |
| *proxy\_config.proxy\_check\_line* | ``` global_line ``` | No | String |  |
| *proxy\_config.proxy\_id* | ``` 6 ``` | No | Integer | ``` Proxy ID Required when proxy_mode is not 2 ``` |
| *proxy\_config.country* | ``` US ``` | No | String | ``` Country Enabled when proxy_mode=1, please refer to the National Appendix for details ``` |
| *proxy\_config.city* |  | No | String | ``` City Enabled when proxy_mode=1, which can be queried in the ixBrowser modification profile - proxy configuration. ``` |
| *proxy\_config.gateway* | ``` Default ``` | No | String | ``` Residential Proxy Enabled when proxy_mode=1, for details, please refer to the Enumeration Variable Appendix. ``` |
| *proxy\_config.proxy\_type* | ``` socks5 ``` | No | String | ``` Proxy Method Required when proxy_mode=2, for details, please refer to the Enumeration Variable Appendix. ``` |
| *proxy\_config.proxy\_ip* | ``` 127.156.1.31 ``` | No | String | ``` Proxy IP  proxy_mode is 2, required when proxy_type is not direct ``` |
| *proxy\_config.proxy\_port* | ``` 1234 ``` | No | String | ``` Proxy Port proxy_mode is 2, required when proxy_type is not direct ``` |
| *proxy\_config.proxy\_user* |  | No | String | ``` Proxy Account ``` |
| *proxy\_config.proxy\_password* |  | No | String | ``` Proxy Password ``` |
| *proxy\_config.proxy\_service* | ``` general ``` | No | String | ``` Service provider general: general api default: effective when general proxy_mode is 4 ``` |
| *proxy\_config.proxy\_data\_format\_type* | ``` txt ``` | No | String | ``` Data format type Optional value: txt/json ``` |
| *proxy\_config.proxy\_data\_txt\_format* | ``` ip:port ``` | No | String | ``` TXT data format Default: ip:port For details, please refer to the enumeration variable appendix. It takes effect when the API extraction proxy data format type is txt. ``` |
| *proxy\_config.proxy\_data\_json\_format* |  | No | Object | ``` json data format mapping relationship ``` |
| *proxy\_config.proxy\_data\_json\_format.ip* | ``` ip ``` | No | String | ``` Proxy IP mapping field Default: ip ``` |
| *proxy\_config.proxy\_data\_json\_format.port* | ``` port ``` | No | String | ``` Proxy Port mapping field Default: port ``` |
| *proxy\_config.proxy\_data\_json\_format.username* | ``` username ``` | No | String | ``` Proxy Username mapping field Default: username ``` |
| *proxy\_config.proxy\_data\_json\_format.password* | ``` password ``` | No | String | ``` Proxy Password mapping field Default: password ``` |
| *proxy\_config.proxy\_url* |  | No | String | ``` Link extraction Required when proxy_mode is 4 ``` |
| *proxy\_config.use\_system\_proxy* | ``` 1 ``` | No | String | ``` Enable system proxy 1:follow global settings 2:Enable 3:Close ``` |
| *proxy\_config.enable\_bypass* | ``` 0 ``` | No | String | ``` Bypass List 0:Close 1:Open Default：0 ``` |
| *proxy\_config.bypass\_list* |  | No | String | ``` The domains that do not go through the proxy, separate by newlines ``` |
| *fingerprint\_config* |  | No | Object | ``` Fingerprint Configuration ``` |
| *fingerprint\_config.hardware\_concurrency* | ``` 4 ``` | No | String | ``` CPU Parameter ``` |
| *fingerprint\_config.device\_memory* | ``` 8 ``` | No | String | ``` Memory Parameters ``` |
| *fingerprint\_config.ua\_type* | ``` 1 ``` | No | Integer | ``` System Type 1: PC 2: Mobile Phone ``` |
| *fingerprint\_config.platform* | ``` Windows ``` | No | String | ``` When system's ua_type is 1, it only supports Windows/Macos. When ua_type is 2, it only supports Android/IOS ``` |
| *fingerprint\_config.br\_version* |  | No | String | ``` Browser Version For details, please refer to the Enumeration Variable Appendix ``` |
| *fingerprint\_config.ua\_info* | ``` Mozilla/5.0 (Windows NT 6.2; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/104.0.0.0 Safari/537.36 ``` | No | String | ``` UA Details ``` |
| *fingerprint\_config.hide\_debug\_panel* | ``` 1 ``` | No | String | ``` Hidedebug panel 1:Open 2:Close (effective when ua_type is 2) ``` |
| *fingerprint\_config.kernel\_version* | ``` 0 ``` | No | String | ``` Kernel version 0: automatch 102:102 kernel 114:114 kernel 121:121kernel ``` |
| *fingerprint\_config.language\_type* | ``` 1 ``` | No | String | ``` Language type 1: Generated based on access IP 2: Customized ``` |
| *fingerprint\_config.language* | ``` cn ``` | No | String | ``` Language For details, please refer to the Enumeration Variable Appendix ``` |
| *fingerprint\_config.timezone\_type* | ``` 1 ``` | No | String | ``` Time zone type 1: Generated based on access IP 2: Customized ``` |
| *fingerprint\_config.timezone* | ``` Asia/Shanghai ``` | No | String | ``` Time zone For details, please refer to the Enumeration Variable Appendix ``` |
| *fingerprint\_config.location* | ``` 1 ``` | No | String | ``` Geolocation type 1: Ask 2: Allow 3: Disable ``` |
| *fingerprint\_config.location\_type* | ``` 1 ``` | No | String | ``` Whether to open geolocation 0: Customized 1: Generated based on access IP ``` |
| *fingerprint\_config.longitude* | ``` 25.7247 ``` | No | Number | ``` Longitude ``` |
| *fingerprint\_config.latitude* | ``` 119.3712 ``` | No | Number | ``` Latitude ``` |
| *fingerprint\_config.accuracy* | ``` 1000 ``` | No | Integer | ``` Default Accuracy ``` |
| *fingerprint\_config.resolving\_power\_type* | ``` 1 ``` | No | String | ``` Resolution type 1: Follow device 2: Custom Default: 1 (Customization is not supported when the system type is mobile) ``` |
| *fingerprint\_config.resolving\_power* | ``` 1920,1080 ``` | No | String | ``` Resolution ``` |
| *fingerprint\_config.fonts\_type* | ``` 1 ``` | No | String | ``` Font 1: System default 2: Custom Default: 1 ``` |
| *fingerprint\_config.fonts* |  | No | Array | ``` Font List Please refer to the Font Appendix for details. ``` |
| *fingerprint\_config.webrtc* | ``` 3 ``` | No | String | ``` WebRTC 1: Replace 2: True 3: Disable ``` |
| *fingerprint\_config.webgl\_image* | ``` 1 ``` | No | String | ``` WebGL image 0: off 1: random ``` |
| *fingerprint\_config.canvas\_type* | ``` 1 ``` | No | String | ``` Canvas 0: Close 1: Random ``` |
| *fingerprint\_config.webgl\_data\_type* | ``` 1 ``` | No | String | ``` WebGL Metadata 1: Random 2: Custom 3:Close ``` |
| *fingerprint\_config.webgl\_factory* |  | No | String | ``` Vendor Please refer to the WebGL Metadata Appendix for details. ``` |
| *fingerprint\_config.webgl\_info* | ``` ANGLE (AMD, ATI Radeon HD 4200 Direct3D9Ex vs_3_0 ps_3_0, atiumd64.dll-8.14.10.678) ``` | No | String | ``` Renderer Please refer to the WebGL Metadata Appendix for details. ``` |
| *fingerprint\_config.webgpu\_data\_type* | ``` 2 ``` | No | String | ``` WebGPU 0:禁用 1:真实 2:基于WebGL ``` |
| *fingerprint\_config.audio\_context* | ``` 1 ``` | No | String | ``` AudioContext 0: Close 1: Random ``` |
| *fingerprint\_config.media\_equipment* | ``` 1 ``` | No | String | ``` Media Device 0: off 1: random ``` |
| *fingerprint\_config.javascript\_memory\_type* | ``` 0 ``` | No | String | ``` JavaScript 内存限制 0:默认 1:最大 ``` |
| *fingerprint\_config.client\_rects* | ``` 1 ``` | No | String | ``` Noise 0: Off 1: Random ``` |
| *fingerprint\_config.speech\_voices* | ``` 1 ``` | No | String | ``` SpeechVoices 0: Off 1: Random ``` |
| *fingerprint\_config.device\_name\_source* | ``` 1 ``` | No | String | ``` Device name source 0: Each browser uses the device name of the current computer 1: Random ``` |
| *fingerprint\_config.track* | ``` 1 ``` | No | String | ``` Do Not Track 0:off 1:default 2:on ``` |
| *fingerprint\_config.allow\_scan\_ports* | ``` 0 ``` | No | String | ``` Port Scan Protection 0: off 1: on ``` |
| *fingerprint\_config.allow\_scan\_ports\_content* |  | No | String | ``` The port scan protection list uses an integer, ranging from 1 to 65535. Multiple ports are separated by commas (half-width), example: 4000,4001 ``` |
| *fingerprint\_config.cloudflare\_challenge\_bypassing* | ``` 0 ``` | No | String | ``` Cloudflare Verification Optimization 0: off 1: on ``` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success"
  },
  "data": {
    "debugging_address": "127.0.0.1:3330", // Remote debugging address
    "debugging_port": 3330, // Remote debugging port
    "profile_id": 1576, // Profile serial number
    "pid": 19916, // Process ID
    "ws": "ws://127.0.0.1:3330/devtools/browser/0cc6ab9b-f8b5-47a0-b92f-4bb5b1c42d99", // WS Address
    "gateway": "Current Node:US【Transit in US】...", // The default node opened by the Residential traffic package, and the custom proxy is not displayed
    "webdriver": "E:\\\\FreeBrower\\\\Brower\\\\resources\\\\chrome\\\\webdriver\\\\114\\\\chromedriver.exe" // The kernel that opened the environment before returns the corresponding kernel webdriver driver path
  }
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ``` 0 ``` | Integer |  |
| *error.message* | ``` success ``` | String |  |
| *data* |  | Object |  |
| *data.debugging\_address* | ``` 127.0.0.1:3330 ``` | String | ``` Remote debugging address ``` |
| *data.debugging\_port* | ``` 3330 ``` | Integer | ``` Remote debugging port ``` |
| *data.profile\_id* | ``` 1576 ``` | Integer | ``` Profile serial number ``` |
| *data.pid* | ``` 19916 ``` | Integer | ``` Process ID ``` |
| *data.ws* | ``` ws://127.0.0.1:3330/devtools/browser/0cc6ab9b-f8b5-47a0-b92f-4bb5b1c42d99 ``` | String | ``` WS Address ``` |
| *data.gateway* | ``` "gateway": "Current Node:US【Transit in US】...", ``` | String | ``` The default node opened by the Residential traffic package, and the custom proxy is not displayed ``` |
| *data.webdriver* | ``` E:\\FreeBrower\\Brower\\resources\\chrome\\webdriver\\114\\chromedriver.exe ``` | String | ``` The kernel that opened the environment before returns the corresponding kernel webdriver driver path ``` |

#### Failed（200）

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | ``` 2003 ``` | Integer | ``` Error Code（1000 1003 1004 1007 1008 2002 2003 2007） ``` |
| *error.message* | ``` Residential Proxy does not exist ``` | String | ``` Error Description ``` |
| *data* | ``` null ``` | Null |  |