# Projeto-vulcan

Importação dos módulos:
``` 
const { sistemaBracoRobotico } = require("./motor");
const { sensor } = require("./sensor");
```
Essas linhas importam funções de outros arquivos do projeto:

sistemaBracoRobotico → responsável pelos cálculos relacionados ao movimento do braço robótico.
sensor → responsável pela análise das temperaturas captadas pelos sensores.
Definição dos dados do motor
let velocidadeAtual = 50;
let aceleracao = 20;

Aqui são definidos os valores iniciais utilizados pelo sistema:

velocidadeAtual: velocidade atual do braço robótico.
aceleracao: valor da aceleração aplicada ao sistema.

Processamento do motor
``` 
let resultado = sistemaBracoRobotico(velocidadeAtual, aceleracao);
``` 

A função sistemaBracoRobotico() recebe a velocidade e a aceleração como parâmetros.

Ela retorna um objeto contendo:

aceleracao
velocidadeFinal
status

Essas informações serão exibidas posteriormente no terminal.

Definição das temperaturas
```
let temperatura = [200, 100, 300, 40, 300]; 
``` 

Criação de um array contendo as temperaturas registradas pelos sensores do sistema.

Cada posição do array representa uma leitura de temperatura.

Processamento dos sensores

``` 
let tempf = sensor(temperatura);
``` 

A função sensor() recebe o array de temperaturas e realiza os cálculos necessários.

Ela retorna um objeto contendo:

media → temperatura média calculada.
status → condição do sistema baseada na média obtida.

Exibição dos resultados
```
console.log("===========================Terminal===========================");
console.log("A aceleração foi de: ", resultado.aceleracao, "m/s²");
console.log("A velocidade atual é de: ", resultado.velocidadeFinal, "km/h");
console.log("Status: ", resultado.status);
console.log("A temperatura média é de: ", tempf.media);
console.log("Status: ", tempf.status);
console.log("==============================================================");
```


Fluxo de execução:
1. Importa os módulos
       ↓
2. Define velocidade e aceleração
       ↓
3. Calcula os dados do motor
       ↓
4. Define as temperaturas
       ↓
5. Calcula a média das temperaturas
       ↓
6. Exibe todos os resultados no terminal
=
