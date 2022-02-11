# node package manager

<sub>[:arrow_upper_left: npm](readme.md)<sub>

## Comandos

1. **install**

    `npm install`
    restaura pacotes de um módulo / projeto

    - **módulo**

        `npm install [target]` || `npm i [target]`<br/>
        `npm uninstall [target]`

        - **parametrôs**

            `npm install -global [target]` || `npm install -G [target]` <br/>
            `npm install -save-dev [target]` || `npm install -D [target]`

            - [**sinopse**](https://docs.npmjs.com/cli/v8/commands/npm-install):
                ```
                npm install (with no args, in package dir)
                npm install [<@scope>/]<name>
                npm install [<@scope>/]<name>@<tag>
                npm install [<@scope>/]<name>@<version>
                npm install [<@scope>/]<name>@<version range>
                npm install <alias>@npm:<name>
                npm install <git-host>:<git-user>/<repo-name>
                npm install <git repo url>
                npm install <tarball file>
                npm install <tarball url>
                npm install <folder>

                aliases: npm i, npm add
                common options: [-P|--save-prod|-D|--save-dev|-O|--save-optional|--save-peer] [-E|--save-exact] [-B|--save-bundle] [--no-save] [--dry-run]
                ```
2. **Update Npm** --<sub>(*[@Angular/Cli](../../web/angular/cli/01-basic/install.md#)*)</sub>

    ```bash
    $ [sudo] npm install -g npm (sudo  is only required on Mac/ Linux)
    ```


<sub></sub>
---
    