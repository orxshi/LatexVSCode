---
layout: default
title: VSCode installation
nav_order: 2
description: "VSCode installation and settings"
---

# VSCode installation

Go to [VSCode website](https://code.visualstudio.com/) and download the installer for Windows. Run the installer and follow the instructions to install VSCode on your computer.

# LaTeX extension in VSCode

In VSCode, click on the Extensions icon on the left sidebar (or press `ctrl-shift-x`), search for *LaTeX Workshop*, and click *Install* to install the extension.

# Turning off editor suggestions

In order to prevent editor (VSCode) suggestions getting in the way of Copilot suggestions, we will turn off editor suggestions.

In VSCode, type `ctrl-shift-p`, type *user settings*, click **Preferences: Open User Settings (Json)**. This will open the `settings.json` file. Paste the following lines into the file and save it.

```
{
    // To turn off suggestions by editor when you type \
    "editor.suggestOnTriggerCharacters": false,
    // To turn off suggestions by editor when you type a character after\
    "editor.quickSuggestions": {
        "other": "off",
        "comments": "off",
        "strings": "off"
    }
}
```