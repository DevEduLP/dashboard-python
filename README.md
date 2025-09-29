# Dashboard de Vendas de Supermercado (Streamlit + Plotly + Pandas)

Um dashboard direto para analisar faturamento por dia, filial, linha de produto e forma de pagamento. Feito para ir do CSV ao insight rapidamente.

## 🚀 Stack
- **Python**
- **Streamlit** (UI web)
- **Pandas** (ETL leve)
- **Plotly Express** (gráficos interativos)

## 📁 Estrutura
```
.
├─ dashboards.py
├─ supermarket_sales.csv
├─ requirements.txt
└─ README.md
```

## 🗃️ Dataset
- Arquivo: `supermarket_sales.csv`
- Separador: `;`
- Decimal: `,`
- Colunas mínimas: `Date`, `City`, `Total`, `Product line`, `Payment`, `Rating`
- `Date` será convertido via `pd.to_datetime` e ordenado.

## 🔧 Setup
```bash
python -m venv .venv
# Windows (PowerShell)
.venv\Scripts\Activate
# macOS/Linux
# source .venv/bin/activate

pip install -r requirements.txt
```

## ▶️ Execução
```bash
streamlit run dashboards.py
# ou
python -m streamlit run dashboards.py
```
Acesse a URL exibida (ex.: `http://localhost:8501`).

## 📊 O que o app entrega
- **Filtro de mês** (sidebar).
- **Faturamento por dia** (barras, por cidade).
- **Faturamento por tipo de produto** (barras horizontais agregadas).
- **Faturamento por filial** (agregado por cidade).
- **Faturamento por tipo de pagamento** (pizza).
- **Avaliação média por filial** (barras).

## ✅ Boas práticas já contempladas
- `st.set_page_config(layout="wide")` para aproveitar a largura.
- Conversão de datas e ordenação.
- Colunas para layout responsivo.


## 🐞 Troubleshooting
- **“missing ScriptRunContext / Session state…”** → use `streamlit run`.
- **Porta ocupada** → `--server.port 8502`.
- **CSV ausente** → confirme caminho relativo e diretório de execução.
- **Gráfico vazio** → não há dados para o mês filtrado.

