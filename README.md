# Modelo HAR ambiente residencial 

## Introdução

O presente modelo pretende reconhecer atividades realizadas por seres humanos em ambiente residencial. A perceção do ambiente é feita por sensores distribuídos pelo ambiente, esta abordagem para além de preservar a privacidade dos residentes tem um consumo computacional menor que a baseada em visão computacional, e não requer dispositivos que necessitam de bateria colado ao corpo. 

As atividades reconhecidas são as seguintes:

- **Meal Preparation (Preparar Refeição)**
- **Relax (Relaxar)**
- **Bed to Toilet (Ir da Cama para Casa de Banho)**
- **Eating (Comer)**
- **Leave Home (Sair de Casa)**
- **Enter Home (Entrar em Casa)**
- **Sleeping (Dormir)**
- **Work (Trabalhar)**


## Conjunto de Dados

O CASAS (Center of Advanced Studies in Adaptive System) Aruba é um projeto coordenado pela Universidade Estatal de Washington (WSU), que incluiu sensores e controladores em diversas residências, com o objetivo de tratar o ambiente de forma inteligente.

O presente dataet apresenta dados coletados ao longo de oito meses em uma residência habitada por uma pessoa. A residencia possuia 40 sensores distribuidos por varios comodos.

link para o dataset: [Dataset](https://casas.wsu.edu/datasets/)

## Metodologia

O desenvolvimento deste projeto seguiu a abordagem CRISP-DM (Cross-Industry Standard Process for Data Mining), uma estrutura amplamente reconhecida e utilizada para orientar o ciclo de vida completo de projetos de mineração de dados e análise preditiva. Através dessa metodologia estruturada, o processo foi dividido em etapas claramente definidas, permitindo uma abordagem sistemática e iterativa para explorar, modelar e prever incidentes rodoviários.

A fim de aplicar esta metodologia baseada em CRISP-DM, foi seguido os
seguintes passos:
* Compreensão do problema proposto e os seus objetivos;
* Obtenção e seleção de dados relevantes para o problema;
* Preparação dos dados: Limpeza, transformação e integração dos dados
para torná-los adequados para analise. Isto incluiu a analise exploratória
dos dados, a limpeza e a transformação dos dados para remover inconsistências e outliers;
* Modelagem: Aplicação de técnicas de aprendizagem automática para construir modelos preditivos. Isto incluiu a seleção de algoritmos, a validação
de modelos e a otimização de parâmetros;
* Avaliação: Avaliar a qualidade dos modelos construídos e escolher o melhor modelo. Isto envolveu a avaliação da precisão e robustez do modelo,
a comparação com modelos alternativos e a seleção do melhor modelo;
* Implantação do modelo escolhido;


## Resultados

Na tabela abaixo, temos a lista de algortimos testados:


| Algoritmo              | Melhores Hiperparâmetros                                     | Acurácia |
|------------------------|-------------------------------------------------------------|----------|
| RandomForestClassifier | max_features = 0.01, min_samples_split = 4, n_estimators = 80,
n_jobs = -1, random_state = 1 | 0.93 |
| SVM      | C = 1000, gamma = 0.001, kernel = ’linear’ | 0.89     |
| LogisticRegression     | fit_intercept = True, max_iter = 100, penalty = ’l2’, tol = 0.0001 | 0.80     |
