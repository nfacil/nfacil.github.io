# Pontos de Entrada NFácil NFse
Aqui você encontrará a documentação para utilização dos Pontos de Entrada disponibilizados para a importação e processamento de arquivos XML de Nota Fiscal de Serviços Eletrônica.

-----

## NFA039MN
- Descrição: Ponto de Entrada para incluir rotina no menu principal
                
- Sintaxe:

```NFA039MN([PARAMIXB]) --> aTempRot```

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
User Function NFA039MN()

Local aTempRot := PARAMIXB[1]

AAdd( aTempRot, { "Pedido Compra", "MATA121()", 0, 2 })

Return aTempRot
```