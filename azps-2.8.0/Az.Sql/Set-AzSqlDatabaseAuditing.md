---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773513"
---
# <span data-ttu-id="ebe14-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ebe14-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="ebe14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ebe14-102">SYNOPSIS</span></span>
<span data-ttu-id="ebe14-103">**Importante: esse cmdlet é preterido, [set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) está substituindo-o.**</span><span class="sxs-lookup"><span data-stu-id="ebe14-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="ebe14-104">Altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe14-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="ebe14-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebe14-105">SYNTAX</span></span>

### <span data-ttu-id="ebe14-106">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ebe14-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe14-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="ebe14-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe14-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="ebe14-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe14-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="ebe14-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe14-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ebe14-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe14-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ebe14-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebe14-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ebe14-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ebe14-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="ebe14-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebe14-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ebe14-114">DESCRIPTION</span></span>
<span data-ttu-id="ebe14-115">O cmdlet **set-AzSqlDatabaseAuditing** altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe14-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="ebe14-116">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ebe14-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ebe14-117">O destino dos logs de auditoria é determinado especificando um dos seguintes parâmetros de switch: BlobStorage, LogAnalytics ou EventHub (se nenhum for especificado, o padrão será BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="ebe14-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="ebe14-118">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="ebe14-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="ebe14-119">Quando o destino de logs de auditoria for armazenamento de BLOBs, especifique o parâmetro *StorageAccountName* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ebe14-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="ebe14-120">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ebe14-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="ebe14-121">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve as configurações atuais de auditoria, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ebe14-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="ebe14-122">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="ebe14-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="ebe14-123">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebe14-123">EXAMPLES</span></span>

### <span data-ttu-id="ebe14-124">Exemplo 1: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="ebe14-125">Exemplo 2: desabilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="ebe14-126">Exemplo 3: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure usando uma conta de armazenamento de uma assinatura diferente</span><span class="sxs-lookup"><span data-stu-id="ebe14-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="ebe14-127">Exemplo 4: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure com filtragem avançada usando um predicado T-SQL</span><span class="sxs-lookup"><span data-stu-id="ebe14-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="ebe14-128">Exemplo 5: remover a configuração de filtragem avançada da política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="ebe14-129">Exemplo 6: habilitar a política de auditoria do hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="ebe14-130">Exemplo 7: desabilitar a política de auditoria do hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="ebe14-131">Exemplo 8: habilitar a política de auditoria de análise de log de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="ebe14-132">Exemplo 9: desabilitar a política de auditoria de análise de log de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="ebe14-133">Exemplo 10: desabilitar, por meio de pipeline, a política de auditoria de análise de logs de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ebe14-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="ebe14-134">OS</span><span class="sxs-lookup"><span data-stu-id="ebe14-134">PARAMETERS</span></span>

### <span data-ttu-id="ebe14-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebe14-135">-AsJob</span></span>
<span data-ttu-id="ebe14-136">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ebe14-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebe14-137">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="ebe14-137">-AuditAction</span></span>
<span data-ttu-id="ebe14-138">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ebe14-138">The set of audit actions.</span></span>  
<span data-ttu-id="ebe14-139">As ações com suporte para auditoria são:</span><span class="sxs-lookup"><span data-stu-id="ebe14-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="ebe14-140">SELECIONADA</span><span class="sxs-lookup"><span data-stu-id="ebe14-140">SELECT</span></span>  
<span data-ttu-id="ebe14-141">ATUALIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="ebe14-141">UPDATE</span></span>  
<span data-ttu-id="ebe14-142">NSERIR</span><span class="sxs-lookup"><span data-stu-id="ebe14-142">INSERT</span></span>  
<span data-ttu-id="ebe14-143">REMOVER</span><span class="sxs-lookup"><span data-stu-id="ebe14-143">DELETE</span></span>  
<span data-ttu-id="ebe14-144">NOVAMENTE</span><span class="sxs-lookup"><span data-stu-id="ebe14-144">EXECUTE</span></span>  
<span data-ttu-id="ebe14-145">Recebi</span><span class="sxs-lookup"><span data-stu-id="ebe14-145">RECEIVE</span></span>  
<span data-ttu-id="ebe14-146">REFERÊNCIAS o formato geral para definir uma ação a ser auditada é: [ação] em [objeto] por [principal] Observe que [objeto] no formato acima pode se referir a um objeto, como uma tabela, um modo de exibição ou um procedimento armazenado ou um esquema ou banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="ebe14-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="ebe14-147">Para os últimos casos, o banco de dados de formulários:: [dbname] e esquema:: [SchemaName] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ebe14-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="ebe14-148">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ebe14-148">For example:</span></span>  
<span data-ttu-id="ebe14-149">SELECIONAR em dbo. myTable por público</span><span class="sxs-lookup"><span data-stu-id="ebe14-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="ebe14-150">SELECIONAR no banco de dados:: MyDatabase por público</span><span class="sxs-lookup"><span data-stu-id="ebe14-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="ebe14-151">SELECIONAR no esquema:: MySchema by Public</span><span class="sxs-lookup"><span data-stu-id="ebe14-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="ebe14-152">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="ebe14-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe14-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ebe14-153">-AuditActionGroup</span></span>
<span data-ttu-id="ebe14-154">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="ebe14-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="ebe14-155">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="ebe14-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="ebe14-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="ebe14-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="ebe14-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="ebe14-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="ebe14-158">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="ebe14-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="ebe14-159">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="ebe14-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="ebe14-160">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="ebe14-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="ebe14-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="ebe14-161">-BlobStorage</span></span>
<span data-ttu-id="ebe14-162">Especifica que o destino dos logs de auditoria é o armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="ebe14-162">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="ebe14-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ebe14-163">-DatabaseName</span></span>
<span data-ttu-id="ebe14-164">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ebe14-164">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe14-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebe14-165">-DefaultProfile</span></span>
<span data-ttu-id="ebe14-166">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ebe14-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebe14-167">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ebe14-167">-EventHub</span></span>
<span data-ttu-id="ebe14-168">Especifica que o destino dos logs de auditoria é o Hub de eventos</span><span class="sxs-lookup"><span data-stu-id="ebe14-168">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="ebe14-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe14-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="ebe14-170">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="ebe14-170">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="ebe14-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="ebe14-171">-EventHubName</span></span>
<span data-ttu-id="ebe14-172">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="ebe14-172">The name of the event hub.</span></span> <span data-ttu-id="ebe14-173">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o Hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="ebe14-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="ebe14-174">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebe14-174">-InputObject</span></span>
<span data-ttu-id="ebe14-175">O objeto de banco de dados para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ebe14-175">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebe14-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="ebe14-176">-LogAnalytics</span></span>
<span data-ttu-id="ebe14-177">Especifica que o destino dos logs de auditoria é análise de logs</span><span class="sxs-lookup"><span data-stu-id="ebe14-177">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="ebe14-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ebe14-178">-PassThru</span></span>
<span data-ttu-id="ebe14-179">Especifica se a política de auditoria deve ser impressa no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="ebe14-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="ebe14-180">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="ebe14-180">-PredicateExpression</span></span>
<span data-ttu-id="ebe14-181">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ebe14-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="ebe14-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebe14-182">-ResourceGroupName</span></span>
<span data-ttu-id="ebe14-183">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ebe14-183">The name of the resource group.</span></span>

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

