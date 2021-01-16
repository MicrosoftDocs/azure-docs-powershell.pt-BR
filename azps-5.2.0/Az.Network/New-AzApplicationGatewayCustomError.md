---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259433"
---
# New-AzApplicationGatewayCustomError

## Sinopse
Cria um erro personalizado com código de status HTTP e URL da página de erro personalizada 

## SYNTAX

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzApplicationGatewayCustomError** cria um erro personalizado.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

Esse comando cria o erro personalizado de código de status HTTP 403.

## OS

### -CustomErrorPageUrl
URL da página de erro do erro do cliente do gateway do aplicativo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -StatusCode
Código do status do erro do cliente do aplicativo gateway.

```yaml
Type: System.String
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

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError

## INFORMA

## LINKS RELACIONADOS

[Add-AzApplicationGatewayCustomError](./Add-AzApplicationGatewayCustomError.md)

[Get-AzApplicationGatewayCustomError](./Get-AzApplicationGatewayCustomError.md)

[Remove-AzApplicationGatewayCustomError](./Remove-AzApplicationGatewayCustomError.md)

[Set-AzApplicationGatewayCustomError](./Set-AzApplicationGatewayCustomError.md)
