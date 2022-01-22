# git

<sub>[:arrow_upper_left: git](readme.md) ---  [*git-scm.com/**documentação***](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases) --- [*teste com padrão de commit*](../../npm/padraocommit/git-commit-msg-linter/teste.md)<sub>

## *apelidos*

### incluíndo apelidos

&nbsp;&nbsp;&nbsp;&nbsp;*incluindo apelidos para os comandos mais usados:
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- facilitamos o uso da ferramenta
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- ganhamos tempo e produtividade*


- :file_folder: **por editor de arquivo de texto** <sub>***.gitconfig***</sub>
<br/>&nbsp;&nbsp;&nbsp;&nbsp;*Editar configurações diretamente no arquivo*

    1. &nbsp;&nbsp;&nbsp;&nbsp;`git config --global --edit`<br/>

        &nbsp;&nbsp;&nbsp;&nbsp;*Arquivo:*
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

- **por comando** <sub>***.gitconfig***</sub>
<br/>&nbsp;&nbsp;&nbsp;&nbsp;*Editar configurações por parâmetro*

    1. &nbsp;&nbsp;&nbsp;&nbsp;apelido: `git s`<br/>

        &nbsp;&nbsp;&nbsp;&nbsp;*comando:*
        `git config --global alias.s "!git status -s"`

    2. &nbsp;&nbsp;&nbsp;&nbsp;apelido: `git c`<br/>

        &nbsp;&nbsp;&nbsp;&nbsp;*comando:*
        `git config --global alias.c "!git add --all && git commit -m"
        `

    3. &nbsp;&nbsp;&nbsp;&nbsp;apelido: `git l`<br/>

        &nbsp;&nbsp;&nbsp;&nbsp;*comando:*
        `git config --global alias.l "!git log --pretty=format:'%C(blue)%h %C(red)%d %C(white)%s - %C(cyan)%cn, %C(green)%cr'"
        `
    


### [*sugestões*](https://haacked.com/archive/2014/07/28/github-flow-aliases/)

```bash
[alias]
co = checkout
ec = config --global -e
up = !git pull --rebase --prune $@ && git submodule update --init --recursive
cob = checkout -b
cm = !git add -A && git commit -m
save = !git add -A && git commit -m 'SAVEPOINT'
wip = !git add -u && git commit -m "WIP"
undo = reset HEAD~1 --mixed
amend = commit -a --amend
wipe = !git add -A && git commit -qm 'WIPE SAVEPOINT' && git reset HEAD~1 --hard
bclean = "!f() { DEFAULT=$(git default); git branch --merged ${1-$DEFAULT} | grep -v " ${1-$DEFAULT}$" | xargs git branch -d; }; f"
bdone = "!f() { DEFAULT=$(git default); git checkout ${1-$DEFAULT} && git up && git bclean ${1-$DEFAULT}; }; f"
```
