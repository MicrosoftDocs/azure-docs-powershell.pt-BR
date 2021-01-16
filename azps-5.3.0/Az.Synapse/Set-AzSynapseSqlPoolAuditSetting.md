---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429617"
---
# <span data-ttu-id="229d2-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="229d2-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="229d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="229d2-102">SYNOPSIS</span></span>
<span data-ttu-id="229d2-103">Altera as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="229d2-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="229d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="229d2-104">SYNTAX</span></span>

### <span data-ttu-id="229d2-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="229d2-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229d2-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="229d2-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229d2-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="229d2-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="229d2-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="229d2-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="229d2-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="229d2-109">DESCRIPTION</span></span>
<span data-ttu-id="229d2-110">O cmdlet **set-AzSynapseSqlPoolAuditSetting** altera as configurações de auditoria de um pool SQL do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="229d2-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="229d2-111">Quando o armazenamento de blob for um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="229d2-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="229d2-112">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="229d2-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="229d2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="229d2-113">EXAMPLES</span></span>

### <span data-ttu-id="229d2-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="229d2-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="229d2-115">Habilite a política de auditoria de armazenamento de blob de um pool SQL do Azure Synapse Analytics chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="229d2-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="229d2-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="229d2-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="229d2-117">Desabilite a política de auditoria de armazenamento de blob de um pool SQL do Azure Synapse Analytics chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="229d2-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="229d2-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="229d2-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="229d2-119">Habilite a política de auditoria de armazenamento de blob de um pool SQL do Azure Synapse Analytics chamado ContosoSqlPool com filtragem avançada usando um predicado T-SQL.</span><span class="sxs-lookup"><span data-stu-id="229d2-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="229d2-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="229d2-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="229d2-121">Remova a configuração de filtragem avançada da política de auditoria de um pool SQL do Azure Synapse Analytics chamado ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="229d2-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="229d2-122">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="229d2-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="229d2-123">Desabilite a política de auditoria de armazenamento de blob de um pool SQL do Azure Synapse Analytics chamado ContosoSqlPool pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="229d2-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="229d2-124">OS</span><span class="sxs-lookup"><span data-stu-id="229d2-124">PARAMETERS</span></span>

### <span data-ttu-id="229d2-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="229d2-125">-AsJob</span></span>
<span data-ttu-id="229d2-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="229d2-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="229d2-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="229d2-127">-AuditAction</span></span>
<span data-ttu-id="229d2-128">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="229d2-128">The set of audit actions.</span></span>

<span data-ttu-id="229d2-129">As ações com suporte para auditoria são:</span><span class="sxs-lookup"><span data-stu-id="229d2-129">The supported actions to audit are:</span></span>

<span data-ttu-id="229d2-130">SELECIONADA</span><span class="sxs-lookup"><span data-stu-id="229d2-130">SELECT</span></span>

<span data-ttu-id="229d2-131">ATUALIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="229d2-131">UPDATE</span></span>

<span data-ttu-id="229d2-132">NSERIR</span><span class="sxs-lookup"><span data-stu-id="229d2-132">INSERT</span></span>

<span data-ttu-id="229d2-133">REMOVER</span><span class="sxs-lookup"><span data-stu-id="229d2-133">DELETE</span></span>

<span data-ttu-id="229d2-134">NOVAMENTE</span><span class="sxs-lookup"><span data-stu-id="229d2-134">EXECUTE</span></span>

<span data-ttu-id="229d2-135">Recebi</span><span class="sxs-lookup"><span data-stu-id="229d2-135">RECEIVE</span></span>

<span data-ttu-id="229d2-136">REFERE</span><span class="sxs-lookup"><span data-stu-id="229d2-136">REFERENCES</span></span>

<span data-ttu-id="229d2-137">A forma geral para definir uma ação a ser auditada é:</span><span class="sxs-lookup"><span data-stu-id="229d2-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="229d2-138">\[ação \] no \[ objeto \] por \[ entidade de segurança\]</span><span class="sxs-lookup"><span data-stu-id="229d2-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="229d2-139">Observe que \[ \] o objeto no formato acima pode se referir a um objeto, como uma tabela, um modo de exibição ou um procedimento armazenado, ou um esquema ou banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="229d2-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="229d2-140">Para os últimos casos, o banco de dados de formulários:: \[ dbname \] e Schema:: \[ SchemaName \] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="229d2-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="229d2-141">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="229d2-141">For example:</span></span>

