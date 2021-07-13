# Desafio de Data Science do Cognitivo

Neste desafio escolhi construir um modelo preditivo para preços de anúncios do AirBnb.

Essas três tabelas passarão por um tratamento prévio no notebook `1 - Preparação de dados`, no qual algumas variáveis serão tratadas e a porção que usarei para teste é reservada. Essa porção é importante para validarmos o comportamento do nosso modelo numa situação real.

## Perguntas

a. Como foi a definição da sua estratégia de modelagem?

Avaliando-se as tabelas disponíveis para a cidade, três me chamaram mais atenção: `calendar`, `listings` e `reviews`.

Primeiramente, no notebook `1 - Preparação de dados` fiz alguns tratamentos prévios nos dados, como abertura dos elementos da lista e extração de informação textual

Em seguida, no notebook `2 - Explora Dados` realizei algumas descobertas como a presença marcante de outliers. Existem alguns anúncios de valores altos, fiz algumas descobertas que virão a ser úteis na aplicação do modelo

Finalmente, no notebook `3 - Modelo` realizei experimentos com o a regressão em randomForrest.

b. Como foi definida a função de custo utilizada?

Observo dois ao analisar os modelos, a média quadrática do erro e a quantidade de erros maiores que 1000. O modelo é extremamente penalizado pelos outliers, por isso achei mais razoável tentar reduzir erros de grande magnitude. Avaliei também erros de magnitude menor que 1000 para avaliar se dentro da mesma faixa o modelo performava bem.

c. Qual foi o critério utilizado na seleção do modelo final?

Após alguns 30 execuções escolhi seguir com o modelo que não separa por bairros. Apesar do comportamento da Zona Sul e Barra ser muito distinto dos demais em relação aos anúncios mais custosos, separar os modelos não trouxe nenhum benefício

d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método?

Executei 30 vezes com os mesmos datasets de treino e validação, para evitar flutuações e avaliando que todos os critérios adotados não mudaram signficativamente, decidi seguir com a solução mais simples.

e. Quais evidências você possui de que seu modelo é suficientemente bom?

Não acredito que ele seja ainda um modelo bom para produção. Mas acredito que o modelo usa todas informações relevantes para determinar o preço. Acredito essa discussão está mais detalhada no notebook `2 - Explora Dados`

---

Para a comissão avaliadora: Se interessar verificar análise da qualidade do modelo que fiz após o prazo, olhe a branch `adiciona_teste` deste repositório
