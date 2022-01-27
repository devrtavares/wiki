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
	  },
	  "include": [
	    "./src"
	  ],
	  "exclude": [
	    "./node_modules"
	  ]
	}
	
	```

	- *exemplo 2019*

	```json
	{
	  "compilerOptions": {
	    "target": "es2017",
	    "lib": ["es6"],
	    "experimentalDecorators": true,
	    "emitDecoratorMetadata": true,
	    "module": "commonjs",
	    "rootDir": "./src",
	    "typeRoots": ["./node_modules/@types", "./src/@types"],
	    "allowJs": true,
	    "outDir": "./dist",
	    "removeComments": true,
	    "esModuleInterop": true,
		"resolveJsonModule": true,
	    "forceConsistentCasingInFileNames": true,
	    "skipLibCheck": true,
	    "baseUrl": ".",
	    "paths": {
	      "@controllers": ["./src/controllers/*"],
	      "@models": ["./src/models/*"],
	      "@views": ["./src/views/*"],
	      "@configs": ["./src/config/*"]
	    }
	  },
	  "include": [
	    "./src"
	  ],
	  "exclude": [
	    "./node_modules"
	  ]
	}

	```
