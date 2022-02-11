# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>


### ngClass

- +:page_facing_up: **servers.component.ts**
    ```diff
    servers = ['TestServer', 'TestServer2'];

    onCreatedServer() {
        this.servers.push(this.serverName);
    }
    ```

- +:page_facing_up: **servers.component.html**
    ```diff
    <app-server *ngFor="let server of servers;"></app-server>
    ```
    - selecionando indices
        ```html
        <div 
            *ngFor="let server of servers; let i = index"
            [ngStyle]="{backgroundColor: i >= 3 ? 'blue' : 'transparent'}"
            [ngClass]="{'white-text': i >= 4 ?}"
        >
        {{ server }}
        </div>
        ```

<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;