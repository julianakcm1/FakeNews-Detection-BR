# Implementação dos Experimentos para Detecção de Fake News em Português

Repositório contendo os códigos utilizados na monografia ****, apresentada no Instituto de Computação da Universidade Federal de Alagoas (UFAL).

### 🎯 Objetivo: 

Este repositório tem como objetivo garantir a **transparência metodológica**, **reprodutibilidade** e **facilidade de acesso** aos experimentos descritos no Trabalho de Conclusão de Curso, incluindo:
- Pré-processamento textual completo;
- Extração de características via TF-IDF;
- Implementação dos modelos KNN, Naive Bayes Gaussiano e Regressão Logística;
- Ajuste de hiperparâmetros por Grid Search;
- Validação cruzada k-fold;
- Geração das matrizes de confusão e métricas finais.

### 🧪 Metodologia dos experimentos

Os experimentos foram realizados seguindo as etapas:

#### **1. Pré-processamento**
- Normalização com `Unidecode`
- Lowercase
- Remoção de URLs, números, pontuação e tokens pequenos
- Tokenização
- Remoção de stopwords (NLTK)

#### **2. Extração de características**
- TF-IDF (`max_features = 5000`)
- Para Naive Bayes na base Fake.Br: grid search testando  
  **3000, 5000, 7000 features**

#### **3. Modelos utilizados**
- **K-Nearest Neighbors (KNN)**  
  - Métrica: Euclidean ou Manhattan  
  - Pesos: uniform ou distance  
  - *Grid Search* para `n_neighbors`

- **Naive Bayes Gaussiano**  
  - Conversão de matriz esparsa → densa com `FunctionTransformer`

- **Regressão Logística**
  - Penalidade `l1` ou `l2`
  - C ∈ {0.1, 1, 5, 10}
  - Solver: `liblinear` ou `lbfgs`

#### **4. Validação**
- Validação cruzada 5-fold
- Métricas: Acurácia, Precisão, Recall, F1, ROC AUC

### 🧠 Tecnologias usadas:
- Python 3.12  
- Google Colab  
- Scikit-learn  
- NLTK  
- NumPy / Pandas  
- Matplotlib / Seaborn

### 📊 Resultados

Os resultados obtidos, incluindo:
- métricas médias dos 5 folds,
- matrizes de confusão,
- gráficos comparativos entre as bases,

estão disponíveis no arquivo `Resultados.ipynb`.

Os valores completos também foram reportados na monografia.

### ▶️ Como Executar

**Via Google Colab (recomendado)**
1. Abra qualquer notebook em `notebooks/`
2. As bases são carregadas automaticamente via link
3. Execute as células na ordem

### 📝 Citação

Caso deseje citar este repositório:

BARACHO, Juliana K. C. M. Fake News Detection BR – Repositório de códigos. <br>
Disponível em: https://github.com/julianakcm1/FakeNews-Detection-BR

### 👩‍💻 Autora

Juliana Karla de Carvalho Melo Baracho <br>
Bacharelado em Ciência da Computação — UFAL

GitHub: https://github.com/julianakcm1 <br>
LinkedIn: https://linkedin.com/in/julianakcmbaracho
