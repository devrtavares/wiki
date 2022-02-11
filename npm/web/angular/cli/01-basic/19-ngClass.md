# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>


### ngClass

- +:page_facing_up: **servers.component.ts**
    ```diff
    @component({
        styles: [`
            .online {
                color: white;
            }
        `]
    })

    ```

- +:page_facing_up: **servers.component.html**
    ```diff
    <p [ngClass]="{online: serverStatus === 'online'}">
    ```

<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;