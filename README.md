# Bank Customer Churn Analysis
Projeto de análise de churn em banco digital com foco na identificação dos principais fatores de evasão. A partir de dados demográficos, produtos, engajamento e reclamações, foram explorados padrões de comportamento e gerados insights para apoiar estratégias de retenção e priorização de clientes.

## Objetivo

Identificar os principais fatores associados ao cancelamento de clientes (churn) em um banco digital, utilizando análises estatísticas e exploração de dados para apoiar estratégias de retenção.

## Base de Dados

A base contém aproximadamente 10 mil clientes com informações como:

- Dados demográficos (idade, geografia)
- Produtos contratados
- Saldo em conta
- Engajamento
- Reclamações
- Pontuação de satisfação
- Status do cliente (ativo ou cancelado)
- 
## Metodologia

O estudo foi dividido em etapas:

1. Análise de poder preditivo das variáveis (Information Value - IV)  
2. Correlação entre atributos  
3. Estatísticas descritivas para ativos vs cancelados  
4. Distribuições e histogramas  
5. Identificação de outliers  
6. Interpretação de impacto no churn  

Todas as análises foram realizadas em **Excel**, utilizando tabelas dinâmicas, fórmulas, segmentações e recursos gráficos.

## Information Value (IV)

Foi calculado o IV para medir a capacidade de cada variável em diferenciar clientes ativos de cancelados.

### Variáveis mais relevantes:
- **Complain** (IV ≈ 1,99) → altíssimo poder de explicação  
- **NumOfProducts** (IV ≈ 0,72) → muito relevante  
- **Faixa de Idade** (IV ≈ 0,65)  
- **IsActiveMember** e **Geography** também apresentaram impacto moderado.

Variáveis como Score, Pontos, Cartão e Salário apresentaram baixo poder discriminatório.

## Correlação

A matriz de correlação indicou algumas relações importantes:

- Reclamações possuem associação positiva com churn.  
- Clientes ativos tendem a apresentar menor probabilidade de saída.  
- Número de produtos mostrou relação relevante com permanência.

## Estatística Descritiva

Comparando clientes ativos e cancelados:

### Idade
Clientes que cancelaram são, em média, **mais velhos**.

### Saldo
Clientes cancelados apresentaram **maiores valores médios de saldo**.

### Número de produtos
Clientes que permanecem geralmente possuem **mais de 1 produto contratado**.

## Distribuições

Os histogramas evidenciaram:

- Maior taxa de cancelamento em clientes com poucos produtos.  
- Concentração de evasão em determinadas faixas etárias.  

## Outliers

Foram calculados quartis, intervalos interquartílicos e limites para identificar valores extremos em variáveis como idade e saldo.  
Esses pontos ajudam a entender perfis atípicos que podem influenciar modelos futuros.

## Conclusões da Análise

### Perfil etário
Clientes mais jovens tendem a permanecer ativos. A maior incidência de cancelamentos ocorre entre clientes de **46 a 60 anos**, mesmo considerando menor volume relativo.

### Sexo
Observou-se maior permanência entre clientes do **sexo masculino**, enquanto o público feminino apresentou proporção superior de evasão.

### Hábitos financeiros (Saldo)
Clientes que cancelaram possuem média de saldo próxima a **R$ 91 mil**.  
Entretanto, a alta dispersão, assimetria e coeficiente de variação indicam grande variabilidade, exigindo cautela na interpretação isolada dessa métrica.

### Quantidade de produtos
Clientes com **apenas 1 produto** apresentam maior risco de churn.  
O menor índice de cancelamento ocorre em clientes com **2 produtos**, sugerindo um ponto ideal de relacionamento.  
A partir de 3 ou mais produtos, o risco volta a aumentar.

### Tempo de relacionamento
O tempo de permanência no banco não se mostrou determinante para explicar o cancelamento.

---

## Variáveis com maior poder explicativo do churn

Com base na análise de Information Value (IV), destacam-se:

- **Complain**
- **NumOfProducts**
- **Faixa etária**
- **IsActiveMember**
- **Saldo**

Essas variáveis devem ser priorizadas em estratégias de monitoramento e em futuros modelos preditivos.
