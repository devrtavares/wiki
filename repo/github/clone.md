# github

<sub>[:arrow_upper_left: Integração](integrations.md) \| [comando clone](commands.md)<sub>

- *requisitos*:
    - [*autenticação configurada*](integrations.md)

## *clonar repositório*

### *usando [*sourcetree*](https://www.sourcetreeapp.com/) <sub>(cliente git para windows)<sub>*
1. <sub>[*Importar chave privada*](sourcetreessh.md)</sub>
2. através da interface do **sourcetree**
```
┌─ sourcetree
└── 1. New tab
    └── Clone
        └── fonte: git@github.com:user/project.git
            └── destino:
                └── nome:
                    └── [Raiz]:
```

### *Usando apenas [git](../../versionamento/git/readme.md) & [ssh-agent](keygenssh.md)*
- prompt de comando
```bash
ssh-agent bash -c 'ssh-add ~/.ssh/id_ed25519; git clone git@github.com:user/project.git'
```
- powershell - subshell
```powershell
ssh-agent $(ssh-add ~/.ssh/id_ed25519; git clone git@github.com:user/project.git)
```