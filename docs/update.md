Aqui você encontrará um passo a passo para auxiliar na atualização do NFácil.

O primeiro passo é baixar a versão atualizada do patch do NFácil, correspondente ao Release do Protheus em uso no seu ambiente.

É recomendado que este procedimento seja realizado em ambiente de Homologação e validado antes de ser implementado em ambiente de produção.

Verifique qual a versão correta para seu ambiente e realize o download através  dos links abaixo.

[Patch de atualização NFácil para Protheus 12.1.2210](https://drive.google.com/file/d/1Hxq7cESxuS9p2LNwN2NHhGn0ZFS4iBCH/view?usp=sharing)

[Patch de atualização NFácil para Protheus 12.1.2310](https://drive.google.com/file/d/1r4Qei4Fj8kn8xGbNfBLuuHryCqagvJ9q/view?usp=sharing)

[Patch de atualização NFácil para Protheus 12.1.2410](https://drive.google.com/file/d/12hHvN7SKD1j6TqPedJ8ZtKirJ_3mCTvm/view?usp=sharing)

Com o arquivo em mãos, efetue a aplicação do patch e em seguida execute a rotina **U_NFACUPDN** para compatibilização do ambiente.

![Parâmetros Iniciais](img/parametros-iniciais.png)

Será apresentada a tela de avisos da atualização, com as recomendações, que devem ser observadas para evitar problemas após uma atualização mal sucedida!

![Avisos](img/aviso.png)

Selecionar as empresas que serão atualizadas.

![Selecionar Empresas](img/seleciona-empresa.png)

A rotina irá realizar uma verificação das tabelas em uso pelo NFácil e/ou pelo Sistema.

![Analisar Tabelas](img/analisar-tabelas.png)

Verifique se as tabelas estão em uso pelo NFácil, se houver alguma nova tabela, observe se a mesma está como "Tabela Disponível" ou "Tabela utilizada - SISTEMA", neste último caso informe uma outra tabela, preferencialmente seguindo o padrão do NFácil "Z?Z" e execute a análise novamente.

Se estiver tudo certo vai ser apresentada a tela abaixo.

![Confirmar Tabelas](img/confirmar-tabelas.png)

Aguarde a finalização da atualização.

![Atualizando...](img/atualizando.png)

Com a finalização da atualização será apresentada a tela para consultar e/ou gravar o log do processamento realizado.

![Tela do Log](img/tela-log.png)

Atualização cocluída!

![Atualização Concluída](img/finalizar.png)

## Atualização Serviços Web Sefaz

Depois de realizar a atualização do NFácil, é recomendável realizar a atualização dos serviços web da Sefaz, siga as instruções disponibilizadas [aqui](webservice.md).
