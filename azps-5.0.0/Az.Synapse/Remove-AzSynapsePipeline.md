---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapsePipeline.md
ms.openlocfilehash: f28abbca41c68ce08e516fb52f69b7de8c54e67a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117926"
---
# <span data-ttu-id="8e2aa-101">Remove-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="8e2aa-101">Remove-AzSynapsePipeline</span></span>

## <span data-ttu-id="8e2aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2aa-103">Remove um pipeline do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-103">Removes a pipeline from workspace.</span></span>

## <span data-ttu-id="8e2aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e2aa-104">SYNTAX</span></span>

### <span data-ttu-id="8e2aa-105">RemoveByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8e2aa-105">RemoveByName (Default)</span></span>
```
Remove-AzSynapsePipeline -WorkspaceName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e2aa-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="8e2aa-106">RemoveByObject</span></span>
```
Remove-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e2aa-107">NewByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e2aa-107">NewByInputObject</span></span>
```
Remove-AzSynapsePipeline -Name <String> -InputObject <PSPipelineResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e2aa-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e2aa-108">DESCRIPTION</span></span>
<span data-ttu-id="8e2aa-109">O cmdlet **Remove-AzSynapsePipeline** remove um pipeline do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-109">The **Remove-AzSynapsePipeline** cmdlet removes a pipeline from workspace.</span></span>

## <span data-ttu-id="8e2aa-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e2aa-110">EXAMPLES</span></span>

### <span data-ttu-id="8e2aa-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e2aa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="8e2aa-112">Esse cmdlet Remove o pipeline chamado ContosoPipeline do espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-112">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="8e2aa-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8e2aa-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="8e2aa-114">Esse cmdlet Remove o pipeline chamado ContosoPipeline do espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-114">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

### <span data-ttu-id="8e2aa-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="8e2aa-115">Example 3</span></span>
```powershell
PS C:\> $pipeline = Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
PS C:\> $pipeline | Remove-AzSynapsePipeline
```

<span data-ttu-id="8e2aa-116">Esse cmdlet Remove o pipeline chamado ContosoPipeline do espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-116">This cmdlet removes the pipeline named ContosoPipeline from the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="8e2aa-117">OS</span><span class="sxs-lookup"><span data-stu-id="8e2aa-117">PARAMETERS</span></span>

### <span data-ttu-id="8e2aa-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e2aa-118">-AsJob</span></span>
<span data-ttu-id="8e2aa-119">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8e2aa-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e2aa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2aa-120">-DefaultProfile</span></span>
<span data-ttu-id="8e2aa-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e2aa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e2aa-122">-InputObject</span></span>
<span data-ttu-id="8e2aa-123">O objeto de pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-123">The pipeline object.</span></span>

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

### <span data-ttu-id="8e2aa-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8e2aa-124">-Name</span></span>
<span data-ttu-id="8e2aa-125">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-125">The pipeline name.</span></span>

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

### <span data-ttu-id="8e2aa-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e2aa-126">-PassThru</span></span>
<span data-ttu-id="8e2aa-127">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-127">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8e2aa-128">Se essa opção for especificada, retornará true se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8e2aa-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e2aa-129">-WorkspaceName</span></span>
<span data-ttu-id="8e2aa-130">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8e2aa-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="8e2aa-131">-WorkspaceObject</span></span>
<span data-ttu-id="8e2aa-132">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-132">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8e2aa-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e2aa-133">-Confirm</span></span>
<span data-ttu-id="8e2aa-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2aa-135">-WhatIf</span></span>
<span data-ttu-id="8e2aa-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e2aa-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2aa-138">CommonParameters</span></span>
<span data-ttu-id="8e2aa-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2aa-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e2aa-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2aa-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e2aa-141">INPUTS</span></span>

### <span data-ttu-id="8e2aa-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e2aa-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8e2aa-143">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="8e2aa-143">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="8e2aa-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e2aa-144">OUTPUTS</span></span>

### <span data-ttu-id="8e2aa-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e2aa-145">System.Boolean</span></span>

## <span data-ttu-id="8e2aa-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e2aa-146">NOTES</span></span>

## <span data-ttu-id="8e2aa-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e2aa-147">RELATED LINKS</span></span>
