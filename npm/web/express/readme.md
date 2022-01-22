# nodejs web frameworks

<sub>[:arrow_upper_left: nodejs web frameworks](../readme.md) --- [expressjs.com](https://expressjs.com/) --- [**sobre o expressjs**](about.md) <sub>


## expressjs

- instalação

    ```bash
    npm install -D express
    ```
    - *(opcional) dependencia para typescript*
        
        ```json
        npm install -D @types/express
        ```

- *package.json - scripts*
    ```json
    "dev": "node src/server.ts"
    ```

- *server de exemplo*
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

