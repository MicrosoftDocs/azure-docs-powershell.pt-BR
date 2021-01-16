---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationTask
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationTask.md
ms.openlocfilehash: 0222900be337cfe9eab97da31fc9d2dd84744e43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271525"
---
# New-AzDataMigrationTask

## Sinopse
Cria e inicia uma tarefa de migração de dados no serviço de migração de banco de dados do Azure.

## SYNTAX

### ComponentNameParameterSet (padrão)
```
New-AzDataMigrationTask -TaskType <TaskTypeEnum> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ComponentObjectParameterSet
```
New-AzDataMigrationTask [-InputObject] <PSProject> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdParameterSet
```
New-AzDataMigrationTask [-ResourceId] <String> -TaskType <TaskTypeEnum> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet New-AzDataMigrationTask cria uma tarefa de migração de dados. Esse cmdlet tem parâmetros para enumerador de tipo de tarefa, grupo de recursos do Azure, nome do serviço de migração de banco de dados do Azure associado e projeto como entrada. 

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzDmsTask -TaskType MigrateSqlServerSqlDb -ResourceGroupName myResourceGroup -ServiceName TestService -ProjectName myDMSProject -TaskName MyMigrationTask -SourceConnection $sourceConnInfo -SourceCred $sourceCred -TargetConnection $targetConnInfo -TargetCred $targetCred -SelectedDatabase  $selectedDbs -MigrationValidation $validationTask
```

Este script de exemplo mostra como criar uma nova tarefa de migração de dados chamada MyMigrationTask no projeto chamado myDMSProject e Service chamado TestService. 

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

### -InputObject
Objeto PSProject.

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProject
Parameter Sets: ComponentObjectParameterSet
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
Parameter Sets: (All)
Aliases: TaskName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProjectName
O nome do projeto.

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
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
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID do recurso do projeto.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Nome do serviço de migração de banco de dados.

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskType
Tipo de tarefa.

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.TaskTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: MigrateSqlServerSqlDb, ConnectToSourceSqlServer, ConnectToTargetSqlDb, GetUserTablesSql, ConnectToTargetSqlDbMi, MigrateSqlServerSqlDbMi, ValidateSqlServerSqlDbMi, MigrateSqlServerSqlDbSync, ConnectToSourceSqlServerSync, ConnectToTargetSqlSync, GetUserTablesSqlSync, ValidateSqlServerSqlDbSync, ConnectToSourceMongoDb, ConnectToTargetMongoDb, MigrateMongoDb, ValidateMongoDbMigration, ConnectToTargetSqlDbMiSync, ValidateSqlServerSqlDbMiSync, MigrateSqlServerSqlDbMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationValidation 
Objeto de resposta de tarefa por chamada de validação, opcional, mas recomendado.

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSProjectTask
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wait
Se deve aguardar a conclusão da tarefa. Se o sinalizador estiver definido, verifica a cada um segundos até que a tarefa seja concluída e retorne ao usuário as propriedades da tarefa onde a saída ou o erro pode ser inspecionado. 
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. datamigration. Models. PSProject

### System. String

## EXIBE

### Microsoft. Azure. Commands. datamigration. Models. PSProjectTask

## INFORMA

## LINKS RELACIONADOS
