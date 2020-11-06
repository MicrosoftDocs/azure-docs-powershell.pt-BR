---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 511207be4094dae96f8d138124021ce2f8ed3913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598803"
---
# <span data-ttu-id="f9988-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="f9988-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="f9988-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9988-102">SYNOPSIS</span></span>
<span data-ttu-id="f9988-103">Altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9988-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="f9988-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9988-104">SYNTAX</span></span>

### <span data-ttu-id="f9988-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9988-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9988-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="f9988-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9988-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="f9988-107">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9988-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="f9988-108">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9988-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f9988-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9988-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f9988-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9988-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f9988-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9988-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="f9988-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9988-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9988-113">DESCRIPTION</span></span>
<span data-ttu-id="f9988-114">O cmdlet **set-AzSqlDatabaseAuditing** altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9988-114">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="f9988-115">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9988-115">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f9988-116">O destino dos logs de auditoria é determinado especificando um dos seguintes parâmetros de switch: BlobStorage, LogAnalytics ou EventHub (se nenhum for especificado, o padrão será BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="f9988-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="f9988-117">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="f9988-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="f9988-118">Quando o destino de logs de auditoria for armazenamento de BLOBs, especifique o parâmetro *StorageAccountName* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f9988-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="f9988-119">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f9988-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="f9988-120">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve as configurações atuais de auditoria, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9988-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="f9988-121">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="f9988-121">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="f9988-122">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9988-122">EXAMPLES</span></span>

### <span data-ttu-id="f9988-123">Exemplo 1: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-123">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="f9988-124">Exemplo 2: desabilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-124">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="f9988-125">Exemplo 3: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure usando uma conta de armazenamento de uma assinatura diferente</span><span class="sxs-lookup"><span data-stu-id="f9988-125">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="f9988-126">Exemplo 4: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure com filtragem avançada usando um predicado T-SQL</span><span class="sxs-lookup"><span data-stu-id="f9988-126">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="f9988-127">Exemplo 5: remover a configuração de filtragem avançada da política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-127">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="f9988-128">Exemplo 6: habilitar a política de auditoria do hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-128">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="f9988-129">Exemplo 7: desabilitar a política de auditoria do hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-129">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="f9988-130">Exemplo 8: habilitar a política de auditoria de análise de log de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-130">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="f9988-131">Exemplo 9: desabilitar a política de auditoria de análise de log de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-131">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="f9988-132">Exemplo 10: desabilitar, por meio de pipeline, a política de auditoria de análise de logs de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="f9988-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="f9988-133">OS</span><span class="sxs-lookup"><span data-stu-id="f9988-133">PARAMETERS</span></span>

### <span data-ttu-id="f9988-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9988-134">-AsJob</span></span>
<span data-ttu-id="f9988-135">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f9988-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9988-136">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="f9988-136">-AuditAction</span></span>
<span data-ttu-id="f9988-137">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f9988-137">The set of audit actions.</span></span>  
<span data-ttu-id="f9988-138">As ações com suporte para auditoria são:</span><span class="sxs-lookup"><span data-stu-id="f9988-138">The supported actions to audit are:</span></span>  
<span data-ttu-id="f9988-139">SELECIONADA</span><span class="sxs-lookup"><span data-stu-id="f9988-139">SELECT</span></span>  
<span data-ttu-id="f9988-140">ATUALIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="f9988-140">UPDATE</span></span>  
<span data-ttu-id="f9988-141">NSERIR</span><span class="sxs-lookup"><span data-stu-id="f9988-141">INSERT</span></span>  
<span data-ttu-id="f9988-142">REMOVER</span><span class="sxs-lookup"><span data-stu-id="f9988-142">DELETE</span></span>  
<span data-ttu-id="f9988-143">NOVAMENTE</span><span class="sxs-lookup"><span data-stu-id="f9988-143">EXECUTE</span></span>  
<span data-ttu-id="f9988-144">Recebi</span><span class="sxs-lookup"><span data-stu-id="f9988-144">RECEIVE</span></span>  
<span data-ttu-id="f9988-145">REFERÊNCIAS o formato geral para definir uma ação a ser auditada é: [ação] em [objeto] por [principal] Observe que [objeto] no formato acima pode se referir a um objeto, como uma tabela, um modo de exibição ou um procedimento armazenado ou um esquema ou banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="f9988-145">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="f9988-146">Para os últimos casos, o banco de dados de formulários:: [dbname] e esquema:: [SchemaName] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f9988-146">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="f9988-147">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f9988-147">For example:</span></span>  
<span data-ttu-id="f9988-148">SELECIONAR em dbo. myTable por público</span><span class="sxs-lookup"><span data-stu-id="f9988-148">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="f9988-149">SELECIONAR no banco de dados:: MyDatabase por público</span><span class="sxs-lookup"><span data-stu-id="f9988-149">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="f9988-150">SELECIONAR no esquema:: MySchema by Public</span><span class="sxs-lookup"><span data-stu-id="f9988-150">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="f9988-151">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="f9988-151">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="f9988-152">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f9988-152">-AuditActionGroup</span></span>
<span data-ttu-id="f9988-153">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="f9988-153">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="f9988-154">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f9988-154">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="f9988-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f9988-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="f9988-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="f9988-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="f9988-157">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="f9988-157">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="f9988-158">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="f9988-158">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="f9988-159">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="f9988-159">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="f9988-160">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="f9988-160">-BlobStorage</span></span>
<span data-ttu-id="f9988-161">Especifica que o destino dos logs de auditoria é o armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="f9988-161">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="f9988-162">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9988-162">-DatabaseName</span></span>
<span data-ttu-id="f9988-163">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="f9988-163">SQL Database name.</span></span>

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

