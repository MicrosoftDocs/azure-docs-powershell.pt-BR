---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: e13e97bd9f636de68344f83b600e440252431a22
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954568"
---
# <span data-ttu-id="34742-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="34742-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="34742-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34742-102">SYNOPSIS</span></span>
<span data-ttu-id="34742-103">Altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="34742-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="34742-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34742-104">SYNTAX</span></span>

### <span data-ttu-id="34742-105">DatabaseParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="34742-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34742-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34742-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34742-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34742-107">DESCRIPTION</span></span>
<span data-ttu-id="34742-108">O cmdlet **set-AzSqlDatabaseAudit** altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="34742-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="34742-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="34742-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="34742-110">Quando o armazenamento de blob for um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="34742-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="34742-111">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="34742-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34742-112">EXAMPLES</span></span>

### <span data-ttu-id="34742-113">Exemplo 1: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="34742-114">Exemplo 2: desabilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="34742-115">Exemplo 3: habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL do Azure com filtragem avançada usando um predicado T-SQL</span><span class="sxs-lookup"><span data-stu-id="34742-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="34742-116">Exemplo 4: remover a configuração de filtragem avançada da política de auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="34742-117">Exemplo 5: habilitar a política de auditoria do hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="34742-118">Exemplo 6: desabilitar a política de auditoria do hub de eventos de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="34742-119">Exemplo 7: habilitar a política de auditoria de análise de log de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="34742-120">Exemplo 8: desabilitar a política de auditoria de análise de log de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="34742-121">Exemplo 9: desabilitar, por meio de pipeline, a política de auditoria de análise de logs de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="34742-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="34742-122">Exemplo 10: desabilitar o envio de registros de auditoria de um banco de dados SQL do Azure para o armazenamento de BLOB e habilitar o envio para a análise de logs.</span><span class="sxs-lookup"><span data-stu-id="34742-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="34742-123">Exemplo 11: habilitar o envio de registros de auditoria de um banco de dados SQL do Azure para o armazenamento de BLOB, o Hub de eventos e a análise de logs.</span><span class="sxs-lookup"><span data-stu-id="34742-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="34742-124">OS</span><span class="sxs-lookup"><span data-stu-id="34742-124">PARAMETERS</span></span>

