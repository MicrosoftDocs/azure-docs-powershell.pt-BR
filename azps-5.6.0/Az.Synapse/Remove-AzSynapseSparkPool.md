---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: 22b006d096d1ab2457d53a97a6265bf950c4658e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886817"
---
# <span data-ttu-id="07f6d-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="07f6d-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="07f6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f6d-102">SYNOPSIS</span></span>
<span data-ttu-id="07f6d-103">Exclui um pool de Spark de Análise de Sinapse.</span><span class="sxs-lookup"><span data-stu-id="07f6d-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="07f6d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07f6d-104">SYNTAX</span></span>

### <span data-ttu-id="07f6d-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="07f6d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f6d-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f6d-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f6d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f6d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07f6d-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07f6d-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f6d-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07f6d-109">DESCRIPTION</span></span>
<span data-ttu-id="07f6d-110">O cmdlet **Remove-AzSynapseSparkPool** exclui permanentemente um pool de Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="07f6d-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="07f6d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07f6d-111">EXAMPLES</span></span>

### <span data-ttu-id="07f6d-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07f6d-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="07f6d-113">Este comando exclui um pool de Spark de Análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="07f6d-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="07f6d-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07f6d-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="07f6d-115">Este comando exclui um pool de Spark de Análise de Synapse do Azure por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="07f6d-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="07f6d-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="07f6d-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="07f6d-117">Este comando exclui um pool de Spark de Análise de Synapse do Azure por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="07f6d-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="07f6d-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="07f6d-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="07f6d-119">Este comando exclui um pool de Spark de Análise do Azure Synapse com uma ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="07f6d-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="07f6d-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07f6d-120">PARAMETERS</span></span>

### <span data-ttu-id="07f6d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07f6d-121">-AsJob</span></span>
<span data-ttu-id="07f6d-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="07f6d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07f6d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f6d-123">-DefaultProfile</span></span>
<span data-ttu-id="07f6d-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07f6d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f6d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="07f6d-125">-Force</span></span>
<span data-ttu-id="07f6d-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="07f6d-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="07f6d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07f6d-127">-InputObject</span></span>
<span data-ttu-id="07f6d-128">Objeto de entrada do pool de centelha, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="07f6d-128">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07f6d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="07f6d-129">-Name</span></span>
<span data-ttu-id="07f6d-130">Nome do pool de spark synapse.</span><span class="sxs-lookup"><span data-stu-id="07f6d-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SparkPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f6d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07f6d-131">-PassThru</span></span>
<span data-ttu-id="07f6d-132">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="07f6d-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="07f6d-133">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="07f6d-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="07f6d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f6d-134">-ResourceGroupName</span></span>
<span data-ttu-id="07f6d-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07f6d-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f6d-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07f6d-136">-ResourceId</span></span>
<span data-ttu-id="07f6d-137">Identificador de recursos do pool de Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="07f6d-137">Resource identifier of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f6d-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07f6d-138">-WorkspaceName</span></span>
<span data-ttu-id="07f6d-139">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="07f6d-139">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f6d-140">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="07f6d-140">-WorkspaceObject</span></span>
<span data-ttu-id="07f6d-141">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="07f6d-141">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07f6d-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07f6d-142">-Confirm</span></span>
<span data-ttu-id="07f6d-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07f6d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f6d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f6d-144">-WhatIf</span></span>
<span data-ttu-id="07f6d-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07f6d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f6d-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07f6d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f6d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f6d-147">CommonParameters</span></span>
<span data-ttu-id="07f6d-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f6d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f6d-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f6d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f6d-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07f6d-150">INPUTS</span></span>

### <span data-ttu-id="07f6d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="07f6d-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="07f6d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="07f6d-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="07f6d-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07f6d-153">OUTPUTS</span></span>

### <span data-ttu-id="07f6d-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07f6d-154">System.Boolean</span></span>

## <span data-ttu-id="07f6d-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="07f6d-155">NOTES</span></span>

## <span data-ttu-id="07f6d-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07f6d-156">RELATED LINKS</span></span>
