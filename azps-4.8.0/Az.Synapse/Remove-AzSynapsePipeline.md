---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955851"
---
# <span data-ttu-id="092af-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="092af-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="092af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="092af-102">SYNOPSIS</span></span>
<span data-ttu-id="092af-103">Remove um pipeline do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="092af-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="092af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="092af-104">SYNTAX</span></span>

### <span data-ttu-id="092af-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="092af-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="092af-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="092af-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="092af-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="092af-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="092af-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="092af-108">DESCRIPTION</span></span>
<span data-ttu-id="092af-109">O cmdlet **Remove-AzSynapsePipeline** remove um pipeline do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="092af-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="092af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="092af-110">EXAMPLES</span></span>

### <span data-ttu-id="092af-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="092af-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="092af-112">Esse cmdlet Remove o pipeline chamado ContosoPipeline do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="092af-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="092af-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="092af-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="092af-114">Esse cmdlet Remove o pipeline chamado ContosoPipeline do espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="092af-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="092af-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="092af-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="092af-116">Esse cmdlet Remove o pipeline chamado ContosoPipeline do espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="092af-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="092af-117">OS</span><span class="sxs-lookup"><span data-stu-id="092af-117">PARAMETERS</span></span>

### <span data-ttu-id="092af-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="092af-118">-AsJob</span></span>
<span data-ttu-id="092af-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="092af-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="092af-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="092af-120">-DefaultProfile</span></span>
<span data-ttu-id="092af-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="092af-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="092af-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="092af-122">-InputObject</span></span>
<span data-ttu-id="092af-123">O objeto de pipeline.</span><span class="sxs-lookup"><span data-stu-id="092af-123">The pipeline object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource
Parameter Sets: NewByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="092af-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="092af-124">-Name</span></span>
<span data-ttu-id="092af-125">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="092af-125">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="092af-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="092af-126">-PassThru</span></span>
<span data-ttu-id="092af-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="092af-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="092af-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="092af-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="092af-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="092af-129">-WorkspaceName</span></span>
<span data-ttu-id="092af-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="092af-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="092af-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="092af-131">-WorkspaceObject</span></span>
<span data-ttu-id="092af-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="092af-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="092af-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="092af-133">-Confirm</span></span>
<span data-ttu-id="092af-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="092af-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="092af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="092af-135">-WhatIf</span></span>
<span data-ttu-id="092af-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="092af-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="092af-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="092af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="092af-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="092af-138">CommonParameters</span></span>
<span data-ttu-id="092af-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="092af-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="092af-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="092af-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="092af-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="092af-141">INPUTS</span></span>

### <span data-ttu-id="092af-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="092af-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="092af-143">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="092af-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="092af-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="092af-144">OUTPUTS</span></span>

### <span data-ttu-id="092af-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="092af-145">System.Boolean</span></span>

## <span data-ttu-id="092af-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="092af-146">NOTES</span></span>

## <span data-ttu-id="092af-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="092af-147">RELATED LINKS</span></span>
