# nodejs 

<sub>[:arrow_upper_left: hooks](../readme.md) | [**exemplo.zip**](exemplo.zip)<sub>

## *jest - resumo*

- instalações
    ```bash
    npm i -D git-commit-msg-linter typescript @types/node express husky lint-staged eslint @eslint/create-config @typescript-eslint/parser @typescript-eslint/eslint-plugin prettier eslint-config-prettier jest @types/jest ts-jest
    ```
    - configurações
        ```bash
        npx tsc --init
        npx eslint --init
        npm set-script prepare "husky install"
        npm run prepare
        npx husky add .husky/pre-commit "npx lint-staged"
        jest --init
        ```
        - scripts
            ```bash
            npm set-script dev "tsc --watch"
            npm set-script "test" "jest --passWithNoTests"
            npm set-script "test:staged" "jest --passWithNoTests"
            npm set-script lint "eslint --ignore-path .gitignore --ext .js,.ts ."
            npm set-script format "prettier --ignore-path .gitignore --write \""**/*.+(js|ts|json)\"""
            ```
    - arquivos de configurações

        - .gitignore
            ```bash
            build
            coverage
            node_modules
            dist
            ```

        - ts-config.json
            ```bash
            {
            "compilerOptions": {
                "target": "es2016",
                "module": "commonjs",
                "rootDir": "./src",
                "allowJs": true,
                "outDir": "./dist",
                "noEmit": true,
                "esModuleInterop": true,
                "forceConsistentCasingInFileNames": true,
                "strict": true,
                "skipLibCheck": true
            }
            }
            ```

        - package.json
            ```bash
            "scripts": {
                "dev": "tsc --watch",
                "lint": "eslint --ignore-path .eslintignore --ext .js,.ts .",
                "format": "prettier --ignore-path .gitignore --write \"**/*.+(js|ts|json)\""
            },
            "lint-staged": {
                "*.ts": [
                    "eslint 'src/**' --ignore-path .gitignore --fix"
                ],
                "**/*": "prettier --write --ignore-unknown"
            }
            ```

        - .eslintrc
            ```bash
            "extends": [
                "eslint:recommended",
                "plugin:@typescript-eslint/recommended",
                "prettier"
            ],
            ```

        - .prettierrc
            ```bash
            {
            "semi": false,
            "singleQuote": true,
            "arrowParens": "avoid"
            }
            ```


        - .eslintignore
            ```bash
            jest.config.js
            ```

        - jest.config.js
            ```bash
            module.exports = {
            roots: ['<rootDir>/src'],
            collectCoverageFrom: ['<rootDir>/src/**/*.ts'],
            coverageDirectory: 'coverage',
            testEnvironment: 'node',
            transform: {
                '.+\\.ts$': 'ts-jest',
            },
            collectCoverage: true,
            clearMocks: true,
            coverageProvider: 'v8',
            }
            ```

