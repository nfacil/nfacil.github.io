# Pontos de Entrada NFácil CTe
Aqui você encontrará a documentação para utilização dos Pontos de Entrada disponibilizados para a importação e processamento de arquivos XML de Conhecimento de Frete Fiscal Eletrônico.

-----

## NFA015MN
- Descrição: Ponto de Entrada para incluir rotina no menu principal
                
- Sintaxe:

```NFA015MN([PARAMIXB]) --> aTempRot```

- Parâmetros:

| Nome | Tipo | Descrição | Obrigatório |
|------|------|-----------|-------------|
| PARAMIXB | Vetor | Array aRotina contendo itens do Menu | Sim |

- Retorno:

| Nome | Tipo | Descrição | Obrigatório |
|------|------|-----------|-------------|
| aTempRot | Array | aRotina atualizado, com novos itens | Sim |

- Exemplo:

```c
User Function NFA015MN()

Local aTempRot := PARAMIXB[1]

AAdd( aTempRot, { "Pedido Compra", "MATA121()", 0, 2 })

Return aTempRot
```
