# Comando : run

<sub>[:arrow_upper_left: docker](readme.md)  <sub>

É um comando resultante da concatenação(união) de 4 outros comandos pull, create, start, exec para um detemrinado container.

- Demonstrativo : Versões diferentes de Kernel, baseado em um container:
	```
	bash --version
	docker container run debian bash --version
	```
- Verificações Verificando Containers em execução:
	```
	docker container ps
	``` 
- Verificando Todos os Containers:
	```
	docker container ps -a
	``` 
- Executando um container e removendo da lista de histórica
	```
	docker container run --rm debian bash --version
	```