# Telecom X - Previsão de Churn (Parte 2)

Este repositório contém a segunda etapa do desafio **Telecom X**, focada no desenvolvimento de modelos de Machine Learning para prever a evasão de clientes (Churn). O objetivo principal é identificar padrões de comportamento e variáveis críticas que influenciam a saída dos usuários.

## Estrutura do Projeto
Conforme a hierarquia do repositório:
- `.gitignore`: Arquivos e diretórios ignorados pelo Git.
- `LICENSE`: Licença MIT de uso do projeto.
- `Mapa de Influencia.png`: Gráfico estatístico de correlação (fatores de risco vs. retenção).
- `README.md`: Documentação completa do projeto.
- `Ranking de Impacto- Variaveis Decisivas.png`: Gráfico de importância de variáveis do modelo.
- `Telecom_Churn_Predictive_Modeling.ipynb`: Notebook com todo o código de Machine Learning.
- `telecomx_churn_limpo_atualizado.csv`: Base de dados tratada utilizada no projeto.

## Tecnologias Utilizadas
- **Python 3.12**
- **Pandas & Numpy:** Manipulação e análise de dados.
- **Scikit-Learn:** Pré-processamento, criação e avaliação de modelos.
- **Matplotlib & Seaborn:** Visualização de dados e gráficos de alta performance.

## Preparação dos Dados
Conforme as diretrizes do desafio, os dados passaram por:
1. **Classificação:** Identificação de variáveis categóricas e numéricas.
2. **Encoding:** Conversão de textos em valores numéricos (LabelEncoder).
3. **Normalização:** Aplicação de `StandardScaler` para otimizar modelos lineares.
4. **Divisão de Dados:** Separação em 70% para treino e 30% para teste.

## Modelagem e Resultados
Foram testados dois algoritmos principais para comparação:

| Modelo | Acurácia | Recall (Classe 1) | F1-Score |
| :--- | :---: | :---: | :---: |
| **Regressão Logística** | **81%** | **90%** | **0.87** |
| Random Forest | 79% | 90% | 0.86 |

**Justificativa:** A Regressão Logística apresentou o melhor equilíbrio técnico, sendo selecionada para a identificação preventiva de clientes em risco.

### Visualizações de Análise

#### 1. Mapa de Influência (Estatística)
![Mapa de Influência](Mapa%20de%20Influencia.png)
*As barras vermelhas indicam variáveis que aumentam o risco de Churn, enquanto as verdes indicam fatores de retenção.*

#### 2. Ranking de Impacto (Machine Learning)
![Ranking de Impacto](Ranking%20de%20Impacto-%20Variaveis%20Decisivas.png)
*Importância relativa de cada atributo para a tomada de decisão do modelo Random Forest.*

## Insights e Conclusão
Com base na análise de **Feature Importance**, os 3 maiores fatores de risco identificados foram:
1. **TotalCharges (18.4%):** Gastos acumulados indicam sensibilidade ao valor do serviço.
2. **MonthlyCharges (17.2%):** O valor da fatura mensal é um gatilho direto para evasão.
3. **Tenure (16.4%):** Clientes em meses iniciais de contrato são os mais voláteis.

> **Estratégia sugerida:** Implementar programas de fidelização para novos clientes e reforçar o suporte técnico (`TechSupport`), que atua como um forte pilar de retenção.

---
Desenvolvido por **Marcos Rivanio Marinho dos Santos**.
