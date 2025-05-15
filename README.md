
# 📊 Trabalho de Econometria — Grupo 2

Este repositório contém três notebooks que compõem um projeto aplicado de análise econométrica sobre os determinantes do preço do petróleo bruto, com base em variáveis macroeconômicas e de mercado.

---

## 🧠 Objetivo

Investigar os principais fatores que influenciam o retorno do preço do petróleo utilizando:

- Regressão linear múltipla (OLS)
- Testes econométricos: heterocedasticidade, autocorrelação, normalidade
- Diagnóstico de multicolinearidade, forma funcional e outliers
- Aplicações práticas com variáveis dummy e termos quadráticos

---

## 🧪 Metodologia por Etapas

### 🔹 **A1 - Análise Exploratória (Descritiva)**

- Importação e visualização de séries temporais macroeconômicas
- Cálculo de estatísticas descritivas
- Correlações e inspeções visuais por meio de `matplotlib` e `seaborn`
- Transformações logarítmicas e diferenciais

### 🔹 **A2 - Modelagem de Regressão Múltipla**

1. **Regressão Linear Base:** retorno do petróleo versus variáveis macro
2. **Termo Quadrático:** inclusão de efeito não linear do dólar
3. **Dummy:** identificação do impacto de choques no período 2014–2016
4. **Testes de Diagnóstico:** 
   - Breusch-Pagan e White (heterocedasticidade)
   - Durbin-Watson e Breusch-Godfrey (autocorrelação)

As saídas são salvas automaticamente na pasta `Saídas/`.

### 🔹 **A3 - Diagnósticos Avançados e Refinamento do Modelo**

- Testes de normalidade: Jarque-Bera, Shapiro-Wilk
- Cálculo do VIF para verificar multicolinearidade
- Teste RESET de Ramsey para avaliar especificação funcional
- Análise de outliers e observações influentes: DFFITS, alavancagem
- Geração de gráficos e tabelas para documentação dos resultados

---

## 🧰 Requisitos

O ambiente pode ser recriado utilizando phyton 3.12.10 e rodando o seguinte comando:

```bash
pip install -r requirements.txt
