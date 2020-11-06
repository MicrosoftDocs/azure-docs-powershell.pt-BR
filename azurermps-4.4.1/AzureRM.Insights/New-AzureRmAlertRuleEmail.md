---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432208"
---
# New-AzureRmAlertRuleEmail

## Sinopse
Cria uma ação de email para uma regra de alerta.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmAlertRuleEmail** cria uma ação de email para uma regra de alerta.

## EXEMPLOS

### Exemplo 1: criar uma ação de email de regra de alerta para proprietários de serviço
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

Esse comando cria uma ação de email de regra de alerta para enviar para seus proprietários de serviço quando uma regra de alerta é acionada.

### Exemplo 2: criar uma regra de alerta ação de email para proprietários que não são de serviço
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

Esse comando cria uma ação de email de regra de alerta para os endereços de email especificados, mas não para os proprietários do serviço.

### Exemplo 3: criar uma regra de alerta ação de email para proprietários de serviços e proprietários não pertencentes ao serviço
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

Esse comando cria uma ação de email de regra de alerta para o endereço especificado e para seus proprietários de serviço.

## OS

### -CustomEmails
Especifica uma lista de endereços de email separados por vírgula.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SendToServiceOwners
Indica que esta operação envia um email para os proprietários do serviço quando a regra é acionada.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## EXIBE

### Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[Add-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[Add-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[New-AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


