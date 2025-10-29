---
title: Gestão e qualidade de software
date: 2025-10-29 09:03:00 -03:00
categories: [estudo, teste, gestão, qualidade]
tags: [estudo, engenharia, teste, qualidade, getão]
---

## Qualidade:
Entrega de produtos/serviço com perfeito funcionamento e atendendo os pedidos do cliente
- Superar expectativas
- Produtos sem defeitos
- Fazer melhor com menos recursos
- Adequação ao uso
- Produzido por empresa certificada

### Qualidade de Software
este atende a determinadas condições, sendo essas:
- **Conformidade com requisitos funcionais e de desempenho**
	o software deve fazer o que se espera dele 
- **Conformidade com padrões de desenvolvimento**
	O processo de desenvolvimento deve seguir o que foi documentado e as boas praticas
- **Conformidade com requisitos implícitos**
	Ele deve ter características de um produto profissional independentemente de ter sido solicitado, e isso se refere basicamente a segurança, usabilidade e confiabilidade

#### organização
A visão básica da qualidade segue os três seguintes pontos:
1. O **usuário** deve ter facilidade no uso e poder confiar 100% no resultado .
2. O **desenvolvedor** deve poder fazer manutenções de maneira fácil e receber claros requisitos do que é preciso ser feito.
3. A **Organização** deve cumprir prazos e se atentar a evitar gastos e garantir boa produtividade 
Porem além desses temos o foco do cliente, melhoria de processo, lado humano da qualidade, e métrica, modelos, medições e análise. Mas em resumo todos esses são apenas nomes específicos para o generalismo dos três prontos acima.

ele pode ser descrito também de outra maneira:
- **Verificação -** Estamos construindo isso certo?
- **Validação -** Estamos construindo o trem certo ou é outra coisa completamente diferente?

#### Classificações
##### CMMI - Capability Maturity Model Integration
ele tem cinco níveis:
1. Inicial:
	todo bagunçado e sem lugar pra fazer certo
2. gerenciado:
	é um pouco melhor que o um já que agora tem requisitos e processos planejados
3. Definido:
	aqui já esta bom o suficiente, o normal que todo mundo espera
4. Gerenciado quantitativamente:
	os processos agora são controlados usando estatísticas e coisas assim
5. Otimizado:
	aqui ja é frescura

##### MPS.BR
aqui tem 7 níveis mas não vale nem apena citar, só existe no brasil e ninguém é tão nacionalista assim

##### ISO 9001:2008
Garante a rastreabilidade do processo e fornece meios apropriados de ação corretiva. Além disso padroniza todos os processos que afetam o produto e o cliente

##### ISO/IEC 9126
norma que propõe atributos de qualidade em 6 partes:
1. funcionalidade
2. confiabilidade
3. usabilidade
4. eficiência
5. manutenibilidade
6. portabilidade 

##### ISO/IEC 12207
Estabelece uma estrutura para o ciclo de vida do software, visando a ajudar na compreensão de tudo. Ele é dividido em fundamentais, apoio e organização 

##### ISO/IEC 15504
parecido com o cmmi


## Teste 
para garantir a qualidade é fundamental fazer testes. Ele nada mais é que um conjunto de atividades feitas para identificar defeitos e falhas
### teste de software
No contexto atual temos dois tipos de teste:
1. Caixa branca
	Faz uso do código do programa
2. Caixa preta
	Não faz uso do código do programa(foco na interface)
### O que o teste combate
Testes são feitos para identificar erros, defeitos e falhas. Podemos encapsular eles os chamando de **Bug**. `Erro humano produz defeito que gera falha.` .
1. **Defeito** é um comportamento inesperado que está em uma parte do produto e se refere a algo mal feito no código.
2. **Erro** é um código defeituoso feito por um dev.
3. **Falha** é quando o problema não deixa o programa funcionar.


