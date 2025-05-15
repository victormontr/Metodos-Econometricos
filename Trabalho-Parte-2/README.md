# 📊 Trabalho Parte 2 — Análise de Determinantes do Preço do Petróleo Cru

Este projeto tem como objetivo aplicar técnicas econométricas para analisar os principais fatores que influenciam o preço do petróleo cru ao longo do tempo.

---

## 🧠 Objetivo

Avaliar a relação entre o preço do petróleo cru e diversas variáveis macroeconômicas e de mercado, utilizando:

- Regressão OLS (Mínimos Quadrados Ordinários)
- Erros robustos de White (HC0)
- Estimadores de Newey-West (HAC)
- Testes estatísticos: Breusch-Pagan, Breusch-Godfrey, Durbin-Watson

---

## 📑 Dados Utilizados

As variáveis explicativas incluem:

- Commodities: ouro, prata, paládio, platina, ródio
- Indicadores de mercado: S&P 500, Dow Jones, US Dollar Index, EUR/USD
- ETFs e taxas: GDX, USO, US 10-Year Bond Yield
- Derivativos de petróleo: Brent, WTI

As séries foram obtidas em nível e posteriormente transformadas em **retornos logarítmicos diários**.

---

## 📈 Modelos Estimados

Três especificações foram testadas:

- **Modelo 1:** Regressão básica com todas as variáveis
- **Modelo 2:** Inclusão de termo quadrático para 'price_us dollar_index'
- **Modelo 3:** Inclusão de uma variável dummy (`price_shock`) para capturar efeitos de choques no petróleo (2014–2016)

---

## 🧪 Testes Estatísticos

Para cada modelo, são executados:

- ✅ **White (HC0)**: robustez à heterocedasticidade
- ✅ **Newey-West (HAC)**: robustez à autocorrelação
- ✅ **Breusch-Pagan**: teste formal de heterocedasticidade
- ✅ **Breusch-Godfrey (nlags=2)**: teste de autocorrelação serial
- ✅ **Durbin-Watson**: diagnóstico adicional de autocorrelação

---

## 📤 Saídas Geradas

Para cada modelo, a pasta `Saídas/Modelo_X/` contém:

- `resumo_white.txt`: Resumo da regressão com erros robustos HC0
- `resumo_neweywest.txt`: Resumo com estimador de Newey-West
- `residuos.png`: Gráfico dos resíduos da regressão
- `tabela_testes.png`: Resultados dos testes estatísticos em imagem

---

## 📚 Referência

- **Zilin Xu et al. (2023)** — [PDF incluído em `Documentos/`]

---

## 🧑‍💻 Execução

Para rodar este projeto:

1. Abra o arquivo `A2_Grupo2.ipynb` em um ambiente Jupyter.
2. Execute as células sequencialmente (dados → modelos → testes → saídas).
3. As pastas e arquivos em `Saídas/` serão gerados automaticamente.

---

## ✍️ Autoria

Victor Gabriel Monteiro

