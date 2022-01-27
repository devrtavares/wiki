# nodejs 

<sub>[:arrow_upper_left: jest](readme.md)<sub>

## *jest.config.js - exemplo 2*

```dash
jest.config.js
```

```dash
npx jest --init
```
- formulário de pré-configuração:
    ```dash
    Would you like to use Jest when running "test" script in "package.json"? ... yes
    Would you like to use Typescript for the configuration file? ... no
    Choose the test environment that will be used for testing » ... node
    Do you want Jest to add coverage reports? ... yes
    Which provider should be used to instrument code for coverage? ... v8
    Automatically clear mock calls and instances between every test? ... yes
    ``` 
    - **roots**
        ```dash
        roots: [
            "<rootDir>/src"
        ],
        ```
        
    - **collectCoverageFrom**
        ```dash
        collectCoverageFrom: ['<rootDir>/src/**/*.ts'],
        ```
        - de onde serão coletados nossos arquivos para cobertura de testes
    - **transform**
        ```dash
        transform: {'.+\\.ts$': 'ts-jest'}
        ```
        - o transform é importante, pois é onde informamos por expressão regular o formado dos arquivos de typescript, e os convertemos em javascript para o jest, que é a linguagem que o jest de fato entende