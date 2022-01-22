# tsconfig.json

<sub>[:arrow_upper_left: typescript](readme.md)  --- [exemplo de configuração](tsconfigjsonsample.md) <sub>

### **abordagem de compitação**



 **"compilerOptions"**:

- **"outDir":**

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
	> <font color="gray">**Diretório de saída da aplicação a objetos *.js:*** 
	>
	> *O typescript, interpreta arquivos no seu formato/sintax de escrita e os compila para arquivos em formato .js (javascript)*	
	>


- **"module":**
	```json
	{ 
		"compilerOptions" :
		{
			"module": "commonjs"
		} 
	}
	```
	><font color="gray">**Os navegadores entendem o formato de linguagem javascript através de modularização.**
	>
	>essa configuração, determina o formato de saída dos arquivos javascript*
	>
	>	"commonjs"
	>
	> este módulo oferece suporte a linguagem que hoje os navegadores e o nodeJS entendem, enquanto a versão do **ES Next** não fica pronta.

- **"target":**
	```json
	{ 
		"compilerOptions" :
		{
			"target": "es2019"
		} 
	}
	```	 
	> <font color="gray">**Vamos lembrar um pouco de padrão de código?**
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
	

- **"esModuleInterop":**
	```json
	{ 
		"compilerOptions" :
		{
			"esModuleInterop": "true"
		} 
	}
	```
	> <font color="gray">**Habilita conversão dos modulos** - "true"
	> 
	> que ainda usam o commonjs de como modulo principal. opções como Require, Model.Export e etc, caso utilizado o import, será convertido.
	>

	**"allowJS":**
	```json
	{ 
		"compilerOptions" :
		{
			"allowJS": "true"
		} 
	}
	```
	>"true"
	>
	> habilita leitura de arquivos no formato javascript de configuração.
	>