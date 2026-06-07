# Exercício Prático Avaliado: Análise de Dados com PySpark

Este repositório contém a resolução de um exercício prático focado na utilização do framework Apache Spark (via biblioteca PySpark) para realizar a ingestão, o tratamento e a análise exploratória de dados.

## Objetivo

Utilizar o PySpark em um ambiente Google Colab para processar o dataset público **"USA.gov Data from Bitly"**, extraindo métricas e insights sobre o perfil dos acessos registrados.

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Big Data / Processamento Distribuído:** Apache Spark (PySpark)
* **Ambiente de Desenvolvimento:** Google Colab

## Estrutura das Análises

O notebook está estruturado de forma lógica e sequencial, contemplando as seguintes etapas:

1. **Configuração do Ambiente:** Instalação direta do PySpark e download automático do arquivo JSON contendo o dataset.
2. **Inicialização:** Criação e configuração da `SparkSession`.
3. **Carregamento e Schema:** Leitura do arquivo, exibição da estrutura de dados (schema) e contagem do total de registros (3.560 linhas).
4. **Análise de Fuso Horário (Timezone):** Filtragem de valores nulos, contagem de fusos distintos (96) e listagem dos 10 mais frequentes.
5. **Análise de Navegadores (User-Agent):** Criação de uma nova coluna para extrair a família do navegador utilizando a função de particionamento `split`.
6. **Análise de Países:** Identificação do país com maior volume de tráfego e filtragem direcionada para visualizar os primeiros acessos originados no Brasil (BR).
7. **Análise de Sistemas Operacionais:** Uso de expressões regulares (`rlike` case-insensitive) para classificar os acessos nas categorias Windows, Mac, Linux ou Outro.

## Como Executar

1. Importe o arquivo `Análise_de_Dados_com_PySpark.ipynb` para o seu **Google Colab**.
2. Execute a **Célula 1** para preparar o ambiente virtual (instalação da biblioteca e download dos dados).
3. Execute a **Célula 2** para iniciar com sucesso a sessão do Spark.
4. Execute as células subsequentes em ordem para acompanhar as análises, tratamentos de dados e saídas dos DataFrames.

## Desafios e Aprendizados

Durante a resolução do exercício, os principais pontos de aprendizado e adaptação envolveram:
* A compreensão e manipulação de strings dentro da sintaxe específica do PySpark (uso das funções `split` e `rlike`).
* A aplicação de boas práticas para a limpeza prévia de valores nulos antes da execução de operações de agrupamento (`groupBy`) e agregação (`count`).
* O entendimento inicial de como configurar e garantir o funcionamento correto da `SparkSession` no ecossistema de nuvem do Colab.

---

*Nota: Ferramentas de Inteligência Artificial foram utilizadas pontualmente para criação do arquivo README.md e como suporte de aprendizado para a compreensão de sintaxes de regex e estruturação de funções de agrupamento, mantendo o controle lógico e a revisão integral do código.*