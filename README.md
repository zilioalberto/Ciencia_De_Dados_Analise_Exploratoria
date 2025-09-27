## Ciencia_De_Dados_Analise_Exploratoria
## Análise Exploratória para Modelagem – Projeto de Classificação (Churn)

Alunos: 
Alberto Zilio
Roni Pereira

# Aula 07 – Parte 1  


### Objetivo
Explorar o dataset **Telco Customer Churn** para entender o perfil dos clientes que cancelam o serviço (Churn = Yes) em comparação com os que não cancelam (Churn = No).  
Responder à pergunta: **“Quais variáveis parecem ser as mais promissoras para incluir em nosso futuro modelo?”**


## 2️⃣ Análise da Variável-Alvo (Churn)

**Reflexão (Passo 02):**  
– Classes desbalanceadas (No ~73–76% e Yes ~24–27%).  
– Necessário métricas adequadas (ROC-AUC, F1) e balanceamento para o modelo.

## 3️⃣ Relação entre Variáveis **Categóricas** e o Churn

**Reflexão (Passo 03):**  
– **Month-to-month** tem maior churn que contratos de 1 ou 2 anos.  
– **Fiber optic** tem churn maior que DSL.  
– Ausência de parceiro/dependentes eleva churn.  
– **Electronic check** concentra churn maior.  

## 4️⃣ Relação entre Variáveis **Numéricas** e o Churn

**Reflexão (Passo 04):**  
– Clientes que cancelam têm **tenure** menor.  
– **MonthlyCharges** mais altas em clientes que cancelam.  
– **TotalCharges** acompanha tenure (redundância).  

## 5️⃣ Visão Geral – **Correlação/Associação**


**Reflexão (Passo 05):**  
– **tenure** correlaciona negativamente com churn.  
– **MonthlyCharges** correlaciona positivamente.  
– **TotalCharges** correlaciona fortemente com tenure (multicolinearidade).


## 6️⃣ Conclusão da EDA (Parte 1)

### Conclusão – Variáveis mais promissoras para classificação (Churn)

**Principais achados:**
- Dataset desbalanceado (Yes minoria) → métricas como ROC-AUC/F1 e técnicas de balanceamento.
- **Contract** e **InternetService** associam-se a churn alto.
- **tenure** baixo e **MonthlyCharges** altos estão ligados a churn elevado.
- **Partner/Dependents**: ausência tende a aumentar churn.
- **TotalCharges** é altamente correlacionada com tenure (cuidado com redundância).

**Variáveis candidatas:**
1. **Contract**  
2. **tenure**  
3. **MonthlyCharges**  
4. **InternetService**  
5. **PaymentMethod**  
6. **Partner/Dependents**  


