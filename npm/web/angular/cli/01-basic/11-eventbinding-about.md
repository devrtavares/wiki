# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Interpolação vs Propriedades


- +**src/app/servers**

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
        +    serverCreationStatus = 'No server was created!';

            constructor() { 
              setTimeout(() => {
                  this.allowNewServer = true;
              }, 2000);

            }

            ngOnInit(): void {
            }

        +    OnCreateServer() {
        +      this.serverCreationStatus = 'Server was created!';
        +    }

          }

        ```

    - +:page_facing_up: **servers.component.html**
        ```diff
        <p>servers works!</p>
        <p><button [disabled]="{{!allowNewServer}}"
        + (click)="onCreateServer()"
        class="btn btn-primary">Add Server</button></p>
        +<p>{{ serverCreationStatus }}</p>
        ```
<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;