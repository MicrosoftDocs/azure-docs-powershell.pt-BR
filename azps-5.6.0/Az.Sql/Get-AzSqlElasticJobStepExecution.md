---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891606"
---
# Get-AzSqlElasticJobStepExecution

## SYNOPSIS
Obtém uma ou mais execuções de etapa de trabalho

## SINTAXE

### DefaultSet (Padrão)
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WithJobStepName
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ObjectSet
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WithJobStepNameUsingParentObject
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdSet
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WithJobStepNameUsingParentResourceId
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O Get-AzSqlElasticJobStepExecution cmdlet obtém uma ou mais execuções de etapa de trabalho de uma execução de trabalho

## EXEMPLOS

### Exemplo 1 - Obtém uma ou mais execuções de etapa de trabalho de execuções de trabalho
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### Exemplo 2 - Obtém uma ou mais execuções de etapa de trabalho de uma execução de trabalho, filtragem por nome de etapa
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

Obtém uma ou mais execuções de etapa de trabalho

## PARÂMETROS

### -Active
Sinalizar para filtrar por execuções ativas.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -AgentName
O nome do agente.

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateTimeMax
Filtrar por criar tempo máximo

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateTimeMin
Filtrar por criar tempo mínimo

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
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

### -EndTimeMax
Filtrar por tempo máximo de término.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTimeMin
Filtrar por tempo mínimo de término.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobExecutionId
A ID de execução do trabalho.

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
O nome do trabalho.

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentObject
O objeto agent.

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentResourceId
A ID do recurso de execução de trabalho.

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
O nome do servidor.

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StepName
O nome da etapa de trabalho.

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel

## SAÍDAS

### Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel

## NOTES

## LINKS RELACIONADOS
