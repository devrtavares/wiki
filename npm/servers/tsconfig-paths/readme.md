# nodejs 

<sub>[:arrow_upper_left: servidores web](../readme.md)<sub>

## *tsconfig-paths*


- instalação
  ```bash
  npm install -g tsconfig-paths # or using yarn: yarn global add tsconfig-paths
  npm install --save-dev tsconfig-paths # or using yarn: yarn add tsconfig-paths -D
  ```

    - uso
    ```json
    tsconfig-paths/register
    ```

    - **package.json** 

        ```json
        scripts: {
        "dev": "ts-node-dev -r tsconfig-paths/register --respawn --transpile-only --ignore-watch node_modules --no-notify src/server.ts"
        }

        ```

