# Sobre o docker

<sub>[:arrow_upper_left: docker](readme.md)<sub>

## O que é Docker?
O termo Docker se refere a muitas coisas: 
-um projeto da comunidade open source; as ferramentas resultantes desse projeto; a empresa Docker Inc., principal apoiadora do projeto; e as ferramentas compatíveis formalmente com a empresa. O fato de que as tecnologias e a empresa têm o mesmo nome pode causar uma certa confusão.

Veja uma simples explicação:

- O software de TI "Docker” é uma tecnologia de containerização para criação e uso de containers Linux®.
- A comunidade open source do Docker trabalha gratuitamente para melhorar essas tecnologias para todos os usuários.
- A empresa Docker Inc. se baseia no trabalho realizado pela comunidade do Docker, tornando-o mais seguro, e compartilha os avanços com a comunidade em geral. Depois, ela oferece aos clientes corporativos o suporte necessário para as tecnologias que foram aprimoradas e fortalecidas.
- Com o Docker, é possível lidar com os containers como se fossem máquinas virtuais modulares e extremamente leves. Além disso, os containers oferecem maior flexibilidade para você criar, implantar, copiar e migrar um container de um ambiente para outro. Isso otimiza as aplicações na nuvem.

### Antes de Proseguir, vamos ver algums problemas comuns com instalações Windows

- Evite Utilizar diretórios como a **area de trabalho**.
os ambientes de desenvolvimento constumam ter paths absolutos
"c/users/seuNome/pasta" ocorrem erros no docker com **paths e
acentos, espacos**.

- Arquivos com *características alteradas* também geram problemas.
o **Onedrive** marca os arquivos como arquivos de nuvem, desabilite
para nao ter problemas.

- Aplicativos e ferramentas que tenham aplicado **alterações de
virtualização** podem ocasionar erros e conflitos, como o **virtualBox** da
oracle, desinstale caso possua componentes que alterem o **Hyper-V**

### TERMOS COMUNS USANDOS COM DOCKER
- IMAGEM
Recebe o nome de imagem, o grupo de dados que agrupa as informaçoes e objetivos
a serem executados pelo Docker.

- CONTAINER
Dentro de uma imagem podemos agrupar um determinado agrupamento de dados 
como exemplo uma determinada aplicação.

### LINKS UTEIS

 - https://www.docker.com/
 - https://www.docker.com/products/docker-desktop
 - http://files.cod3r.com.br/apostila-docker.pdf
 - https://github.com/cod3rcursos/curso-docker
- https://www.youtube.com/watch?v=N6G4bv-qo4w
- https://www.redhat.com/pt-br/topics/containers/what-is-docker
