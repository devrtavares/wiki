# github

<sub>[:arrow_upper_left: Integração](integrations.md)  <sub>

## ***Gerar chave ssh segura publica e privada***

*Podemos escolher um dos passos a seguir:*

1. *Aplicativos* [*puTTY*](https://www.chiark.greenend.org.uk/~sgtatham/putty/) ou [*sourcetree*](https://www.sourcetreeapp.com/)

    1. *quando utilizado sourcetree*: (*opcional*)
        ```
        ┌─ Windows
        └── 1. sourcetree
            └── ferramentas
                └── criar ou importar chaves ssh
        ```

    2. *Gerar chave pelo puTTY*
        ```
        ┌─ 2. PuTTY key generator
        └── (Tipo de chave)
            └── ED25519 
                └── Salvar a chave
                    └── Pública
                    ├── Privada
                    └── (opcional: incluir senha)
        ```

2. *[ssh-keygen para windows](../../so/windows/ferramentas/ssh-keygen/readme.md)*
```diff
┌─ iniciar do windows
└── 1. Prompt de comando [cmd] > botão direito 
    └── Executar como administrador
+       └── sh-keygen -o -a 100 -t ed25519 -f ~/.ssh/id_ed25519 -C "example@example.com"
            └── Enter passphrase (empty for no passphrase):
                └── Salvar os arquivos
                    └── .ssh\id_ed25519
                    └── .ssh\id_ed25519.pub
```

