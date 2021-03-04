---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 6e3c5c935f6703f5c4f29b2a4ae793fc48e9b16f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890952"
---
# <span data-ttu-id="96e85-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="96e85-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="96e85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96e85-102">SYNOPSIS</span></span>
<span data-ttu-id="96e85-103">Altera as configurações de auditoria para um banco de dados SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="96e85-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="96e85-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="96e85-104">SYNTAX</span></span>

### <span data-ttu-id="96e85-105">DatabaseParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="96e85-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e85-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e85-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e85-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="96e85-107">DESCRIPTION</span></span>
<span data-ttu-id="96e85-108">O cmdlet **Set-AzSqlDatabaseAudit** altera as configurações de auditoria de um banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="96e85-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="96e85-109">Para usar o cmdlet, use os *parâmetros ResourceGroupName,* *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="96e85-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="96e85-110">Quando o armazenamento de blob é um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento dos logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="96e85-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="96e85-111">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="96e85-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96e85-112">EXAMPLES</span></span>

### <span data-ttu-id="96e85-113">Exemplo 1: Habilitar a política de auditoria de armazenamento de blob de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96e85-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="96e85-114">Exemplo 2: desabilitar a política de auditoria de armazenamento de blob de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96e85-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="96e85-115">Exemplo 3: Habilitar a política de auditoria de armazenamento de blob de um banco de dados do Azure SQL com filtragem usando um predicado T-SQL</span><span class="sxs-lookup"><span data-stu-id="96e85-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="96e85-116">Exemplo 4: Remover a filtragem da política de auditoria de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96e85-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="96e85-117">Exemplo 5: Habilitar a política de auditoria do hub de eventos de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96e85-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="96e85-118">Exemplo 6: desabilitar a política de auditoria do hub de eventos de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96e85-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="96e85-119">Exemplo 7: Habilitar a política de auditoria de análise de log de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96e85-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="96e85-120">Exemplo 8: Desabilitar a política de auditoria de análise de log de um banco de dados SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96e85-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="96e85-121">Exemplo 9: Desabilitar, por meio de pipeline, a política de auditoria de análise de log de um banco de dados do Azure SQL banco de dados</span><span class="sxs-lookup"><span data-stu-id="96e85-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="96e85-122">Exemplo 10: desabilite o envio de registros de auditoria de um banco de dados do Azure SQL blob storage e habilita o envio para análise de log.</span><span class="sxs-lookup"><span data-stu-id="96e85-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="96e85-123">Exemplo 11: Habilitar o envio de registros de auditoria de um banco de dados do Azure SQL blob storage, event hub e log analytics.</span><span class="sxs-lookup"><span data-stu-id="96e85-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="96e85-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="96e85-124">PARAMETERS</span></span>

### <span data-ttu-id="96e85-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="96e85-125">-AuditAction</span></span>
<span data-ttu-id="96e85-126">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-126">The set of audit actions.</span></span>  
<span data-ttu-id="96e85-127">As ações com suporte para auditoria são:</span><span class="sxs-lookup"><span data-stu-id="96e85-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="96e85-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="96e85-128">SELECT</span></span>  
<span data-ttu-id="96e85-129">UPDATE</span><span class="sxs-lookup"><span data-stu-id="96e85-129">UPDATE</span></span>  
<span data-ttu-id="96e85-130">INSERT</span><span class="sxs-lookup"><span data-stu-id="96e85-130">INSERT</span></span>  
<span data-ttu-id="96e85-131">DELETE</span><span class="sxs-lookup"><span data-stu-id="96e85-131">DELETE</span></span>  
<span data-ttu-id="96e85-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="96e85-132">EXECUTE</span></span>  
<span data-ttu-id="96e85-133">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="96e85-133">RECEIVE</span></span>  
<span data-ttu-id="96e85-134">REFERÊNCIAS</span><span class="sxs-lookup"><span data-stu-id="96e85-134">REFERENCES</span></span>  
<span data-ttu-id="96e85-135">O formulário geral para definir uma ação a ser auditada é: [action] ON [object] BY [principal] Observe que [objeto] no formato acima pode se referir a um objeto como uma tabela, modo de exibição ou procedimento armazenado, ou um banco de dados ou esquema inteiro.</span><span class="sxs-lookup"><span data-stu-id="96e85-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="96e85-136">Para os últimos casos, os formulários DATABASE:::[dbname] e SCHEMA:::[schemaname] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="96e85-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="96e85-137">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="96e85-137">For example:</span></span>  
<span data-ttu-id="96e85-138">SELECT em dbo.myTable por público</span><span class="sxs-lookup"><span data-stu-id="96e85-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="96e85-139">SELECT on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="96e85-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="96e85-140">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="96e85-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="96e85-141">Para obter mais informações, consulte https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="96e85-141">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="96e85-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="96e85-142">-AuditActionGroup</span></span>
<span data-ttu-id="96e85-143">O conjunto recomendado de grupos de ações a ser usado é a seguinte combinação : isso audita todas as consultas e procedimentos armazenados executados no banco de dados, bem como logons bem-sucedidos e com falha:</span><span class="sxs-lookup"><span data-stu-id="96e85-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="96e85-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="96e85-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="96e85-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="96e85-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="96e85-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="96e85-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="96e85-147">Essa combinação acima também é o conjunto configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="96e85-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="96e85-148">Esses grupos abrangem todas as SQL e procedimentos armazenados executados no banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="96e85-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="96e85-149">Para obter mais informações, consulte https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="96e85-149">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="96e85-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="96e85-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="96e85-151">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-151">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="96e85-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96e85-152">-DatabaseName</span></span>
<span data-ttu-id="96e85-153">SQL Nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="96e85-153">SQL Database name.</span></span>

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

