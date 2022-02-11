# vs-code

<sub>[:arrow_upper_left: home](../../../README.md) --[recomendações](vsutils.recs.md) <sub>

- *adicionar e remover extenções ao vscode por terminal de comando*

## extenções 
- listar
    ```bash
    code --list-extensions
    ```
- adicionar
    ```bash
    code --install-extension
    ```
- remover 
    ```bash
    code --uninstall-extension
    ```

### lista de extenções

- [`vscode-icons`](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)

    - 
        ```bash
        code --install-extension vscode-icons-team.vscode-icons
        ```
        <image src="../../../imgs/vscode-icons-team.vscode-icons.png" height="50" width="300"/>

- [`GitHub Markdown Preview`](https://marketplace.visualstudio.com/items?itemName=bierner.github-markdown-preview)

    - 
        ```bash
        code --install-extension bierner.github-markdown-preview
        ```
        <image src="../../../imgs/github-markdown-preview-github.png" height="50" width="300"/>


- [`jest-snippets`](https://marketplace.visualstudio.com/items?itemName=andys8.jest-snippets)



    - 
        ```bash
        code --install-extension andys8.jest-snippets
        ```
        <image src="../../../imgs/ts-ext-jestcodesnipperts.PNG" height="50" width="300"/>

- [`thekalinga.bootstrap4-vscode`](https://marketplace.visualstudio.com/items?itemName=thekalinga.bootstrap4-vscode)

    - 
        ```bash
        code --install-extension thekalinga.bootstrap4-vscode
        ```



- [`dbaeumer.vscode-eslint`](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

    - 
        ```bash
        code --install-extension dbaeumer.vscode-eslint
        ```
        
       [<image src="../../../imgs/ide-vscode-plugin-eslint.png" height="50" width="300"/>](dbaeumer-vscode-eslintc.md)
        

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

- [`esbenp-prettier-vscode`](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

    - 
        ```bash
        code --install-extension esbenp.prettier-vscode
        ```
        
       [prettier](esbenp-prettier-vscode.md)

        - [**settings.json**](../../../utils/ide/vscode/settings.md) - ***formatação do visual studio code:***
        <br/><sup>substituir formatação pela extenção prettier
        esbenp.prettier-vscode</sup>
            ```bash
            // settings.json
            {
            "editor.defaultFormatter": "esbenp.prettier-vscode",
            "editor.formatOnSave": true,
            "editor.formatOnPaste": false
            ...
            }
            ```

<sup></sup>
---
<image src="../../../imgs/ide-vscode.png" height="30" width="30"/>