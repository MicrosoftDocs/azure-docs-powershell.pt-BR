---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433213"
---
# Get-AzSentinelIncident

## Sinopse
Obter um incidente.

## SYNTAX

### WorkspaceScope (padrão)
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Incidentid
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Identificação
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzSentinelIncident** Obtém um incidente do espaço de trabalho especificado.
Se você especificar o parâmetro *incidentid* , um único objeto de **incidente** será retornado.
Se você não especificar o parâmetro *incidentid* , uma matriz contendo todos os incidentes no espaço de trabalho especificado será retornada.
Você pode usar o objeto de **incidente** para atualizar o incidente, por exemplo, você pode adicionar anotações ao **incidente**.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

Este exemplo obtém todos os **incidentes** no espaço de trabalho especificado e, em seguida, armazena-os na variável $Incidents.

### Exemplo 2
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

Este exemplo obtém um **incidente** no espaço de trabalho especificado e, em seguida, armazena-o na variável $Incident.

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

### -Incidentid
ID do incidente.

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
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
Parameter Sets: WorkspaceScope, IncidentId
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

### Microsoft. Azure. Commands. SecurityInsights. Models. Incidents. PSSentinelIncident
## INFORMA

## LINKS RELACIONADOS
