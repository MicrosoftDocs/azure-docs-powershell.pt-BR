---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 481105ca99a2bdc797a7a539f54ab69fd9935ebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888872"
---
# New-AzAlertRuleEmail

## SYNOPSIS
Cria uma ação de email para uma regra de alerta.

## SINTAXE

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzAlertRuleEmail** cria uma ação de email para uma regra de alerta.

## EXEMPLOS

### Exemplo 1: Criar uma ação de email de regra de alerta para proprietários de serviço
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

Este comando cria uma ação de email de regra de alerta para enviar para seus proprietários de serviço quando uma regra de alerta é disparada.

### Exemplo 2: Criar uma ação de email de regra de alerta para proprietários que não são do serviço
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

Este comando cria uma ação de email de regra de alerta para os endereços de email especificados, mas não para os proprietários do serviço.

### Exemplo 3: Criar uma ação de email de regra de alerta para proprietários de serviços e proprietários que não são do serviço
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

Este comando cria uma ação de email de regra de alerta para o endereço especificado e para seus proprietários de serviço.

## PARÂMETROS

### -CustomEmail
Especifica uma lista de endereços de email separados por vírgulas.

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
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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
Indica que essa operação envia um email para os proprietários do serviço quando a regra é a incêndio.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String[]

### System.Management.Automation.SwitchParameter

## SAÍDAS

### Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction

## NOTES

## LINKS RELACIONADOS

[Add-AzLogAlertRule](./Add-AzLogAlertRule.md)

[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


