# Competição ML @SBS/DAA - 5ª Edição (2022/2023)

## Introdução

O presente modelo tem como objetivo reconhecer atividades realizadas por seres humanos em ambiente residencial. A percepção do ambiente é feita por sensores distribuidos pelo ambiente, esta abordagem para alem de preservar a privacidade dos residentes tem um consumo computacional menor que a baseada em visão computacional, e não requer dispositivos que necessitam de bateria colado ao corpo. 

As atividades reconhecidas são as seguintes:

Meal_Preparation (Preparar refeição)
Relax (relaxar), 
Bed_to_Toilet (ir da cama para
casa de banho), 
Eating (comer),  
Leave_Home (sair de casa), 
Enter_Home (entrar em casa), 
Sleeping (dormir), 
Work (trabalhar).

## Conjunto de Dados

O conjunto de dados utilizado é o CASAS (Center of
Advanced Studies in Adaptive System) Aruba. O CASAS é um projeto encabeçado pela Universidade Estatal de Washington
(WSU), onde em várias residências foram integrados sensores e controladores, que visam tratar o ambiente
como um agente inteligente.

O presente dataset tem dados coletados durante 8 meses em uma residencia habitada por uma pessoa. A residencia possuia 40 sensores distribuidos por varios comodos.

link para competição: [Dataset](https://casas.wsu.edu/datasets/)

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
| RandomForestClassifier | 'criterion': 'entropy', 'max depth': None, 'max features': 1.0, 'n estimators': 100 | 0.94 |
| BaggingClassifier      | 'max features': 1.0, 'max samples': 0.5, 'n estimators': 100, 'random state': None | 0.93     |
| LogisticRegression     | 'fit intercept': True, 'max iter': 10, 'penalty': 'l2', 'tol': 0.0001 | 0.41     |
