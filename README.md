# Análise de Churn e Modelagem Preditiva - TelecomX

Este projeto aplica técnicas de Ciência de Dados para entender e prever a evasão de clientes (Churn) em uma operadora de telecomunicações. O objetivo é transformar dados brutos de uma API em insights acionáveis e modelos de Machine Learning.

## 🛠️ Pipeline de Dados

### 1. ETL e Limpeza (Pandas & NumPy)
- **Extração:** Consumo de dados em formato JSON via API.
- **Normalização:** Tratamento de colunas aninhadas (customer, phone, internet, account).
- **Sanitização:** Conversão de tipos de dados (strings para floats) e tratamento de valores vazios.
- **Engenharia de Features:** Criação da métrica `Gastos_Diarios` para análise de custo por cliente.

### 2. Análise Exploratória (EDA)
- **Correlação:** Identificação de variáveis com maior impacto no Churn (Ex: Tenure e MonthlyCharges).
- **Visualização:** Uso de Boxplots e Heatmaps para identificar o perfil do cliente que cancela o serviço.
- **Segmentação:** Cruzamento de variáveis categóricas como Tipo de Contrato e Método de Pagamento.

### 3. Pré-processamento para Machine Learning
- **Encoding:** Transformação de variáveis categóricas via *One-Hot Encoding*.
- **Balanceamento:** Aplicação de **SMOTE** para lidar com o desequilíbrio entre clientes ativos e evadidos.
- **Escalonamento:** Padronização de dados com *StandardScaler* para modelos sensíveis à escala.

## 📈 Insights de Negócio
- **Ponto Crítico:** A evasão é maior nos primeiros 12 meses de contrato.
- **Tipo de Plano:** Contratos mensais (month-to-month) apresentam a maior taxa de Ch
