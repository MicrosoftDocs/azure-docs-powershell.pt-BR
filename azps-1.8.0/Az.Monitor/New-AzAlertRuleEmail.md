---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: cfdd18a02a5e0507e86a37dee1e1662bb5094f37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770308"
---
# New-AzAlertRuleEmail

## Sinopse
Cria uma ação de email para uma regra de alerta.

## SYNTAX

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzAlertRuleEmail** cria uma ação de email para uma regra de alerta.

## EXEMPLOS

### Exemplo 1: criar uma ação de email de regra de alerta para proprietários de serviço
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Esse comando cria uma ação de email de regra de alerta para enviar para seus proprietários de serviço quando uma regra de alerta é acionada.

### Exemplo 2: criar uma regra de alerta ação de email para proprietários que não são de serviço
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

Esse comando cria uma ação de email de regra de alerta para os endereços de email especificados, mas não para os proprietários do serviço.

### Exemplo 3: criar uma regra de alerta ação de email para proprietários de serviços e proprietários não pertencentes ao serviço
```
PS C:\>New-AzAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

Esse comando cria uma ação de email de regra de alerta para o endereço especificado e para seus proprietários de serviço.

## OS

### -CustomEmail
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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -SendToServiceOwner
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String []

### System. Management. Automation. SwitchParameter

## EXIBE

### Microsoft. Azure. Management. monitor. Management. Models. RuleEmailAction

## INFORMA

## LINKS RELACIONADOS

[Add-AzLogAlertRule](./Add-AzLogAlertRule.md)

[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


