---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426331"
---
# Set-AzureRmFirewall

## Sinopse
Salva um firewall modificado.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmFirewall** atualiza um firewall do Azure.

## EXEMPLOS

### 1: atualizar a prioridade de um conjunto de regras de aplicativo de firewall
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

Este exemplo atualiza a prioridade de um conjunto de regras existente de um firewall do Azure.
Pressupondo que o Firewall do Azure "AzureFirewall" no grupo de recursos "RG" contenha uma coleção de regras de aplicativo chamada "ruleCollectionName", os comandos acima alterarão a prioridade dessa coleção de regras e atualizarão o Firewall do Azure posteriormente. Sem o comando Set-AzureRmFirewall, todas as operações executadas no objeto de $azFw local não são refletidas no servidor.

### 2: criar um firewall do Azure e definir uma coleção de regras de aplicativo mais tarde
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

Neste exemplo, um firewall é criado primeiro sem nenhuma coleção de regras de aplicativo. Posteriormente, uma regra de aplicativo e uma coleção de regras de aplicativo são criadas, o objeto de firewall é modificado na memória, sem afetar a configuração real na nuvem. Para que as alterações sejam refletidas na nuvem, Set-AzureRmFirewall devem ser chamadas.

## OS

### -AsJob
Executar o cmdlet em segundo plano

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureFirewall
O AzureFirewall

```yaml
Type: PSAzureFirewall
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSAzureFirewall
O parâmetro ' AzureFirewall ' aceita o valor do tipo ' PSAzureFirewall ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSAzureFirewall

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[New-AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)
