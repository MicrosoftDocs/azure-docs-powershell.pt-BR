---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseDataset.md
ms.openlocfilehash: b70c30b7652c331571030917057339a9d2d7de3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886818"
---
# <span data-ttu-id="f2fe9-101">Remove-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="f2fe9-101">Remove-AzSynapseDataset</span></span>

## <span data-ttu-id="f2fe9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fe9-103">Remove um conjuntos de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-103">Removes a dataset from workspace.</span></span>

## <span data-ttu-id="f2fe9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f2fe9-104">SYNTAX</span></span>

### <span data-ttu-id="f2fe9-105">RemoveByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2fe9-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapseDataset -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fe9-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="f2fe9-106">RemoveByObject</span></span>
```
Remove-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2fe9-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2fe9-107">RemoveByInputObject</span></span>
```
Remove-AzSynapseDataset -InputObject <PSDatasetResource> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2fe9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f2fe9-108">DESCRIPTION</span></span>
<span data-ttu-id="f2fe9-109">O cmdlet **Remove-AzSynapseDataset** remove um conjuntos de dados do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-109">The **Remove-AzSynapseDataset** cmdlet removes a dataset from workspace.</span></span>

## <span data-ttu-id="f2fe9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2fe9-110">EXAMPLES</span></span>

### <span data-ttu-id="f2fe9-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f2fe9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="f2fe9-112">Este comando remove o conjuntos de dados chamado ContosoDataset do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-112">This command removes the dataset named ContosoDataset from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="f2fe9-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f2fe9-113">PARAMETERS</span></span>

### <span data-ttu-id="f2fe9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2fe9-114">-AsJob</span></span>
<span data-ttu-id="f2fe9-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f2fe9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2fe9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fe9-116">-DefaultProfile</span></span>
<span data-ttu-id="f2fe9-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2fe9-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f2fe9-118">-Force</span></span>
<span data-ttu-id="f2fe9-119">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f2fe9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2fe9-120">-InputObject</span></span>
<span data-ttu-id="f2fe9-121">O objeto dataset.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-121">The dataset object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fe9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f2fe9-122">-Name</span></span>
<span data-ttu-id="f2fe9-123">O nome do conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-123">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName, RemoveByObject
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2fe9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2fe9-124">-PassThru</span></span>
<span data-ttu-id="f2fe9-125">Este Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f2fe9-126">Se essa opção for especificada, ela retornará true se tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f2fe9-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f2fe9-127">-WorkspaceName</span></span>
<span data-ttu-id="f2fe9-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2fe9-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f2fe9-129">-WorkspaceObject</span></span>
<span data-ttu-id="f2fe9-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2fe9-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2fe9-131">-Confirm</span></span>
<span data-ttu-id="f2fe9-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2fe9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2fe9-133">-WhatIf</span></span>
<span data-ttu-id="f2fe9-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2fe9-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2fe9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fe9-136">CommonParameters</span></span>
<span data-ttu-id="f2fe9-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2fe9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2fe9-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2fe9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fe9-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2fe9-139">INPUTS</span></span>

### <span data-ttu-id="f2fe9-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f2fe9-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f2fe9-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="f2fe9-141">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="f2fe9-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f2fe9-142">OUTPUTS</span></span>

### <span data-ttu-id="f2fe9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2fe9-143">System.Boolean</span></span>

## <span data-ttu-id="f2fe9-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="f2fe9-144">NOTES</span></span>

## <span data-ttu-id="f2fe9-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2fe9-145">RELATED LINKS</span></span>
