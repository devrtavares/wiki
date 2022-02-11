# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](../readme.md) <sub>

### Configurando uso de bootstrap para estilização


1. **bootstrap - Instalação**
    ```bash
    npm install save-dev bootstrap@3
    ```

2. **Configuração**
    - :page_facing_up: **angular.json**
        ```diff
        ...
        "architect": {
            ...
            "build": {
                "styles": [
        +           "node_modules/bootstrap/dist/css/bootstrap.min.css",
                    "src/styles.css"
                ],
                ...
        }
        ...
        ```
3. **Teste**
    - executar o comando **`ng serve`**
    - abrir o navegador e verificar através da inspeção de elementos
        - localhost:[1~4200]
            - Sources
                - styles.css
                    - menção ao bootstrap
                        ```css
                        /*!
                         * Bootstrap vx.x.x (https://getbootstrap.com/)
                         * Copyright xxxx-xxx Twitter, Inc.
                         */
                        ```

<br/><br/><br/>

<image src="img/checkbootstrapv3.png" width="912px" height="322px"/>

<sub></sub>
---
<image src="../../img/icon.svg" width="34px" height="36px"/>

&nbsp;
