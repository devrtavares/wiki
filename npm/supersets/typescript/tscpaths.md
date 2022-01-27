# tsconfig.json

<sub>[:arrow_upper_left: paths](paths.md)<sub>

- **tscpaths**

    ```bash
    npm i -D tscpaths
    npx tsc
    ```

    - **package.json**

        - **scripts**

            ```json
            "scripts": {
              "build": "tsc --project tsconfig.json && tscpaths -p tsconfig.json -s ./src -o ./out",
            }
            ```

            - Options

                | flag | description |
                |--|--|
                | -p --project | 	project configuration file (tsconfig.json)
                | -s --src | 	source code root directory
                | -o --out | 	output directory of transpiled code (tsc --outDir)