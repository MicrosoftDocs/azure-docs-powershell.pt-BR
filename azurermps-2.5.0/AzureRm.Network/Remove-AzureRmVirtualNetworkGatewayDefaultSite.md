---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 65E9C4D5-4D2C-4039-A87B-4E693B97C4CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewaydefaultsite
schema: 2.0.0
ms.openlocfilehash: ded608261981073ef5544df2b64e99171eef7710
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785459"
---
# Remove-AzureRmVirtualNetworkGatewayDefaultSite

## Sinopse
Remove o site padrão de um gateway de rede virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmVirtualNetworkGatewayDefaultSite** remove o site padrão de encapsulamento forçado de um gateway de rede virtual.
O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.
O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.

**Remove-AzureRmVirtualNetworkGatewayDefaultSite** remove o site padrão atribuído a um gateway.
Se fizer isso, você precisará usar o Set-AzureRmVirtualNetworkGatewayDefaultSite para atribuir um novo site padrão antes que o gateway possa ser usado para encapsulamento forçado.

## EXEMPLOS

### Exemplo 1: remover o site padrão atribuído a um gateway de rede virtual
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Remove-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworknGateway $Gateway
```

Este exemplo remove o site padrão atribuído atualmente a um gateway de rede virtual chamado ContosoVirtualGateway.

O primeiro comando usa **Get-AzureRmVirtualNetworkGateway** para criar uma referência de objeto para o gateway; Essa referência de objeto é armazenada em uma variável chamada $Gateway.

Em seguida, o segundo comando usa **Remove-AzureRmVirtualNetworkGatewayDefaultSite** para remover o site padrão atribuído a esse gateway.

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

### -VirtualNetworkGateway
Especifica uma referência de objeto para o gateway de rede virtual que contém o site padrão a ser removido.
Você pode criar uma referência de objeto para um gateway de rede virtual usando o Get-AzureRmVirtualNetworkGateway e especificando o nome do gateway.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

###  
Esse cmdlet aceita instâncias em pipeline do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## EXIBE

###  
Esse cmdlet modifica instâncias existentes do objeto **Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway** .

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Set-AzureRmVirtualNetworkGatewayDefaultSite](./Set-AzureRmVirtualNetworkGatewayDefaultSite.md)