### <span data-ttu-id="34742-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="34742-125">-AuditAction</span></span>
<span data-ttu-id="34742-126">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-126">The set of audit actions.</span></span>  
<span data-ttu-id="34742-127">As ações com suporte para auditoria são:</span><span class="sxs-lookup"><span data-stu-id="34742-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="34742-128">SELECIONADA</span><span class="sxs-lookup"><span data-stu-id="34742-128">SELECT</span></span>  
<span data-ttu-id="34742-129">ATUALIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="34742-129">UPDATE</span></span>  
<span data-ttu-id="34742-130">NSERIR</span><span class="sxs-lookup"><span data-stu-id="34742-130">INSERT</span></span>  
<span data-ttu-id="34742-131">REMOVER</span><span class="sxs-lookup"><span data-stu-id="34742-131">DELETE</span></span>  
<span data-ttu-id="34742-132">NOVAMENTE</span><span class="sxs-lookup"><span data-stu-id="34742-132">EXECUTE</span></span>  
<span data-ttu-id="34742-133">Recebi</span><span class="sxs-lookup"><span data-stu-id="34742-133">RECEIVE</span></span>  
<span data-ttu-id="34742-134">REFERE</span><span class="sxs-lookup"><span data-stu-id="34742-134">REFERENCES</span></span>  
<span data-ttu-id="34742-135">A forma geral para definir uma ação a ser auditada é: [ação] em [objeto] por [entidade] Observe que [objeto] no formato acima pode se referir a um objeto, como uma tabela, um modo de exibição ou um procedimento armazenado ou um esquema ou banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="34742-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="34742-136">Para os últimos casos, o banco de dados de formulários:: [dbname] e esquema:: [SchemaName] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="34742-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="34742-137">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="34742-137">For example:</span></span>  
<span data-ttu-id="34742-138">SELECIONAR em dbo. myTable por público</span><span class="sxs-lookup"><span data-stu-id="34742-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="34742-139">SELECIONAR no banco de dados:: MyDatabase por público</span><span class="sxs-lookup"><span data-stu-id="34742-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="34742-140">SELECIONAR no esquema:: MySchema by Public</span><span class="sxs-lookup"><span data-stu-id="34742-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="34742-141">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="34742-141">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="34742-142">-AuditActionGroup</span></span>
<span data-ttu-id="34742-143">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="34742-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="34742-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="34742-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="34742-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="34742-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="34742-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="34742-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="34742-147">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="34742-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="34742-148">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="34742-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="34742-149">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="34742-149">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="34742-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="34742-151">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34742-152">-DatabaseName</span></span>
<span data-ttu-id="34742-153">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="34742-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-154">-Databaseobject</span><span class="sxs-lookup"><span data-stu-id="34742-154">-DatabaseObject</span></span>
<span data-ttu-id="34742-155">O objeto de banco de dados para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34742-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34742-156">-DefaultProfile</span></span>
<span data-ttu-id="34742-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34742-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34742-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="34742-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="34742-159">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="34742-159">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="34742-160">-EventHubName</span></span>
<span data-ttu-id="34742-161">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="34742-161">The name of the event hub.</span></span> <span data-ttu-id="34742-162">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o Hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="34742-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="34742-163">-EventHubTargetState</span></span>
<span data-ttu-id="34742-164">Indica se o Hub de eventos é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="34742-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="34742-166">Indica se a análise de log é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34742-167">-PassThru</span></span>
<span data-ttu-id="34742-168">Especifica se a política de auditoria deve ser impressa no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="34742-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="34742-169">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="34742-169">-PredicateExpression</span></span>
<span data-ttu-id="34742-170">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34742-171">-ResourceGroupName</span></span>
<span data-ttu-id="34742-172">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="34742-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="34742-173">-RetentionInDays</span></span>
<span data-ttu-id="34742-174">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-175">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="34742-175">-ServerName</span></span>
<span data-ttu-id="34742-176">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="34742-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="34742-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="34742-178">A ID do recurso da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="34742-178">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="34742-179">-StorageKeyType</span></span>
<span data-ttu-id="34742-180">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="34742-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="34742-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="34742-182">A ID do espaço de trabalho (ID do recurso de um espaço de trabalho de análise de log) para um espaço de trabalho de análise de log ao qual você gostaria de enviar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="34742-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="34742-183">Exemplo:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="34742-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34742-184">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34742-184">-Confirm</span></span>
<span data-ttu-id="34742-185">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34742-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34742-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34742-186">-WhatIf</span></span>
<span data-ttu-id="34742-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34742-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34742-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34742-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34742-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34742-189">CommonParameters</span></span>
<span data-ttu-id="34742-190">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34742-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34742-191">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34742-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34742-192">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34742-192">INPUTS</span></span>

### <span data-ttu-id="34742-193">System. String</span><span class="sxs-lookup"><span data-stu-id="34742-193">System.String</span></span>

### <span data-ttu-id="34742-194">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="34742-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="34742-195">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="34742-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="34742-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="34742-196">System.String[]</span></span>

### <span data-ttu-id="34742-197">System. GUID</span><span class="sxs-lookup"><span data-stu-id="34742-197">System.Guid</span></span>

### <span data-ttu-id="34742-198">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="34742-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="34742-199">Microsoft. Azure. Commands. Sql. Auditing. Model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="34742-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="34742-200">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34742-200">OUTPUTS</span></span>

### <span data-ttu-id="34742-201">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34742-201">System.Boolean</span></span>

## <span data-ttu-id="34742-202">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34742-202">NOTES</span></span>

## <span data-ttu-id="34742-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34742-203">RELATED LINKS</span></span>
