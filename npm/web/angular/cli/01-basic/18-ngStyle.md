# NodeJs @Angular

<sub>[:arrow_upper_left: @angular](readme.md) <sub>

### ngStyle

- +:page_facing_up: **servers.component.ts**
    ```diff
    getColor() {
        return this.serverStatus === 'online' ? 'green' : 'red';
    }

    ```

- +:page_facing_up: **servers.component.html**
    ```diff
    <p [ngStyle]="{backgroundColor: getColor()}>
    ```

<sub></sub>
---
<image src="../img/icon.svg" width="34px" height="36px"/>

<br/>&nbsp;