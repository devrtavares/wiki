# npm

<sub>[:arrow_upper_left: padrões de código](../eslintprettier.md)</sub>

## eslint-config-prettier 

- Requisitos:

    *Instalados e configurados eslint e prettier*

    - **Instalação**
        ```
        npm install --D eslint-config-prettier
        ```
    - **configurações**
        - *.eslintrc:*
            ```diff
            -{
            -  "parser": "@typescript-eslint/parser",
            -  "parserOptions": {
            -      "ecmaVersion": 12,
            -      "sourceType": "module",
            -  },
            -  "plugins": ["@typescript-eslint"],
            -  // HERE
            +  "extends": ["eslint:recommended", "plugin:@typescript-eslint/recommended", "prettier"],
            - 
            -  "rules": {
            -    "@typescript-eslint/no-unused-vars": "error",
            -    "@typescript-eslint/consistent-type-definitions": ["error", "type"],
            -},

 