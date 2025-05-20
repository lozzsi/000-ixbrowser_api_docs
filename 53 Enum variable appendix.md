# 53 Enum variable appendix

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=a81eb170-444e-4ebf-8b77-0cb702f24c07"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

Update Time: 2025-04-30 00:22:51

## Variable: site_id (Platform ID)

| Value | Meaning |
|-------|---------|
| 1 | facebook.com |
| 2 | amazon.com |
| 3 | paypal.com |
| 4 | gmail.com |
| 5 | aliexpress.com |
| 6 | ebay.com |
| 7 | lazada.com |
| 8 | mail.com |
| 9 | outlook.com |
| 10 | payoneer.com |
| 11 | shopify.com |
| 12 | shoplineapp.com |
| 13 | stripe.com |
| 14 | walmart.com |
| 15 | wish.com |
| 16 | shopee.com |
| 17 | etsy.com |
| 18 | dhgate.com |
| 19 | alibaba.com |
| 20 | tiktok.com |
| 21 | Other Platform |
| 22 | Blank Page |

## Variable: proxy_mode (Proxy Method)

| Value | Meaning |
|-------|---------|
| 1 | Purchased Residential Proxy |
| 2 | Custom |
| 3 | Purchased Static Proxy |
| 4 | API Extraction |

## Variable: proxy_check_line (Proxy Detection Line)

| Value | Meaning |
|-------|---------|
| global_line | Global Line |
| cn_line | Chinese Line |

## Variable: proxy_type (Proxy Type)

| Value | Meaning |
|-------|---------|
| direct | Direct Mode |
| http | HTTP |
| https | HTTPS |
| socks5 | SOCKS5 |
| ssh | SSH |

## Variable: proxy_data_txt_format (API extracts the data format when the proxy data format type is txt)

| Format |
|--------|
| ip:port |
| ip:port:username:password |
| username:password@ip:port |
| ip:port@username:password |
| username:password:ip:port |

## Variable: gateway

### Cost-effective traffic provider A (Residential Proxy Node)

| Value | Meaning |
|-------|---------|
| Default | Automatic Matching |
| US | United States【Direct connection】 |
| SG | Singapore【Direct connection】 |
| AU | Australia【Direct connection】 |
| CN-SG | Singapore【Transit in China】 |
| CN-US | US【Transit in China 1】 |
| CN-US2 | US【Transit in China 2】 |
| GEO | Smart Access【Direct connection】 |

### Cost-effective traffic provider B (Residential Proxy Node)

| Value | Meaning |
|-------|---------|
| Default | Automatic Matching |
| HK | East Asia【Direct】 |
| US | US【Direct】 |
| SEA | Southeast Asia【Direct】 |
| EU | Europe【Direct】 |
| GB | GB【Direct】 |
| UA | Australia【Direct】 |
| IN | South Asia【Direct】 |
| TH | Thailand【Direct】 |
| JP | Japan【Direct】 |
| CN-HK | East Asia【Transit in China 1】 |
| CN-HK2 | East Asia【Transit in China 2】 |

## Variable: use_system_proxy (Enable System Proxy)

| Value | Meaning |
|-------|---------|
| 1 | Follow global settings |
| 2 | Enable |
| 3 | Close |

## Variable: ua_type (System Type)

| Value | Meaning |
|-------|---------|
| 1 | PC |
| 2 | Mobile |

## Variable: platform (System)

| Value | Meaning |
|-------|---------|
| windows | windows system(PC) |
| macos | macos system(PC) |
| Android | Android system(mobile) |
| iOS | iOS system(mobile) |

## Variable: br_version (Browser Version)

88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99, 100, 101, 102, 103, 104, 105, 106, 107, 108, 109, 110, 111, 112, 113, 114, 115, 116, 117, 118, 119, 120, 121, 122, 123, 124, 125, 126, 127, 128, 129, 130, 131, 132, 133, 134, 135

## Variable: kernel_version (Kernel version)

