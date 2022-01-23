# tsconfig - exemplo

<sub>[:arrow_upper_left: arquivo de configuração](tsconfigjson.md) <sub>

- com isso já podemos compilar nosso projeto:

	```json
	{
		"compilerOptions": {
			"target": "es2017",
			"module": "commonjs",
			"rootDir": "./src",
			"outDir": "./dist",
			"esModuleInterop": true,
			"allowJS": true,
			"strictNullChecks": true
		}
	}
	```
