# git

<sub>[:arrow_upper_left: git](readme.md)<sub>

## .gitignore

ao trabalhar com git nem todos os arquivos precisam de controle de versão! Por esse motivo temos o .gitignore.
<br/> Um arquivo que ignora o controle de versão das pastas e arquivos descritos por ele. <br/>A exemplo módulos de código compartilhado não precisam de controle de versão.

---

1. Exemplos

    Vamos incluir no nosso módulo um arquivo chamado .gitignore  
    e edita-lo com o(s) nome(s) dos arquivos a serem ignorados.
    >O diretório **"node_modules"**
    >
    > - Terminal do Windows -
    >através do terminal, na pasta corrente do projeto, podemos executar o comando
    >```
    >cd /d "Desktop/novo-modulo"
    >code .gitignore
    >```
    >que ira incluir o arquivo no projeto e o deixando pronto para edição no visual studio code ou vim, vamos incluir uma linha com o valor "**node_modules"** e salvar o arquivo.
    > 
    ><img src="../../imgs/gitignore.gif" width="636" height="267"/>
    #### Exemplo 2: VS Code
    > Criar no diretório do projeto o arquivo .gitignore incluir em uma linha o valor "**node_modules**" e salvar o arquivo.