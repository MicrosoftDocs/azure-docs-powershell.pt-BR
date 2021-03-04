---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 8b47466c2f40ff769c1755ea1d59873a120e5d5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892920"
---
# <span data-ttu-id="37228-101">Reset-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="37228-101">Reset-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="37228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37228-102">SYNOPSIS</span></span>
<span data-ttu-id="37228-103">Remove as configurações de auditoria de um pool do Azure Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="37228-103">Removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="37228-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="37228-104">SYNTAX</span></span>

### <span data-ttu-id="37228-105">RemoveByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="37228-105">RemoveByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37228-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37228-106">RemoveByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37228-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="37228-107">RemoveByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37228-108">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37228-108">RemoveByResourceIdParameterSet</span></span>
```
Reset-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37228-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="37228-109">DESCRIPTION</span></span>
<span data-ttu-id="37228-110">O cmdlet **Reset-AzSynapseSqlPoolAuditSetting** remove as configurações de auditoria de um pool do Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="37228-110">The **Reset-AzSynapseSqlPoolAuditSetting** cmdlet removes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="37228-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37228-111">EXAMPLES</span></span>

### <span data-ttu-id="37228-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37228-112">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="37228-113">Este comando remove as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="37228-113">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="37228-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="37228-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Reset-AzSynapseSqlPoolAuditSetting
```

<span data-ttu-id="37228-115">Este comando remove as configurações de auditoria de um pool SQL chamado ContosoSqlPool no espaço de trabalho ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="37228-115">This command removes the auditing settings of a SQL pool called ContosoSqlPool in the workspace ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="37228-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="37228-116">PARAMETERS</span></span>

### <span data-ttu-id="37228-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37228-117">-AsJob</span></span>
<span data-ttu-id="37228-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="37228-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37228-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37228-119">-DefaultProfile</span></span>
<span data-ttu-id="37228-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37228-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37228-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37228-121">-InputObject</span></span>
<span data-ttu-id="37228-122">SQL objeto de entrada do pool, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="37228-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37228-123">-Name</span><span class="sxs-lookup"><span data-stu-id="37228-123">-Name</span></span>
<span data-ttu-id="37228-124">Nome do pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="37228-124">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37228-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37228-125">-PassThru</span></span>
<span data-ttu-id="37228-126">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="37228-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="37228-127">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="37228-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="37228-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37228-128">-ResourceGroupName</span></span>
<span data-ttu-id="37228-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37228-129">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37228-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37228-130">-ResourceId</span></span>
<span data-ttu-id="37228-131">Identificador de recursos do Pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="37228-131">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37228-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="37228-132">-WorkspaceName</span></span>
<span data-ttu-id="37228-133">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="37228-133">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37228-134">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="37228-134">-WorkspaceObject</span></span>
<span data-ttu-id="37228-135">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="37228-135">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37228-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37228-136">-Confirm</span></span>
<span data-ttu-id="37228-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37228-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37228-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37228-138">-WhatIf</span></span>
<span data-ttu-id="37228-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37228-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37228-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37228-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37228-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37228-141">CommonParameters</span></span>
<span data-ttu-id="37228-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37228-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37228-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37228-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37228-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="37228-144">INPUTS</span></span>

### <span data-ttu-id="37228-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="37228-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="37228-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="37228-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="37228-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="37228-147">OUTPUTS</span></span>

### <span data-ttu-id="37228-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="37228-148">System.Boolean</span></span>

## <span data-ttu-id="37228-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="37228-149">NOTES</span></span>

## <span data-ttu-id="37228-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37228-150">RELATED LINKS</span></span>
