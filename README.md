# Telecom X - Previsão de Churn (Parte 2)

Este repositório contém a segunda etapa do desafio **Telecom X**, focada no desenvolvimento de modelos de Machine Learning para prever a evasão de clientes (Churn). O objetivo principal é identificar padrões de comportamento e variáveis críticas que influenciam a saída dos usuários.

## Estrutura do Projeto
- `telecomx_churn_limpo_atualizado.csv`: Base de dados tratada na Fase 1.
- `Telecom_Churn_Predictive_Modeling.ipynb`: Notebook principal com a análise e modelagem.
- `LICENSE`: Licença MIT para uso do código.
- `.gitignore`: Arquivos ignorados pelo controle de versão.

## Tecnologias Utilizadas
- **Python 3.12**
- **Pandas & Numpy:** Manipulação e análise de dados.
- **Scikit-Learn:** Pré-processamento, criação e avaliação de modelos.
- **Matplotlib & Seaborn:** Visualização de dados e gráficos de importância.

## Preparação dos Dados
Conforme exigido pelo desafio, os dados passaram pelas seguintes etapas:
1. **Classificação:** Separação entre variáveis categóricas e numéricas.
2. **Encoding:** Transformação de variáveis de texto em numéricas via `LabelEncoder`.
3. **Normalização:** Aplicação de `StandardScaler` para garantir a convergência da Regressão Logística.
4. **Divisão de Dados:** Separação em 70% para treino e 30% para teste (Random State: 42).

## Modelagem e Resultados
Foram testados dois algoritmos principais para comparação:

| Modelo | Acurácia | Recall (Classe 1) | F1-Score |
| :--- | :---: | :---: | :---: |
| **Regressão Logística** | **81%** | **90%** | **0.87** |
| Random Forest | 79% | 90% | 0.86 |

**Justificativa:** A Regressão Logística foi selecionada como o modelo final devido ao seu melhor equilíbrio entre acurácia e a capacidade de classificar corretamente clientes que permanecem na empresa, mantendo um alto índice de detecção de evasão.

## Insights e Conclusão
Com base na análise de **Feature Importance**, identificamos os 3 maiores fatores de risco:
1. **TotalCharges (18.4%):** Clientes com gastos acumulados altos são mais sensíveis a mudanças.
2. **MonthlyCharges (17.2%):** O valor da fatura mensal é um gatilho direto para o churn.
3. **Tenure (16.4%):** Clientes no início do contrato têm maior probabilidade de sair.

> **Estratégia sugerida:** Implementar programas de retenção focados em suporte técnico (`TechSupport`) e segurança digital, que se mostraram variáveis de peso para a permanência do cliente.

---
Desenvolvido por **Marcos Rivanio Marinho dos Santos, PhD**.
