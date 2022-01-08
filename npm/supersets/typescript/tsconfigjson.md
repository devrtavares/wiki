# tsconfig.json

<sub>[:arrow_upper_left: typescript](readme.md) | [exemplo de configuração](tsconfigjsonsample.md) <sub>

## **abordagem de compitação**



 <font color="green">**"compilerOptions"**</font>:

- <font color="green">**"outDir":**</font>

	```json
	{ 
		"compilerOptions" :
		{
			"outDir": "./dist"
		} 
	}
	``` 
	> *obs: é interessante incluir o repositório **dist** ao .**gitignore***
	>
	> <font color="gray">**Diretório de saída da aplicação a objetos *.js:***</font> 
	>
	> *O typescript, interpreta arquivos no seu formato/sintax de escrita e os compila para arquivos em formato .js (javascript)*	
	>


- <font color="green">**"module":**</font>
	```json
	{ 
		"compilerOptions" :
		{
			"module": "commonjs"
		} 
	}
	```
	><font color="gray">**Os navegadores entendem o formato de linguagem javascript através de modularização.**</font>
	>
	>essa configuração, determina o formato de saída dos arquivos javascript*
	>
	>	<font color="green">"commonjs"</font>
	>
	> este módulo oferece suporte a linguagem que hoje os navegadores e o nodeJS entendem, enquanto a versão do **ES Next** não fica pronta.

- <font color="green">**"target":**</font>
	```json
	{ 
		"compilerOptions" :
		{
			"target": "es2019"
		} 
	}
	```	 
	> <font color="gray">**Vamos lembrar um pouco de padrão de código?**</font>
	>
	>[***Ecma International***](https://www.ecma-international.org/)
	>
	>javascript é uma linguagem que segue um padão identificado como **ES** - ***Ecma Script***, através do target podemos definir em qual vesão desse padrão bem como novidades inclusas, podemos utilizar.
	Para saber mais sobre o ES siga para:
	>
	>
	>[***Node Green***](https://node.green/)
	>
	> Antes de escolher a versão do Ecma Script, é interessante saber se ela da suporte aos recursos necessários para o módulo.
	>
	> - Node Green é uma boa fonte para verificar a versão do ecmascript por que relaciona as versões do nodejs.
	> - Podemos verificar em diversos sites e documentações.
	>
	

- <font color="green">**"esModuleInterop":**</font>
	```json
	{ 
		"compilerOptions" :
		{
			"esModuleInterop": "true"
		} 
	}
	```
	> <font color="gray">**Habilita conversão dos modulos**</font> - <font color="green">"true"</font>
	> 
	> que ainda usam o commonjs de como modulo principal. opções como Require, Model.Export e etc, caso utilizado o import, será convertido.
	>

	<font color="green">**"allowJS":**</font>
	```json
	{ 
		"compilerOptions" :
		{
			"allowJS": "true"
		} 
	}
	```
	><font color="green">"true"</font>
	>
	> habilita leitura de arquivos no formato javascript de configuração.
	>