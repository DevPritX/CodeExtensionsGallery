# Hello World Chrome Extension

![Hello World Icon](./images/128_HelloWorld.png)

## Overview

Welcome to the **Hello World** Chrome Extension project! This is the first extension created by Pritam Satapathy (GitHub: pritamUGDeveloper). The extension is a simple, fun project designed to get hands-on experience with developing Chrome extensions. It displays a friendly "Hello World" message to users and includes basic functionalities to showcase the foundational aspects of extension development.

## Features

- **Manifest Version 3**: Utilizes the latest version of the Chrome Extensions Manifest, ensuring modern features and security.
- **Simple Interface**: A clean and straightforward popup displaying "Hello World".
- **Permissions**: Requires minimal permissions for active tab and storage.
- **Content Script**: Injects JavaScript into all web pages.
- **Background Script**: Handles background tasks via a service worker.
- **Custom Icons**: Includes custom icons in various sizes for a polished look.
- **Options Page**: Placeholder for future configurations and settings.

## File Structure

### `manifest.json`
This file defines the extension's properties, permissions, and resources.

```json
{
    "manifest_version": 3,
    "name": "Hello World",
    "description": "An Simple Hello World Extension Made for Fun (1st Time Trial Extension made for Practice)",
    "version": "1.0",
    "permissions": [
        "activeTab",
        "storage"
    ],
    "background": {
        "service_worker": "/background.js"
    },
    "content_scripts": [
        {
            "matches": ["<all_urls>"],
            "js": ["/content.js"]
        }
    ],
    "action": {
        "default_popup": "/popup.html",
        "default_icon": {
            "48": "/images/48_HelloWorld.png",
            "64": "/images/64_HelloWorld.png",
            "128": "/images/128_HelloWorld.png"
        }
    },
    "options_page": "/options.html",
    "icons": {
        "48": "/images/48_HelloWorld.png",
        "64": "/images/64_HelloWorld.png",
        "128": "/images/128_HelloWorld.png"
    }
}
