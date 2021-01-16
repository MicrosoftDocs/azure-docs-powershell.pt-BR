---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261420"
---
# <span data-ttu-id="81ea4-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="81ea4-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="81ea4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81ea4-102">SYNOPSIS</span></span>
<span data-ttu-id="81ea4-103">Altera as configurações de auditoria de um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="81ea4-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="81ea4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81ea4-104">SYNTAX</span></span>

### <span data-ttu-id="81ea4-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="81ea4-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81ea4-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="81ea4-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81ea4-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="81ea4-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81ea4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81ea4-108">DESCRIPTION</span></span>
<span data-ttu-id="81ea4-109">O cmdlet **set-AzSynapseSqlAuditSetting** altera as configurações de auditoria de um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="81ea4-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="81ea4-110">Quando o armazenamento de blob for um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="81ea4-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="81ea4-111">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="81ea4-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="81ea4-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81ea4-112">EXAMPLES</span></span>

### <span data-ttu-id="81ea4-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81ea4-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="81ea4-114">Habilite a política de auditoria de armazenamento de blob de um espaço de trabalho de análise do Azure Synapse chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="81ea4-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="81ea4-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="81ea4-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="81ea4-116">Desabilite a política de auditoria de armazenamento de blob de um espaço de trabalho de análise do Azure Synapse chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="81ea4-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="81ea4-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="81ea4-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="81ea4-118">Habilite a política de auditoria de armazenamento de blob de um espaço de trabalho de análise do Azure Synapse chamado ContosoWorkspace com filtragem avançada usando um predicado T-SQL.</span><span class="sxs-lookup"><span data-stu-id="81ea4-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="81ea4-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="81ea4-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="81ea4-120">Remova a configuração de filtragem avançada da política de auditoria de um espaço de trabalho de análise do Azure Synapse chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="81ea4-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="81ea4-121">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="81ea4-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="81ea4-122">Desabilite a política de auditoria de armazenamento de blob de um espaço de trabalho de análise do Azure Synapse chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="81ea4-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="81ea4-123">OS</span><span class="sxs-lookup"><span data-stu-id="81ea4-123">PARAMETERS</span></span>

### <span data-ttu-id="81ea4-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81ea4-124">-AsJob</span></span>
<span data-ttu-id="81ea4-125">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="81ea4-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81ea4-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="81ea4-126">-AuditActionGroup</span></span>
<span data-ttu-id="81ea4-127">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="81ea4-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="81ea4-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="81ea4-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="81ea4-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="81ea4-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="81ea4-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="81ea4-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="81ea4-131">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="81ea4-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="81ea4-132">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="81ea4-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="81ea4-133">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="81ea4-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="81ea4-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="81ea4-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="81ea4-135">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="81ea4-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="81ea4-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81ea4-136">-DefaultProfile</span></span>
<span data-ttu-id="81ea4-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81ea4-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81ea4-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81ea4-138">-InputObject</span></span>
<span data-ttu-id="81ea4-139">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="81ea4-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81ea4-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81ea4-140">-PassThru</span></span>
<span data-ttu-id="81ea4-141">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="81ea4-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="81ea4-142">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="81ea4-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="81ea4-143">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="81ea4-143">-PredicateExpression</span></span>
<span data-ttu-id="81ea4-144">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="81ea4-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="81ea4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81ea4-145">-ResourceGroupName</span></span>
<span data-ttu-id="81ea4-146">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81ea4-146">Resource group name.</span></span>

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

### <span data-ttu-id="81ea4-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="81ea4-147">-ResourceId</span></span>
<span data-ttu-id="81ea4-148">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="81ea4-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="81ea4-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="81ea4-149">-RetentionInDays</span></span>
<span data-ttu-id="81ea4-150">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="81ea4-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="81ea4-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="81ea4-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="81ea4-152">A ID do recurso da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="81ea4-152">The storage account resource id</span></span>

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

### <span data-ttu-id="81ea4-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="81ea4-153">-StorageKeyType</span></span>
<span data-ttu-id="81ea4-154">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="81ea4-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="81ea4-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="81ea4-155">-WorkspaceName</span></span>
<span data-ttu-id="81ea4-156">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="81ea4-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="81ea4-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81ea4-157">-Confirm</span></span>
<span data-ttu-id="81ea4-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81ea4-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81ea4-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81ea4-159">-WhatIf</span></span>
<span data-ttu-id="81ea4-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81ea4-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81ea4-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81ea4-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81ea4-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81ea4-162">CommonParameters</span></span>
<span data-ttu-id="81ea4-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81ea4-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81ea4-164">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81ea4-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81ea4-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81ea4-165">INPUTS</span></span>

### <span data-ttu-id="81ea4-166">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="81ea4-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="81ea4-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81ea4-167">OUTPUTS</span></span>

### <span data-ttu-id="81ea4-168">Microsoft. Azure. Commands. Synapse. Models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="81ea4-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="81ea4-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81ea4-169">NOTES</span></span>

## <span data-ttu-id="81ea4-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81ea4-170">RELATED LINKS</span></span>
