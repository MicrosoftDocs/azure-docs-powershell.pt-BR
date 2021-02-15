---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113904"
---
# <span data-ttu-id="21378-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="21378-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="21378-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21378-102">SYNOPSIS</span></span>
<span data-ttu-id="21378-103">Altera as configurações de auditoria de um Espaço de Trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="21378-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="21378-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21378-104">SYNTAX</span></span>

### <span data-ttu-id="21378-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="21378-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21378-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21378-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21378-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21378-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21378-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="21378-108">DESCRIPTION</span></span>
<span data-ttu-id="21378-109">O cmdlet **Set-AzSynapseSqlAuditSetting** altera as configurações de auditoria de um Espaço de Trabalho de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="21378-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="21378-110">Quando o armazenamento de blob é um destino para logs de auditoria, especifique o parâmetro *StorageAccountResourceId* para determinar a conta de armazenamento dos logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="21378-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="21378-111">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="21378-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="21378-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21378-112">EXAMPLES</span></span>

### <span data-ttu-id="21378-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21378-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="21378-114">Habilitar a política de auditoria de armazenamento em blob de um Espaço de Trabalho do Azure Synapse Analytics chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="21378-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="21378-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="21378-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="21378-116">Desabilite a política de auditoria de armazenamento em blob de um Espaço de Trabalho do Azure Synapse Analytics chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="21378-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="21378-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="21378-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="21378-118">Habilitar a política de auditoria de armazenamento em blob de um Espaço de Trabalho de Análise do Azure Synapse chamado ContosoWorkspace com filtragem avançada usando um predicado T-SQL.</span><span class="sxs-lookup"><span data-stu-id="21378-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="21378-119">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="21378-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="21378-120">Remova a configuração de filtragem avançada da política de auditoria de um Espaço de Trabalho do Azure Synapse Analytics chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="21378-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="21378-121">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="21378-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="21378-122">Desabilite a política de auditoria de armazenamento em blob de um Espaço de Trabalho do Azure Synapse Analytics chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="21378-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="21378-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21378-123">PARAMETERS</span></span>

### <span data-ttu-id="21378-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21378-124">-AsJob</span></span>
<span data-ttu-id="21378-125">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21378-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21378-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="21378-126">-AuditActionGroup</span></span>
<span data-ttu-id="21378-127">O conjunto recomendado de grupos de ações a ser usado é a seguinte combinação: isso audita todas as consultas e procedimentos armazenados executados no banco de dados, bem como logons bem-sucedidos e com falha:</span><span class="sxs-lookup"><span data-stu-id="21378-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="21378-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="21378-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="21378-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="21378-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="21378-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="21378-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="21378-131">Essa combinação acima também é o conjunto configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="21378-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="21378-132">Esses grupos abrangem todas as instruções SQL e os procedimentos armazenados executados no banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="21378-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="21378-133">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="21378-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="21378-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="21378-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="21378-135">Indica se o armazenamento de blob é um destino para registros de auditoria.</span><span class="sxs-lookup"><span data-stu-id="21378-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="21378-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21378-136">-DefaultProfile</span></span>
<span data-ttu-id="21378-137">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21378-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21378-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21378-138">-InputObject</span></span>
<span data-ttu-id="21378-139">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="21378-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="21378-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21378-140">-PassThru</span></span>
<span data-ttu-id="21378-141">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="21378-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="21378-142">Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="21378-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="21378-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="21378-143">-PredicateExpression</span></span>
<span data-ttu-id="21378-144">O predicado T-SQL (cláusula WHERE) usado para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="21378-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="21378-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21378-145">-ResourceGroupName</span></span>
<span data-ttu-id="21378-146">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21378-146">Resource group name.</span></span>

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

### <span data-ttu-id="21378-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21378-147">-ResourceId</span></span>
<span data-ttu-id="21378-148">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="21378-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="21378-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="21378-149">-RetentionInDays</span></span>
<span data-ttu-id="21378-150">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="21378-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="21378-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="21378-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="21378-152">A ID de recurso da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="21378-152">The storage account resource id</span></span>

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

### <span data-ttu-id="21378-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="21378-153">-StorageKeyType</span></span>
<span data-ttu-id="21378-154">Especifica qual das teclas de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="21378-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="21378-155">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="21378-155">-WorkspaceName</span></span>
<span data-ttu-id="21378-156">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="21378-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="21378-157">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="21378-157">-Confirm</span></span>
<span data-ttu-id="21378-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21378-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21378-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21378-159">-WhatIf</span></span>
<span data-ttu-id="21378-160">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="21378-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21378-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21378-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21378-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21378-162">CommonParameters</span></span>
<span data-ttu-id="21378-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21378-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21378-164">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21378-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21378-165">Entradas</span><span class="sxs-lookup"><span data-stu-id="21378-165">INPUTS</span></span>

### <span data-ttu-id="21378-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="21378-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="21378-167">Saídas</span><span class="sxs-lookup"><span data-stu-id="21378-167">OUTPUTS</span></span>

### <span data-ttu-id="21378-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="21378-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="21378-169">Notas</span><span class="sxs-lookup"><span data-stu-id="21378-169">NOTES</span></span>

## <span data-ttu-id="21378-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21378-170">RELATED LINKS</span></span>
