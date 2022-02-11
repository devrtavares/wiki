# NodeJs @Angular

<sub>[:arrow_upper_left: ng](readme.md) <sub>

### ngModel

Vamos editar os arquivos no visual studio code e visualisar a atualização do dado em tempo real. Através do modelo e servidor criado pelo **ng serve**

- **my-first-app/**
    - **src/app/**
        - :page_facing_up: **app.component.html**
            ```html
            <input type="text" [(ngModel)]="name" />
            {{name}}
            ```
        - :page_facing_up: **app.component.ts**
            ```diff
            import { Component } from '@angular/core';

            @Component({
              selector: 'app-root',
              templateUrl: './app.component.html',
              styleUrls: ['./app.component.css']
            })
            export class AppComponent {
            -  title = 'my-first-app';
            +  name = 'my-first-app';
            }
            ```
        - :page_facing_up: **app.module.ts**
            ```diff
            import { NgModule } from '@angular/core';
            import { BrowserModule } from '@angular/platform-browser';
            +import { FormsModule } from '@angular/forms';

            import { AppComponent } from './app.component';

            @NgModule({
              declarations: [
                AppComponent
              ],
              imports: [
                BrowserModule
            +    ,FormsModule
              ],
              providers: [],
              bootstrap: [AppComponent]
            })
            export class AppModule { }
            ```
<sub></sub>
---
<image src="../../img/icon.svg" width="34px" height="36px"/>

&nbsp;
