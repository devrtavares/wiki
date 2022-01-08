# react-redux.js exemplo

<sub>[:arrow_upper_left: react-redux.js](../readme.md)  <sub>

### controlador para estado de um objeto com valores de texto

#### Inicialização

1. store.js

```javascript
import { createStore } from 'redux'
import appReducer from './appReducer'

export default createStore(appReducer)
```

2. appReducer.js

```javascript
const initialState = { text: 'Este texto' }

export default (state = initialState, action) => {
    switch (action.type) {
        case 'SET_TEXT':
            return { ...state, text: action.payload }
        default:
            return state
    }
}
```

3. index.js

```javascript
import ReactDOM from 'react-dom'
import React from 'react'
import { Provider } from 'react-redux'
import store from './store'
import App from './App'

ReactDOM.render(
    <Provider store={store}>
        <App />
    </Provider>, document.getElementById('root'))
```


[referência](https://medium.com/@heliojuniorkroger/entenda-react-e-redux-de-uma-vez-por-todas-c761bc3194ca)