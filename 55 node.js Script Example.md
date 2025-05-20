# 55 node.js Script Example

---
title: "ixBrowser Local API"
source: "https://ixbrowser.com/doc/v2/local-api/en?target_id=906435d7-eabc-4da8-bac8-0774205c8d1f"
author:
published:
created: 2025-05-20
description:
tags:
  - "clippings"
---

## node.js Script Example

Update Time：2023-09-22 03:46:46

**demo:** [https://cdn.ixspy.com/ixbrowser/files/ixbrowser-local-api/node-demo/demo.zip](https://cdn.ixspy.com/ixbrowser/files/ixbrowser-local-api/node-demo/demo.zip)

### Script Example:

```javascript
const puppeteer = require('puppeteer-core');
const {ixbRequest} = require('./ixbRequest');

async function main() {
    const action = 'profile-open'
    const body = {
        "profile_id": 4186,
        "args": [
            "--disable-extension-welcome-page"
        ],
        "load_extensions": false,
        "load_profile_info_page": false,
        "cookies_backup": false,
        "cookie": ""
    }

    try {
        const response_body = await ixbRequest(action, body);

        /**your business code**/
        try {
            const browser = await puppeteer.connect({
                browserWSEndpoint: response_body.data.ws
            });
            const page = await browser.newPage();
            await page.goto('https://www.ixbrowser.com');
            await page.waitForTimeout(5000);
            await browser.close();
        } catch (err) {
            console.log(err.message);
        }
        /** end **/

    } catch (error) {
        console.error(error.code);
        console.error(error.message);
    }
}

main();
```