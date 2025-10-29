---
title: Gestão e qualidade de software
date: 2025-10-29 09:03:00 -03:00
categories: [estudo, teste, gestão, qualidade]
tags: [estudo, engenharia, teste, qualidade, getão]
---

## Índice dos Tipos de Teste

1. [Teste de Unidade](#teste-de-unidade)
2. [Teste de Integração](#teste-de-integração)
3. [Teste de Validação](#teste-de-validação)
4. [Teste de Sistema](#teste-de-sistema)
5. [Teste de Recuperação](#teste-de-recuperação)
6. [Teste de Segurança](#teste-de-segurança)
7. [Teste de Estresse](#teste-de-estresse)
8. [Teste de Desempenho](#teste-de-desempenho)
9. [Teste de Dublês](#teste-de-dublês)
10. [Teste de Regressão](#teste-de-regressão)
11. [Teste de Fumaça](#teste-de-fumaça)
12. [Teste de Aceitação](#teste-de-aceitação)

## Qualidade

Entrega de produtos/serviço com perfeito funcionamento e atendendo os pedidos do cliente

- Superar expectativas
- Produtos sem defeitos
- Fazer melhor com menos recursos
- Adequação ao uso
- Produzido por empresa certificada

### Qualidade de Software

Este atende a determinadas condições, sendo essas:

- **Conformidade com requisitos funcionais e de desempenho**  
  O software deve fazer o que se espera dele
- **Conformidade com padrões de desenvolvimento**  
  O processo de desenvolvimento deve seguir o que foi documentado e as boas práticas
- **Conformidade com requisitos implícitos**  
  Ele deve ter características de um produto profissional independentemente de ter sido solicitado, e isso se refere basicamente a segurança, usabilidade e confiabilidade

#### Organização

A visão básica da qualidade segue os três seguintes pontos:

1. O **usuário** deve ter facilidade no uso e poder confiar 100% no resultado
2. O **desenvolvedor** deve poder fazer manutenções de maneira fácil e receber claros requisitos do que é preciso ser feito
3. A **Organização** deve cumprir prazos e se atentar a evitar gastos e garantir boa produtividade

Porém além desses temos o foco do cliente, melhoria de processo, lado humano da qualidade, e métrica, modelos, medições e análise. Mas em resumo todos esses são apenas nomes específicos para o generalismo dos três pontos acima.

Ele pode ser descrito também de outra maneira:

- **Verificação -** Estamos construindo isso certo?
- **Validação -** Estamos construindo o trem certo ou é outra coisa completamente diferente?

#### Classificações

##### CMMI - Capability Maturity Model Integration

Ele tem cinco níveis:

1. Inicial:  
   Todo bagunçado e sem lugar pra fazer certo
2. Gerenciado:  
   É um pouco melhor que o um já que agora tem requisitos e processos planejados
3. Definido:  
   Aqui já está bom o suficiente, o normal que todo mundo espera
4. Gerenciado quantitativamente:  
   Os processos agora são controlados usando estatísticas e coisas assim
5. Otimizado:  
   Aqui já é frescura

##### MPS.BR

Aqui tem 7 níveis mas não vale nem a pena citar, só existe no Brasil e ninguém é tão nacionalista assim

##### ISO 9001:2008

Garante a rastreabilidade do processo e fornece meios apropriados de ação corretiva. Além disso padroniza todos os processos que afetam o produto e o cliente

##### ISO/IEC 9126

Norma que propõe atributos de qualidade em 6 partes:

1. Funcionalidade
2. Confiabilidade
3. Usabilidade
4. Eficiência
5. Manutenibilidade
6. Portabilidade

##### ISO/IEC 12207

Estabelece uma estrutura para o ciclo de vida do software, visando a ajudar na compreensão de tudo. Ele é dividido em fundamentais, apoio e organização

##### ISO/IEC 15504

Parecido com o CMMI

## Teste

Para garantir a qualidade é fundamental fazer testes. Ele nada mais é que um conjunto de atividades feitas para identificar defeitos e falhas.

### O que o teste combate

Testes são feitos para identificar erros, defeitos e falhas. Podemos encapsular eles os chamando de **Bug**. `Erro humano produz defeito que gera falha`.

1. **Defeito** é um comportamento inesperado que está em uma parte do produto e se refere a algo mal feito no código
2. **Erro** é um código defeituoso feito por um dev
3. **Falha** é quando o problema não deixa o programa funcionar

## Tipos de Teste

### Teste de Unidade

- Verificação da menor unidade
- Baseado na caixa branca
- Verificar se tem erro antes de integrar
- Pode acontecer muitos ao mesmo tempo

### Teste de Integração

- Verifica a comunicação de diferentes partes
- Tenta garantir a amizade de todos os componentes
- Se faz depois do unitário e antes do de sistema
- Feito pra validar requisitos e verificar a comunicação

### Teste de Validação

- Verificar se os dois últimos foi feito certo
- Ter certeza se os trem está atendendo as expectativas do usuário
- Olha a parte de segurança e desempenho
- Garante que o produto esteja pronto pra lançar
- Da feedback pra ter certeza
- Feito pra garantir que o usuário fique feliz

### Teste de Sistema

Esse é um monte de teste diferente, mas é principalmente feito olhando no ponto de vista do usuário

### Teste de Recuperação

Ele força a falha de todo jeito e verifica se a recuperação vai funcionar

### Teste de Segurança

Verifica se está protegido de invasão

### Teste de Estresse

Faz um bilhão de coisa ao mesmo tempo pra ver se não vai cair

### Teste de Desempenho

Testa o desempenho...

### Teste de Dublês

Literalmente dublês. Dai ele garante que que você consiga escrever em algo que tenha dependência.

#### Mock
Simular a interface ou classes, assim dá pra isolar o problema

#### Dummies
Dados falsos pra deixar o teste mais fácil

#### Fake
Objetos reais que não dá pra usar

#### Spies
É um agente russo infiltrado que olha se a função foi chamada, quantas vezes foi, o que precisou e assim vai

#### Stubs
Igual o spies porém ele consegue substituir coisa e simular execução

### Teste de Regressão

- Verifica se novas mudanças não fizeram voltar erros antigos

### Teste de Fumaça

- Verifica se o software liga sem falhas críticas
- Garante que as funcionalidades básicas estão funcionando antes dos mais avançados
- Basicamente garante que o mínimo está funcionando #FelizNoSimples

### Teste de Aceitação

- Coloca pra um monte de random pra testar
- Verifica se fez o check em tudo que precisava

## Padrões de Teste

### Padrão AAA

> **Nota:** Este padrão é comumente usado em testes unitários

#### Arrange
Configura o cenário: Variáveis, objetos, mocks, dependências...

#### Act
Executa a função/comportamento do que está sendo testado

#### Assert
Confere se funcionou