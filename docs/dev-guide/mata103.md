# Pontos de entrada da rotina MATA103

```c
/*/{Protheus.doc} MT100AGR
O PE é chamado após a confirmação da NF, porém fora da transação.

@description Isto foi feito pois clientes que utilizavam TTS e tinham interface
             com o usuário no ponto MATA100 "travavam" os registros utilizados,
             causando parada para outros usuários que estavam acessando a base.

@obs Para verificar em que opção o programa está, deverá ser testado o conteúdo 
	 das variáveis INCLUI e ALTERA.
	 Quando estiver em modo de EXCLUSÃO, ambas as variáveis ficam com 
	 conteúdo = .F.

@author 	AFSouza

@type 		function
/*/
User Function MT100AGR()

Local aArea := GetArea()  

If INCLUI .Or. ALTERA
	
	// Realiza a manifestação
	U_NFAC025(1)         

ElseIf !INCLUI .And. !ALTERA

	// Atualiza o status do xml integrado
	U_NFAC025(2) 	

EndIf

RestArea(aArea)

Return Nil
```

```c
/*/{Protheus.doc} MT103EXC
PE para validação da exclusão do documento de entrada.

@author 	AFSouza

@return 	lRet, logical, .T.
@type 		function
/*/
User Function MT103EXC()

Local aArea := GetArea()
Local lRet  := .T.  

// Atualiza o status do xml integrado
U_NFAC025(2) 	

RestArea(aArea)

Return lRet
```
