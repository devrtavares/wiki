# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

&nbsp;&nbsp;&nbsp;&nbsp;<sub>até aqui usamos diretivas apenas de componentes nos exemplos, contudo, para incluir objetivos podemos precisar de auxilio na integração com DOM</sub>

### ngIf

&nbsp;&nbsp;&nbsp;&nbsp;<sub>ngIf é um auxiliar no angular, que renderiza o objeto no DOM apensa quando a condição é atingida</sub><br/>
&nbsp;&nbsp;&nbsp;&nbsp;<sub>*ngIf para que funcione corretamente é importante adicionar o asterisco antes</sub>

- +:page_facing_up: **servers.component.ts**
    ```diff
    import { Component, OnInit } from '@angular/core';

    @Component({
        selector: '.app-servers',
        templateUrl: './servers.component.html',
        styleUrls: ['./servers.component.css']
    })
    export class ServersComponent implements OnInit {

        allowNewServer = false;
        serverCreationStatus = 'No server was created!';
        serverName = 'TestServer';
    +    serverCreated = false; 

        constructor() { 
            setTimeout(() => {
                this.allowNewServer = true;
            }, 2000);

        }

        ngOnInit(): void {
        }

        OnCreateServer() {
    +        this.serverCreated = true;
            this.serverCreationStatus = `Server was created! Name is ${this.serverName}`;
        }

        OnUpdateServerName(event: Event) {
            this.serverName = (<HTMLInputElement>event.target).value;
        }
        }

    ```

- +:page_facing_up: **servers.component.html**
    ```diff
    <!--Interpolação & Propriedade (Ligação de duas vias)-->
    <input
        type="text"
        class="form-control"
        [(ngModel)]="serverName" />
    <!--Evento-->
    <p>
        <button 
            [disabled]="!allowNewServer"
            class="btn btn-primary" 
            (click)="OnCreateServer()"
        >
        Add Server
        </button>
    </p>
    <!--Interpolação de texto-->
    - <p>{{ serverCreationStatus }}</p>
    + <p *ngIf="serverCreated">{{ serverCreationStatus }}</p>
    ```

### ngIf else

&nbsp;&nbsp;&nbsp;&nbsp;<sub>*ngIf else, gera elemento no DOM quando a condição não é atingida, baseado no template informado, poderiamos simplismente negar a condição com "!" mas isso não é uma boa prática.</sub>


- +:page_facing_up: **servers.component.html**
    ```diff
    <!--Interpolação & Propriedade (Ligação de duas vias)-->
    <input
        type="text"
        class="form-control"
        [(ngModel)]="serverName" />
    <!--Evento-->
    <p>
        <button 
            [disabled]="!allowNewServer"
            class="btn btn-primary" 
            (click)="OnCreateServer()"
        >
        Add Server
        </button>
    </p>
    <!--Interpolação de texto-->
    - <p>{{ serverCreationStatus }}</p>
    + <p *ngIf="serverCreated; else noServer">{{ serverCreationStatus }}</p>
    + <ng-template #noServer>
    +     <p>No server was created!</p>
    + </ng-template>
    ```

<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;