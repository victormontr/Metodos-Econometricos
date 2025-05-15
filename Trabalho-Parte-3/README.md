# 📊 Trabalho Parte 3 — Diagnóstico, Correções e Regressão Quantílica

Este notebook é a terceira parte do projeto de análise econométrica sobre os determinantes do preço do petróleo cru. Após a estimação inicial dos modelos na Parte 2, esta etapa foca em aplicar **testes de diagnóstico**, **ajustes econométricos** e **regressão quantílica**, oferecendo uma análise robusta e mais completa dos resultados.

---

## 🧠 Objetivo

- Avaliar e corrigir falhas nos pressupostos do modelo de regressão linear múltipla.
- Realizar testes de normalidade, heterocedasticidade, autocorrelação, forma funcional e multicolinearidade.
- Aplicar um modelo alternativo com regressão quantílica para investigar a sensibilidade dos coeficientes ao longo da distribuição condicional da variável dependente.

---

## 📑 Dados Utilizados

Foram utilizados os mesmos dados da Parte 2, contendo **retornos logarítmicos diários** de:

- Commodities: ouro, prata, paládio, platina, ródio
- Indicadores de mercado: S&P 500, Dow Jones, DXY, EUR/USD
- ETFs e taxas: GDX, USO, US 10-Year Bond Yield
- Petróleo: Brent, WTI
- Variável dependente: preço do petróleo cru

---

## 🔍 Análises Realizadas

### ✅ ETAPA I — Diagnóstico do Modelo Inicial (MQO)
- **Normalidade dos resíduos:** Jarque-Bera e Shapiro-Wilk
- **Gráficos dos resíduos:** histograma, Q-Q plot, resíduos vs valores ajustados
- **Matriz de correlação**
- **Multicolinearidade:** Fator de Inflação da Variância (VIF) e número condicional
- **Forma funcional:** Teste RESET de Ramsey

---

### 🧪 ETAPA II — Modelo com Correções

- **Seleção Stepwise** para lidar com multicolinearidade
- **MQO com Erros Robustos HC0**
- Novos testes:
  - Breusch-Pagan
  - White
  - Durbin-Watson
  - RESET (forma funcional)
- Novos gráficos: resíduos, VIF, correlação

---

### 📉 ETAPA III — Análise Avançada e Alternativa

- **Testes de normalidade para o modelo corrigido**
- **Outliers e observações influentes:**
  - Distância de Cook
  - DFFITS, DFBETA e resíduos studentizados
- **Regressão Quantílica:**
  - Estimação para múltiplos quantis (0.1 a 0.9)
  - Coeficientes e Pseudo R² ao longo dos quantis
  - Comparação visual entre coeficientes do MQO e da regressão quantílica

---

## 📤 Saídas Geradas

Duas pastas são criadas automaticamente:

### 📁 `Saídas/Modelo sem correcoes/`
- Tabelas e gráficos com testes e diagnósticos do modelo inicial

### 📁 `Saídas/Modelo Corrigido/`
- Resultados do modelo com Stepwise + HC0
- Diagnósticos atualizados
- Gráficos da regressão quantílica
- Comparação com modelo MQO

---

## 🧑‍💻 Como Executar

1. Abra o notebook `A3_Grupo2.ipynb` em um ambiente Jupyter.
2. Execute todas as células sequencialmente.
3. As pastas com os arquivos de saída serão geradas automaticamente.

---

## ✍️ Autoria

Victor Gabriel Monteiro