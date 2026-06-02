# Projeto-vulcan

##Pessoa a

``` // Valores que o usuário pode modificar de acordo com o seu uso.
let velocidadeAtual = 0;
let aceleracao = 0;
let status = 0 

// Função para calcular os valores e verificar o estado do braço.
function sistemaBracoRobotico(velocidadeAtual, aceleracao) {
    let velocidadeFinal = velocidadeAtual + aceleracao;
    
    if (velocidadeFinal <= 100) {
        status = ("SISTEMA SEGURO");
    } else {
        status = ("ALERTA DE SOBRECARGA");
    }
    
    return {
        velocidadeAtual: velocidadeAtual,
        velocidadeFinal: velocidadeFinal,
        status: status,
        aceleracao: aceleracao
    }
}
module.exports = { sistemaBracoRobotico }
``` 

## Pessoa b

```
let temperatura = [];
let soma = 0
let media = 0
let status = 0 

function sensor (temperatura) {
for(let i = 0; i < temperatura.length; i++){

    soma+=temperatura[i]
    
}

media  = soma/temperatura.length

if(media < 15){
    status = ("Atenção!!!. Temperatura muito baixa, aquecedores necessários")
   
}else if(media >= 15 && media <= 25){
        status = ("Temperatura ideal")
}else{
   status = ("\nTemperatura fora do ideal!!! ligue o resfriamento!!!")
    }

    return {
temperatura: temperatura,
soma: soma,
media: media,
status: status
    }
}

module.exports = {sensor}

```

## Pessoa c

```

const { sistemaBracoRobotico } = require("./motor");

let velocidadeAtual = 50
let aceleracao = 20
let resultado = sistemaBracoRobotico (velocidadeAtual, aceleracao)

const { sensor } = require ("./sensor")

let temperatura = [200, 100, 300, 40, 300]
let tempf = sensor (temperatura)

console.log ("===========================Terminal===========================")
console.log ("A aceleração foi de: ", resultado.aceleracao, "m/s²")
console.log ("A velocidade atual é de: ", resultado.velocidadeFinal, "km/h")
console.log ("Status: ", resultado.status)
console.log ("A temperatura média é de: ", tempf.media)
console.log ("Status: ", tempf.status)
console.log ("==============================================================")

```
