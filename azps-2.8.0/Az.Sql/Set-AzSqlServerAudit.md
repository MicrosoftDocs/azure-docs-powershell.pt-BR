---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8601be969ce08c86a723af51e82be89125367d4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773699"
---
# <span data-ttu-id="01fbf-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="01fbf-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="01fbf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="01fbf-102">SYNOPSIS</span></span>
<span data-ttu-id="01fbf-103">Altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="01fbf-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="01fbf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01fbf-104">SYNTAX</span></span>

### <span data-ttu-id="01fbf-105">ServerParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="01fbf-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01fbf-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01fbf-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01fbf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="01fbf-107">DESCRIPTION</span></span>
<span data-ttu-id="01fbf-108">O cmdlet **set-AzSqlServerAudit** altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="01fbf-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="01fbf-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="01fbf-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="01fbf-110">Quando o armazenamento de blob for um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="01fbf-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="01fbf-111">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="01fbf-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="01fbf-112">EXAMPLES</span></span>

### <span data-ttu-id="01fbf-113">Exemplo 1: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="01fbf-114">Exemplo 2: desabilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="01fbf-115">Exemplo 3,1: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure com filtragem avançada usando um predicado T-SQL</span><span class="sxs-lookup"><span data-stu-id="01fbf-115">Example 3.1: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="01fbf-116">Exemplo 3,2: remover a configuração de filtragem avançada da política de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-116">Example 3.2: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="01fbf-117">Exemplo 4: habilitar a política de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-117">Example 4: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="01fbf-118">Exemplo 5: desabilitar a política de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-118">Example 5: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="01fbf-119">Exemplo 6: habilitar a política de auditoria de análise de logs de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-119">Example 6: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="01fbf-120">Exemplo 7: desabilitar a política de auditoria de análise de logs de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-120">Example 7: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="01fbf-121">Exemplo 8: desabilitar, por meio de pipeline, a política de auditoria de análise de logs de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="01fbf-121">Example 8: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="01fbf-122">Exemplo 9: desabilitar o envio de registros de auditoria de um SQL Server do Azure para o armazenamento de BLOB e habilitar o envio para a análise de logs.</span><span class="sxs-lookup"><span data-stu-id="01fbf-122">Example 9: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="01fbf-123">Exemplo 10: habilitar o envio de registros de auditoria de um SQL Server do Azure para o armazenamento de BLOB, o Hub de eventos e a análise de logs.</span><span class="sxs-lookup"><span data-stu-id="01fbf-123">Example 10: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="01fbf-124">OS</span><span class="sxs-lookup"><span data-stu-id="01fbf-124">PARAMETERS</span></span>

### <span data-ttu-id="01fbf-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01fbf-125">-AsJob</span></span>
<span data-ttu-id="01fbf-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="01fbf-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01fbf-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="01fbf-127">-AuditActionGroup</span></span>
<span data-ttu-id="01fbf-128">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="01fbf-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="01fbf-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="01fbf-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="01fbf-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="01fbf-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="01fbf-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="01fbf-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="01fbf-132">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="01fbf-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="01fbf-133">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="01fbf-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="01fbf-134">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="01fbf-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="01fbf-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="01fbf-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="01fbf-136">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="01fbf-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01fbf-137">-DefaultProfile</span></span>
<span data-ttu-id="01fbf-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="01fbf-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01fbf-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="01fbf-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="01fbf-140">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="01fbf-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="01fbf-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="01fbf-141">-EventHubName</span></span>
<span data-ttu-id="01fbf-142">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="01fbf-142">The name of the event hub.</span></span> <span data-ttu-id="01fbf-143">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o Hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="01fbf-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="01fbf-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="01fbf-144">-EventHubTargetState</span></span>
<span data-ttu-id="01fbf-145">Indica se o Hub de eventos é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="01fbf-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="01fbf-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="01fbf-147">Indica se a análise de log é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="01fbf-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01fbf-148">-PassThru</span></span>
<span data-ttu-id="01fbf-149">Especifica se a política de auditoria deve ser impressa no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="01fbf-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="01fbf-150">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="01fbf-150">-PredicateExpression</span></span>
<span data-ttu-id="01fbf-151">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="01fbf-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01fbf-152">-ResourceGroupName</span></span>
<span data-ttu-id="01fbf-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="01fbf-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fbf-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="01fbf-154">-RetentionInDays</span></span>
<span data-ttu-id="01fbf-155">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="01fbf-156">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="01fbf-156">-ServerName</span></span>
<span data-ttu-id="01fbf-157">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="01fbf-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01fbf-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="01fbf-158">-ServerObject</span></span>
<span data-ttu-id="01fbf-159">O objeto do servidor para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01fbf-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="01fbf-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="01fbf-161">A ID do recurso da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="01fbf-161">The storage account resource id</span></span>

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

### <span data-ttu-id="01fbf-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="01fbf-162">-StorageKeyType</span></span>
<span data-ttu-id="01fbf-163">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="01fbf-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="01fbf-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="01fbf-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="01fbf-165">A ID do espaço de trabalho (ID do recurso de um espaço de trabalho de análise de log) para um espaço de trabalho de análise de log ao qual você gostaria de enviar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="01fbf-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="01fbf-166">Exemplo:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="01fbf-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="01fbf-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="01fbf-167">-Confirm</span></span>
<span data-ttu-id="01fbf-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01fbf-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01fbf-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01fbf-169">-WhatIf</span></span>
<span data-ttu-id="01fbf-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="01fbf-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01fbf-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="01fbf-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01fbf-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fbf-172">CommonParameters</span></span>
<span data-ttu-id="01fbf-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01fbf-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fbf-174">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01fbf-174">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fbf-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="01fbf-175">INPUTS</span></span>

### <span data-ttu-id="01fbf-176">System. String</span><span class="sxs-lookup"><span data-stu-id="01fbf-176">System.String</span></span>

### <span data-ttu-id="01fbf-177">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="01fbf-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="01fbf-178">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="01fbf-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="01fbf-179">System. GUID</span><span class="sxs-lookup"><span data-stu-id="01fbf-179">System.Guid</span></span>

### <span data-ttu-id="01fbf-180">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="01fbf-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="01fbf-181">Microsoft. Azure. Commands. Sql. Auditing. Model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="01fbf-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="01fbf-182">EXIBE</span><span class="sxs-lookup"><span data-stu-id="01fbf-182">OUTPUTS</span></span>

### <span data-ttu-id="01fbf-183">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01fbf-183">System.Boolean</span></span>

## <span data-ttu-id="01fbf-184">INFORMA</span><span class="sxs-lookup"><span data-stu-id="01fbf-184">NOTES</span></span>

## <span data-ttu-id="01fbf-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="01fbf-185">RELATED LINKS</span></span>