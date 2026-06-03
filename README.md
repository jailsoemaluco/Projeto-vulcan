# Projeto Vulcan - Equipe: jailsonémaluco
## Sensores Térmicos - Reponsáveis: Jailson Santana e Maria Eduarda Oliveira

### 1. Como Funciona os Sensores
- Os sensores do robô são movidos por um sistema de JS utilizando-se de Array (lista) que calcula a média térmica através de um laço de repetição, que caso a temperatura esteja acima ou abaixo do recomendado, haverá um aviso para que o problema possa ser detectado e corrigido.
---
### 2. Para que Serve
- Nosso sistema servirá para detectar alterações drásticas de temperatura, servindo para zelar da vida útil dok sistema e facilitar a verificação, suibstuituindo a forma manual por uma automatizada que otimiza o tempo, ajudando o funcionário e evitando possíveis falhas humanas.
---
### 3. Importância
- É importante para auxiliar a empresa a reduzir possíveis gastos comn acidente, diminuir custos necessários em manuntenção e tornando o serviço mais fácil, por requirir apenas um aparelho para ver a resposta do robô.
---
### 4. Variáveis Utilizadas e suas Funções
- As variáveis utilizadas e suas funções foram:
- Temperatura - é o array (lista) para checar a temperatura dos robôs
- soma - é usado para somar a temperatura dos robôs que estão no array
- media - é usado para fazer a media dessa soma e verificar a temperatura
---
### 5. Condicionais Utilizadas e suas Funções:
- let temperatura = [] - cria um array (vetor) vazio para armazenar as temperaturas informadas

- let soma = 0 - cria uma variável que irá armazenar a soma de todas as temperaturas

- let media = 0 - cria uma variável que irá armazenar a média das temperaturas

- let status = 0 - cria uma variável que irá armazenar a mensagem final sobre a situação da temperatura

- function sensor(temperatura) - cria uma função chamada sensor que recebe um array de temperaturas como parâmetro

- for - significa "para", é um laço de repetição que executa um bloco de código várias vezes

- let i = 0 - cria a variável de controle do laço e inicia ela com o valor 0

- i < temperatura.length - verifica se o índice ainda é menor que a quantidade de elementos do array

- i++ - significa "incrementar", adiciona 1 ao valor de i a cada repetição

- temperatura.length - retorna a quantidade de elementos existentes no array

- soma += temperatura[i] - adiciona o valor da posição atual do array à variável soma

- += - significa "somar e atribuir", é o mesmo que escrever:
  soma = soma + temperatura[i]

- media = soma / temperatura.length - calcula a média dividindo a soma pela quantidade de temperaturas

- / - significa divisão

- if - significa "se", se acontecer certa coisa, a condição irá ocorrer

- else if - significa "senão se", caso outra condição seja verdadeira, esse bloco será executado

- else - significa "senão", se nenhuma das condições anteriores for verdadeira, esse bloco será executado

- < - significa "menor que"

- > - significa "maior que"

- <= - significa "menor ou igual a"

- >= - significa "maior ou igual a"

- && - significa "e", as duas condições precisam ser verdadeiras ao mesmo tempo

- status = ("Atenção!!! Temperatura muito baixa, aquecedores necessários") - atribui uma mensagem de alerta para temperaturas baixas

- status = ("Temperatura ideal") - atribui uma mensagem informando que a temperatura está adequada

- status = ("Temperatura fora do ideal!!! ligue o resfriamento!!!") - atribui uma mensagem informando que a temperatura está acima do ideal

- return - significa "retornar", devolve os dados calculados pela função

- return { temperatura, soma, media, status } - retorna um objeto contendo as temperaturas, a soma, a média e o status

- module.exports = {sensor} - exporta a função sensor para que ela possa ser utilizada em outros arquivos do projeto

- array - estrutura que permite armazenar vários valores em uma única variável

- objeto - estrutura que armazena dados em pares de chave e valor, como temperatura, soma, media e status
----
### 6. Código feito 

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
