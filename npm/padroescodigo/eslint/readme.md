# npm

<sub>[:arrow_upper_left: padrões de código](../eslintprettier.md) --- [eslint.org](https://eslint.org/)

## eslint 

- **Instalação**
    ```
    npm i -D eslint
    ```
    - *(typescript) adicionar transição de arquivos  para eslint*
        ```
        npm i -D eslint @eslint/create-config @typescript-eslint/parser @typescript-eslint/eslint-plugin 
        ```

- **configurações**
    - *global:*
        ```
        npx eslint --init
        ```
    - ***save-dev**: - <sub>podemos iniciar apenas com esse comando e depois instalar as dependências em modo local: -D</sub>*
        ```
        npm i -D eslint @eslint/create-config
        npx eslint --init
        ```
        ou
        `yarn run eslint --init`
    
    - *questionário*:
        ```
        √ How would you like to use ESLint? · problems
        √ What type of modules does your project use? · esm
        √ Which framework does your project use? · none
        √ Does your project use TypeScript? · Yes
        √ Where does your code run? · browser
        √ What format do you want your config file to be in? · JSON
        Local ESLint installation not found.
        The config that you've selected requires the following dependencies:

        @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser@latest eslint@latest
        √ Would you like to install them now with npm? · No
        Successfully created .eslintrc.json
        ```

        ```bash
        npm install -D @typescript-eslint/eslint-plugin@latest @typescript-eslint/parser@latest eslint@latest
        ```
- **add. scripts**
    ```
    npm set-script lint "eslint --ignore-path .gitignore --ext .js, ."
    ```
    - *(opcional) incluir watch ao type-script-compiler*
        ```
        npm set-script lint "eslint --ignore-path .gitignore --ext .js,.ts ."
        npm set-script dev "tsc --watch"
        ```
- **Teste de correções**
    ```
    npm run lint -- --fix
    ```

[*referencia*](https://eslint.org/docs/user-guide/getting-started)