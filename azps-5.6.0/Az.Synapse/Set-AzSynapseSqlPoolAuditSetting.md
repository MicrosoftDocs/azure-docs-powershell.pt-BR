---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 102d8f9e33a90d97cadb984a671797a89d6f3833
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890538"
---
# <span data-ttu-id="0f373-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="0f373-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="0f373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f373-102">SYNOPSIS</span></span>
<span data-ttu-id="0f373-103">Altera as configurações de auditoria para um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="0f373-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="0f373-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0f373-104">SYNTAX</span></span>

### <span data-ttu-id="0f373-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0f373-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f373-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f373-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f373-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f373-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f373-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f373-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f373-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0f373-109">DESCRIPTION</span></span>
<span data-ttu-id="0f373-110">O cmdlet **Set-AzSynapseSqlPoolAuditSetting** altera as configurações de auditoria de um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="0f373-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="0f373-111">Quando o armazenamento de blob é um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento dos logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0f373-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="0f373-112">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período dos logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0f373-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="0f373-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f373-113">EXAMPLES</span></span>

### <span data-ttu-id="0f373-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f373-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="0f373-115">Habilita a política de auditoria de armazenamento de blob de um pool do Azure Synapse Analytics SQL chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="0f373-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="0f373-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0f373-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="0f373-117">Desabilite a política de auditoria de armazenamento de blob de um pool do Azure Synapse Analytics SQL chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="0f373-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="0f373-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0f373-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="0f373-119">Habilita a política de auditoria de armazenamento de blob de um pool do Azure Synapse Analytics SQL chamado ContosoSqlPool com filtragem avançada usando um predicado T-SQL.</span><span class="sxs-lookup"><span data-stu-id="0f373-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="0f373-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0f373-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="0f373-121">Remova a configuração de filtragem avançada da política de auditoria de um pool do Azure Synapse Analytics SQL chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="0f373-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="0f373-122">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="0f373-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="0f373-123">Desabilite a política de auditoria de armazenamento de blob de um pool do Azure Synapse Analytics SQL chamado ContosoSqlPool por pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f373-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="0f373-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0f373-124">PARAMETERS</span></span>

### <span data-ttu-id="0f373-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f373-125">-AsJob</span></span>
<span data-ttu-id="0f373-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f373-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f373-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="0f373-127">-AuditAction</span></span>
<span data-ttu-id="0f373-128">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0f373-128">The set of audit actions.</span></span>

<span data-ttu-id="0f373-129">As ações com suporte para auditoria são:</span><span class="sxs-lookup"><span data-stu-id="0f373-129">The supported actions to audit are:</span></span>

<span data-ttu-id="0f373-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="0f373-130">SELECT</span></span>

<span data-ttu-id="0f373-131">UPDATE</span><span class="sxs-lookup"><span data-stu-id="0f373-131">UPDATE</span></span>

<span data-ttu-id="0f373-132">INSERT</span><span class="sxs-lookup"><span data-stu-id="0f373-132">INSERT</span></span>

<span data-ttu-id="0f373-133">DELETE</span><span class="sxs-lookup"><span data-stu-id="0f373-133">DELETE</span></span>

<span data-ttu-id="0f373-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="0f373-134">EXECUTE</span></span>

<span data-ttu-id="0f373-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="0f373-135">RECEIVE</span></span>

<span data-ttu-id="0f373-136">REFERÊNCIAS</span><span class="sxs-lookup"><span data-stu-id="0f373-136">REFERENCES</span></span>

<span data-ttu-id="0f373-137">O formulário geral para definir uma ação a ser auditada é:</span><span class="sxs-lookup"><span data-stu-id="0f373-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="0f373-138">\[action \] ON object BY \[ \] \[ principal\]</span><span class="sxs-lookup"><span data-stu-id="0f373-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="0f373-139">Observe que o objeto no formato acima pode se referir a um objeto como uma tabela, exibição ou procedimento armazenado ou um banco de dados \[ \] ou esquema inteiro.</span><span class="sxs-lookup"><span data-stu-id="0f373-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="0f373-140">Para os últimos casos, os formulários DATABASE:: dbname e \[ \] SCHEMA:: \[ schemaname \] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="0f373-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="0f373-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="0f373-141">For example:</span></span>

<span data-ttu-id="0f373-142">SELECT em dbo.myTable por público</span><span class="sxs-lookup"><span data-stu-id="0f373-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="0f373-143">SELECT on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="0f373-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="0f373-144">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="0f373-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="0f373-145">Para obter mais informações, consulte https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="0f373-145">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="0f373-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="0f373-146">-AuditActionGroup</span></span>
<span data-ttu-id="0f373-147">O conjunto recomendado de grupos de ações a ser usado é a seguinte combinação : isso audita todas as consultas e procedimentos armazenados executados no banco de dados, bem como logons bem-sucedidos e com falha:</span><span class="sxs-lookup"><span data-stu-id="0f373-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="0f373-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="0f373-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="0f373-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="0f373-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="0f373-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="0f373-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="0f373-151">Essa combinação acima também é o conjunto configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="0f373-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="0f373-152">Esses grupos abrangem todas as SQL e procedimentos armazenados executados no banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="0f373-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="0f373-153">Para obter mais informações, consulte https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="0f373-153">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f373-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="0f373-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="0f373-155">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0f373-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="0f373-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f373-156">-DefaultProfile</span></span>
<span data-ttu-id="0f373-157">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f373-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f373-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f373-158">-InputObject</span></span>
<span data-ttu-id="0f373-159">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f373-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f373-160">-Name</span><span class="sxs-lookup"><span data-stu-id="0f373-160">-Name</span></span>
<span data-ttu-id="0f373-161">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="0f373-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f373-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f373-162">-PassThru</span></span>
<span data-ttu-id="0f373-163">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="0f373-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0f373-164">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="0f373-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="0f373-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="0f373-165">-PredicateExpression</span></span>
<span data-ttu-id="0f373-166">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0f373-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="0f373-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f373-167">-ResourceGroupName</span></span>
<span data-ttu-id="0f373-168">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f373-168">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f373-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f373-169">-ResourceId</span></span>
<span data-ttu-id="0f373-170">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="0f373-170">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f373-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0f373-171">-RetentionInDays</span></span>
<span data-ttu-id="0f373-172">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="0f373-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="0f373-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0f373-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="0f373-174">A ID do recurso de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="0f373-174">The storage account resource id</span></span>

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

### <span data-ttu-id="0f373-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="0f373-175">-StorageKeyType</span></span>
<span data-ttu-id="0f373-176">Especifica qual das teclas de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="0f373-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="0f373-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f373-177">-WorkspaceName</span></span>
<span data-ttu-id="0f373-178">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="0f373-178">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f373-179">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0f373-179">-WorkspaceObject</span></span>
<span data-ttu-id="0f373-180">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f373-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f373-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f373-181">-Confirm</span></span>
<span data-ttu-id="0f373-182">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f373-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f373-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f373-183">-WhatIf</span></span>
<span data-ttu-id="0f373-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0f373-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f373-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f373-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f373-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f373-186">CommonParameters</span></span>
<span data-ttu-id="0f373-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f373-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f373-188">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f373-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f373-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f373-189">INPUTS</span></span>

### <span data-ttu-id="0f373-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0f373-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="0f373-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0f373-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="0f373-192">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0f373-192">OUTPUTS</span></span>

### <span data-ttu-id="0f373-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="0f373-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="0f373-194">NOTES</span><span class="sxs-lookup"><span data-stu-id="0f373-194">NOTES</span></span>

## <span data-ttu-id="0f373-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f373-195">RELATED LINKS</span></span>
