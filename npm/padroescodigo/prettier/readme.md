# npm

<sub>[:arrow_upper_left: padrões de código](../readme.md) \| [prettier.io](https://prettier.io/)<sub>

## prettier 

- **Instalação \| *(extensão para code: [**esbenp.prettier-vscode**](../../../utils/ide/vscode/esbenp-prettier-vscode.md))***
    ```bash
    npm install --D prettier
    ```
    - *(opcional)*
        ```bash
        npm set-script format "prettier --ignore-path .gitignore --write \"**/*.+(js|ts|json)\""
        npm run format
        ```

- **configurações** *(arquivos)*
    - **.prettierrc**
        ```json
        // .prettierrc
        {
          "semi": false, // Specify if you want to print semicolons at the end of statements
          "singleQuote": true, // If you want to use single quotes
          "arrowParens": "avoid" // Include parenthesis around a sole arrow function parameter
        }
        ```

    - **package.json**:
        ```json
        {
        // ...
        "scripts": {
            "dev": "tsc --watch",
            "lint": "eslint --ext .js,.ts .",
            "format": "prettier --ignore-path .gitignore --write \"**/*.+(js|ts|json)\""
        },
        // ...
        }
        ```

    - **.prettierignore**

        *ignorar arquivos e diretórios para formatação, podemos subistitui-lo pelo .gitignore a fim de ter um único ponto de verdade*

- **formatando arquivo:**
    ```bash
    npx prettier --write src/index.ts
    ```

[*referencia*](https://prettier.io/docs/en/install.html)