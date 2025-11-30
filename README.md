# list of config files

### VS Code

> [!NOTE]
> Files: `keybindings.json`, `settings.json`, `mcp.json` in `vscode/` folder

**Tip:** Enable "Settings Sync" in VS Code for automatic syncing across devices

Manual step - Copy configuration files to VS Code user directory:

```bash
cp vscode/* ~/Library/Application\ Support/Code/User/
```

### Maccy --clipbard manager

> [!NOTE]
> File: `org.p0deje.Maccy.plist` [[Link](https://github.com/p0deje/Maccy)]

First make sure the path to the preferences (Property list) has not been changed, it shold be at `~/Library/Containers/org.p0deje.Maccy/Data/Library/Preferences/org.p0deje.Maccy.plist`.

1. Replce the config `cp org.p0deje.Maccy.plist ~/Library/Containers/org.p0deje.Maccy/Data/Library/Preferences/org.p0deje.Maccy.plist`
2. `killall Maccy`
3. `open -a Maccy`

<details>
<summary>Click if you wanted to see the configs in an xml format.</summary>

1.  Convert preferences into xml:
    ```bash
    plutil -convert xml1 <paht_to_org.p0deje.Maccy.plist>
    ```
2.  Do your changes.
3.  Convert it back to binary:
`bash
      plutil -convert binary1 <paht_to_org.p0deje.Maccy.plist>
      `
</details>
