---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 144d70318463b7c5ffebfa6b7d942ec2a351fc24
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785470"
---
# Remove-AzureRmExpressRouteCircuitAuthorization

## Sinopse
Remove uma autorização de configuração do ExpressRoute existente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmExpressRouteCircuitAuthorization** remove uma autorização atribuída a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam a sua rede local ao Azure usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito. Só pode haver uma autorização por rede virtual. No entanto, a qualquer momento, o proprietário do circuito pode usar **Remove-AzureRmExpressRouteCircuitAuthorization** para remover a autorização atribuída a uma rede virtual. Quando isso acontece, a rede virtual correspondente não consegue mais usar o circuito do ExpressRoute para se conectar ao Azure.

## EXEMPLOS

### Exemplo 1: remover a autorização de um circuito de um circuito do ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

Este exemplo remove uma autorização de circuito de um circuito do ExpressRoute. O primeiro comando usa o cmdlet **Get-AzureRmExpressRouteCircuit** para criar uma referência de objeto para um circuito do ExpressRoute chamado ContosoCircuit e armazena o resultado na variável chamada $Circuit.

O segundo comando marca a ContosoCircuitAuthorization de autorização de circuito para remoção.

O terceiro comando usa o cmdlet Set-AzureRmExpressRouteCircuit para confirmar a remoção do circuito do ExpressRoute armazenado na variável $Circuit.

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
Especifica o objeto ExpressRouteCircuit que este cmdlet Remove.

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
Especifica o nome da autorização de circuito que este cmdlet Remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSExpressRouteCircuit
Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## EXIBE

### PSExpressRouteCircuit
Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[Get-AzureRmExpressRouteCircuitAuthorization](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Set-AzureRmExpressRouteCircuit](./Set-AzureRmExpressRouteCircuit.md)
