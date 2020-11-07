---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773752"
---
# <span data-ttu-id="20dfb-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="20dfb-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="20dfb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="20dfb-103">**Importante: esse cmdlet é preterido, [set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) está substituindo-o.**</span><span class="sxs-lookup"><span data-stu-id="20dfb-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="20dfb-104">Altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="20dfb-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="20dfb-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20dfb-105">SYNTAX</span></span>

### <span data-ttu-id="20dfb-106">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="20dfb-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dfb-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="20dfb-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20dfb-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="20dfb-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dfb-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="20dfb-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dfb-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="20dfb-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dfb-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="20dfb-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20dfb-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="20dfb-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20dfb-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="20dfb-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20dfb-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20dfb-114">DESCRIPTION</span></span>
<span data-ttu-id="20dfb-115">O cmdlet **set-AzSqlServerAuditing** altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="20dfb-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="20dfb-116">Para usar o cmdlet, use os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="20dfb-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="20dfb-117">O destino dos logs de auditoria é determinado especificando um dos seguintes parâmetros de switch: BlobStorage, LogAnalytics ou EventHub (se nenhum for especificado, o padrão será BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="20dfb-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="20dfb-118">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="20dfb-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="20dfb-119">Quando o destino de logs de auditoria for armazenamento de BLOBs, especifique o parâmetro *StorageAccountName* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20dfb-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="20dfb-120">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="20dfb-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="20dfb-121">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve as configurações atuais de auditoria, além dos identificadores de servidor.</span><span class="sxs-lookup"><span data-stu-id="20dfb-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="20dfb-122">Os identificadores de servidor incluem, entre outros, **ResourceGroupName** e **nomedoservidor**.</span><span class="sxs-lookup"><span data-stu-id="20dfb-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="20dfb-123">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20dfb-123">EXAMPLES</span></span>

### <span data-ttu-id="20dfb-124">Exemplo 1: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="20dfb-125">Exemplo 2: desabilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="20dfb-126">Exemplo 3: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure usando uma conta de armazenamento de uma assinatura diferente</span><span class="sxs-lookup"><span data-stu-id="20dfb-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="20dfb-127">Exemplo 4: habilitar a política de auditoria de armazenamento de blob de um SQL Server do Azure com filtragem avançada usando um predicado T-SQL</span><span class="sxs-lookup"><span data-stu-id="20dfb-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="20dfb-128">Exemplo 5: remover a configuração de filtragem avançada da política de armazenamento de auditoria de blob de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="20dfb-129">Exemplo 6: habilitar a política de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="20dfb-130">Exemplo 7: desabilitar a política de auditoria do hub de eventos de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="20dfb-131">Exemplo 8: habilitar a política de auditoria de análise de logs de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="20dfb-132">Exemplo 9: desabilitar a política de auditoria de análise de logs de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="20dfb-133">Exemplo 10: desabilitar, por meio de pipeline, a política de auditoria de análise de logs de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="20dfb-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="20dfb-134">OS</span><span class="sxs-lookup"><span data-stu-id="20dfb-134">PARAMETERS</span></span>

### <span data-ttu-id="20dfb-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20dfb-135">-AsJob</span></span>
<span data-ttu-id="20dfb-136">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20dfb-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20dfb-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="20dfb-137">-AuditActionGroup</span></span>
<span data-ttu-id="20dfb-138">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="20dfb-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="20dfb-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="20dfb-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="20dfb-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="20dfb-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="20dfb-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="20dfb-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="20dfb-142">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="20dfb-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="20dfb-143">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="20dfb-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="20dfb-144">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="20dfb-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="20dfb-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="20dfb-145">-BlobStorage</span></span>
<span data-ttu-id="20dfb-146">Especifica que o destino dos logs de auditoria é o armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="20dfb-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="20dfb-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20dfb-147">-DefaultProfile</span></span>
<span data-ttu-id="20dfb-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20dfb-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20dfb-149">-EventHub</span><span class="sxs-lookup"><span data-stu-id="20dfb-149">-EventHub</span></span>
<span data-ttu-id="20dfb-150">Especifica que o destino dos logs de auditoria é o Hub de eventos</span><span class="sxs-lookup"><span data-stu-id="20dfb-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="20dfb-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="20dfb-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="20dfb-152">A ID do recurso para a regra de autorização do hub de eventos</span><span class="sxs-lookup"><span data-stu-id="20dfb-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="20dfb-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="20dfb-153">-EventHubName</span></span>
<span data-ttu-id="20dfb-154">O nome do hub de eventos.</span><span class="sxs-lookup"><span data-stu-id="20dfb-154">The name of the event hub.</span></span> <span data-ttu-id="20dfb-155">Se nenhum for especificado ao fornecer EventHubAuthorizationRuleResourceId, o Hub de eventos padrão será selecionado.</span><span class="sxs-lookup"><span data-stu-id="20dfb-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="20dfb-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20dfb-156">-InputObject</span></span>
<span data-ttu-id="20dfb-157">O objeto do servidor para gerenciar sua política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="20dfb-157">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="20dfb-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="20dfb-158">-LogAnalytics</span></span>
<span data-ttu-id="20dfb-159">Especifica que o destino dos logs de auditoria é análise de logs</span><span class="sxs-lookup"><span data-stu-id="20dfb-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="20dfb-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20dfb-160">-PassThru</span></span>
<span data-ttu-id="20dfb-161">Especifica se a política de auditoria deve ser impressa no final da execução do cmdlet</span><span class="sxs-lookup"><span data-stu-id="20dfb-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="20dfb-162">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="20dfb-162">-PredicateExpression</span></span>
<span data-ttu-id="20dfb-163">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="20dfb-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="20dfb-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20dfb-164">-ResourceGroupName</span></span>
<span data-ttu-id="20dfb-165">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="20dfb-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="20dfb-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="20dfb-166">-RetentionInDays</span></span>
<span data-ttu-id="20dfb-167">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="20dfb-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="20dfb-168">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="20dfb-168">-ServerName</span></span>
<span data-ttu-id="20dfb-169">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="20dfb-169">SQL server name.</span></span>

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

### <span data-ttu-id="20dfb-170">-Estado</span><span class="sxs-lookup"><span data-stu-id="20dfb-170">-State</span></span>
<span data-ttu-id="20dfb-171">O estado da política.</span><span class="sxs-lookup"><span data-stu-id="20dfb-171">The state of the policy.</span></span>

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

### <span data-ttu-id="20dfb-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="20dfb-172">-StorageAccountName</span></span>
<span data-ttu-id="20dfb-173">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20dfb-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="20dfb-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20dfb-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="20dfb-175">A ID da assinatura da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="20dfb-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="20dfb-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="20dfb-176">-StorageKeyType</span></span>
<span data-ttu-id="20dfb-177">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="20dfb-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="20dfb-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="20dfb-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="20dfb-179">A ID do espaço de trabalho (ID do recurso de um espaço de trabalho de análise de log) para um espaço de trabalho de análise de log ao qual você gostaria de enviar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="20dfb-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="20dfb-180">Exemplo:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="20dfb-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="20dfb-181">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20dfb-181">-Confirm</span></span>
<span data-ttu-id="20dfb-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20dfb-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20dfb-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20dfb-183">-WhatIf</span></span>
<span data-ttu-id="20dfb-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20dfb-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20dfb-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20dfb-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20dfb-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20dfb-186">CommonParameters</span></span>
<span data-ttu-id="20dfb-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20dfb-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20dfb-188">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20dfb-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20dfb-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20dfb-189">INPUTS</span></span>

### <span data-ttu-id="20dfb-190">System. String</span><span class="sxs-lookup"><span data-stu-id="20dfb-190">System.String</span></span>

### <span data-ttu-id="20dfb-191">Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="20dfb-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="20dfb-192">Microsoft. Azure. Commands. Sql. Auditing. Model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="20dfb-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="20dfb-193">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="20dfb-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="20dfb-194">System. GUID</span><span class="sxs-lookup"><span data-stu-id="20dfb-194">System.Guid</span></span>

### <span data-ttu-id="20dfb-195">System. Nullable ' 1 [[System. UInt32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20dfb-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="20dfb-196">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20dfb-196">OUTPUTS</span></span>

### <span data-ttu-id="20dfb-197">Microsoft. Azure. Commands. Sql. Auditing. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="20dfb-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="20dfb-198">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20dfb-198">NOTES</span></span>

## <span data-ttu-id="20dfb-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20dfb-199">RELATED LINKS</span></span>
