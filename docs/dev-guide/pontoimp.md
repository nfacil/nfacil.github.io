# Pontos de Entrada NFácil - Importador XML
Aqui você encontrará a documentação para utilização dos Pontos de Entrada disponibilizados para o processamento da importação de arquivos XML.

-----

## NFA012SM
- Descrição: Ponto de Entrada para verificar o CNPJ de outras empresas na tabela SM0, antigo _sigamat.emp_, atual _SYS_COMPANY_.

- Sintaxe:

```NFA012SM([PARAMIXB]) --> nPosEmp```

- Parâmetros:

| Nome | Tipo | Descrição | Obrigatório |
|------|------|-----------|-------------|
| PARAMIXB | Vetor | Array contendo dados da empresa | Sim |

- Retorno:

| Nome | Tipo | Descrição | Obrigatório |
|------|------|-----------|-------------|
| nPosEmp | Número | Índice do registro localizado | Sim |

- Exemplo:

```c
User Function NFA012SM()

Local nPosLoc  := PARAMIXB[1]
Local cCGC := Alltrim(PARAMIXB[2]) 
Local cMemoXml := PARAMIXB[3]

/* Processamento Customizado */

Return nPosLoc
```