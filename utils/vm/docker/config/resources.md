# docker

<sub>[:arrow_upper_left: docker](../readme.md)<sub> 

## resourses

### WSL 2 (Windows Subsystem for Linux)  --- [sobre o WSL 2](../../../../so/windows/ferramentas/wsl2/readme.md)

1. Migração de imagens para outro diretório:

    ```
    Docker stopped
    ```
    ```
    wsl --list -v
    ```
    ```
    wsl --shutdown
    ```
    ```
    wsl --export docker-desktop-data docker-desktop-data.tar
    ```
    ```
    wsl --unregister docker-desktop-data
    ```
    ```
    wsl --import docker-desktop-data D:\docker-new-repo\ docker-desktop-data.tar --version=2
    ```

2. Alterar por Symbolic link

    Quando o motor de execução é o WSL 2, o padrão de diretório segue na parta "**C:\Users\\** *[user-name]* **\AppData\Local\Docker**"
    Podemos alterar criando um link simbólico:
    
    ```bash
    docker stop
    wsl --shutdown
    ```
    Copiar arquivos do wsl para o novo diretório, 
    
    de:
    "C:\Users\[user-name]\AppData\Local\Docker"
    
    para: [Novo diretório]

    ```bash
    cd /d "C:\Users\[user-name]\AppData\Local\Docker"
    $ mklink /D wsl "[novo-diretório]"
    ```
    
    - Exemplo:
    
        1. Para a execução do docker
        
        2. por prompt de comando do windows:

            ```
            cd /d d:/
            mkdir docker
            cd /d docker
            mkdir wsl
            Xcopy "C:\Users\[user-name]\AppData\Local\Docker\wsl" "D:\docker\wsl" /E /H /I
            cd /d "C:\Users\Joao\AppData\Local\Docker"
            rd /s wsl
            $ mklink /D wsl "D:\docker\wsl"
            ```