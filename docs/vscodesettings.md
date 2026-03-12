# Turning off editor suggestions

In order to prevent editor (VSCode) suggestions getting in the way of Copilot suggestions, we will turn off editor suggestions.

In VSCode, type ctrl-shift-p, type *user settings*, click *Preferences: Open User Settings (Json)*

```
{
    // To turn of suggestions by editor when you type \
    "editor.suggestOnTriggerCharacters": false,
    // To turn of suggestions by editor when you type a character after\
    "editor.quickSuggestions": {
        "other": "off",
        "comments": "off",
        "strings": "off"
    }
}
```