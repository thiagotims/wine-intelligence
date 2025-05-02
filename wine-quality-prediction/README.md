
# 🍷 Classificação da Qualidade de Vinhos Tintos com Machine Learning

Este projeto utiliza **técnicas de análise exploratória de dados (EDA)** e **modelos de machine learning supervisionado** para prever se um vinho tinto possui **boa qualidade** com base em suas propriedades físico-químicas.

---

## ✨ Apresentação

A previsão da qualidade de um vinho é uma tarefa desafiadora e interessante, principalmente por envolver tanto variáveis químicas mensuráveis quanto aspectos sensoriais subjetivos. Neste projeto, utilizamos o dataset **Wine Quality – Red Wine**, disponível no UCI Machine Learning Repository, para realizar:

- Análises estatísticas e visuais
- Engenharia de atributos (target binário: vinho bom ou não)
- Treinamento e avaliação de múltiplos modelos de classificação
- Comparação de desempenho entre os modelos

---

## 🔍 Origem do Dataset

**Fonte:** UCI Machine Learning Repository  
**Título original:** Wine Quality Data Set  
**Link:** [https://archive.ics.uci.edu/ml/datasets/Wine+Quality](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)

### 📁 Características

- Tipo: Vinho Tinto
- Número de amostras: **1599**
- Número de atributos: **12** (11 variáveis independentes + qualidade sensorial)
- Atributo alvo: `quality` (escala de 0 a 10, geralmente entre 3 e 8)
- Alvo binarizado no projeto: `goodquality` (1 se `quality >= 7`, senão 0)

---

## 🍷 Atributos físico-químicos (variáveis independentes)

| Atributo                 | Descrição                                       |
|--------------------------|-------------------------------------------------|
| fixed acidity            | Acidez fixa (principalmente ácido tartárico)   |
| volatile acidity         | Ácido acético — em excesso gera odor ruim      |
| citric acid              | Ácido cítrico — dá frescor e conservação       |
| residual sugar           | Açúcar residual — influência no sabor final    |
| chlorides                | Cloretos — concentração de sal                 |
| free sulfur dioxide      | Dióxido de enxofre livre — combate oxidação    |
| total sulfur dioxide     | Total de dióxido de enxofre                    |
| density                  | Densidade — relacionada ao teor alcoólico      |
| pH                       | pH da bebida — acidez total                    |
| sulphates                | Sulfatos — conservante                         |
| alcohol                  | Teor alcoólico                                 |

---

## 📊 Estatísticas Resumidas

| Variável               | Média   | Desvio Padrão | Mínimo | Máximo |
|------------------------|---------|----------------|--------|--------|
| **fixed acidity**       | 8.32    | 1.74           | 4.60   | 15.90  |
| **volatile acidity**    | 0.53    | 0.18           | 0.12   | 1.58   |
| **citric acid**         | 0.27    | 0.19           | 0.00   | 1.00   |
| **residual sugar**      | 2.54    | 1.41           | 0.90   | 15.50  |
| **chlorides**           | 0.09    | 0.05           | 0.01   | 0.61   |
| **free sulfur dioxide** | 15.87   | 10.46          | 1.00   | 72.00  |
| **total sulfur dioxide**| 46.47   | 32.90          | 6.00   | 289.00 |
| **density**             | 0.9967  | 0.0019         | 0.9901 | 1.0037 |
| **pH**                  | 3.31    | 0.15           | 2.74   | 4.01   |
| **sulphates**           | 0.66    | 0.17           | 0.33   | 2.00   |
| **alcohol**             | 10.42   | 1.07           | 8.40   | 14.90  |
| **quality**             | 5.64    | 0.81           | 3.00   | 8.00   |

---

## 🛠️ Modelos Treinados

Foram avaliados os seguintes algoritmos de classificação:

- Regressão Logística
- K-Nearest Neighbors (KNN)
- Support Vector Classifier (SVC)
- Árvore de Decisão
- Naive Bayes
- Random Forest
- XGBoost

Cada modelo foi avaliado com as métricas: **Accuracy, F1 Score, Precision, Recall** e matriz de confusão.

---

## 📊 Ficha Técnica

| 🔍 Item                | 📄 Descrição                                                              |
|------------------------|---------------------------------------------------------------------------|
| 🛠️ Tecnologias         | Python, Scikit-learn, Seaborn, Matplotlib, NumPy, Pandas, XGBoost         |
| 📦 Dependências         | `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`     |
| 📊 Dataset Utilizado   | `winequality-red.csv` — disponível em UCI Machine Learning Repository     |
| 📌 Modelos             | Vários: Logistic Regression, KNN, SVC, Decision Tree, Naive Bayes, etc.   |
| 🎯 Target              | Qualidade do vinho (binarizado: bom ≥ 7, ruim < 7)                        |
| 📈 Avaliação           | Accuracy, Precision, Recall, F1-Score, Matriz de Confusão                 |
| 🔄 Split               | Treinamento/Teste (70/30) usando `train_test_split`                      |

---

## 📂 Estrutura do Projeto



```
wine-quality-ml/
│
├── src/
│   └── winequality-red.csv      # Dataset 
│
├── wine_analysis.ipynb          # Notebook completo com EDA + ML
├── README.md                    # Este arquivo
└── requirements.txt             # Lista de dependências (pip install -r requirements.txt)
```

---

## 💡 Próximos Passos

- Testar normalização/padronização nos modelos
- Aplicar GridSearchCV para ajuste de hiperparâmetros
- Criar dashboard visual em Streamlit ou Gradio
- Exportar os modelos com `joblib` ou `pickle`

---

## 📬 Contato

Para dúvidas, sugestões ou colaboração, sinta-se à vontade para abrir uma *issue* ou me enviar uma mensagem!
