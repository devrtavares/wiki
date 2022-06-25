# dotnet core 6.0

<sub>[:arrow_upper_left: home](../../README.md) --Plataforma back-end em c#<sub>

<details open>
<summary><b>Preparação de ambiente</b></summary>
<ul>

<li><details open>

<summary><b>visual studio 2022</b></summary>

- downloads    
    - **IDE**
        - [**visualstudio**](https://visualstudio.microsoft.com/pt-br)
</details>
</li>

<li><details open>

<summary><b>visual studio code</b></summary>

- downloads    
    - [**dotnet 6.0**](https://dotnet.microsoft.com/en-us/download)
    - **IDE**
        - [*Visual studio code*](https://code.visualstudio.com/)
            - **plugins**
                - [ms-dotnettools.csharp](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp), [jchannon.csharpextensions](
        https://marketplace.visualstudio.com/items?itemName=jchannon.csharpextensions) & [k--kato.docomment](https://marketplace.visualstudio.com/items?itemName=k--kato.docomment)
                    ```bash
                    code --install-extension ms-dotnettools.csharp --force 
                    code --install-extension jchannon.csharpextensions --force
                    code --install-extension k--kato.docomment --force
                    ```
</details>
</li>
<ul>
</details>

<details OPEN>
<summary><b>Documentações</b></summary>

- [.netcore 6](https://docs.microsoft.com/pt-br/aspnet/core/?view=aspnetcore-6.0) --[tools](https://docs.microsoft.com/pt-br/dotnet/core/tools/dotnet)

</details>

- *Iniciar novo projeto*
    ```bash
    dotnet new webapi -o TestApi
    ```

<sup></sup>
---

https://www.youtube.com/watch?v=q4EGRq-q7Xs
https://docs.microsoft.com/pt-br/ef/core/get-started/overview/install

https://marketplace.visualstudio.com/items?itemName=SimonHughes.EntityFrameworkReversePOCOGenerator

https://www.reversepoco.co.uk/


Microsoft.EntityFrameworkCore
Microsoft.EntityFrameworkCore.Design
Microsoft.EntityFrameworkCore.SqlServer



------
version: '3.9'

services:
  mssql:
    image: mcr.microsoft.com/mssql/server:2019-latest
    ports:
      - 1433:1433
    volumes:
      - ~/apps/mssql/data:/var/lib/mssqlql/data
    environment:
      - ACCEPT_EULA=Y
      - SA_PASSWORD=mssql1Ipw


https://citizix.com/how-to-run-mssql-server-2019-with-docker-and-docker-compose/

https://docs.microsoft.com/pt-br/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver15