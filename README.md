# Projeto Power BI - Varejo Intermediário

Este projeto foi criado para estudar Power BI do zero ao nível intermediário usando uma base fictícia de varejo omnichannel.

## Objetivo

Construir um dashboard executivo e analítico para acompanhar vendas, margem, metas, devoluções, canais, produtos, lojas e clientes.

## Estrutura

- `dados/`: arquivos CSV para importar no Power BI.
- `scripts/`: script para recriar a base de dados.
- `docs/`: roteiro de estudo, modelo de dados e orientações de dashboard.
- `dax/`: medidas DAX organizadas por nível.

## Como usar

1. Execute `scripts/gerar_dados_varejo.py` se quiser recriar os CSVs.
2. Abra o Power BI Desktop.
3. Importe todos os arquivos da pasta `dados/`.
4. Configure os relacionamentos seguindo `docs/modelo_dados.md`.
5. Crie as medidas de `dax/medidas_dax.md`.
6. Monte as paginas seguindo `docs/roteiro_dashboard.md`.

## Nível esperado ao final

Ao concluir o projeto, você terá praticado importação de dados, Power Query, modelo estrela, relacionamentos, tabela calendário, medidas DAX, inteligência temporal, KPIs, segmentadores, drill-through e storytelling com dashboards.