### <span data-ttu-id="96e85-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="96e85-154">-DatabaseObject</span></span>
<span data-ttu-id="96e85-155">O objeto database para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-155">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="96e85-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e85-156">-DefaultProfile</span></span>
<span data-ttu-id="96e85-157">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96e85-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96e85-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="96e85-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="96e85-159">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="96e85-159">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="96e85-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="96e85-160">-EventHubName</span></span>
<span data-ttu-id="96e85-161">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="96e85-161">The name of the event hub.</span></span> <span data-ttu-id="96e85-162">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="96e85-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="96e85-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="96e85-163">-EventHubTargetState</span></span>
<span data-ttu-id="96e85-164">Indica se o hub de eventos é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-164">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="96e85-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="96e85-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="96e85-166">Indica se a análise de log é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-166">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="96e85-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96e85-167">-PassThru</span></span>
<span data-ttu-id="96e85-168">Especifica se a política de auditoria deve ser saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="96e85-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="96e85-169">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="96e85-169">-PredicateExpression</span></span>
<span data-ttu-id="96e85-170">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="96e85-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e85-171">-ResourceGroupName</span></span>
<span data-ttu-id="96e85-172">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96e85-172">The name of the resource group.</span></span>

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

### <span data-ttu-id="96e85-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="96e85-173">-RetentionInDays</span></span>
<span data-ttu-id="96e85-174">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-174">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="96e85-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96e85-175">-ServerName</span></span>
<span data-ttu-id="96e85-176">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="96e85-176">SQL server name.</span></span>

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

### <span data-ttu-id="96e85-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="96e85-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="96e85-178">A ID do recurso de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="96e85-178">The storage account resource id</span></span>

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

### <span data-ttu-id="96e85-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="96e85-179">-StorageKeyType</span></span>
<span data-ttu-id="96e85-180">Especifica qual das teclas de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="96e85-180">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="96e85-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="96e85-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="96e85-182">A ID do espaço de trabalho (ID de recurso de um espaço de trabalho do Log Analytics) para um espaço de trabalho do Log Analytics para o qual você gostaria de enviar Logs de Auditoria.</span><span class="sxs-lookup"><span data-stu-id="96e85-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="96e85-183">Exemplo: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="96e85-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="96e85-184">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96e85-184">-Confirm</span></span>
<span data-ttu-id="96e85-185">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96e85-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e85-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e85-186">-WhatIf</span></span>
<span data-ttu-id="96e85-187">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="96e85-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96e85-188">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="96e85-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e85-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e85-189">CommonParameters</span></span>
<span data-ttu-id="96e85-190">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e85-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e85-191">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96e85-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e85-192">INPUTS</span><span class="sxs-lookup"><span data-stu-id="96e85-192">INPUTS</span></span>

### <span data-ttu-id="96e85-193">System.String</span><span class="sxs-lookup"><span data-stu-id="96e85-193">System.String</span></span>

### <span data-ttu-id="96e85-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="96e85-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="96e85-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="96e85-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="96e85-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="96e85-196">System.String[]</span></span>

### <span data-ttu-id="96e85-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="96e85-197">System.Guid</span></span>

### <span data-ttu-id="96e85-198">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96e85-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96e85-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="96e85-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="96e85-200">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="96e85-200">OUTPUTS</span></span>

### <span data-ttu-id="96e85-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="96e85-201">System.Boolean</span></span>

## <span data-ttu-id="96e85-202">NOTES</span><span class="sxs-lookup"><span data-stu-id="96e85-202">NOTES</span></span>

## <span data-ttu-id="96e85-203">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96e85-203">RELATED LINKS</span></span>