| Value | Meaning |
|-------|---------|
| 0 | Automatch |
| 102 | 102 kernel |
| 114 | 114 kernel |
| 121 | 121 kernel |
| 126 | 126 kernel |
| 130 | 130 kernel |
| 134 | 134 kernel |

## Variable: hide_debug_panel (Hide Debug Panel)

| Value | Meaning |
|-------|---------|
| 1 | Open (Hide developer tool's elements, console, and other panels, valid for kernel 130 and above) |
| 2 | Close (Display developer tool's elements, console, and other panels, valid for kernel 130 and above) |

## Variable: language_type (Language Type)

| Value | Meaning |
|-------|---------|
| 1 | Random |
| 2 | Custom |

## Variable: timezone_type (Time Zone Type)

| Value | Meaning |
|-------|---------|
| 1 | Random |
| 2 | Custom |

## Variable: location (Geolocation Type)

| Value | Meaning |
|-------|---------|
| 1 | Ask |
| 2 | Allow |
| 3 | Block |

## Variable: location_type (Whether to enable geolocation)

| Value | Meaning |
|-------|---------|
| 0 | Close |
| 1 | Enable |

## Variable: resolving_power_type (Resolution Type)

| Value | Meaning |
|-------|---------|
| 1 | Random |
| 2 | Custom |

## Variable: fonts_type (Font)

| Value | Meaning |
|-------|---------|
| 1 | System Default |
| 2 | Custom |

## Variable: canvas_type (Canvas)

| Value | Meaning |
|-------|---------|
| 0 | Close |
| 1 | Random |

## Variable: webgl_data_type (WebGL Metadata)

| Value | Meaning |
|-------|---------|
| 1 | Random |
| 2 | Custom |
| 3 | Close(uses default WebGL Info of the current computer) |

## Variable: webgpu_data_type (WebGPU)

| Value | Meaning |
|-------|---------|
| 0 | Disable |
| 1 | Real |
| 2 | Based on WebGL |

## Variable: javascript_memory_type (JavaScript Memory Restrictions)

| Value | Meaning |
|-------|---------|
| 0 | Default |
| 1 | Maximum |

## Variable: client_rects (Noise)

| Value | Meaning |
|-------|---------|
| 0 | Close |
| 1 | Random |

## Variable: speech_voices (SpeechVoices)

| Value | Meaning |
|-------|---------|
| 0 | Close |
| 1 | Random |

## Variable: device_name_source (Device Name Source)

| Value | Meaning |
|-------|---------|
| 0 | Close |
| 1 | Enable |
| 2 | Custom |

## Variable: track (Do Not Track)

| Value | Meaning |
|-------|---------|
| 0 | Close |
| 1 | Default |
| 2 | Enable |

## Variable: allow_scan_ports (Port Scan Protection)

| Value | Meaning |
|-------|---------|
| 0 | Close |
| 1 | Enable |

## Variable: cloudflare_challenge_bypassing (Cloudflare Verification Optimization)

| Value | Meaning |
|-------|---------|
| 0 | Close(Fully retain the anti-detection function, but this may disrupt the 5-second verification challenge, potentially leaving visitors stuck on the verification page.) |
| 1 | Enable(Relax certain anti-detection mechanisms to reduce the impact on the 5-second verification challenge and improve compatibility, but this may slightly increase the probability of being identified as a robot.) |

## Variable: transfer_proxy (Transfer Proxy)

| Value | Meaning |
|-------|---------|
| 0 | Don't Transfer |
| 1 | Transfer |

## Variable: transfer_proxy_mode (Options of Transfering Proxy)

| Value | Meaning |
|-------|---------|
| 1 | Proxy Sharing(The recipient can continue to use the proxy) |
| 2 | Proxy Transfer(The recipient can not only continue to use it but also renew it for long-term holding) |

## Variable: transfer_note (Transfer Notes)

| Value | Meaning |
|-------|---------|
| 0 | Don't Transfer |
| 1 | Transfer |