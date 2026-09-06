# GitHub Action: Run VSCode Server

Runs a web version of Visual Studio Code in the background.  
Useful for debugging GitHub Actions.

```yaml
- uses: zongou/run-vscode-server@main
  name: Run vscode server
  with:
    # Connection token for vscode server, required, you should append `?tkn=your_token` to the output url to authenticate the server.
    connection-token: ${{ inputs.connection-token || secrets.VSCODE_SERVER_CONNECTION_TOKEN }}
    # VSCode release quality, true for insider, false for stable, default is false, not required.
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



| **Input**                         | **Description**                                                      | **Default**                                                    | **Required** |
| --------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------- | ------------ |
| **<code>connection-token</code>** | connection token for vscode server                                   | <code></code>                                                  | **true**     |
| **<code>insider</code>**          | true for insider quality, false for stable quality, default is false | <code>false</code>                                             | **false**    |
| **<code>settings</code>**         | vscode settings                                                      | <code>{ "workbench.colorTheme": "Default Dark Modern" }</code> | **false**    |
