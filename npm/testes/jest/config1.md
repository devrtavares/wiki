# nodejs 

<sub>[:arrow_upper_left: jest](readme.md)<sub>

## *jest.config.js - exemplo 1*

```dash
npx jest --init
```
- formulário de pré-configuração:
    ```dash
    Would you like to use Jest when running "test" script in "package.json"? ... yes
    Choose the test environment that will be used for testing » ... node
    Do you want Jest to add coverage reports? ... no
    Automatically clear mock calls and instances between every test? ... yes
    ``` 

- **jest.config.js**
    ```diff
    // A preset that is used as a base for Jest's configuration
    - // preset: undefined,
    + preset: 'ts-jest',
    ```

    - **conflitos com eslint**
        - .eslintrc...
        <br/><sub> no arquivo de configurações do eslint, basta incluir o jest como true
        ```diff
        "env": {
            "browser": true,
            "es2021": true,
        +    "node": true
        +    "jest": true
        },
        ```