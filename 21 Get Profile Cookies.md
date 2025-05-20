# 21 Get Profile Cookies

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=6f5ae8c3-b5ac-4a43-889e-f16c9f90735c"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Get Profile Cookies

Update Time：2024-09-09 00:18:15

### Basic information

- Status： Completed
- Interface URL： *POST* *http://127.0.0.1:53200/api/v2/profile-get-cookies*
- Content-Type： *application/json*
- Authentication： *No description yet*

### Example request

#### Header Example request

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String |  |

#### Body Example request

```json
{
  "profile_id": 13421 //Profile serial number
}
```

| parameter name | example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `1342` | Yes | Integer | `Profile serial number` |

### Response example

#### Success（200）

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1693308463
  },
  "data": "[\n{\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BAIDUID\",\"value\":\"851E73F95773C19D133365C87AD90608:FG=1\",\"path\":\"/\",\"expiration_time\":\"1722583157\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BA_HECTOR\",\"value\":\"ak21202g212gag04042k2k0f1icml7m1o\",\"path\":\"/\",\"expiration_time\":\"1691133557\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BIDUPSID\",\"value\":\"851E73F95773C19D5FF8CC8838218E3A\",\"path\":\"/\",\"expiration_time\":\"1725607157\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"PSTM\",\"value\":\"1691047156\",\"path\":\"/\",\"expiration_time\":\"1725607157\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"ZFY\",\"value\":\"T2MFXetHwtSdupZOPpsmbRNY9ixO:BaEYizOkGCKZ:A9g:C\",\"path\":\"/\",\"expiration_time\":\"1722583158\",\"last_access_time\":\"1691119532\",\"secure\":true,\"http_only\":false,\"same_site\":\"0\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119532\",\"domain\":\"www.baidu.com\",\"name\":\"BD_HOME\",\"value\":\"1\",\"path\":\"/\",\"expiration_time\":\"0\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":true},\n{\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"H_PS_PSSID\",\"value\":\"36556_39110_38831_39114_39116_39040_38918_26350_39132_22159_39100_39043\",\"path\":\"/\",\"expiration_time\":\"0\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119532\",\"domain\":\"www.baidu.com\",\"name\":\"BD_UPN\",\"value\":\"12314753\",\"path\":\"/\",\"expiration_time\":\"1691983534\",\"last_access_time\":\"1691119534\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":true},\n{\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BAIDUID_BFESS\",\"value\":\"851E73F95773C19D133365C87AD90608:FG=1\",\"path\":\"/\",\"expiration_time\":\"1722655535\",\"last_access_time\":\"1691119535\",\"secure\":true,\"http_only\":false,\"same_site\":\"0\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119537\",\"domain\":\".ixbrowser.com\",\"name\":\"_ga_8XCJ3YF17N\",\"value\":\"GS1.1.1691117948.2.1.1691119537.0.0.0\",\"path\":\"/\",\"expiration_time\":\"1725679537\",\"last_access_time\":\"1691119537\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},\n{\"creation_time\":\"1691119532\",\"domain\":\".ixbrowser.com\",\"name\":\"_ga\",\"value\":\"GA1.1.1114785102.1691053919\",\"path\":\"/\",\"expiration_time\":\"1725679537\",\"last_access_time\":\"1691119537\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false}\n]" //Cookies json format
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1693308463` | Integer |  |
| *data* | `[ {"creation_time":"1691119532","domain":".baidu.com","name":"BAIDUID","value":"851E73F95773C19D133365C87AD90608:FG=1","path":"/","expiration_time":"1722583157","last_access_time":"1691119532","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119532","domain":".baidu.com","name":"BA_HECTOR","value":"ak21202g212gag04042k2k0f1icml7m1o","path":"/","expiration_time":"1691133557","last_access_time":"1691119532","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119532","domain":".baidu.com","name":"BIDUPSID","value":"851E73F95773C19D5FF8CC8838218E3A","path":"/","expiration_time":"1725607157","last_access_time":"1691119532","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119532","domain":".baidu.com","name":"PSTM","value":"1691047156","path":"/","expiration_time":"1725607157","last_access_time":"1691119532","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119532","domain":".baidu.com","name":"ZFY","value":"T2MFXetHwtSdupZOPpsmbRNY9ixO:BaEYizOkGCKZ:A9g:C","path":"/","expiration_time":"1722583158","last_access_time":"1691119532","secure":true,"http_only":false,"same_site":"0","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119532","domain":"www.baidu.com","name":"BD_HOME","value":"1","path":"/","expiration_time":"0","last_access_time":"1691119532","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":true}, {"creation_time":"1691119532","domain":".baidu.com","name":"H_PS_PSSID","value":"36556_39110_38831_39114_39116_39040_38918_26350_39132_22159_39100_39043","path":"/","expiration_time":"0","last_access_time":"1691119532","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119532","domain":"www.baidu.com","name":"BD_UPN","value":"12314753","path":"/","expiration_time":"1691983534","last_access_time":"1691119534","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":true}, {"creation_time":"1691119532","domain":".baidu.com","name":"BAIDUID_BFESS","value":"851E73F95773C19D133365C87AD90608:FG=1","path":"/","expiration_time":"1722655535","last_access_time":"1691119535","secure":true,"http_only":false,"same_site":"0","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119537","domain":".ixbrowser.com","name":"_ga_8XCJ3YF17N","value":"GS1.1.1691117948.2.1.1691119537.0.0.0","path":"/","expiration_time":"1725679537","last_access_time":"1691119537","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false}, {"creation_time":"1691119532","domain":".ixbrowser.com","name":"_ga","value":"GA1.1.1114785102.1691053919","path":"/","expiration_time":"1725679537","last_access_time":"1691119537","secure":false,"http_only":false,"same_site":"-1","priority":"1","same_party":false,"source_scheme":"2","source_port":"443","is_host_cookie":false} ]` | String | `Cookies json format` |

#### Failed（200）

```json
{
  "error": {
    "code": 2007, //Error Code（1000 1007 1008 2001 2007）
    "message": "Profile does not exist", //Error Description
    "time": 1694762947
  },
  "data": []
}
```

| parameter name | example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `2007` | Integer | `Error Code（1000 1007 1008 2001 2007）` |
| *error.message* | `Profile does not exist` | String | `Error Description` |
| *error.time* | `1694762947` | Integer |  |
| *data* |  | Array |  |