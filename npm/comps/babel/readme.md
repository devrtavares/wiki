# nodejs

<sub>[:arrow_upper_left: compiladores](../readme.md)  <sub>

- babel
```bash
npm i -D @babel/cli @babel/core @babel/node @babel/preset-env @babel/preset-typescript babel-plugin-module-resolver
```
- **configurações**

    - package.json
        - "scripts
            ```json
            "build": "babel src --extensions \".js,.ts\" --out-dir dist --copy-files --no-copy-ignored"
            ```
            - terminal
                ```bash
                npm set-script build "babel src --extensions \"".js,.ts\"" --out-dir dist --copy-files --no-copy-ignored"
                ```
    - **babel.config.json**<br/><sub>&nbsp;&nbsp;&nbsp;&nbsp;vamos adicionar o arquivo manualmente</sub>
        ```json
        module.exports = {
          presets: [
            [
              '@babel/preset-env',
              {
                targets: {
                  node: 'current'
                }
              }
            ],
            '@babel/preset-typescript'
          ],
          plugins: [
            ['module-resolver', {
              alias: {
                '@controllers': './src/controllers',
                '@models': './src/models',
                '@views': './src/views',
                '@configs': './src/config'
              }
            }]
          ],
          ignore: [
            '**/*.spec.ts'
          ]
        }

        ```
