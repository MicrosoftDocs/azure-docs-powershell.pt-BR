---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: d70a0b6abd31d4104301e877fb21bf1d0589a24f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891609"
---
# Get-AzSqlElasticJobStep

## SYNOPSIS
Obtém uma ou mais etapas de trabalho

## SINTAXE

### DefaultSet (Padrão)
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetVersion
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ObjectSet
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetVersionUsingJobObject
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdSet
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetVersionUsingParentResourceId
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O Get-AzSqlElasticJobStep cmdlet obtém uma ou mais etapas de trabalho de um trabalho

## EXEMPLOS

### Exemplo 1: obtém uma etapa de trabalho de um trabalho
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

Obtém uma etapa de trabalho de um trabalho

## PARÂMETROS

### -AgentName
O nome do agente

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -JobName
O nome do trabalho

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
O nome da etapa de trabalho

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentObject
O objeto de entrada do trabalho

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentResourceId
A ID do recurso de trabalho

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
O nome do servidor

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
O nome da etapa de trabalho

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel

## SAÍDAS

### Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel

## NOTES

## LINKS RELACIONADOS
