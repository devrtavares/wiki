# nodejs 

<sub>[:arrow_upper_left: ts-node-dev](../readme.md) --- [rocketseat](https://blog.rocketseat.com.br/ferramentas-de-compilacao-execucao-em-tempo-de-desenvolvimento-dos-projetos-em-node-js/) --- [youtube-rocketseat](https://www.youtube.com/watch?v=rCeGfFk-uCk)<sub>

## *ts-node-dev - exemplo*


- **package.json** 

    ```json
    scripts: {
      "dev": "ts-node-dev --respawn --transpile-only --ignore-watch node_modules --no-notify src/server.ts"
    }

    ```

    - **server.ts**
        ```javascript
        import express from "express";

        const app = express();

        app.get(`/`, (request, response) => {
        return response.json({ message: `hello World` });
        });

        app.listen(3333);

        ```
        - run
            ```bash
            npm run dev
            ```