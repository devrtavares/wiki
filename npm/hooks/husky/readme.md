# nodejs 

<sub>[:arrow_upper_left: hooks](../readme.md) --- [husky](https://typicode.github.io/husky.io/#/)<sub>

## *husky*


- ***Instalação***
    ```dash
    npm install -D husky lint-staged
    ```
    - ***Uso***
        ```dash
        npm set-script prepare "husky install"
        npm run prepare
        ```
        - ***incluir hook de pré-commit***
            ```dash
            npx husky add .husky/pre-commit "npx lint-staged"
            git add .husky/pre-commit
            ```

<sup></sup>
---

