# git

<sub>[:arrow_upper_left: Git](readme.md)  <sub>

## *comandos locais*

### `git add .`<br />`git add [path]`
&nbsp;&nbsp;&nbsp;&nbsp;incluir arquivos alterados para versionamento<br/>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*pode ser feito por interface*

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;┌ **Visual Studio Code**<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ controle do código *(CTRL+SHIT+G)*<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ lista de alterações<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ arquivo<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└─ preparar alterações

### `git commit -m "texto"`
&nbsp;&nbsp;&nbsp;&nbsp;criar versão dos ***arquivos adiconais com git add***

### `git checkout {commit hash}`
&nbsp;&nbsp;&nbsp;&nbsp;retorna a versão

### `git reset HEAD^ or HEAD^^ --mixed`
&nbsp;&nbsp;&nbsp;&nbsp;retorna para 1 ou 2 commits

### `git revert HEAD & git revert <rev commit hash>`
&nbsp;&nbsp;&nbsp;&nbsp;cria um commit de reversão e escolhe o hash de retorno

### `git status`
&nbsp;&nbsp;&nbsp;&nbsp;exibe alterações 

### `git log`
&nbsp;&nbsp;&nbsp;&nbsp;lista de versões 

### `git rebase -i`
&nbsp;&nbsp;&nbsp;&nbsp;refatorar versões<br/>&nbsp;&nbsp;&nbsp;&nbsp;remover, unir ou alterar descritivo 
