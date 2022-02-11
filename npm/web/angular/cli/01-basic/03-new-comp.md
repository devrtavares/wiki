# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Componente

- **criar novo**
    - **my-first-app/**
        - +**src/app/server**
            - +:page_facing_up: **server.component.html**
                ```html
                <p>html server simple</p>
                ```
        - +**src/app/server**
            - +:page_facing_up: **server.component.ts**
                ```ts
                import { Component } from '@angular/core';

                @Component({
                    selector: 'app-server',
                    templateUrl: './ server.component.html',
                })
                export class ServerComponent {

                }
                ```
- **registrar o**
    - **my-first-app/**
        - +:page_facing_up: app.module.ts
            ```diff
            import { NgModule } from '@angular/core';
            import { BrowserModule } from '@angular/platform-browser';

            import { AppComponent } from './app.component';
            +import { ServerComponent } from './server/server.component';

            @NgModule({
            declarations: [
                AppComponent 
            +    ,ServerComponent
            ],
            imports: [
                BrowserModule
            ],
            providers: [],
            bootstrap: [AppComponent]
            })
            export class AppModule { }

            ```

- **usar o**
    - **my-first-app/**
        - +**src/app**
            - :page_facing_up: **app.component.html**
                ```html
                <h1>I'm in the AppComponent!</h1>
                <hr>
                <app-server></app-server>
                ```


<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;