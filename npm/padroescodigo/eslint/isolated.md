# npm

<sub>[:arrow_upper_left: padrões de código](../readme.md) --- [eslint.org](https://eslint.org/)

## eslint 

- **Instalação --- *(extensão para code: [**eslint**](../../../utils/ide/vscode/dbaeumer-vscode-eslint.md))***
    ```
    npm i -D eslint
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
        How would you like to use ESLint? · style
        √ What type of modules does your project use? · none
        √ Which framework does your project use? · none
        √ Does your project use TypeScript? · Yes
        √ Where does your code run? · browser
        √ How would you like to define a style for your project? · guide
        √ Which style guide do you want to follow? · standard
        √ What format do you want your config file to be in? · JSON
        Checking peerDependencies of eslint-config-standard@latest
        The config that you've selected requires the following dependencies:

        @typescript-eslint/eslint-plugin@latest eslint-config-standard@latest eslint@^7.12.1 eslint-plugin-import@^2.22.1 eslint-plugin-node@^11.1.0 eslint-plugin-promise@^4.2.1 || ^5.0.0 @typescript-eslint/parser@latest
        √ Would you like to install them now with npm? · No
        Successfully created .eslintrc.json file in ..\node-setup
        PS ..\node-setup> npm i -D @typescript-eslint/eslint-plugin@latest eslint-config-standard@latest eslint@^7.12.1 eslint-plugin-import@^2.22.1 eslint-plugin-node@^11.1.0 eslint-plugin-promise@^4.2.1 @typescript-eslint/parser@latest
        ```

        <image src="../../../imgs/eslint-installer-sample.gif">
- **incluir scripts**
    ```
    npm set-script lint "eslint --ignore-path .gitignore --ext .js, ."
    ```
    - *(opcional) incluir watch ao type-script-compiler*
        ```
        npm set-script lint "eslint --ignore-path .gitignore --ext .js,.ts ."
        npm set-script dev "tsc --watch"
        ```
- **teste de correções**
    ```
    npm run lint -- --fix
    ```
