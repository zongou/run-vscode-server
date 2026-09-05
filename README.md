# GitHub Action: Run VSCode Server

Runs a web version of Visual Studio Code in the background.  
Useful for debugging GitHub Actions.

```yaml
# Please set your secrects.VSCODE_SERVER_CONNECTION_TOKEN before use
- uses: zongou/run-vscode-server@main
  name: Run vscode server
  with:
    # vscode quality, optional, default value "stable", can be "stable" or "insider"
    insider: false
    # vscode settings, optional, default sets color theme to "Default Dark Modern"
    settings:
      default: |
        {
            "workbench.colorTheme": "Default Dark Modern"
        }

- name: Keep alive
  run: sleep 6h
```

append `?tkn=your_token_here` to the url to authenticate the server.

| **Input**                 | **Description**                                                      | **Default**                                                    | **Required** |
| ------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------- | ------------ |
| **<code>insider</code>**  | true for insider quality, false for stable quality, default is false | <code>false</code>                                             | **false**    |
| **<code>settings</code>** | vscode Settings                                                      | <code>{ "workbench.colorTheme": "Default Dark Modern" }</code> | **false**    |
