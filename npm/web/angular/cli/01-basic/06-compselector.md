# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Componente Selector

- **padrão selector**
    - **my-first-app/**
        - +**src/app/server**
            - +:page_facing_up: **server.component.ts**
                ```diff
                import { Component, OnInit } from '@angular/core';

                @Component({
                -  selector: 'app-servers',
                +  selector: '[app-servers]',
                  templateUrl: './servers.component.html',
                  styleUrls: ['./servers.component.css']
                })
                export class ServersComponent implements OnInit {

                constructor() { }

                  ngOnInit(): void {
                  }

                }

                ```
        - +**src/app**
            - :page_facing_up: **app.component.html**
                ```html
                <h1>I'm in the AppComponent!</h1>
                <hr>
                <app-server></app-server>
                ```



- **div element selector**
    - **my-first-app/**
        - +**src/app/server**
            - +:page_facing_up: **server.component.ts**
                ```diff
                import { Component, OnInit } from '@angular/core';

                @Component({
                -  selector: 'app-servers',
                +  selector: '[app-servers]',
                  templateUrl: './servers.component.html',
                  styleUrls: ['./servers.component.css']
                })
                export class ServersComponent implements OnInit {

                constructor() { }

                  ngOnInit(): void {
                  }

                }

                ```
        - +**src/app**
            - :page_facing_up: **app.component.html**
                ```html
                <h1>I'm in the AppComponent!</h1>
                <hr>
                <div app-servers></div>
                ```

- **div class selector**
    - **my-first-app/**
        - +**src/app/server**
            - +:page_facing_up: **server.component.ts**
                ```diff
                import { Component, OnInit } from '@angular/core';

                @Component({
                -  selector: 'app-servers',
                +  selector: '.app-servers',
                  templateUrl: './servers.component.html',
                  styleUrls: ['./servers.component.css']
                })
                export class ServersComponent implements OnInit {

                constructor() { }

                  ngOnInit(): void {
                  }

                }

                ```
        - +**src/app**
            - :page_facing_up: **app.component.html**
                ```html
                <h1>I'm in the AppComponent!</h1>
                <hr>
                <div class="app-servers"></div>
                ```
<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;