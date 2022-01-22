# nodejs 

<sub>[:arrow_upper_left: nodejs em módulos](../readme.md)<sub>

## *nodemon*


- instalação
```bash
npm install -g nodemon # or using yarn: yarn global add nodemon
npm install --save-dev nodemon # or using yarn: yarn add nodemon -D
```

- start
```
nodemon ./server.js localhost 8080
```

- inspect
```

nodemon --inspect ./server.js 80
```

- ajuda
    ```
    nodemon -h
    ```

- nodemon.json ou nodemon -- config $[path]
```bash
{
  "verbose": true,
  "ignore": ["*.test.js", "fixtures/*"],
  "execMap": {
    "rb": "ruby",
    "pde": "processing --sketch={{pwd}} --run"
  }
}
```