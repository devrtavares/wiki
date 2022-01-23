# tsconfig.json

<sub>[:arrow_upper_left: configuração](config.md)  --- [exemplo de configuração](tsconfigjsonsample.md) <sub>

### **abordagem de compitação**

&nbsp;{ **"compilerOptions"** }

&nbsp;&nbsp;&nbsp;&nbsp;{ **"target"** : "es2017" }
<br/><sub>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;define qual vesão do **padrão de código** para javascript utilizar<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*falando um pouco sobre padrão de código:<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - [***Ecma International***](https://www.ecma-international.org/)<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**ES** - ***Ecma Script*** padrão de escrita de código para navegadores.<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;escolher a versão do ES depende do recurso disponível -<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; para o **nodejs**: <br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[***Node Green***](https://node.green/) é uma boa fonte para verificar<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a versão do ecmascript e a disponibilidade do recurso no nodejs*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ [**"lib"**](https://www.typescriptlang.org/tsconfig#lib) : [ "es6" ] }
<br/><sub>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;habilita compatibilidade para navegadores que ainda não tem todos os recursos do target, mas oferece adaptações (cambiaras)<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Seu programa não roda em um navegador, então você não quer as definições do tipo "dom"<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Você tem [polyfills](polyfill.md) ou implementações nativas para algumas, mas não todas, de uma versão ECMAScript de nível superior*</sub>


&nbsp;&nbsp;&nbsp;&nbsp;{ **"module"** : "commonjs" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*Os navegadores entendem o formato de linguagem javascript através de modularização. Essa configuração, determina o formato de saída dos arquivos javascript. Este módulo oferece suporte a linguagem que hoje os navegadores e o nodeJS entendem, enquanto a versão do **ES Next** não fica pronta*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"rootDir"** : "./src" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*diretório dos arquivos de código da aplicação*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"outDir"** : "./dist" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*diretório de saída da aplicação a objetos .js. O typescript interpreta arquivos (.ts) no seu formato/sintax  de escrita e os compila para arquivos em formato .js (javascript). é interessante incluir o repositório **dist** ao .gitignore*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"typeRoots"** : [
      "./node_modules/@types",
      "./src/@types"
    ] }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*possibilita substituir tipagens, incluir variaveis adicionais. por exemplo incluir variaveis no request do express*</sub>


&nbsp;&nbsp;&nbsp;&nbsp;{ **"esModuleInterop"** : "true" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*Habilita importação de módulos que ainda usam CommonJS. Opções como Require, Model.Export e etc, caso utilizado o import, será convertido*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"allowJS"** : "true" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*habilita leitura de arquivos no formato javascript como parte da aplicação*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"removeComments"** : "true" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*no processo de build remove todos os comentários*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"strict"** : "false" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*permite não validar a tipagem de um retorno de objeto, return null para strings por exemplo*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"experimentalDecorators"** : "true" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*habilita decorações como typeORM*</sub>

&nbsp;&nbsp;&nbsp;&nbsp;{ **"emitDecoratorMetadata"** : "true" }
<br/>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<sub>*habilita decorações como typeORM*</sub>
