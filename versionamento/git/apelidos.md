## *Apelidos*

<sub>[:arrow_upper_left:](readme.md)<sub>

1. Incluíndo apelidos

    Vamos facilitar o uso da ferramenta incluindo apelidos para os comandos mais utilizados:


    1. ##### Inclusão por editor de arquivo
        ###### ***edit*** :file_folder: **.gitconfig** 
        `git config --global --edit`<br/>
        &nbsp;&nbsp;&nbsp;&nbsp;*Editar configurações diretamente no arquivo*

        ```git
        [credential]
            helper = osxkeychain
        [user]
            name = Nome.Sobrenome
            email = nomesobrenome@domain.com
        [push]
            followTags = true
        [core]
            editor = code --wait
        [alias]
            s = !git status -s
            c = !git add --all && git commit -m
            l = !git log --pretty=format:'%C(blue)%h %C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'
        ```


    2. ##### Outro exemplo: Inclusão por comando

        ##### `git s`
        &nbsp;&nbsp;&nbsp;&nbsp;*comando:*<br/>&nbsp;&nbsp;&nbsp;&nbsp; `git config --global alias.s "!git status -s"`
        ##### `git c`
        &nbsp;&nbsp;&nbsp;&nbsp; *comando:*<br/>&nbsp;&nbsp;&nbsp;&nbsp; `git config --global alias.c "!git add --all && git commit -m"`
        ##### `git l`
        &nbsp;&nbsp;&nbsp;&nbsp; *comando:*<br/>&nbsp;&nbsp;&nbsp;&nbsp; `git config --global alias.l "!git log --pretty=format:'%C(blue)%h %C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'"`

