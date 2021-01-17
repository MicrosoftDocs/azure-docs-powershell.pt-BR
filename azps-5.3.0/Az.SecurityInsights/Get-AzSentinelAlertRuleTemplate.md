---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433216"
---
# Get-AzSentinelAlertRuleTemplate

## Sinopse
Obter modelo de regra analítica.

## SYNTAX

### WorkspaceScope (padrão)
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AlertRuleTemplateId
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Identificação
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzSentinelAlertRuleTemplate** Obtém um modelo de regra de alerta do espaço de trabalho especificado.
Se você especificar o parâmetro *AlertRuleTemplateId* , um único objeto **AlertRuleTemplate** será retornado.
Se você não especificar o parâmetro *AlertRuleTemplateId* , uma matriz que contenha todos os modelos de regra de alerta no espaço de trabalho especificado será retornada.
Você pode usar o objeto **AlertRuleTemplate** para criar uma nova regra de alerta.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

Este exemplo obtém todos os **AlertRuleTemplates** no espaço de trabalho especificado e, em seguida, armazena-os na variável $AlertRuleTemplates.

### Exemplo 2
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

Este exemplo obtém um **AlertRuleTemplate** no espaço de trabalho especificado e, em seguida, armazena-o na variável $AlertRuleTemplate.

## OS

### -AlertRuleTemplateId
ID da regra de alerta de modelo.

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
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
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
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
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
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

### Microsoft. Azure. Commands. SecurityInsights. Models. AlertRuleTemplates. PSSentinelAlertRuleTemplate
## INFORMA

## LINKS RELACIONADOS