### <span data-ttu-id="f9988-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9988-164">-DefaultProfile</span></span>
<span data-ttu-id="f9988-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9988-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9988-166">-EventHub</span><span class="sxs-lookup"><span data-stu-id="f9988-166">-EventHub</span></span>
<span data-ttu-id="f9988-167">Especifica que o destino dos logs de auditoria é o Hub de eventos</span><span class="sxs-lookup"><span data-stu-id="f9988-167">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="f9988-168">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="f9988-168">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="f9988-169">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="f9988-169">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="f9988-170">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="f9988-170">-EventHubName</span></span>
<span data-ttu-id="f9988-171">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="f9988-171">The name of the event hub.</span></span> <span data-ttu-id="f9988-172">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o Hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="f9988-172">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="f9988-173">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9988-173">-InputObject</span></span>
<span data-ttu-id="f9988-174">O objeto de banco de dados para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f9988-174">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="f9988-175">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="f9988-175">-LogAnalytics</span></span>
<span data-ttu-id="f9988-176">Especifica que o destino dos logs de auditoria é análise de logs</span><span class="sxs-lookup"><span data-stu-id="f9988-176">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="f9988-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9988-177">-PassThru</span></span>
<span data-ttu-id="f9988-178">Especifica se a política de auditoria deve ser impressa no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="f9988-178">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="f9988-179">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="f9988-179">-PredicateExpression</span></span>
<span data-ttu-id="f9988-180">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f9988-180">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="f9988-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9988-181">-ResourceGroupName</span></span>
<span data-ttu-id="f9988-182">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f9988-182">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9988-183">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f9988-183">-RetentionInDays</span></span>
<span data-ttu-id="f9988-184">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f9988-184">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="f9988-185">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f9988-185">-ServerName</span></span>
<span data-ttu-id="f9988-186">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f9988-186">SQL server name.</span></span>

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

### <span data-ttu-id="f9988-187">-Estado</span><span class="sxs-lookup"><span data-stu-id="f9988-187">-State</span></span>
<span data-ttu-id="f9988-188">O estado da política.</span><span class="sxs-lookup"><span data-stu-id="f9988-188">The state of the policy.</span></span>

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

### <span data-ttu-id="f9988-189">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f9988-189">-StorageAccountName</span></span>
<span data-ttu-id="f9988-190">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f9988-190">The name of the storage account.</span></span>

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

### <span data-ttu-id="f9988-191">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9988-191">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="f9988-192">A ID da assinatura da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f9988-192">The storage account subscription id</span></span>

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

### <span data-ttu-id="f9988-193">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f9988-193">-StorageKeyType</span></span>
<span data-ttu-id="f9988-194">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="f9988-194">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="f9988-195">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="f9988-195">-WorkspaceResourceId</span></span>
<span data-ttu-id="f9988-196">A ID do espaço de trabalho (ID do recurso de um espaço de trabalho de análise de log) para um espaço de trabalho de análise de log ao qual você gostaria de enviar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="f9988-196">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="f9988-197">Exemplo:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="f9988-197">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="f9988-198">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9988-198">-Confirm</span></span>
<span data-ttu-id="f9988-199">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9988-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9988-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9988-200">-WhatIf</span></span>
<span data-ttu-id="f9988-201">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9988-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9988-202">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9988-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9988-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9988-203">CommonParameters</span></span>
<span data-ttu-id="f9988-204">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9988-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9988-205">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9988-205">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9988-206">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9988-206">INPUTS</span></span>

### <span data-ttu-id="f9988-207">System. String</span><span class="sxs-lookup"><span data-stu-id="f9988-207">System.String</span></span>

### <span data-ttu-id="f9988-208">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f9988-208">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="f9988-209">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="f9988-209">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="f9988-210">System. String []</span><span class="sxs-lookup"><span data-stu-id="f9988-210">System.String[]</span></span>

### <span data-ttu-id="f9988-211">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9988-211">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f9988-212">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f9988-212">System.Guid</span></span>

### <span data-ttu-id="f9988-213">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f9988-213">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f9988-214">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9988-214">OUTPUTS</span></span>

### <span data-ttu-id="f9988-215">Microsoft. Azure. Commands. Sql. Auditing. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="f9988-215">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="f9988-216">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9988-216">NOTES</span></span>

## <span data-ttu-id="f9988-217">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9988-217">RELATED LINKS</span></span>
