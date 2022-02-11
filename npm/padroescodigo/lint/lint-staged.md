# nodejs 

<sub>[:arrow_upper_left: padrões de código](../../padroescodigo/eslintprettier.md) -- [:arrow_upper_left: hooks](../../hooks/readme.md)<sub>

## *lint-staged*

- ***Instalação***
    ```dash
    npm install -D lint-staged
    ```
        
    - ***arquivo de configurações***
        ```bash
        "lint-staged": {
            "*.ts": [
                "eslint 'src/**' --ignore-path .gitignore --fix"
            ],
            "**/*": "prettier --write --ignore-unknown"
        }
        ```

        - **filtros de arquivo**
            - Se o padrão glob não contiver barras (/), a opção matchBase do micromatch será habilitada, então os globs correspondem ao nome base de um arquivo, independentemente do diretório:
                - "*.js" corresponderá a todos os arquivos JS, como /teste.js e /foo/bar/teste.js
                - "!(*teste).js". corresponderá a todos os arquivos JS, exceto aqueles que terminam em teste.js, então foo.js, mas não foo.teste.js
            - Se o padrão glob contiver uma barra (/), ele também corresponderá aos caminhos:
                - "./*.js" corresponderá a todos os arquivos JS na raiz do repositório git, então /teste.js, mas não /foo/bar/teste.js
                - "foo/**/\*.js" corresponderá a todos os arquivos JS dentro do diretório/foo, então/foo/bar/teste.jsmas não/teste.js
            - *package.json*
                ```bash
                {
                    "lint-staged": {
                        "*": "seu-cmd"
                    }
                }
                ```
            - *.lintstagedrc*
                ```bash
                {
                    "*": "seu-cmd"
                }
                ```
    - alterar arquivo de configurações
        - `npx lint-staged`
            - `--config` [path]: <br/>Especifique manualmente um caminho para um arquivo de configuração ou nome de pacote npm. <sub>Observação: quando usado, o lint-staged não realizará a pesquisa do arquivo de configuração e imprimirá um erro se o arquivo especificado não puder ser encontrado. Se '-' for fornecido como o nome do arquivo, a configuração será lida de stdin, permitindo a tubulação na configuração como cat my-config.json</sub> <br/>
                - `npx lint-staged --config`
                    - exemplo
                        ```bash
                        npx lint-staged --config .lintstagedrc
                        ```     