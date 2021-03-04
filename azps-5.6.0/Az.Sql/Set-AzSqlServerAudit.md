---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: 8b0312ddcdce5c538b80f0245470496c534bf07f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890697"
---
# <span data-ttu-id="595ed-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="595ed-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="595ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595ed-102">SYNOPSIS</span></span>
<span data-ttu-id="595ed-103">Altera as configurações de auditoria de um servidor SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="595ed-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="595ed-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="595ed-104">SYNTAX</span></span>

### <span data-ttu-id="595ed-105">ServerParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="595ed-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="595ed-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="595ed-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="595ed-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="595ed-107">DESCRIPTION</span></span>
<span data-ttu-id="595ed-108">O cmdlet **Set-AzSqlServerAudit** altera as configurações de auditoria de um servidor SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="595ed-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="595ed-109">Para usar o cmdlet, use os *parâmetros ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="595ed-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="595ed-110">Quando o armazenamento de blob é um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento dos logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="595ed-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="595ed-111">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="595ed-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="595ed-112">EXAMPLES</span></span>

### <span data-ttu-id="595ed-113">Exemplo 1: Habilitar a política de auditoria de armazenamento de blob de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="595ed-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="595ed-114">Exemplo 2: Desabilitar a política de auditoria de armazenamento de blob de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="595ed-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="595ed-115">Exemplo 3: Habilitar a política de auditoria de armazenamento de blob de um servidor do Azure SQL com filtragem avançada usando um predicado T-SQL</span><span class="sxs-lookup"><span data-stu-id="595ed-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="595ed-116">Exemplo 4: Remover a configuração de filtragem avançada da política de auditoria de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="595ed-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="595ed-117">Exemplo 5: Habilitar a política de auditoria do hub de eventos de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="595ed-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="595ed-118">Exemplo 6: desabilitar a política de auditoria do hub de eventos de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="595ed-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="595ed-119">Exemplo 7: Habilitar a política de auditoria de análise de log de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="595ed-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="595ed-120">Exemplo 8: desabilitar a política de auditoria de análise de log de um servidor SQL Azure</span><span class="sxs-lookup"><span data-stu-id="595ed-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="595ed-121">Exemplo 9: Desabilitar, por meio de pipeline, a política de auditoria de análise de log de um servidor do Azure SQL servidor</span><span class="sxs-lookup"><span data-stu-id="595ed-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="595ed-122">Exemplo 10: desabilitar o envio de registros de auditoria de um servidor do Azure SQL blob storage e permitir enviá-los para análise de log.</span><span class="sxs-lookup"><span data-stu-id="595ed-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="595ed-123">Exemplo 11: Habilitar o envio de registros de auditoria de um servidor do Azure SQL blob storage, event hub e log analytics.</span><span class="sxs-lookup"><span data-stu-id="595ed-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="595ed-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="595ed-124">PARAMETERS</span></span>

### <span data-ttu-id="595ed-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="595ed-125">-AsJob</span></span>
<span data-ttu-id="595ed-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="595ed-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="595ed-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="595ed-127">-AuditActionGroup</span></span>
<span data-ttu-id="595ed-128">O conjunto recomendado de grupos de ações a ser usado é a seguinte combinação : isso audita todas as consultas e procedimentos armazenados executados no banco de dados, bem como logons bem-sucedidos e com falha:</span><span class="sxs-lookup"><span data-stu-id="595ed-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="595ed-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="595ed-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="595ed-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="595ed-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="595ed-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="595ed-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="595ed-132">Essa combinação acima também é o conjunto configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="595ed-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="595ed-133">Esses grupos abrangem todas as SQL e procedimentos armazenados executados no banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="595ed-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="595ed-134">Para obter mais informações, consulte https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="595ed-134">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="595ed-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="595ed-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="595ed-136">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="595ed-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595ed-137">-DefaultProfile</span></span>
<span data-ttu-id="595ed-138">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="595ed-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="595ed-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="595ed-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="595ed-140">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="595ed-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="595ed-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="595ed-141">-EventHubName</span></span>
<span data-ttu-id="595ed-142">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="595ed-142">The name of the event hub.</span></span> <span data-ttu-id="595ed-143">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="595ed-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="595ed-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="595ed-144">-EventHubTargetState</span></span>
<span data-ttu-id="595ed-145">Indica se o hub de eventos é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="595ed-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="595ed-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="595ed-147">Indica se a análise de log é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="595ed-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="595ed-148">-PassThru</span></span>
<span data-ttu-id="595ed-149">Especifica se a política de auditoria deve ser saída no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="595ed-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="595ed-150">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="595ed-150">-PredicateExpression</span></span>
<span data-ttu-id="595ed-151">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="595ed-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595ed-152">-ResourceGroupName</span></span>
<span data-ttu-id="595ed-153">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="595ed-153">The name of the resource group.</span></span>

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

### <span data-ttu-id="595ed-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="595ed-154">-RetentionInDays</span></span>
<span data-ttu-id="595ed-155">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="595ed-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="595ed-156">-ServerName</span></span>
<span data-ttu-id="595ed-157">SQL nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="595ed-157">SQL server name.</span></span>

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

### <span data-ttu-id="595ed-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="595ed-158">-ServerObject</span></span>
<span data-ttu-id="595ed-159">O objeto server para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-159">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="595ed-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="595ed-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="595ed-161">A ID do recurso de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="595ed-161">The storage account resource id</span></span>

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

### <span data-ttu-id="595ed-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="595ed-162">-StorageKeyType</span></span>
<span data-ttu-id="595ed-163">Especifica qual das teclas de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="595ed-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="595ed-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="595ed-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="595ed-165">A ID do espaço de trabalho (ID de recurso de um espaço de trabalho do Log Analytics) para um espaço de trabalho do Log Analytics para o qual você gostaria de enviar Logs de Auditoria.</span><span class="sxs-lookup"><span data-stu-id="595ed-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="595ed-166">Exemplo: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="595ed-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="595ed-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="595ed-167">-Confirm</span></span>
<span data-ttu-id="595ed-168">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="595ed-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="595ed-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="595ed-169">-WhatIf</span></span>
<span data-ttu-id="595ed-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="595ed-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="595ed-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="595ed-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="595ed-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595ed-172">CommonParameters</span></span>
<span data-ttu-id="595ed-173">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="595ed-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595ed-174">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="595ed-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595ed-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="595ed-175">INPUTS</span></span>

### <span data-ttu-id="595ed-176">System.String</span><span class="sxs-lookup"><span data-stu-id="595ed-176">System.String</span></span>

### <span data-ttu-id="595ed-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="595ed-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="595ed-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="595ed-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="595ed-179">System.Guid</span><span class="sxs-lookup"><span data-stu-id="595ed-179">System.Guid</span></span>

### <span data-ttu-id="595ed-180">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="595ed-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="595ed-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="595ed-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="595ed-182">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="595ed-182">OUTPUTS</span></span>

### <span data-ttu-id="595ed-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="595ed-183">System.Boolean</span></span>

## <span data-ttu-id="595ed-184">NOTES</span><span class="sxs-lookup"><span data-stu-id="595ed-184">NOTES</span></span>

## <span data-ttu-id="595ed-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="595ed-185">RELATED LINKS</span></span>
