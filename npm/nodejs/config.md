# nodejs

<sub>[:arrow_upper_left: node em módulos](../readme.md)<sub>

## :file_folder: ***package.json***
&nbsp;&nbsp;&nbsp;&nbsp;*- arquivo para controle de pacotes e suas versões* <br/>&nbsp;&nbsp;&nbsp;&nbsp;*- gerado automáticamente ou manualmente*

- ***automáticamente por terminal de comandos***
    ```bash
    npm init -y
    ```

    - `npm init`
    <br/>&nbsp;&nbsp;&nbsp;&nbsp;*- cria o arquivo **package.json***
    <br/>&nbsp;&nbsp;&nbsp;&nbsp;*- apresenta questionário sobre informações do **módulo***
    - `npm init -y`
<br/>&nbsp;&nbsp;&nbsp;&nbsp;--y ou -yes (*pula o questionário*)
        - ***exemplo***
            ```bash
            cd /d Desktop/novo-modulo
            npm init -y
            git add package.json
            git commit -m "chore: add node package manager"
            ```
