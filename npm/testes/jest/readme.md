# nodejs 

<sub>[:arrow_upper_left: testes](../readme.md)  --- [exemplo - jest.config.js](exemplo.md) --- [**exemplo: node-setup.zip**](node-setup.zip) --- [resumo](resumo.md)<sub>

## *jest*

- ***Instalação* (extensão para code: [**jest-snippets**](../../../utils/ide/vscode/jest-snippets.md))** 
    ```dash
    npm install -D jest @types/jest
    ```
    - (typescript)
        ```dash
        npm install -D jest @types/jest ts-jest
        ```
- **configurações**
    - --***jest init***
        ```dash
        npx jest --init
        ```
        - [*exemplo 1*](config1.md), [*exemplo 2*](config2.md)

    - [***ts-jest --init***](https://kulshekhar.github.io/ts-jest/docs/getting-started/installation/)
        ```dash
        npx ts-jest config:init
        ```

     - ***jest paths***
        - .eslintrc...
        <br/><sub> no arquivo de configurações do eslint, na propriedade **"env"** basta incluir o node e jest como true

            ```diff
            "env": {
                "browser": true,
                "es2021": true,
            +    "node": true
            +    "jest": true
            },
            ```
     - ***jest e ESLint***
        - .eslintrc...
        <br/><sub> no arquivo de configurações do eslint, na propriedade **"env"** basta incluir o node e jest como true

            ```diff
            "env": {
                "browser": true,
                "es2021": true,
            +    "node": true
            +    "jest": true
            },
            ```
- ***package.json***
    ```dash
    "scripts": {
        "test": "jest --passWithNoTests",
        "test:staged": "jest --passWithNoTests"
    },
    ```
    - *incluir por comando:*
        ```bash
        npm set-script "test" "jest --passWithNoTests"
        npm set-script "test:staged" "jest --passWithNoTests"
        ```

<sup></sup>
---

