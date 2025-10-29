---
title: Gestão e qualidade de software
date: 2025-10-29 09:03:00 -03:00
categories: [estudo, teste, gestão, qualidade]
tags: [estudo, engenharia, teste, qualidade, getão]
---
## qualidade:
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
## Teste 
para garantir a qualidade é fundamental fazer testes. Ele nada mais é que um conjunto de atividades feitas para identificar defeitos e falhas
### teste de software
No contexto atual temos dois tipos de teste:
1. Caixa branca
	Faz uso do código do programa
2. Caixa preta
	Não faz uso do código do programa(foco na interface)
#### O que o teste combate
Testes são feitos para identificar erros, defeitos e falhas. Podemos encapsular eles os chamando de **Bug**. `Erro humano produz defeito que gera falha.` .
1. **Defeito** é um comportamento inesperado que está em uma parte do produto e se refere a algo mal feito no código.
2. **Erro** é um código defeituoso feito por um dev.
3. **Falha** é quando o problema não deixa o programa funcionar.

