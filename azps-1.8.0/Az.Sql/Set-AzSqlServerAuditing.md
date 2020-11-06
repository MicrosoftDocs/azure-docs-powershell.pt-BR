---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: 44db866488459382a3b66f77328b5cbc9259754b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598758"
---
# Set-AzSqlServerAuditing

## Sinopse
Altera as configurações de auditoria de um SQL Server do Azure.

## SYNTAX

### DefaultParameterSet (padrão)
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### StorageAccountSubscriptionIdSet
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### EventHubSet
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogAnalyticsSet
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### BlobStorageByParentResourceSet
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### StorageAccountSubscriptionIdByParentResourceSet
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### EventHubByParentResourceSet
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogAnalyticsByParentResourceSet
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzSqlServerAuditing** altera as configurações de auditoria de um SQL Server do Azure.
Para usar o cmdlet, use os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.
O destino dos logs de auditoria é determinado especificando um dos seguintes parâmetros de switch: BlobStorage, LogAnalytics ou EventHub (se nenhum for especificado, o padrão será BlobStorage).
Use o parâmetro *State* para habilitar/desabilitar a política.
Quando o destino de logs de auditoria for armazenamento de BLOBs, especifique o parâmetro *StorageAccountName* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento. Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.
Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve as configurações atuais de auditoria, além dos identificadores de servidor.
Os identificadores de servidor incluem, entre outros, **ResourceGroupName** e **nomedoservidor**.

## EXEMPLOS

### Exemplo 1: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### Exemplo 2: desabilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### Exemplo 3: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure usando uma conta de armazenamento de uma assinatura diferente
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### Exemplo 4: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure com filtragem avançada usando um predicado T-SQL
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### Exemplo 5: remover a configuração de filtragem avançada da política de armazenamento de auditoria de blob de um SQL Server do Azure
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### Exemplo 6: habilitar a política de auditoria do hub de eventos de um SQL Server do Azure
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### Exemplo 7: desabilitar a política de auditoria do hub de eventos de um SQL Server do Azure
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### Exemplo 8: habilitar a política de auditoria de análise de logs de um SQL Server do Azure
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### Exemplo 9: desabilitar a política de auditoria de análise de logs de um SQL Server do Azure
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### Exemplo 10: desabilitar, por meio de pipeline, a política de auditoria de análise de logs de um SQL Server do Azure
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

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

### -AuditActionGroup
O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:  
  
"BATCH_COMPLETED_GROUP",  
"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",  
"FAILED_DATABASE_AUTHENTICATION_GROUP"  
Esta combinação acima também é o conjunto que é configurado por padrão. Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.
Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BlobStorage
Especifica que o destino dos logs de auditoria é o armazenamento de BLOB

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
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

### -EventHub
Especifica que o destino dos logs de auditoria é o Hub de eventos

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHubAuthorizationRuleResourceId
A ID do recurso para a regra de autorização do hub de eventos

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventHubName
O nome do hub de eventos. Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o Hub de eventos padrão será selecionado.

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
O objeto do servidor para gerenciar sua política de auditoria.

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogAnalytics
Especifica que o destino dos logs de auditoria é análise de logs

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Especifica se a política de auditoria deve ser impressa no final da execução do cmdlet

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

### -Predicateie
O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
O número de dias de retenção para os logs de auditoria.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomedoservidor
Nome do SQL Server.

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Estado
O estado da política.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
O nome da conta de armazenamento.

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountSubscriptionId
A ID da assinatura da conta de armazenamento

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
Especifica quais das chaves de acesso de armazenamento usar.

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WorkspaceResourceId
A ID do espaço de trabalho (ID do recurso de um espaço de trabalho de análise de log) para um espaço de trabalho de análise de log ao qual você gostaria de enviar logs de auditoria. Exemplo:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel

### Microsoft. Azure. Commands. Sql. Auditing. Model. AuditActionGroups []

### System. Management. Automation. SwitchParameter

### System. GUID

### System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## EXIBE

### Microsoft. Azure. Commands. Sql. Auditing. Model. ServerBlobAuditingSettingsModel

## INFORMA

## LINKS RELACIONADOS
