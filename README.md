**# VALIDAÇÃO DE MODELOS DE CLUSTERIZAÇÃO**

Projeto final da disciplina Validação de Modelos de Clusterização – Instituto Infnet.
Este repositório contém toda a implementação prática, documentação e artefatos solicitados no enunciado oficial do projeto.

***Objetivo do Projeto***

O objetivo é demonstrar a aplicação completa de técnicas de clusterização e validação de modelos, incluindo:

* Preparação do ambiente e uso de ambiente virtual.
* Análise exploratória de dados.
* Pré-processamento.
* Clusterização utilizando K-Means e DBScan.
* Validação por índices como Silhouette, Davies-Bouldin, Calinski-Harabasz.
* Análise comparativa entre técnicas.
* Construção de medidas de similaridade para séries temporais.

***1. Infraestrutura Utilizada***

Conforme solicitado no projeto:

* Python 3.12+

* Ambiente virtual configurado (Anaconda)

* Todas as dependências registradas em requirements.txt

* Notebook Jupyter rodando em ambiente local/Colab

* Registro do ambiente e versão dos pacotes

***2. Escolha da Base de Dados***

A base utilizada foi:

- Diabetes Dataset (2019)

Justificativa da escolha:

* A base foi selecionada pois contém variáveis:
  
* Numéricas (BMI, horas de sono etc.)
  
* Categóricas (gênero, hábitos, alimentação)
  
* Risco e estilo de vida (tabagismo, sedentarismo, pressão arterial)
  
* Ela permite um estudo robusto de clusterização, exige pré-processamento realista e apresenta padrões relevantes para saúde pública.

***3. Análise Exploratória de Dados (EDA)***

Foram avaliadas:

* Distribuições (histogramas)
  
* Presença de outliers (boxplots)
  
* Dados ausentes
  
* Codificação de variáveis categóricas com one-hot encoding

As variáveis numéricas foram padronizadas com StandardScaler, como é recomendado antes da clusterização.

***4. Pré-processamento Realizado***

* Tratamento de valores nulos
  
* Correção de inconsistências textuais
  
* Transformação de variáveis categóricas (One-Hot Encoding)
  
* Padronização das variáveis numéricas
  
* Seleção das colunas relevantes para clusterização

***5. Clusterização – K-Means***

Após testar valores de K de 2 a 10 usando o índice de Silhouette:

* Número ótimo de clusters: 2
  
* Silhouette médio: 0.399
  
* Clusters visualizados via PCA

O K-Means apresentou separações claras baseadas principalmente em BMI e Qualidade do Sono.

***6. Clusterização – DBScan***
O método DBScan foi aplicado com diferentes valores de:

* eps
  
* min_samples

Principais observações:

* Identificou grupos menores e pontos classificados como outliers.
  
* Produziu clusters diferentes do K-Means, por ser um algoritmo baseado em densidade.

***7. Medidas de Validação Utilizadas***
Além do Silhouette, foram aplicadas:

* Davies-Bouldin Score

Avalia compacidade e separação.

* Calinski-Harabasz Index

Avalia dispersão intra e intercluster.

Conclusão da Validação

* O K-Means obteve melhor estabilidade nas 3 métricas.
  
* O DBScan depende fortemente da escolha de eps e não é adequado para usar Silhouette como critério de escolha do número de clusters — conforme pedido no projeto.

***8. Medidas de Similaridade – Séries Temporais***

Foi desenvolvida uma abordagem baseada em:

* Correlação cruzada (cross-correlation) → para medir similaridade temporal.
  
* Passo a passo incluído no relatório.
  
* Algoritmo recomendado: Agglomerative Clustering, por lidar bem com matrizes de distância.

Também foi sugerida:

* Similaridade por DTW (Dynamic Time Warping)

***9. Resultados Obtidos***

* Clusters bem formados com K-Means.
  
* DBScan capturou padrões locais e outliers.
  
* Silhouette foi eficiente para K-Means, mas não adequado para DBScan.
  
* Medidas adicionais reforçaram a escolha do modelo.
  
* Toda a infraestrutura solicitada foi entregue conforme a rubrica.

**AUTOR**

Luiz Felipe Souza Ivo

Projeto acadêmico (Validação de Modelos de Clusterização) – Instituto Infnet
