# EcoMonitor

## Identificação

Integrantes: Cecília Telles, Cauan Henrique e Davi Delmiro
Curso: Ciências da Computação
Disciplina: IHCUX

---

## Heurísticas de Nielsen aplicadas

*1. Visibilidade do status do sistema*
O sistema mantém o usuário informado ao exibir o contador de pontos atualizado em tempo real a cada interação com o botão.

*2. Feedback imediato*
Cada ação realizada pelo usuário gera uma resposta instantânea, com a atualização do contador e da barra de progresso, indicando claramente o resultado da interação.

*3. Consistência e padrões*
Os componentes seguem um padrão visual e funcional consistente, facilitando o aprendizado e uso do sistema.

---

## Guia de Execução

Para executar o projeto, utilize os comandos abaixo no terminal:

bash
dotnet restore
dotnet run --launch-profile https


Após a execução, acesse o endereço exibido no terminal (geralmente [https://localhost:xxxx](https://localhost:xxxx)) no navegador.

---

## Explicação Técnica

O componente EcoStatus foi desenvolvido utilizando o recurso de parâmetros do Blazor ([Parameter]), permitindo que ele seja reutilizado em diferentes contextos.

Foram utilizados os seguintes parâmetros:

* Titulo: define o nome da ação exibida no componente
* Peso: define o valor que será incrementado ao contador a cada clique

Exemplo de uso:

razor
<EcoStatus Titulo="Reciclagem de Plástico" Peso="1" />
<EcoStatus Titulo="Plantio de Árvores" Peso="10" />
<EcoStatus Titulo="Descarte de Eletrônicos" Peso="5" />


Dessa forma, o mesmo componente pode ser utilizado diversas vezes com comportamentos diferentes, evitando repetição de código e facilitando a manutenção.

---

## Funcionalidades

* Contador dinâmico por ação
* Incremento baseado no peso definido
* Barra de progresso visual
* Limite máximo de 100 pontos
* Exibição de mensagem ao atingir a meta

---
