
# Relatório Final – Análise de Evasão de Clientes da Telecom X

## 1. Introdução

Este relatório apresenta o resultado da análise de dados realizada no contexto do projeto **Telecom X**, com o objetivo de entender os fatores que influenciam a evasão de clientes (churn) em uma empresa de telecomunicações. O foco principal foi aplicar o processo de ETL (Extração, Transformação e Carga) e realizar uma análise exploratória de dados (EDA), a fim de gerar insights que ajudem na construção de modelos preditivos por parte da equipe de ciência de dados.

---

## 2. Problema

A **Telecom X** vem enfrentando uma taxa elevada de evasão de clientes, o que impacta diretamente sua receita e estabilidade no mercado. No entanto, os motivos exatos para essa evasão ainda são incertos. A proposta deste trabalho é preparar os dados de forma adequada e explorar possíveis padrões que possam justificar esse comportamento.

---

## 3. Processo de ETL

### 📌 Extração
Os dados foram extraídos via API diretamente do repositório público no GitHub:
```
https://raw.githubusercontent.com/alura-cursos/challenge2-data-science/main/TelecomX_Data.json
```

### 🔧 Transformação
As etapas de transformação envolveram:

- Conversão de colunas numéricas com erros de formatação.
- Padronização de campos textuais (ex.: gênero, forma de pagamento).
- Tratamento de valores nulos e vazios.
- Criação de novas variáveis, como **Valor Diário da Fatura**.
- Conversão de colunas binárias ('Yes'/'No') em valores 1 e 0.
- Tradução e renomeação das colunas para facilitar a leitura.

### 📊 Carga e Análise
Com os dados tratados, foi realizada a análise exploratória com foco em:

#### Distribuição de Churn
- **27%** dos clientes deixaram a empresa.
- Gráficos de barra e pizza representaram essa distribuição.

#### Análise por Categoria
Foram analisados os impactos do churn em variáveis como:

- **Gênero** (sem grandes diferenças)
- **Tipo de Contrato**: contratos mensais estão mais associados ao churn.
- **Forma de Pagamento**: pagamentos eletrônicos e automáticos têm maior evasão.
- **Internet e Streaming**: clientes com serviços extras têm mais churn.

#### Análise Numérica (Boxplots)
- **Clientes com menos meses de contrato** tendem a sair mais.
- Faturas mensais e totais mais altas estão relacionadas com evasão.

#### Matriz de Correlação
- As variáveis mais correlacionadas com churn foram:
  - `Tipo de Contrato`
  - `Fatura Digital`
  - `Valor Mensal`
  - `Meses de Contrato` (inversamente)

---

## 4. Conclusão

A análise demonstrou que os principais fatores associados ao churn são:

- Baixo tempo de contrato
- Alta fatura mensal
- Pagamentos eletrônicos ou automatizados
- Contratos mensais e sem fidelização

Esses padrões podem ser explorados em futuros modelos preditivos para identificar clientes com maior risco de evasão.

---

📌 *Este relatório resume a primeira fase do projeto Telecom X, focando na estruturação e análise inicial dos dados. As próximas etapas poderão se beneficiar deste trabalho para tomada de decisão e desenvolvimento de soluções baseadas em dados.*
