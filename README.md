# Telecom-churn-analysis-v2
Fase 2 do Challenge Telecom X: Desenvolvimento de modelos preditivos para identificação de risco de evasão de clientes utilizando Scikit-Learn.
Insights e Conclusão (Telecom X - Parte 2)

1. Performance dos Modelos
Após testar dois algoritmos, a Regressão Logística apresentou o melhor equilíbrio para este problema de negócio:

Acurácia: 81%

Recall (Classe 1): 90% (O modelo identifica 9 de cada 10 clientes que pretendem sair, permitindo uma ação preventiva eficaz).

2. O que mais influencia a saída do cliente? (Feature Importance)
Com base no modelo Random Forest, o ranking de impacto mostrou:

Perfil Financeiro (35,6% de impacto): O valor da fatura mensal e o total gasto acumulado são os maiores gatilhos. Clientes com faturas muito altas têm maior propensão à evasão.

Fidelidade (16,4% de impacto): O tenure (tempo de contrato) mostra que clientes nos primeiros meses de serviço são extremamente voláteis.

Serviços de Retenção: TechSupport e OnlineSecurity apareceram no Top 7, confirmando que a oferta de suporte técnico e segurança digital atua como uma barreira contra o churn.

3. Recomendações Estratégicas
Ação Preventiva: Criar um programa de descontos ou bônus para clientes de "alto valor" (MonthlyCharges alto) que estão no início do contrato (tenure baixo).

Foco em Suporte: Clientes sem TechSupport devem ser o alvo de campanhas de upgrade gratuito desse serviço para aumentar o engajamento.
