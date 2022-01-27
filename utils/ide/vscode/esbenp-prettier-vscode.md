# vs-code

<sub>[:arrow_upper_left: vs-code](readme.md) --- [npm-prettier](../../../npm/padroescodigo/prettier/readme.md)<sub>

## prettier - formatador de código

- ***instalação via terminal:***
    ```bash
    code --list-extensions
    code --install-extension esbenp.prettier-vscode
    ```
    - remoção:
        ```bash
        code --uninstall-extension esbenp.prettier-vscode
        ```
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
