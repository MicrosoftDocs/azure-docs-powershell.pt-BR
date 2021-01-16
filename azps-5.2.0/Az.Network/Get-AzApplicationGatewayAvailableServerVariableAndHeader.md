---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261729"
---
# Get-AzApplicationGatewayAvailableServerVariableAndHeader

## Sinopse
Obter as variáveis de servidor com suporte e os cabeçalhos de solicitação e resposta disponíveis.

## SYNTAX

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** Obtém as variáveis de servidor com suporte e os cabeçalhos de solicitação e resposta disponíveis. Os parâmetros podem ser usados para obter as listas de variáveis ou de cabeçalhos.

## EXEMPLOS

### Exemplo 1
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

Esses comandos retornam todas as variáveis de servidor disponíveis.

### Exemplo 2
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

Esses comandos retornam todos os cabeçalhos de solicitação disponíveis.

### Exemplo 3
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

Esses comandos retornam todos os cabeçalhos de resposta disponíveis.

### Exemplo 4
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

Esses comandos retornam todas as variáveis de servidor disponíveis, cabeçalhos de solicitação e resposta.

### Exemplo 5
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

Esses comandos retornam todas as variáveis de servidor disponíveis, cabeçalhos de solicitação e resposta.

## OS

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

### -RequestHeader
O Application Gateway disponibilizou cabeçalhos de solicitação.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResponseHeader
Cabeçalhos de resposta do Application Gateway disponíveis.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerVariable
Variáveis de servidor disponíveis do Application Gateway.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult

## INFORMA
**List-AzApplicationGatewayAvailableServerVariableAndHeader** é um alias para o cmdlet **Get-AzApplicationGatewayAvailableServerVariableAndHeader** .

## LINKS RELACIONADOS
