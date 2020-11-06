---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428476"
---
# Get-AzureRmServiceEndpointPolicy

## Sinopse
{{Preencher o resumo}}

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmServiceEndpointPolicy** Obtém uma política de ponto de extremidade do serviço.

## EXEMPLOS

### Exemplo 1
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

Esse comando obtém a política de ponto de extremidade do serviço chamada ServiceEndpointPolicy1 que pertence ao grupo de recursos chamado ResourceGroup01 e a armazena na variável $policy.

### Exemplo 2
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

Esse comando obtém uma lista de todas as políticas de ponto de extremidade do serviço no grupo de recursos chamado ResourceGroup01 e as armazena na variável $policyList.

## OS

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

### -Nome
O nome da política de ponto de extremidade do serviço

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

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.
Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String


## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy


## INFORMA

## LINKS RELACIONADOS
