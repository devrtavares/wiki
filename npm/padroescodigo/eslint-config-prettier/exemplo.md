# npm

<sub>[:arrow_upper_left: padrões de código](../readme.md)</sub>

## resumo :: eslint-config-prettier 

- **instalações**:
    - git
        ```diff
        cd /d Desktop
        mkdir "novo-modulo"
        cd /d "novo-modulo"
        + git init
        ```
        - <sub>*(opcional) incluir linha: "node_modules" salvar e fechar*</sub>
            ```diff
            + notepad .gitignore 
            ```
            - <sub>*(opcional) criar versão*</sub>
                ```diff
                + git add .gitignore
                - git commit -m "chore: module started"
                ```
    - npm
        ```diff
        + npm init -y
        ```
        - <sub>*(opcional) criar versão*</sub>

            ```diff
            + git add package.json
            - git commit -m "chore: add package manager"
            ```

    ```diff
    + npm install -D 
        typescript @types/node
        eslint @typescript-eslint/parser
        @typescript-eslint/eslint-plugin
        prettier eslint-config-prettier
        husky lint-staged
    ```

- **execuções**:
    ```diff
    + npx tsc --init
    + npx .\node_modules\.bin\eslint --init
    + npx husky install
    + npx husky add .husky/pre-commit "npx lint-staged"

    + npm set-script dev "tsc --watch"
    + npm set-script prepare "husky install"
    + npm set-script lint "eslint --ignore-path .gitignore --ext .js,.ts ."
    + npm set-script format "prettier --ignore-path .gitignore --write \"**/*.+(js|ts|json)\""
    ```


- **arquivos**:

    - gitignore
        ```bash
        build
        coverage
        node_modules
        dist
        ```

    - package.json:
        ```json
        {
            "name": "novo-modulo",
            "version": "1.0.0",
            "description": "",
            "main": "index.js",
            "scripts": {
                "dev": "tsc --watch",
                "lint": "eslint --ignore-path .eslintignore --ext .js,.ts .",
                "format": "prettier --ignore-path .gitignore --write \"**/*.+(js|ts|json)\""
            },
            "keywords": [],
            "author": "",
            "license": "ISC",
            "devDependencies": {
                "@types/node": "^17.0.8",
                "@typescript-eslint/eslint-plugin": "^5.9.1",
                "@typescript-eslint/parser": "^5.9.1",
                "eslint": "^8.6.0",
                "eslint-config-prettier": "^8.3.0",
                "husky": "^7.0.4",
                "lint-staged": "^12.1.7",
                "prettier": "^2.5.1",
                "typescript": "^4.5.4"
            },
            "lint-staged": {
                "*.ts": [
                    "eslint 'src/**' --ignore-path .gitignore --fix"
                ],
                "**/*": "prettier --write --ignore-unknown"
            }
        }
        ```

    - tsconfig.json
        ```json
        {
            "compilerOptions": {
                "outDir": "dist", 
                "target": "es2020",
                "module": "commonjs",
                "esModuleInterop": true,
                "forceConsistentCasingInFileNames": true,
                "strict": true,
                "skipLibCheck": true,
                "noImplicitAny": true, 
            }, 
            "include": ["src"],
            "exclude": ["node_modules"],
        }

        ```

    - .eslintrc
        ```diff
        {
            "env": {
                "browser": true,
                "es2021": true
            },
            "extends": [
                "eslint:recommended",
                "plugin:@typescript-eslint/recommended",
                "prettier"
            ],
            "parser": "@typescript-eslint/parser",
            "parserOptions": {
                "ecmaVersion": 13,
                "sourceType": "module"
            },
            "plugins": ["@typescript-eslint"],
            "rules": {
                "@typescript-eslint/no-unused-vars": "error",
                "@typescript-eslint/consistent-type-definitions": ["error", "type"]
            }
        }

        ```

    - .prettierrc
        ```json
        {
            "semi": false,
            "singleQuote": true,
            "arrowParens": "avoid"
        }
        ```

    [referencia](https://blog.logrocket.com/linting-typescript-using-eslint-and-prettier/)