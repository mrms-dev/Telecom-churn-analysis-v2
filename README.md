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

>
## Insights e Análise de Risco
Com base na análise de Feature Importance e nos coeficientes de correlação, os fatores que mais exigem atenção da Telecom X são:

Ciclo de Vida do Cliente (Tenure - 16.4%): Clientes em meses iniciais de contrato apresentam a maior volatilidade. O risco de evasão diminui drasticamente à medida que o tempo de relacionamento aumenta.

Impacto Financeiro (Total & Monthly Charges - 35.6% combinados): O valor da fatura é o principal gatilho de saída. Clientes com faturas acima da média e sem serviços de valor agregado tendem a buscar concorrentes.

Fatores de Retenção Críticos: O suporte técnico (TechSupport) e a segurança online (OnlineSecurity) não são apenas serviços extras, mas sim as principais barreiras que impedem o Churn.

## Conclusão
O desenvolvimento deste projeto permitiu a criação de um modelo preditivo com 90% de Recall, garantindo que a empresa identifique quase a totalidade dos clientes em risco antes que a evasão ocorra.

Diferente de uma abordagem genérica, os dados mostram que a estratégia de retenção deve ser segmentada:

Fidelização Preventiva: Implementar um onboarding assistido para novos clientes nos primeiros 6 meses, focando na percepção de valor e não apenas no custo.

Blindagem de Serviços: Oferecer gratuitamente períodos de teste de TechSupport para clientes com faturas elevadas, criando uma dependência positiva do ecossistema da empresa.

Otimização de Custos: Clientes com alto TotalCharges devem ser migrados para planos de fidelidade de longo prazo (Contract) com descontos progressivos, reduzindo a sensibilidade ao preço mensal.

---
---
<div align="center">
  <img src="https://github.com/mrms-dev.png" width="100px;" alt="Foto de Marcos Rivanio"/><br>
  <sub><b>Desenvolvido por:</b></sub><br>
  <b>Marcos Rivanio Marinho dos Santos,</b>
  <br>

  [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/SEU_PERFIL_AQUI)
  [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/mrms-dev)
  [![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://mrms-dev.github.io)
</div>
