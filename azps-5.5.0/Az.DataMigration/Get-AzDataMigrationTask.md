---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationTask.md
ms.openlocfilehash: bcc1c39af722d5f12c333152e8458228f583a842
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110986"
---
# Get-AzDataMigrationTask

## Sinopse
Recupera o objeto PSProjectTask associado a uma tarefa de migração do Serviço de Migração de Banco de Dados do Azure.

## Sintaxe

### ListByComponent (Padrão)
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-TaskType <TaskTypeEnum>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListByInputObject
```
Get-AzDataMigrationTask [-InputObject] <PSProject> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByInputObject
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByInputObjectResultType
```
Get-AzDataMigrationTask [-InputObject] <PSProject> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListByResourceId
```
Get-AzDataMigrationTask [-ResourceId] <String> [-TaskType <TaskTypeEnum>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceId
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceIdResultType
```
Get-AzDataMigrationTask [-ResourceId] <String> -Name <String> [-Expand] -ResultType <ResultTypeEnum>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByComponent
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String>
 [-Name <String>] [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByComponentResultType
```
Get-AzDataMigrationTask -ResourceGroupName <String> -ServiceName <String> -ProjectName <String> -Name <String>
 [-Expand] -ResultType <ResultTypeEnum> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O Get-AzDataMigrationTask cmdlet recupera as propriedades associadas a uma tarefa de migração do Serviço de Migração de Banco de Dados do Azure.

## Exemplos

### Exemplo 1
```
PS C:\> Get -AzDataMigrationTask -TaskName myTestTask -ServiceName myTestService -ProjectName MyTestProject -ResourceGroupName MyResourceGroup -Expand
```

O exemplo acima ilustra o uso do cmdlet Get-AzDataMigrationTask para recuperar as propriedades associadas a uma tarefa de migração do Serviço de Migração de Banco de Dados do Azure com base no nome da tarefa passada como parâmetro de entrada

### Exemplo 2
```
PS C:\> Get -AzDataMigrationTask -Project $myProject
```

O exemplo acima ilustra o uso do cmdlet Get-AzDataMigrationTask para recuperar todas as tarefas de migração associadas ao objeto PSProject passado como parâmetro de entrada

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -Expandir
Expandir saída

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObject, GetByResourceId, GetByComponent
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Objeto PSProject.

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ListByInputObject
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: GetByInputObject, GetByInputObjectResultType
Aliases: Project

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
O nome da tarefa.

```yaml
Type: System.String
Parameter Sets: GetByInputObject, GetByInputObjectResultType, GetByResourceId, GetByResourceIdResultType, GetByComponentResultType
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByComponent
Aliases: TaskName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName
O nome do projeto.

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do Recurso do Projeto.

```yaml
Type: System.String
Parameter Sets: ListByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceId, GetByResourceIdResultType
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResultType
Expandir a saída de determinado tipo de resultado.

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ResultTypeEnum
Parameter Sets: GetByInputObjectResultType, GetByResourceIdResultType, GetByComponentResultType
Aliases:
Accepted values: MigrationLevelOutput, DatabaseLevelOutput, TableLevelOutput, MigrationValidationOutput, MigrationValidationDatabaseLevelOutput, LoginLevelOutput, AgentJobLevelOutput, Command

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Nome do serviço de migração de banco de dados.

```yaml
Type: System.String
Parameter Sets: ListByComponent, GetByComponent, GetByComponentResultType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskType
Filtrar por TaskType.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum]
Parameter Sets: ListByComponent, ListByInputObject, ListByResourceId
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.DataMigration.Models.PSProject

### System.String

## Saídas

### Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask

## Notas

## LINKS RELACIONADOS
