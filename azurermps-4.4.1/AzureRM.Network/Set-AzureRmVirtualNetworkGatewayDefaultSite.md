---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A27EE9C0-C7F5-4BF6-AE52-58087BD1B1C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayDefaultSite.md
ms.openlocfilehash: 4ab32ab5830356740cdb1709799b7dcb8f811c90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429214"
---
# Set-AzureRmVirtualNetworkGatewayDefaultSite

## Sinopse
Define o site padrão para um gateway de rede virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmVirtualNetworkGatewayDefaultSite -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -GatewayDefaultSite <PSLocalNetworkGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmVirtualNetworkGatewayDefaultSite** atribui um site padrão de encapsulamento forçado a um gateway de rede virtual.
O tunelamento forçado fornece uma maneira de redirecionar o tráfego associado à Internet das máquinas virtuais do Azure para a sua rede local; Isso permite que você inspecione e audite o tráfego antes de liberá-lo.
O encapsulamento forçado é executado usando um encapsulamento de rede virtual privada (VPN); Esse encapsulamento exige um site padrão, um gateway local onde todo o tráfego associado à Internet do Azure é redirecionado.
**Set-AzureRmVirtualNetworkGatewayDefaultSite** fornece uma maneira de alterar o site padrão atribuído a um gateway.

## EXEMPLOS

### Exemplo 1: atribuir um site padrão a um gateway de rede virtual
```
PS C:\>$LocalGateway = Get-AzureRmLocalNetworkGateway -Name "ContosoLocalGateway " -ResourceGroup "ContosoResourceGroup"
PS C:\> $VirtualGateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayDefaultSite -GatewayDefaultSite $LocalGateway -VirtualNetworkGateway $VirtualGateway
```

Este exemplo atribui um site padrão a um gateway de rede virtual chamado ContosoVirtualGateway.

O primeiro comando cria uma referência de objeto para um gateway local chamado ContosoLocalGateway.
Esta referência de objeto armazenada na variável chamada $LocalGateway representa o gateway a ser configurado como o site padrão

.
Em seguida, o segundo comando cria uma referência de objeto para o gateway de rede virtual e armazena o resultado na variável chamada $VirtualGateway.

O terceiro comando usa o cmdlet **set-AzureRmVirtualNetworkGatewayDefaultSite** para atribuir o site padrão ao ContosoVirtualGateway.

## OS

### -GatewayDefaultSite
Especifica uma referência de objeto para o gateway de rede local a ser atribuído como o site padrão para a rede virtual especificada.
Você pode usar o cmdlet Get-AzureRmLocalNetworkGateway para criar uma referência de objeto para um gateway local.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Especifica uma referência de objeto para o gateway de rede virtual em que o site padrão será atribuído.
Você pode criar uma referência de objeto para um gateway de rede virtual usando **Get-AzureRmVirtualNetworkGateway** e especificando o nome do gateway.

A variável $VirtualGateway pode ser usada como o valor do parâmetro para o parâmetro *VirtualNetworkGateway* :

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

[Get-AzureRmLocalNetworkGateway](./Get-AzureRmLocalNetworkGateway.md)

[Get-AzureRmVirtualNetworkGateway](./Get-AzureRmVirtualNetworkGateway.md)

[Remove-AzureRmVirtualNetworkGatewayDefaultSite](./Remove-AzureRmVirtualNetworkGatewayDefaultSite.md)