<span data-ttu-id="229d2-142">SELECIONAR em dbo. myTable por público</span><span class="sxs-lookup"><span data-stu-id="229d2-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="229d2-143">SELECIONAR no banco de dados:: MyDatabase por público</span><span class="sxs-lookup"><span data-stu-id="229d2-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="229d2-144">SELECIONAR no esquema:: MySchema by Public</span><span class="sxs-lookup"><span data-stu-id="229d2-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="229d2-145">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="229d2-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="229d2-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="229d2-146">-AuditActionGroup</span></span>
<span data-ttu-id="229d2-147">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="229d2-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="229d2-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="229d2-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="229d2-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="229d2-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="229d2-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="229d2-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="229d2-151">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="229d2-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="229d2-152">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="229d2-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="229d2-153">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="229d2-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="229d2-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="229d2-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="229d2-155">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="229d2-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="229d2-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229d2-156">-DefaultProfile</span></span>
<span data-ttu-id="229d2-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="229d2-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="229d2-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="229d2-158">-InputObject</span></span>
<span data-ttu-id="229d2-159">Objeto de entrada de pool SQL, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="229d2-159">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="229d2-160">-Nome</span><span class="sxs-lookup"><span data-stu-id="229d2-160">-Name</span></span>
<span data-ttu-id="229d2-161">Nome do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="229d2-161">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="229d2-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="229d2-162">-PassThru</span></span>
<span data-ttu-id="229d2-163">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="229d2-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="229d2-164">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="229d2-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="229d2-165">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="229d2-165">-PredicateExpression</span></span>
<span data-ttu-id="229d2-166">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="229d2-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="229d2-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="229d2-167">-ResourceGroupName</span></span>
<span data-ttu-id="229d2-168">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="229d2-168">Resource group name.</span></span>

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

### <span data-ttu-id="229d2-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="229d2-169">-ResourceId</span></span>
<span data-ttu-id="229d2-170">Identificador de recurso do pool do SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="229d2-170">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="229d2-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="229d2-171">-RetentionInDays</span></span>
<span data-ttu-id="229d2-172">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="229d2-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="229d2-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="229d2-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="229d2-174">A ID do recurso da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="229d2-174">The storage account resource id</span></span>

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

### <span data-ttu-id="229d2-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="229d2-175">-StorageKeyType</span></span>
<span data-ttu-id="229d2-176">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="229d2-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="229d2-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="229d2-177">-WorkspaceName</span></span>
<span data-ttu-id="229d2-178">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="229d2-178">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="229d2-179">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="229d2-179">-WorkspaceObject</span></span>
<span data-ttu-id="229d2-180">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="229d2-180">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="229d2-181">-Confirme</span><span class="sxs-lookup"><span data-stu-id="229d2-181">-Confirm</span></span>
<span data-ttu-id="229d2-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="229d2-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="229d2-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="229d2-183">-WhatIf</span></span>
<span data-ttu-id="229d2-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="229d2-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="229d2-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="229d2-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="229d2-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229d2-186">CommonParameters</span></span>
<span data-ttu-id="229d2-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="229d2-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229d2-188">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="229d2-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229d2-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="229d2-189">INPUTS</span></span>

### <span data-ttu-id="229d2-190">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="229d2-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="229d2-191">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="229d2-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="229d2-192">EXIBE</span><span class="sxs-lookup"><span data-stu-id="229d2-192">OUTPUTS</span></span>

### <span data-ttu-id="229d2-193">Microsoft. Azure. Commands. Synapse. Models. SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="229d2-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="229d2-194">INFORMA</span><span class="sxs-lookup"><span data-stu-id="229d2-194">NOTES</span></span>

## <span data-ttu-id="229d2-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="229d2-195">RELATED LINKS</span></span>
