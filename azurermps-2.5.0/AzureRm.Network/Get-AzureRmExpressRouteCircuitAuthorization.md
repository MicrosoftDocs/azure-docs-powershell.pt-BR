---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: ec11ab37bc3fcb787de2b97f46941f23ede1b45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785509"
---
# Get-AzureRmExpressRouteCircuitAuthorization

## Sinopse
Obtém informações sobre as autorizações de circuito do ExpressRoute.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** Obtém informações sobre as autorizações atribuídas a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar sua rede ao circuito (uma autorização por rede virtual). As chaves de autorização, bem como outras informações sobre a autorização, podem ser visualizadas a qualquer momento ao executar **Get-AzureRmExpressRouteCircuitAuthorization**.

## EXEMPLOS

### Exemplo 1: obter todas as autorizações do ExpressRoute
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit
```

Esses comandos retornam informações sobre todas as autorizações do ExpressRoute associadas a um circuito do ExpressRoute. O primeiro comando usa o cmdlet **Get-AzureRmExpressRouteCircuit** para criar uma referência de objeto um Circuit chamado ContosoCircuit; Essa referência de objeto é armazenada na variável $Circuit. Em seguida, o segundo comando usa essa referência de objeto e o cmdlet **Get-AzureRmExpressRouteCircuitAuthorization** para retornar informações sobre as autorizações associadas ao ContosoCircuit.

### Exemplo 2: obter todas as autorizações do ExpressRoute usando o cmdlet Where-Object
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzureRmExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

Esses comandos representam uma variação nos comandos usados no exemplo 1. Nesse caso, no entanto, as informações são retornadas apenas para as autorizações que estão disponíveis para uso (ou seja, para autorizações que não foram atribuídas a uma rede virtual). Para fazer isso, as informações de autorização de circuito são retornadas no comando 2 e são canalizadas para o cmdlet **Where-Object** .
Em seguida, **Object** , em seguida, escolhe apenas as autorizações em que a propriedade *AuthorizationUseStatus* está definida como available. Para listar apenas as autorizações que não estão disponíveis, use esta sintaxe para a cláusula WHERE:

`{$_.AuthorizationUseStatus -ne "Available"}`

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
Especifica a autorização de circuito do ExpressRoute.

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
Especifica o nome da autorização de circuito do ExpressRoute que esse cmdlet obtém.

-Name "ContosoCircuitAuthorization"

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
**Get-AzureRmExpressRouteCircuitAuthorization** aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** .

## EXIBE

### PSExpressRouteCircuitAuthorization
**Get-AzureRmExpressRouteCircuitAuthorization** retorna instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmExpressRouteCircuitAuthorization](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[Get-AzureRmExpressRouteCircuit](./Get-AzureRmExpressRouteCircuit.md)

[New-AzureRmExpressRouteCircuitAuthorization](./New-AzureRmExpressRouteCircuitAuthorization.md)

[Remove-AzureRmExpressRouteCircuitAuthorization](./Remove-AzureRmExpressRouteCircuitAuthorization.md)
