# Python para Finanças B3

Análise de dividendos e cálculo de preço-teto pelo Método Bazin para ações da B3, usando Python e dados históricos via Yahoo Finance. Projeto desenvolvido para o canal **OpenBI** no YouTube.

## Sobre o projeto

O Método Bazin é uma estratégia de valuation que calcula o preço-teto de uma ação a partir da média de dividendos pagos, dividida pela taxa de retorno mínima desejada. Este projeto automatiza esse cálculo para diferentes ativos da bolsa brasileira, usando 5 anos de histórico de dividendos.

## Ações analisadas

- **BBAS3** - Banco do Brasil
- **BBSE3** - BB Seguridade
- **TAEE11** - Taesa

## Metodologia

1. Busca do histórico de 5 anos via `yfinance`
2. Filtro dos dividendos pagos (valores > 0)
3. Cálculo do pagamento médio anual
4. Cálculo do preço-teto para diferentes taxas de retorno (6%, 8%, 10%)

```python
def preco_teto(pagamento_medio, retorno_esperado):
    return pagamento_medio / retorno_esperado
```

## Tecnologias

![Python](https://img.shields.io/badge/Python-FFD43B?style=flat-square&logo=python&logoColor=blue)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![yfinance](https://img.shields.io/badge/yfinance-7931E3?style=flat-square&logo=yahoo&logoColor=white)

## Técnicas aplicadas

- Extração de dados financeiros históricos (`yfinance`)
- Filtragem e tratamento de séries temporais com pandas
- Cálculo de indicadores financeiros (preço-teto, retorno esperado)

## Como executar

```bash
uv sync
uv run main.py
```

---

📺 Projeto produzido para o canal [OpenBI](https://www.youtube.com/@openbi) no YouTube
📫 [openbiinteligencia.com.br](https://openbiinteligencia.com.br/)

> ⚠️ Conteúdo educacional. Não constitui recomendação de investimento.
