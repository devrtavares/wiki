#

<sub>[:arrow_upper_left:](readme.md)  <sub>

*Agora com o modulo instalado podemos testar a validação de formato para mensagens de commit*

- [`git s`](../../../versionamento/git/apelidos.md/)

- [`git c "add commit linter"`](../../../versionamento/git/apelidos.md/)

    Teste de commit com padrão de formatação
    
    *devera emitir uma mensagem de falha como:*
    ```
    ************* Mensagem de commit inválida **************
    mensagem de commit: add commit linter
    formato correto: <type>[scope]: <subject>
    exemplo: docs: Atualiza o README com link para a nova documentação

    type:
        feat     Adição de funcionalidade.
        fix      Correção de defeito.
        docs     Mudança em documentação.
        style    Mudança de formatação ou estilo, que não afeta a execução do código (espaço, tabulação, etc).
        refactor Mudança na organização do código, que não afeta o comportamento existente.
        test     Adição ou mudança de um teste.
    chore    Adição ou mudança em script de build, que não afeta o código de produção.
        perf     Mudança de código para melhoria de desempenho.
        ci       Mudança de configuração de integração contínua.
        build    Mudança em arquivos de build ou em dependências externas.
        temp     Commit temporário, que não deve ser incluído no CHANGELOG.

    scope:
        Opcional, pode ser qualquer coisa que especifique o escopo da mudança.
        Exemplos: subpacote, workspace, módulo, componente, página.

    subject:
        Breve resumo da mudança, escrito no tempo verbal presente. Começa com letra minúscula e não há ponto final.
    ```

[`git c "chore: add commit linter"`]()

*Respeitando o formado solicitado o commit ocorre com sucesso.*