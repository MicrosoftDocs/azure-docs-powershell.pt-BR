---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891804"
---
# Get-AzApplicationGatewayHttpListenerCustomError

## SYNOPSIS
Obtém erros personalizados de um ouvinte http de um gateway de aplicativo.

## SINTAXE

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzApplicationGatewayCustomError** obtém erros personalizados de um ouvinte http de um gateway de aplicativo.

## EXEMPLOS

### Exemplo 1: obtém um erro personalizado em um ouvinte http
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

Este comando obtém e retorna o erro personalizado do código de status http 502 do ouvinte http $listener 01.

### Exemplo 2: Obtém a lista de todos os erros personalizados em um ouvinte http
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

Este comando obtém e retorna a lista de todos os erros personalizados do ouvinte http $listener 01.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -HttpListener
O Ouvinte Http do Gateway de Aplicativos

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
Código de status do erro do cliente do gateway de aplicativo.

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

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener

## SAÍDAS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError

## NOTES

## LINKS RELACIONADOS

[Add-AzApplicationGatewayHttpListenerCustomError](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[Remove-AzApplicationGatewayHttpListenerCustomError](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[Set-AzApplicationGatewayHttpListenerCustomError](./Set-AzApplicationGatewayHttpListenerCustomError.md)
