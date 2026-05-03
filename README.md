<!-- start title -->

# GitHub Action: Run vscode Server

<!-- end title -->
<!-- start description -->

Runs a web version of Visual Studio Code to debug GitHub Actions.

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: zongou/run-vscode-server@0.0.3
  name: Run vscode server to debug
  if: ${{ failure() }}
  # with:
  #   # vscode quality, optional, default value "stable", can be "stable" or "insider"
  #   quality: "stable"
  #   # vscode settings, optional, default sets color theme to "Default Dark Modern"
  #   settings:
  #     default: |
  #       {
  #           "workbench.colorTheme": "Default Dark Modern"
  #       }
```

<!-- end usage -->
<!-- start inputs -->

| **Input**                 | **Description**  | **Default**                                                    | **Required** |
| ------------------------- | ---------------- | -------------------------------------------------------------- | ------------ |
| **<code>quality</code>**  | vscode quality  | <code>stable</code>                                            | **false**    |
| **<code>settings</code>** | vscode Settings | <code>{ "workbench.colorTheme": "Default Dark Modern" }</code> | **false**    |

<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start [.github/ghadocs/examples/] -->
<!-- end [.github/ghadocs/examples/] -->
