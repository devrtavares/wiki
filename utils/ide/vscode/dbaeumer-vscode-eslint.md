# vs-code

<sub>[:arrow_upper_left: vs-code](readme.md) --[npm-eslint](../../../npm/padroescodigo/readme.md) --[marketplace](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) <sub>

### eslint integrado ao visual studio code

- ***instalação via terminal:***
    ```bash
    code --list-extensions
    code --install-extension dbaeumer.vscode-eslint
    ```
    - remoção:
        ```bash
        code --uninstall-extension dbaeumer.vscode-eslint
        ```

- [**settings.json**](../../../utils/ide/vscode/settings.md) - ***formatação do visual studio code:***

    ```bash
    // settings.json
    {
        /* "eslint.validate": [
            "javascript",
            "javascriptreact",
            "typescript",
            "typescriptreact",
        ],*/
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        }
    ...
    }
    ```
<sup></sup>
---
<image src="../../../imgs/ide-vscode-plugin-eslint.png" height="40" width="190"/>