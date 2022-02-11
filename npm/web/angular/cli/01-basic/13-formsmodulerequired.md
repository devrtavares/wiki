# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Importante: FormsModule é uma requisição para Ligação de duas vias

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
    
    Para que o Two-Way-Binding funcione, é necesspario habilitar a diretiva `ngModel`. Isso é feito adicionando o `FormsModule` à matriz `imports[]` no AppModule.

    Você também precisa adicionar a importação de `@angular/forms` no arquivo `app.module.ts`:

    `import { FormsModule } from '@angular/forms';`

<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;