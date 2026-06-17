# Machine Learning

Repositorio com notebooks desenvolvidos para a disciplina de Machine Learning no IBMEC. O material cobre conceitos introdutorios, preparacao de dados, analise exploratoria, pipelines de classificacao, avaliacao de modelos e uso de ferramentas de AutoML.

## O que e Machine Learning?

Machine Learning, ou aprendizado de maquina, e uma area da inteligencia artificial em que algoritmos aprendem padroes a partir de dados para fazer previsoes, classificacoes ou recomendacoes. Em vez de escrever regras fixas manualmente, treinamos modelos com exemplos historicos e avaliamos se eles conseguem generalizar para novos dados.

Nos notebooks deste repositorio aparecem etapas comuns de um projeto de ML:

1. definicao do problema e da variavel-alvo;
2. coleta e carregamento dos dados;
3. analise exploratoria dos dados (EDA);
4. tratamento de valores ausentes e variaveis categoricas;
5. engenharia de atributos;
6. divisao entre treino, validacao e teste;
7. treinamento de modelos;
8. comparacao por metricas;
9. interpretacao dos resultados e cuidados como data leakage, desbalanceamento e fairness.

## Notebooks

### `aula01_ML.ipynb`

Notebook introdutorio da disciplina. Apresenta o carregamento inicial de dados, manipulacao com `pandas`, visualizacoes com `matplotlib` e `seaborn`, e os primeiros conceitos praticos usados em problemas de aprendizado de maquina.

### `ML_Ap1.ipynb`

Projeto de modelagem preditiva sobre saude mental durante a COVID-19. O notebook trabalha um problema de classificacao binaria, passando por tratamento de dados, EDA, engenharia de atributos, validacao cruzada estratificada, ajuste de hiperparametros, comparacao estatistica entre modelos, calibracao de probabilidades e analise de equidade por subgrupos demograficos.

Principais topicos:

- tratamento de missing values;
- avaliacao de desbalanceamento de classes;
- pipelines com `scikit-learn`;
- modelos como Regressao Logistica, Naive Bayes, Random Forest, Gradient Boosting e XGBoost;
- metricas como AUC-ROC, F1-score, precision, recall, Brier Score e matriz de confusao;
- teste de McNemar;
- interpretabilidade com SHAP;
- analise de fairness.

### `AP2_ML_AutoGluon_JoaoGabriel.ipynb`

Projeto de classificacao supervisionada usando AutoGluon. O problema consiste em prever se um cliente de uma instituicao bancaria aceitaria um deposito a prazo com base em dados de campanha de marketing.

Principais topicos:

- formulacao do problema de negocio;
- classificacao binaria;
- EDA de variaveis numericas e categoricas;
- identificacao de data leakage na variavel `duracao`;
- divisao treino/teste estratificada;
- baselines com classe majoritaria e Regressao Logistica;
- treinamento com `AutoGluon TabularPredictor`;
- comparacao entre modelos e interpretacao das metricas.

### `Pipeline_Sinistros.ipynb`

Notebook voltado para a construcao de um pipeline de machine learning para prever o tipo de sinistro a partir de dados historicos de nao conformidades em transportes.

Principais topicos:

- definicao do problema;
- separacao inicial de dados de trabalho e validacao;
- EDA;
- limpeza e imputacao;
- engenharia de atributos, incluindo variaveis derivadas de data;
- codificacao de variaveis categoricas;
- balanceamento com SMOTE;
- treinamento e avaliacao de modelos de classificacao.

## Bibliotecas utilizadas

Os notebooks usam principalmente:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `imbalanced-learn`
- `xgboost`
- `statsmodels`
- `shap`
- `joblib`
- `holidays`
- `requests`
- `autogluon`

Nem todos os notebooks usam todas as bibliotecas. Algumas dependencias, como `autogluon`, podem ser mais pesadas e sao mais faceis de executar em ambientes como Google Colab.

## Como executar

Clone o repositorio e abra os notebooks no Jupyter, VS Code ou Google Colab.

Exemplo de instalacao das dependencias principais:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost statsmodels shap joblib holidays requests
```

Para o notebook com AutoGluon:

```powershell
pip install autogluon
```

Tambem e possivel executar diretamente no Google Colab quando o notebook tiver o botao "Open in Colab".

## Observacoes importantes

- Sempre separe dados de treino e teste antes de avaliar o desempenho final.
- Evite data leakage: variaveis que so seriam conhecidas depois do evento previsto nao devem entrar no treinamento.
- Em problemas com classes desbalanceadas, acuracia isolada pode enganar. Use metricas como recall, precision, F1-score, AUC-ROC e matriz de confusao.
- Pipelines ajudam a manter o pre-processamento consistente entre treino, validacao e teste.
- A interpretacao dos resultados deve considerar o contexto do problema, o custo dos erros e possiveis vieses nos dados.

## Estrutura do repositorio

```text
.
+-- AP2_ML_AutoGluon_JoaoGabriel.ipynb
+-- ML_Ap1.ipynb
+-- Pipeline_Sinistros.ipynb
+-- aula01_ML.ipynb
+-- README.md
```
