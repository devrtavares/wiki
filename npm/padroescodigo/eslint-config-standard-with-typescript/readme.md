### Eslint Config Standard With Typescript

<sub>[:arrow_upper_left: Notas](../readme.md) \| [*ECMAScript*](https://www.ecma-international.org/publications-and-standards/standards/) \| [*npmjs.com/eslint-config-standard-with-typescript*](https://www.npmjs.com/package/eslint-config-standard-with-typescript)  <sub>

- *Instalação*:

```
npm install --save-dev \
  typescript@^4 \
  eslint@^7.12.1 \
  eslint-plugin-promise@^5.0.0 \
  eslint-plugin-import@^2.22.1 \
  eslint-plugin-node@^11.1.0 \
  @typescript-eslint/eslint-plugin@^4.0.1 \
  eslint-config-standard-with-typescript@latest
```

ESLint v7:
```
npx eslint .
```

ESLint v6:
```
 npx eslint --ext .js,.ts .
```

- .eslintrc.js
```
module.exports = {
  extends: 'standard-with-typescript',
  parserOptions: {
    project: './tsconfig.json'
  }
}
```