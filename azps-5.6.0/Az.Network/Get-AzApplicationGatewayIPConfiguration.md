---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 367d4efc8332b862a8db276934acfa971d7c0d9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891803"
---
# Get-AzApplicationGatewayIPConfiguration

## SYNOPSIS
Obtém a configuração IP de um gateway de aplicativo.

## SINTAXE

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzApplicationGatewayIPConfiguration obtém** a configuração IP de um gateway de aplicativo.
A configuração ip contém a sub-rede na qual o gateway de aplicativo é implantado.

## EXEMPLOS

### Exemplo 1: Obter uma configuração IP específica
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

O primeiro comando obtém um gateway de aplicativo e o armazena na $AppGw variável. O segundo comando obtém uma configuração IP chamada GateSubnet01 do gateway armazenado $AppGw.

### Exemplo 2: obter uma lista de configurações IP
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

O primeiro comando obtém um gateway de aplicativo e o armazena na $AppGw variável. O segundo comando obtém uma lista de todas as configurações ip.

## PARÂMETROS

### -ApplicationGateway
Especifica o objeto gateway de aplicativo que contém configuração IP.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Especifica o nome da configuração IP que esse cmdlet obtém.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration

## NOTES

## LINKS RELACIONADOS

[Add-AzApplicationGatewayIPConfiguration](./Add-AzApplicationGatewayIPConfiguration.md)

[New-AzApplicationGatewayIPConfiguration](./New-AzApplicationGatewayIPConfiguration.md)

[Remove-AzApplicationGatewayIPConfiguration](./Remove-AzApplicationGatewayIPConfiguration.md)

[Set-AzApplicationGatewayIPConfiguration](./Set-AzApplicationGatewayIPConfiguration.md)


