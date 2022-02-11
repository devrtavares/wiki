# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Interpolação de texto

- +**src/app/server**
    - +:page_facing_up: **server.component.html**
        ```diff
        +<p>{{ 'Server' }} with ID {{ serverId }} is {{  getServerStatus() }}</p>
        ```
    - +:page_facing_up: **server.component.ts**
        ```diff
        import { Component } from '@angular/core';

        @Component({
            selector: 'app-server',
            templateUrl: './ server.component.html',
        })
        export class ServerComponent {
        +    serverId: number = 10;
        +    serverStatus: string = 'offline';
        +
        +   getServerStatus() {
        +       return this.serverStatus;
        +   }
        }
        ```
<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;