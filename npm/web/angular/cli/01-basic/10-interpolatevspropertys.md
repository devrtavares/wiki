# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### Interpolação vs Propriedades

- +**src/app/servers**
    - +:page_facing_up: **servers.component.html**
      - ***Interpolação informando a propriedade não funciona***
        ```html
        <p>servers works!</p>
        + <p><button [disabled]="{{!allowNewServer}}" class="btn btn-primary">Add Server</button></p>
        ```
      - ***Interpolação informando o valor do DOM funciona***
          ```html
          <p>servers works!</p>
          + <p>{{allowNewServer}}</p>
          + <p [innerText]="allowNewServer"></p>
          ```
<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;