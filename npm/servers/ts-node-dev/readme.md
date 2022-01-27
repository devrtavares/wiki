# nodejs 

<sub>[:arrow_upper_left: servidores web](../readme.md) --- [trends](https://openbase.com/js/ts-node-dev) --- [exemplo](exemplo.md)<sub>

## *ts-node-dev*


- instalação
  ```bash
  npm install -g ts-node-dev # or using yarn: yarn global add ts-node-dev
  npm install --save-dev ts-node-dev # or using yarn: yarn add ts-node-dev -D
  ```

  - uso

    ```json
    ts-node-dev [node-dev|ts-node flags] [ts-node-dev flags] [node cli flags] [--] [script] [script arguments]
    ```

    -  --package.json ***--exemplo***
      ```json
      scripts: {
        "dev" : "dev ts-node-dev --respawn --transpile-only --ignore-watch node_modules --no-notify src/server.ts"
      }

      ```


