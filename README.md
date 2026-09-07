# GitHub Action: Run VSCode Server

Runs a web version of Visual Studio Code in the background.  
Useful for debugging GitHub Actions.

```yaml
- uses: zongou/run-vscode-server@main
  name: Run vscode server
  with:
    # Connection token for vscode server, required
    # After link is generated, append `?tkn=your_token` to the output url to authenticate.
    token: ${{ inputs.vscode-server-token || secrets.VSCODE_SERVER_TOKEN }}
    # # Release quality of vscode server, true for insider, false for stable, default is false, not required.
    # insider: false
    # # JSON string of vscode settings, optional, default sets color theme to "Default Dark Modern"
    # settings:
    #   default: |
    #     {
    #         "workbench.colorTheme": "Default Dark Modern"
    #     }

- name: Keep alive
  shell: bash
  run: sleep 6h
```

| **Input**                 | **Description**                                                      | **Default**                                                    | **Required** |
| ------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------- | ------------ |
| **<code>token</code>**    | Connection token for vscode server                                   | <code></code>                                                  | **true**     |
| **<code>insider</code>**  | Release quality of vscode server, true for insider, false for stable | <code>false</code>                                             | **false**    |
| **<code>settings</code>** | JSON string of vscode settings                                       | <code>{ "workbench.colorTheme": "Default Dark Modern" }</code> | **false**    |
