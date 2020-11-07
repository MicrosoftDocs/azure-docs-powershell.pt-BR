---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785734"
---
# Add-AzureRmExpressRouteCircuitAuthorization

## Sinopse
Adiciona uma autorização de circuito do ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** adiciona uma autorização a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual). **Add-AzureRmExpressRouteCircuitAuthorization** adiciona uma nova autorização a um circuito e, ao mesmo tempo, gera a chave de autorização correspondente. Essas chaves podem ser visualizadas a qualquer momento executando o cmdlet Get-AzureRmExpressRouteCircuitAuthorization e, conforme necessário, podem ser copiados e encaminhados para o proprietário da rede apropriado.

Observe que, depois de executar **Add-AzureRmExpressRouteCircuitAuthorization** , você deve chamar o cmdlet Set-AzureRmExpressRouteCircuit para ativar a chave. Se você não chamar **set-AzureRmExpressRouteCircuit** , a autorização será adicionada ao circuito, mas não será habilitada para uso.

## EXEMPLOS

### Exemplo 1: adicionar uma autorização ao circuito do ExpressRoute especificado
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Os comandos neste exemplo adicionam uma nova autorização a um circuito ExpressRoute existente. O primeiro comando usa **Get-AzureRmExpressRouteCircuit** para criar uma referência de objeto para um circuito chamado ContosoCircuit. Essa referência de objeto é armazenada em uma variável chamada $Circuit.

No segundo comando, o cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** é usado para adicionar uma nova autorização (ContosoCircuitAuthorization) ao circuito do ExpressRoute. Esse comando adiciona a autorização, mas não ativa essa autorização. Ativar uma autorização requer o **set-AzureRmExpressRouteCircuit** mostrado no comando final do exemplo.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressRouteCircuit
Especifica o circuito do ExpressRoute ao qual esse cmdlet adiciona a autorização.

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da autorização de circuito a ser adicionada.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSExpressRouteCircuit
**Add-AzureRmExpressRouteCircuitAuthorization** aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## EXIBE

### PSExpressRouteCircuit
**Add-AzureRmExpressRouteCircuitAuthorization** modifica instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
