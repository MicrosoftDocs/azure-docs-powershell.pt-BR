---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 574c41fe8b0f3266a6fff80c020b60c9832cb431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262127"
---
# New-AzSynapseSqlPoolRestorePoint

## Sinopse
Cria um novo ponto de restauração em um pool SQL do Azure Synapse Analytics.

## SYNTAX

### CreateByNameParameterSet (padrão)
```
New-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateByParentObjectParameterSet
```
New-AzSynapseSqlPoolRestorePoint -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 -RestorePointLabel <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### CreateByInputObjectParameterSet
```
New-AzSynapseSqlPoolRestorePoint -InputObject <PSSynapseSqlPool> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateByResourceIdParameterSet
```
New-AzSynapseSqlPoolRestorePoint -ResourceId <String> -RestorePointLabel <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzSynapseSqlPoolRestorePoint** cria um novo ponto de restauração no qual um pool SQL do Azure Synapse Analytics pode ser restaurado.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> New-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -RestorePointLabel ContosoRestorePoint
```

Esse comando cria um ponto de restauração do pool do SQL chamado ContosoSqlPool na ContosoWorkspace do espaço de trabalho.

## OS

### -AsJob
Executar o cmdlet em segundo plano

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

### -InputObject
Objeto de entrada de pool SQL, geralmente passado pelo pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome do pool do SQL Synapse.

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
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
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identificador de recurso do pool do SQL Synapse.

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestorePointLabel
O rótulo ao qual associamos um ponto de restauração pode não ser exclusivo.

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
Nome do espaço de trabalho do Synapse.

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Workspaceobject
objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace

### Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool

## EXIBE

### Microsoft. Azure. Commands. Synapse. Models. PSRestorePoint

## INFORMA

## LINKS RELACIONADOS
