# 📊 Trabalho Parte 1 — Estudo de Eventos no Mercado de Ações

Este projeto aplica metodologia de estudo de eventos para avaliar os impactos de eventos informacionais sobre os retornos de ações de empresas listadas na B3.

---

## 🧠 Objetivo

Investigar como os **retornos das ações** reagem a eventos específicos (ex: divulgação de resultados) utilizando janelas temporais em torno da data do evento.

---

## ⚙️ Metodologia

1. **Importação e filtragem** dos preços de ativos e do índice de mercado (IBOV).
2. **Cálculo de retornos logarítmicos diários**.
3. **Alinhamento das janelas de eventos** (ex: 90 dias antes e depois).
4. **Regressão OLS** entre os retornos da ação e do IBOV para estimar o beta.
5. **Cálculo dos retornos anormais** e sua significância.

---

## 📈 Resultados Gerados

Para cada evento por empresa:
- Gráfico de dispersão dos retornos vs. IBOV.
- Linha temporal dos retornos.
- Histograma dos retornos anormais.
- Estatísticas de regressão e significância.
- Tabela `.csv` com resultados descritivos.

Além disso, o gráfico `R-sqr.png` compara os coeficientes de determinação dos modelos por empresa.

---

## 📑 Dados Utilizados

- Ações: BRKM5, LIGT3, ITUB4, USIM5, CMIG4
- Índice de mercado: ^BVSP (Ibovespa)
- Período: personalizado por evento (ver `Lista_Empresas.csv`)

---

## 📚 Referência

- **Takamatsu et al. (2008)** — Abordagem metodológica sobre eventos e reações de preços de ações.

---

## ▶️ Execução

Para reproduzir a análise:

1. Abrir `A1_Grupo2.ipynb` em Jupyter Notebook.
2. Executar sequencialmente as células (já configuradas para importar os dados locais).
3. As figuras e estatísticas serão salvas automaticamente em `Plot/`.

---

## ✍️ Autoria

Victor Gabriel Monteiro
