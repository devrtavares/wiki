# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### componente

- **criar novo**
    - **por terminal**
        ```bash
        ng generate component [name]
        ```
        - *simplificando a chamada do comando por apelido*
            ```bash
            ng g c [name]
            ```
            - **ng generate registra o componente de modo automático**
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