## Fracasso
motivos que podem causar o fracasso de um software seriam os seguintes:
1. O escopo mal feito pode fazer o analista não conseguir entender nada do que é pra fazer, o usuário ficar perdido e falhar completamente a comunicação entre os dois. e isso piora se o usuário não se envolver pra tentar deixar mais claro as coisas.
2. Não analisarem os possíveis riscos que pode ter que atrasaria a entrega e/ou deixaria mais caro.
3. Pessoas que não sabem trabalhar em equipe que atrapalha mais do que ajuda.
4. Liderança meia boca que não faz nem o mínimo de acompanhar como o projeto vai indo.
5. Falta de teste ou ter feito eles de maneira porca

## Modelos de qualidade
- Ciclo PDCA: plan, do, check, act
- Ciclo IDEAL: inicio, diagnostico, estabelecimento, ação, ligação

## Teste shippuden 
voltando a falar de teste só que agora com mais coisa.
### Objetivos do teste
Ele deve ser feito muitas vezes em toda a vida do software pq sempre pode da b.o. Dai você sabendo o que é o esperado vai analisando se realmente ta chegando no objetivo.

### Caixa preta (black box)
Esse é um tipo de teste focado em verificar se o sistema responde corretamente as entradas do usuário, exibindo os dados de forma adequada e processando formulários certinho.
### Caixa branca (white box)
Esse é um tipo de teste focado em verificar o funcionamento interno do sistema, analisando código fonte, estrutura de decisão e fluxo de execução. basicamente garantir que a logica está correta.
`sequencia, if, while, case`

# Estratégia de teste
### Teste de unidade
- Verificação da menor unidade 
- baseado na caixa branca
- verificar se tem erro antes de integrar 
- pode acontecer muitos ao mesmo tempo
### Teste de integração
- Verifica a comunicação de diferentes partes
- tenta garantir a amizade de todos os componentes
- se faz depois do unitário e antes do de sistema
- feito pra validar requisitos e verificar a comunicação
### Teste de validação
- Verificar se os dois últimos foi feito certo
- Ter certeza se os trem esta atendendo as expectativas do usuário
- Olha a parte de segurança e desempenho
- garante que o produto esteja pronto pra lançar
- da feedback pra ter certeza
- feito pra garantir que o usuário fique feliz
### Teste de sistema
esse é um monte de teste diferente, mas é principalmente feito olhando no ponto de vista do usuário.
#### Teste de recuperação
ele força a falha de todo jeito e verifica se a recuperação vai funcionar
#### Teste de segurança
verifica se ta protegido de invasão
#### Teste de estresse
Faz um bilhão de coisa ao mesmo tempo pra ve se não vai cair
#### Teste de desempenho
testa o desempenho...

## Teste, o império contra ataca
mais do mesmo só que diferente

### Padrão/pattern AAA
> eu acho que isso aqui faz parte do teste unitário, o slide é muito confuso pra ter certeza.  chega ta escrito em ingles
{: .prompt-danger  }

#### Arrange
configura o cenário: Variaveis, objetos, mocks, dependencias...
#### Act
Executa a função/comportamento do que está sendo testado
#### Assert
confere se funcionou

### Teste de Dublês
literalmente dublês. dai ele garante que que você consiga escrever em algo que tenha dependencia.

#### Mock
Simular a interface ou classes, assim da pra isolar o problema
#### Dummies
Dados falso pra deixar o teste mais fácil
#### Fake
Objetos reais que não da pra usar
#### Spies
é um agente russo infiltrado que olha se a função foi chamada, quantas vezes foi, oq precisou e assim vai
#### Stubs
Igual o spies porem ele consegue substituir coisa e simular execução 


### Teste de Regressão
- Verifica se novas mudanças não fizeram voltar erros antigos

### Teste de Fumaça
- verifica se o software liga sem falhas criticas
- garante que as funcionalidades básicas estão funcionando antes dos mais avançados
- basicamente garante que o mínimo esta funcionando #FelizNoSimples

### Teste de aceitação
- coloca pra um monte de random pra testar
- verifica se fez o check em tudo que precisava