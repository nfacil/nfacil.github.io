# Pontos de entrada da rotina MATA140

```c
/*/{Protheus.doc} MT140SAI
PE responsável por controlar a interface de um pré-documento de entrada.
Ponto de entrada disparado antes do retorno da rotina ao browse.
Dessa forma, a tabela SF1 pode ser reposicionada antes do retorno 
ao browse.

@author 	AFSouza

@param		PARAMIXB[1], numeric, Numero da operacao
			PARAMIXB[2], character, Numero Doc
			PARAMIXB[3], character, Serie Doc
			PARAMIXB[4], character, Fornecedor
			PARAMIXB[5], character, Loja
			PARAMIXB[6], character, Tipo
			PARAMIXB[7], numeric, Opcao Confirmacao
			
@type 		function
/*/
User Function MT140SAI()
     
// Verifica se é exclusão
If PARAMIXB[1] == 5  

	// Verifica se foi confirmado (Ok)
	If PARAMIXB[7] == 1
				
		// Atualiza o status do xml integrado
		U_NFAC025(2)    
		
	EndIf
	
EndIf

Return
```

```c
/*/{Protheus.doc} MT140PC
PE para o tratamento do parâmetro MV_PCNFE 
(Nota Fiscal tem que ser amarrada a um Pedido de Compra ?)

@author 	AFSouza

@return 	lRetOk, logical, .T.
@type 		function
/*/
User Function MT140PC()

Local lRetOk := .T.

// Valida a obrigatoriedade da amarração do pedido de venda
lRetOk := U_NFAC025(3) 

Return lRetOk
```