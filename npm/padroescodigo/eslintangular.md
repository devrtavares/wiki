# npm

<sub>[:arrow_upper_left: nodejs em módulos](readme.md) | [exemplo](eslintangular.zip)<sub>

### *ESLint + @angular/cli* <sub></sub>

- **Instalação**
  ```bash
  npm i -D @angular-eslint/schematics
  ng add @angular-eslint/schematics
  ```
    - dependencias
    <sup></sup>
        ```bash
        npm i -D @angular-eslint/schematics @angular-eslint/eslint-plugin @angular-eslint/eslint-plugin-template @angular-eslint/builder @angular-eslint/template-parser @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint @types/jasmine
        ```

    - Habilitar o standard style (ecma-262, ES2020)
        ```bash
        npm i -D eslint@^7.12.1 eslint-config-standard
        ```
        - dependencias
          ```bash
          npm i -D eslint@^7.12.1 eslint-config-standard eslint-plugin-import eslint-plugin-node eslint-plugin-promise
          ```
-eslintrc.json
```diff
{
  "root": true,
-  "ignorePatterns": [
-      "projets/**/*"
-  ]
  "overrides": [
    {
      "files": [
+        "*.{ts,js,json}"
      ],
+      "parser": "@typescript-eslint/parser",
      "parserOptions": {
        "project": [
          "tsconfig.json"
        ],
        "createDefaultProgram": true,
+        "ecmaVersion": "latest"
      },
+      "env": {
+        "browser": true,
+        "es2020": true,
+        "jasmine": true
+      },
      "extends": [
        "plugin:@angular-eslint/recommended",
        "plugin:@angular-eslint/template/process-inline-templates",
+        "standard"
      ],
      "rules": {
        "@angular-eslint/directive-selector": [
          "error",
          {
            "type": "attribute",
            "prefix": "app",
            "style": "camelCase"
          }
        ],
        "@angular-eslint/component-selector": [
          "error",
          {
            "type": "element",
            "prefix": "app",
            "style": "kebab-case"
          }
        ],
+        "no-useless-constructor": "off",
+        "no-unused-vars": "off"
      }
    },
    {
      "files": [
        "*.html"
      ],
      "extends": [
        "plugin:@angular-eslint/template/recommended"
      ],
      "rules": {}
    }
  ]
}
```