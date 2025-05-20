# 22 Update Profile Cookies

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=74a61616-f73e-4116-a96a-a294c1581b35"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## Update Profile Cookies

Update Time: 2024-09-09 00:18:40

### Basic information

- Status: Completed
- Interface URL: *POST* *http://127.0.0.1:53200/api/v2/profile-update-cookies*
- Content-Type: *application/json*
- Authentication: *No description yet*

### Example request

#### Header Example request

| Parameter name | Example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *Content-Type* | `application/json` | Yes | String |  |

#### Body Example request

```json
{
  "profile_id": 1342, // Profile serial number
  "cookie": "[
    {\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BAIDUID\",\"value\":\"851E73F95773C19D133365C87AD90608:FG=1\",\"path\":\"/\",\"expiration_time\":\"1722583157\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BA_HECTOR\",\"value\":\"ak21202g212gag04042k2k0f1icml7m1o\",\"path\":\"/\",\"expiration_time\":\"1691133557\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BIDUPSID\",\"value\":\"851E73F95773C19D5FF8CC8838218E3A\",\"path\":\"/\",\"expiration_time\":\"1725607157\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"PSTM\",\"value\":\"1691047156\",\"path\":\"/\",\"expiration_time\":\"1725607157\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"ZFY\",\"value\":\"T2MFXetHwtSdupZOPpsmbRNY9ixO:BaEYizOkGCKZ:A9g:C\",\"path\":\"/\",\"expiration_time\":\"1722583158\",\"last_access_time\":\"1691119532\",\"secure\":true,\"http_only\":false,\"same_site\":\"0\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119532\",\"domain\":\"www.baidu.com\",\"name\":\"BD_HOME\",\"value\":\"1\",\"path\":\"/\",\"expiration_time\":\"0\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":true},
    {\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"H_PS_PSSID\",\"value\":\"36556_39110_38831_39114_39116_39040_38918_26350_39132_22159_39100_39043\",\"path\":\"/\",\"expiration_time\":\"0\",\"last_access_time\":\"1691119532\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119532\",\"domain\":\"www.baidu.com\",\"name\":\"BD_UPN\",\"value\":\"12314753\",\"path\":\"/\",\"expiration_time\":\"1691983534\",\"last_access_time\":\"1691119534\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":true},
    {\"creation_time\":\"1691119532\",\"domain\":\".baidu.com\",\"name\":\"BAIDUID_BFESS\",\"value\":\"851E73F95773C19D133365C87AD90608:FG=1\",\"path\":\"/\",\"expiration_time\":\"1722655535\",\"last_access_time\":\"1691119535\",\"secure\":true,\"http_only\":false,\"same_site\":\"0\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119537\",\"domain\":\".ixbrowser.com\",\"name\":\"_ga_8XCJ3YF17N\",\"value\":\"GS1.1.1691117948.2.1.1691119537.0.0.0\",\"path\":\"/\",\"expiration_time\":\"1725679537\",\"last_access_time\":\"1691119537\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false},
    {\"creation_time\":\"1691119532\",\"domain\":\".ixbrowser.com\",\"name\":\"_ga\",\"value\":\"GA1.1.1114785102.1691053919\",\"path\":\"/\",\"expiration_time\":\"1725679537\",\"last_access_time\":\"1691119537\",\"secure\":false,\"http_only\":false,\"same_site\":\"-1\",\"priority\":\"1\",\"same_party\":false,\"source_scheme\":\"2\",\"source_port\":\"443\",\"is_host_cookie\":false}
  ]" // Cookie json format
}
```

| Parameter name | Example value | Is it required? | Parameter Type | Parameter Description |
| --- | --- | --- | --- | --- |
| *profile_id* | `1342` | Yes | Integer | `Profile serial number` |
| *cookie* | `[...]` | Yes | String | `Cookie json format` |

### Response example

#### Success (200)

```json
{
  "error": {
    "code": 0,
    "message": "success",
    "time": 1693311358
  },
  "data": "success"
}
```

| Parameter name | Example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `0` | Integer |  |
| *error.message* | `success` | String |  |
| *error.time* | `1693311358` | Integer |  |
| *data* | `success` | String |  |

#### Failed (200)

```json
{
  "error": {
    "code": 1008, // Error Code (1000 1007 1008 1011 2001 2006 2007)
    "message": "Your permissions are restricted", // Error Description
    "time": 1694590214
  },
  "data": []
}
```

| Parameter name | Example value | Parameter Type | Parameter Description |
| --- | --- | --- | --- |
| *error* |  | Object |  |
| *error.code* | `1008` | Integer | `Error Code (1000 1007 1008 1011 2001 2006 2007)` |
| *error.message* | `Your permissions are restricted` | String | `Error Description` |
| *error.time* | `1694590214` | Integer |  |
| *data* |  | Array |  |