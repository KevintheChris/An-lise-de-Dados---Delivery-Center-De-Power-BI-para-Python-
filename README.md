# 🛵 Análise de Dados - Delivery Center (De BI para Python)

## 📌 Contexto do Projeto
Este projeto tem como objetivo analisar os dados de uma operação de delivery (Delivery Center), respondendo a demandas reais de diferentes áreas de negócio (Marketing, Pricing e Diretoria Executiva). 

Originalmente desenvolvido utilizando ferramentas tradicionais de Business Intelligence (criação de dashboards), este repositório representa a **migração e evolução da análise para Python**. O foco principal é demonstrar a manipulação programática de um banco de dados modelado em **Esquema Snowflake**, realizando múltiplos cruzamentos (joins) e agregações para extrair inteligência de negócio.

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python
* **Bibliotecas:** Pandas (Manipulação de dados)
* **Ambiente:** Google Colab / Jupyter Notebook
* **Conceitos Aplicados:** Manipulação de Esquema Snowflake, Análise Exploratória (EDA), Lógica de Negócios (DRE), Limpeza e Formatação de Dados.

## 📊 Demandas de Negócio Resolvidas

O script responde às seguintes perguntas estratégicas:

1. **Ação de Marketing (Aquisição de Entregadores):** * Identificação dos Top 20 entregadores com maior distância percorrida, segmentados por modalidade (Bikers e Motoboys), para distribuição de bonificação.
2. **Estratégia de Pricing:** * Mapeamento da distância média percorrida pelos motoboys, agrupada por Estado, para ajuste regionalizado de repasses.
3. **Indicadores para a Diretoria Executiva (CFO):** * Cálculo da Receita Total e Receita Média, segmentadas tanto por Categoria de Produto (Food x Good) quanto por Estado.
4. **Demonstração de Resultado e Bônus (DRE):** * Estruturação de um DRE simplificado calculando o Custo Total (R$ 5 fixo por entrega), Receita da Empresa (15% sobre os pedidos), Lucro Total do período e a distribuição de 20% do lucro como bônus para o quadro de funcionários.

## 🧠 Principais Desafios Técnicos
* **Navegação no Esquema Snowflake:** Utilização intensiva de `pd.merge()` para conectar a tabela fato (`deliveries` e `orders`) com múltiplas tabelas dimensão (`drivers`, `stores`, `hubs`), garantindo a integridade dos dados.
* **Otimização de Memória:** Seleção estrita de colunas durante os *joins* para simular boas práticas em ambientes de Big Data.
* **Tratamento de Regras de Negócio:** Filtros rigorosos de status de pedido (`DELIVERED` / `FINISHED`) antes da aplicação de cálculos financeiros, evitando distorções nas métricas de receita.

## 🚀 Como Executar
1. Clone este repositório.
2. Certifique-se de ter o Python e o Pandas instalados, ou abra o arquivo `.ipynb` diretamente no Google Colab.
3. Insira os arquivos `.csv` do dataset na mesma pasta do script (ou ajuste os caminhos de leitura no início do código).(link para o dataset: https://www.kaggle.com/datasets/nosbielcs/brazilian-delivery-center/data)
4. Execute as células sequencialmente.

---
*Desenvolvido para consolidar habilidades em Data Analysis e Business Intelligence usando Python.*
