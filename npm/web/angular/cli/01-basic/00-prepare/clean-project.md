# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](../readme.md) <sub>

### Iniciando um projeto limpo


- **my-first-app/**
    - **src/app/**
        - :page_facing_up: **app.component.html**
        <br/><sup>*vamos limpar o componente app.component.html*</sup>
            ```html
            ```
        - :page_facing_up: **app.component.ts**
        <br/><sup>*vamos limpar o componente app.component.ts*</sup>
            ```ts
            import { Component } from '@angular/core';

            @Component({
              selector: 'app-root',
              templateUrl: './app.component.html',
              styleUrls: ['./app.component.css']
            })
            export class AppComponent {
            }
            ```
        - :page_facing_up: **app.module.ts**
        <br/><sup>*e limpar quaisquer alterações no app.module.ts*</sup>
            ```ts
            import { NgModule } from '@angular/core';
            import { BrowserModule } from '@angular/platform-browser';

            import { AppComponent } from './app.component';

            @NgModule({
              declarations: [
                AppComponent
              ],
              imports: [
                BrowserModule
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