### <span data-ttu-id="ebe14-184">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ebe14-184">-RetentionInDays</span></span>
<span data-ttu-id="ebe14-185">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ebe14-185">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="ebe14-186">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ebe14-186">-ServerName</span></span>
<span data-ttu-id="ebe14-187">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebe14-187">SQL server name.</span></span>

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

### <span data-ttu-id="ebe14-188">-Estado</span><span class="sxs-lookup"><span data-stu-id="ebe14-188">-State</span></span>
<span data-ttu-id="ebe14-189">O estado da política.</span><span class="sxs-lookup"><span data-stu-id="ebe14-189">The state of the policy.</span></span>

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

### <span data-ttu-id="ebe14-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ebe14-190">-StorageAccountName</span></span>
<span data-ttu-id="ebe14-191">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ebe14-191">The name of the storage account.</span></span>

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

### <span data-ttu-id="ebe14-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ebe14-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="ebe14-193">A ID da assinatura da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ebe14-193">The storage account subscription id</span></span>

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

### <span data-ttu-id="ebe14-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="ebe14-194">-StorageKeyType</span></span>
<span data-ttu-id="ebe14-195">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="ebe14-195">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="ebe14-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ebe14-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="ebe14-197">A ID do espaço de trabalho (ID do recurso de um espaço de trabalho de análise de log) para um espaço de trabalho de análise de log ao qual você gostaria de enviar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ebe14-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="ebe14-198">Exemplo:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="ebe14-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="ebe14-199">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ebe14-199">-Confirm</span></span>
<span data-ttu-id="ebe14-200">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebe14-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebe14-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebe14-201">-WhatIf</span></span>
<span data-ttu-id="ebe14-202">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebe14-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebe14-203">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebe14-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebe14-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebe14-204">CommonParameters</span></span>
<span data-ttu-id="ebe14-205">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebe14-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebe14-206">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebe14-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebe14-207">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ebe14-207">INPUTS</span></span>

### <span data-ttu-id="ebe14-208">System. String</span><span class="sxs-lookup"><span data-stu-id="ebe14-208">System.String</span></span>

### <span data-ttu-id="ebe14-209">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ebe14-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="ebe14-210">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="ebe14-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="ebe14-211">System. String []</span><span class="sxs-lookup"><span data-stu-id="ebe14-211">System.String[]</span></span>

### <span data-ttu-id="ebe14-212">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ebe14-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ebe14-213">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ebe14-213">System.Guid</span></span>

### <span data-ttu-id="ebe14-214">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ebe14-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ebe14-215">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ebe14-215">OUTPUTS</span></span>

### <span data-ttu-id="ebe14-216">Microsoft. Azure. Commands. Sql. Auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ebe14-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="ebe14-217">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ebe14-217">NOTES</span></span>

## <span data-ttu-id="ebe14-218">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebe14-218">RELATED LINKS</span></span>
