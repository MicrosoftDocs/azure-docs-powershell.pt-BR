---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSparkPool.md
ms.openlocfilehash: d9e3160d5ba0620ff881c940bf8383a7046136a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956073"
---
# <span data-ttu-id="ce086-101">Remove-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ce086-101">Remove-AzSynapseSparkPool</span></span>

## <span data-ttu-id="ce086-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce086-102">SYNOPSIS</span></span>
<span data-ttu-id="ce086-103">Exclui um pool Spark do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce086-103">Deletes a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ce086-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce086-104">SYNTAX</span></span>

### <span data-ttu-id="ce086-105">DeleteByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce086-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce086-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce086-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce086-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce086-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSparkPool -InputObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce086-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce086-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSparkPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce086-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce086-109">DESCRIPTION</span></span>
<span data-ttu-id="ce086-110">O cmdlet **Remove-AzSynapseSparkPool** exclui permanentemente um pool do Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce086-110">The **Remove-AzSynapseSparkPool** cmdlet permanently deletes an Azure Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="ce086-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce086-111">EXAMPLES</span></span>

### <span data-ttu-id="ce086-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce086-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="ce086-113">Esse comando exclui um pool Spark do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce086-113">This command deletes an Azure Synapse Analytics Spark pool.</span></span>

### <span data-ttu-id="ce086-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce086-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Remove-AzSynapseSparkPool
```

<span data-ttu-id="ce086-115">Esse comando exclui um pool do Spark do Azure Synapse Analytics pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce086-115">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="ce086-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce086-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSparkPool -Name ContosoSparkPool
```

<span data-ttu-id="ce086-117">Esse comando exclui um pool do Spark do Azure Synapse Analytics pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce086-117">This command deletes an Azure Synapse Analytics Spark pool through pipeline.</span></span>

### <span data-ttu-id="ce086-118">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ce086-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSparkPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/bigDataPools/ContosoSparkPool
```

<span data-ttu-id="ce086-119">Esse comando exclui um pool Spark do Azure Synapse Analytics com uma ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ce086-119">This command deletes an Azure Synapse Analytics Spark pool with a resource ID.</span></span>

## <span data-ttu-id="ce086-120">OS</span><span class="sxs-lookup"><span data-stu-id="ce086-120">PARAMETERS</span></span>

### <span data-ttu-id="ce086-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce086-121">-AsJob</span></span>
<span data-ttu-id="ce086-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ce086-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce086-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce086-123">-DefaultProfile</span></span>
<span data-ttu-id="ce086-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce086-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce086-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce086-125">-InputObject</span></span>
<span data-ttu-id="ce086-126">Objeto de entrada do pool do Spark, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce086-126">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ce086-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce086-127">-Name</span></span>
<span data-ttu-id="ce086-128">Nome do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="ce086-128">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ce086-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce086-129">-PassThru</span></span>
<span data-ttu-id="ce086-130">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="ce086-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ce086-131">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ce086-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ce086-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce086-132">-ResourceGroupName</span></span>
<span data-ttu-id="ce086-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ce086-133">Resource group name.</span></span>

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

### <span data-ttu-id="ce086-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce086-134">-ResourceId</span></span>
<span data-ttu-id="ce086-135">Identificador de recurso do pool do Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="ce086-135">Resource identifier of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="ce086-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce086-136">-WorkspaceName</span></span>
<span data-ttu-id="ce086-137">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="ce086-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ce086-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="ce086-138">-WorkspaceObject</span></span>
<span data-ttu-id="ce086-139">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ce086-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ce086-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce086-140">-Confirm</span></span>
<span data-ttu-id="ce086-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce086-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce086-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce086-142">-WhatIf</span></span>
<span data-ttu-id="ce086-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce086-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce086-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce086-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce086-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce086-145">CommonParameters</span></span>
<span data-ttu-id="ce086-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce086-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce086-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce086-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce086-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce086-148">INPUTS</span></span>

### <span data-ttu-id="ce086-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce086-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ce086-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="ce086-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="ce086-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce086-151">OUTPUTS</span></span>

### <span data-ttu-id="ce086-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce086-152">System.Boolean</span></span>

## <span data-ttu-id="ce086-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce086-153">NOTES</span></span>

## <span data-ttu-id="ce086-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce086-154">RELATED LINKS</span></span>
