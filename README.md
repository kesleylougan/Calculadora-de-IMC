# Calculadora de Índice de Massa Corporal (IMC)

## Introdução

Esta é uma simples calculadora de IMC criada utilizando HTML, CSS e JavaScript. O Índice de Massa Corporal (IMC) é uma medida que relaciona o peso e a altura de uma pessoa, sendo amplamente utilizada para avaliar se uma pessoa está dentro de faixas consideradas saudáveis.

## Funcionalidade

A calculadora oferece as seguintes funcionalidade:

- **Entrada de Dados:** Campos para inserção do peso e altura.

- **Botão de Cálculo:** Um botão que, ao ser clicado, realiza o cálculo do IMC.

- **Exibição de Resultado:** A exibição do resultado do cálculo, indicando se o índice está dentro da faixa considerada normal, abaixo do peso, com sobrepeso, obesidade leve, obesidade moderada ou obesidade grave.


## Tecnologias Utilizadas

**HTML:** Utilizado para a estrutura básica do formulário.

**CSS:** Aplicado para estilizar e formatar a aparência da calculadora.

**JavaScript:** Implementado para realizar o cálculo do IMC e exibir o resultado dinamicamente na página.

## Código (JavaScript) da aplicação


var peso;
var altura;
var imc;
var resultado;


function calcular(event){
  event.preventDefault();

  peso = document.getElementById('peso').value;
  altura = document.getElementById('altura').value;

  imc = peso / (altura * altura)

  resultado = document.getElementById('resultado');

  if(imc < 17){
    resultado.innerHTML = '<br> Seu resultado foi: ' + imc.toFixed(2) + '<br>' + 'Cuidado você está muito abaixo do peso!';
  }else if(imc > 17 && imc <= 18.49){
    resultado.innerHTML = '<br> Seu resultado foi: ' + imc.toFixed(2) + '<br>' + 'Você está muito Abaixo do peso!';
  }else if(imc >= 18.5 && imc < 24.99){
    resultado.innerHTML = '<br> Seu resultado foi: ' + imc.toFixed(2) + '<br>' + 'Você está no peso ideal!';
  }else if(imc > 25 && imc <= 29.99){
    resultado.innerHTML = '<br> Seu resultado foi: ' + imc.toFixed(2) + '<br>' + 'Você está com Acima do peso.';
  }else if(imc > 30){
    resultado.innerHTML = '<br> Seu resultado foi: ' + imc.toFixed(2) + '<br>' + 'Cuidado Obesidade.';
  }
}


