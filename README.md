# Previsão de Vendas e Regressão Linear Simples

## Visão geral

Este projeto aplica **regressão linear simples** para estimar vendas de sorvetes a partir da temperatura ambiente. O desenvolvimento foi realizado em Python, em um notebook Jupyter, contemplando exploração dos dados, análise de correlação, treinamento de modelo supervisionado, previsões e avaliação de desempenho.

O objetivo é demonstrar, em um cenário didático, como uma variável explicativa pode ser utilizada para construir e avaliar um modelo de previsão numérica.

## Objetivo

Investigar a relação entre temperatura e vendas de sorvetes e treinar um modelo capaz de estimar as vendas com base nos registros disponíveis.

## Dados utilizados

A base `Sorvete.xlsx` possui **100 registros** e duas colunas:

| Variável | Descrição | Papel no modelo |
|---|---|---|
| `Temperatura` | Temperatura ambiente, em °C | Variável explicativa (X) |
| `Vendas_Sorvetes` | Vendas de sorvetes, indicadas no notebook em milhares | Variável-alvo (y) |

A origem e o processo de coleta dos dados não estão documentados no material fornecido. Portanto, os resultados devem ser interpretados como um exercício de modelagem, e não como uma validação para operação comercial real.

## Tecnologias

- **Python** — implementação das análises;
- **Pandas** — leitura da planilha e manipulação dos dados;
- **Matplotlib** — visualizações gráficas;
- **Scikit-learn** — divisão treino/teste, regressão linear e métricas de avaliação;
- **Jupyter Notebook** — execução e documentação do experimento;
- **Excel (.xlsx)** — formato da base de dados.

## Metodologia

1. **Importação dos dados:** leitura do arquivo `Sorvete.xlsx` com Pandas.
2. **Análise exploratória:** gráfico de dispersão e matriz de correlação entre temperatura e vendas.
3. **Preparação para modelagem:** definição de temperatura como entrada e vendas como variável-alvo.
4. **Separação dos dados:** 80 observações para treinamento e 20 para teste, com `random_state=42`.
5. **Treinamento:** ajuste de `LinearRegression` do Scikit-learn.
6. **Avaliação:** previsões no conjunto de teste, cálculo de MSE, MAE e R², além da visualização de valores reais e previstos.

## Resultados

| Indicador | Valor |
|---|---:|
| Registros | 100 |
| Treinamento | 80 registros |
| Teste | 20 registros |
| Correlação de Pearson (temperatura × vendas) | 0,9856 |
| Erro quadrático médio (MSE) | 101,65 |
| Erro absoluto médio (MAE) | 7,68 |
| Coeficiente de determinação (R²) | 0,9594 |

Os resultados exibidos no notebook indicam uma **forte associação linear positiva** entre temperatura e vendas. No conjunto de teste, o modelo obteve R² de aproximadamente **95,94%**, explicando essa proporção da variabilidade observada nas vendas da amostra de teste.

O bom resultado nesta base não comprova causalidade nem assegura desempenho com dados de outras lojas, localidades ou períodos.

## Como executar

1. Instale Python e abra o projeto em um ambiente com suporte a Jupyter Notebook.
2. Instale as dependências:

   ```bash
   pip install pandas matplotlib scikit-learn openpyxl notebook
   ```

3. Mantenha `Sorvete.xlsx` na mesma pasta de `Regressao_Linear_Simples.ipynb`.
4. Abra o notebook e execute as células sequencialmente:

   ```bash
   jupyter notebook Regressao_Linear_Simples.ipynb
   ```

## Estrutura do repositório

```text
previsao-vendas-regressao-linear/
├── Regressão_Linear_Simples.ipynb  # Análise exploratória e modelo de regressão
├── Sorvete.xlsx                   # Base de dados utilizada
└── README.md                      # Documentação
```

## Limitações e próximos passos

- Investigar resíduos e possíveis desvios das premissas do modelo linear.
- Avaliar o comportamento em novos conjuntos de dados ou períodos.
- Comparar o desempenho com um modelo de referência simples.
- Registrar a procedência dos dados e contextualizar a unidade de vendas.

Essas possibilidades são **evoluções sugeridas** e não funcionalidades já implementadas no notebook.
