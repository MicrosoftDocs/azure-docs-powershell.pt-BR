---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 0f17d30b6f47effab5b0039bd56172cbe580392c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775405"
---
# New-AzExpressRouteCircuitAuthorization

## Sinopse
Cria uma autorização de circuito do ExpressRoute.

## SYNTAX

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzExpressRouteCircuitAuthorization** cria uma autorização de circuito que pode ser adicionada a um circuito do ExpressRoute. Os circuitos do ExpressRoute conectam a sua rede local à nuvem da Microsoft usando um provedor de conectividade em vez da Internet pública. O proprietário de um circuito do ExpressRoute pode criar cerca de 10 autorizações para cada circuito; essas autorizações geram uma chave de autorização que pode ser usada por um proprietário de rede virtual para conectar uma rede ao circuito. Só pode haver uma autorização por rede virtual.

Depois de criar um circuito do ExpressRoute, você pode usar **Add-AzExpressRouteCircuitAuthorization** para adicionar uma autorização para esse circuito.
Você também pode usar **New-AzExpressRouteCircuitAuthorization** para criar uma autorização que pode ser adicionada a um novo circuito ao mesmo tempo em que o circuito é criado.

## EXEMPLOS

### Exemplo 1: criar uma nova autorização de circuito
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

Esse comando cria uma nova autorização de circuito chamada ContosoCircuitAuthorization e, em seguida, armazena esse objeto em uma variável chamada $Authorization. Salvar o objeto em uma variável é importante: embora **New-AzExpressRouteCircuitAuthorization** possa criar uma autorização de circuito, ele não pode adicionar essa autorização a uma rota de circuito. Em vez disso, o $Authorization variável é usado New-AzExpressRouteCircuit durante a criação de um circuito do ExpressRoute com nova marca.

Para obter mais informações, consulte a documentação do cmdlet New-AzExpressRouteCircuit.

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

### -Nome
Especifica um nome exclusivo para a nova autorização de circuito do ExpressRoute.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita entrada em pipeline.

## EXIBE

### PSExpressRouteCircuitAuthorization
Esse cmdlet cria instâncias do objeto **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzExpressRouteCircuitAuthorization](./Add-AzExpressRouteCircuitAuthorization.md)

[Get-AzExpressRouteCircuitAuthorization](./Get-AzExpressRouteCircuitAuthorization.md)

[Remove-AzExpressRouteCircuitAuthorization](./Remove-AzExpressRouteCircuitAuthorization.md)

