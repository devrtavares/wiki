# tsconfig.json

<sub>[:arrow_upper_left: abordagem de compitação](tsconfigjson.md) <sub>

### **pollyfill**

- Explicando de forma prática, para que qualquer um entenda: Você quer usar um recurso muito bom do javascript, por exemplo fetch() ou Promise().

- Mas alguns navegadores, como o Internet Explorer, não possuem suporte a estes recursos. De uma forma bem mal feita, você coloca aquele if maroto para saber se o navegador tem suporte e, caso não tenha, você usa alguma forma alternativa, ou até mesmo diz logo ao usuário que ele não pode usar tal recurso.

- Usando um pollyfill, este vai detectar que o navegador não tem suporte e vai implementar na hora ali, usando gambiarras funções disponíveis para aquele navegador, e vai fazer com que seja possível usar o recurso com a mesma interface inclusive. No caso é como se o navegador tivesse suporte a tal recurso.

- Futuramente, se o navegador passar a ter suporte ao recurso, o pollyfill pode ser desativado para ele, já que a implementação do código é a mesma, nada muda.

[*referencia*](https://pt.stackoverflow.com/questions/194857/o-que-%C3%A9-polyfill)