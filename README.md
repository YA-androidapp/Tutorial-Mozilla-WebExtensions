# Tutorial-Mozilla-WebExtensions

---

* [ブラウザー拡張機能](https://developer.mozilla.org/ja/docs/Mozilla/Add-ons/WebExtensions)
  * [mdn/webextensions-examples](https://github.com/mdn/webextensions-examples)

---

<br><br><br><br>

## borderify

```bash
mkdir borderify
cd borderify
```

<br><br><br>

### Download an icon file

```bash
wget https://github.com/mdn/webextensions-examples/raw/master/borderify/icons/border-48.png -O icons/border-48.png
```

<br><br><br>

### manifest.json

```bash
nano manifest.json
```

```json
{
    "manifest_version": 2,
    "name": "Borderify",
    "version": "1.0",
    "description": "Adds a solid red border to all webpages matching mozilla.org.",
    "icons": {
        "48": "icons/border-48.png"
    },
    "content_scripts": [
        {
            "matches": [
                "*://*.mozilla.org/*"
            ],
            "js": [
                "borderify.js"
            ]
        }
    ]
}
```

<br><br><br>

### borderify.js

```bash
nano borderify.js
```

```js
document.body.style.border = "5px solid red";
```

<br><br><br>

### Load the extension

* [about:debugging](about:debugging)

![borderify01.png](img/borderify01.png "borderify01.png")

![borderify02.png](img/borderify02.png "borderify02.png")

![borderify03.png](img/borderify03.png "borderify03.png")

---

Copyright (c) 2022 YA-androidapp(https://github.com/YA-androidapp) All rights reserved.
