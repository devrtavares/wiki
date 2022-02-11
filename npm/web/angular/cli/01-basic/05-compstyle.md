# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Componente Styles


- **my-first-app/**
    - +**src/app/server**
        - +:page_facing_up: **server.component.ts**
            ```diff
            import { Component } from '@angular/core';

            @Component({
            selector: 'app-root',
            templateUrl: './app.component.html',
            - styleUrls: ['./app.component.css']
            + //styleUrls: ['./app.component.css']
            + styles: [`
            +    h3 {
            +           color: dodgerblue;
            +       }
            +`]
            })
            export class AppComponent {
            title = 'my-first-app';
            }

            ```
<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;