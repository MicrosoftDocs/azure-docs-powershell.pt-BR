---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433209"
---
# New-AzSentinelAlertRuleAction

## Sinopse
Adicionar uma resposta automática a um Analatic.

## SYNTAX

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzSentinelAlertRuleAction** cria uma resposta automática para uma regra de alerta no espaço de trabalho especificado.
Você deve fornecer a ID Resorce do aplicativo lógico e o URI Trigger que podem ser encontrados usando o módulo do aplicativo lógico.
Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

Este exemplo cria um **AlertRuleAction** para a regra de alerta especificada usando propriedades do aplicativo lógico e, em seguida, armazena-o na variável $AlertRuleAction.

## OS

### -ActionID
ID da ação.

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

### -AlertRuleId
ID da regra de alerta.

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

### -LogicAppResourceId
ID do recurso de aplicativo lógica da ação.

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
Nome do grupo de recursos.

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

### -TriggerUri
URI de gatilho do aplicativo lógica da ação.

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

### -WorkspaceName
Nome do espaço de trabalho.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse
## INFORMA

## LINKS RELACIONADOS
