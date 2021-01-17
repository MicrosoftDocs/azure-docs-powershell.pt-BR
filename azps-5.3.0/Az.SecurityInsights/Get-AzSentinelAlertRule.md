---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433226"
---
# Get-AzSentinelAlertRule

## Sinopse
Obtém um analítico (regra de alerta).

## SYNTAX

### WorkspaceScope (padrão)
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AlertRuleId
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Identificação
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzSentinelAlertRule** Obtém uma análise (regra de alerta) do espaço de trabalho especificado.
Se você especificar o parâmetro *AlertRuleId* , um único objeto **AlertRule** será retornado.
Se você não especificar o parâmetro *AlertRuleId* , uma matriz contendo todas as regras de alerta no espaço de trabalho especificado será retornada.
Você pode usar o objeto **AlertRule** para atualizar o AlertRule, por exemplo, você pode desabilitar o **AlertRule**.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

Este exemplo obtém todos os **AlertRules** no espaço de trabalho especificado e, em seguida, armazena-os na variável $AlertRules.

### Exemplo 2
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

Este exemplo obtém um **AlertRule** no espaço de trabalho especificado e, em seguida, armazena-o na variável $AlertRule.

## OS

### -AlertRuleId
ID da regra de alerta.

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do recurso.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceName
Nome do espaço de trabalho.

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String
## EXIBE

### Microsoft. Azure. Commands. SecurityInsights. Models. AlertRules. PSSentinelAlertRule
## INFORMA

## LINKS RELACIONADOS
