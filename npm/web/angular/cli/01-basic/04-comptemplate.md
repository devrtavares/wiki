# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Componente Template


- **my-first-app/**
    - +**src/app/server**
        - +:page_facing_up: **server.component.ts**
            ```diff
            import { Component } from '@angular/core';

            @Component({
                selector: 'app-server',
            -    templateUrl: './ server.component.html',
            +    template: '<app-server></app-server>',
            })
            export class ServerComponent {

            }
            ```

            ou 

            ```diff
            import { Component } from '@angular/core';

            @Component({
                selector: 'app-server',
            -    templateUrl: './ server.component.html',
            +    template: `
            +      <app-server></app-server>
            +      <app-server></app-server>`,
            })
            export class ServerComponent {

            }
            ```

<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;