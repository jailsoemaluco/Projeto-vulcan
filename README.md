# Sistema de Controle de Braço Robótico

## Descrição do Projeto

Este projeto simula um sistema simples de controle de um braço robótico utilizando JavaScript. O programa calcula a velocidade final com base na velocidade atual e na aceleração aplicada, verificando se o sistema está operando dentro de um limite seguro.

---

## Objetivos

- Utilizar variáveis em JavaScript.
- Criar e utilizar funções.
- Aplicar estruturas condicionais (if/else).
- Trabalhar com retorno de objetos.
- Desenvolver lógica de programação.

---

## Como Funciona

O sistema utiliza duas variáveis principais:

| Variável | Descrição |
|-----------|-----------|
| `velocidadeAtual` | Velocidade inicial do braço robótico |
| `aceleracao` | Aumento de velocidade aplicado |

A função `sistemaBracoRobotico()` calcula a velocidade final e verifica se ela está dentro do limite de segurança.

### Regra de Segurança

```javascript
if (velocidadeFinal <= 100)
```

Resultado:

```text
SISTEMA SEGURO
```

ou

```text
ALERTA DE SOBRECARGA
```

---

## Exemplo

### Entrada

```javascript
let velocidadeAtual = 50;
let aceleracao = 30;
```

### Saída

```text
SISTEMA SEGURO
Velocidade Final: 80
```

---

## Tecnologias Utilizadas

- JavaScript
- Git
- GitHub

---

## Autor

Desenvolvido por **Lucas Augusto** para praticar conceitos básicos de JavaScript e lógica de programação.
