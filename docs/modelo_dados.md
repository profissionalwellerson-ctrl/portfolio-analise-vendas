# Modelo De Dados

## Grao Das Tabelas

- `fato_vendas`: uma linha por item vendido em um pedido.
- `fato_devolucoes`: uma linha por item devolvido.
- `fato_metas_mensais`: uma linha por mes, loja e categoria.
- `dim_calendario`: uma linha por dia.
- `dim_clientes`: uma linha por cliente.
- `dim_produtos`: uma linha por produto.
- `dim_lojas`: uma linha por loja.
- `dim_vendedores`: uma linha por vendedor.

## Relacionamentos

Crie estes relacionamentos no Power BI:

| Tabela origem | Coluna | Tabela destino | Coluna | Cardinalidade | Direcao |
|---|---:|---|---:|---|---|
| dim_calendario | Data | fato_vendas | Data | 1:* | Unica |
| dim_calendario | Data | fato_devolucoes | DataDevolucao | 1:* | Unica |
| dim_clientes | ClienteID | fato_vendas | ClienteID | 1:* | Unica |
| dim_produtos | ProdutoID | fato_vendas | ProdutoID | 1:* | Unica |
| dim_lojas | LojaID | fato_vendas | LojaID | 1:* | Unica |
| dim_vendedores | VendedorID | fato_vendas | VendedorID | 1:* | Unica |
| fato_vendas | VendaItemID | fato_devolucoes | VendaItemID | 1:* | Unica |
| dim_calendario | Data | fato_metas_mensais | DataMeta | 1:* | Unica |
| dim_lojas | LojaID | fato_metas_mensais | LojaID | 1:* | Unica |

## Observacao Sobre Metas

`fato_metas_mensais` usa `Categoria`, mas `dim_produtos` nao deve se relacionar diretamente por categoria no inicio. Para o nivel intermediario, crie medidas usando `TREATAS` para aplicar a categoria do produto sobre a tabela de metas.

## Boas Praticas

- Use modelo estrela.
- Esconda colunas tecnicas como IDs depois de criar os relacionamentos.
- Marque `dim_calendario` como tabela de datas.
- Configure tipos de dados: datas como Data, valores monetarios como Numero decimal, IDs como Numero inteiro ou Texto.
- Evite relacionamento bidirecional enquanto estiver aprendendo; ele pode mascarar problemas de modelagem.
