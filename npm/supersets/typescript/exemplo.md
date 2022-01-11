# typescript

<sub>[:arrow_upper_left: typescript](readme.md)<sub>

## exemplo:


```diff
+ cd /d Desktop
+ mkdir "novo-modulo"
+ cd /d "novo-modulo"
+ git init
+ notepad .gitignore 
```

&nbsp;&nbsp;&nbsp;&nbsp; <sub>*(opcional) incluir linha: "node_modules" salvar e fechar*</sub>

```diff
+ git add .gitignore
```
&nbsp;&nbsp;&nbsp;&nbsp; <sub>*(opcional) criar versão*</sub>

```diff
- git commit -m "chore: module started"
```

```diff
+ npm init -y
+ git add package.json
```

&nbsp;&nbsp;&nbsp;&nbsp; <sub>*(opcional) criar versão*</sub>

```diff
- git commit -m "chore: add package manager"
```

```diff
+ npm install -D typescript @types/node
+ npx tsc --init
+ git add tsconfig.json
```

&nbsp;&nbsp;&nbsp;&nbsp; <sub>*(opcional) criar versão*</sub>

```diff
- git commit -m "chore: add dependence typescript"
```