---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapsePipeline.md
ms.openlocfilehash: cd79d9315c6352b604a40269286073792596a41e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890542"
---
# <span data-ttu-id="7929c-101">Set-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="7929c-101">Set-AzSynapsePipeline</span></span>

## <span data-ttu-id="7929c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7929c-102">SYNOPSIS</span></span>
<span data-ttu-id="7929c-103">Cria um pipeline no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7929c-103">Creates a pipeline in workspace.</span></span>

## <span data-ttu-id="7929c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7929c-104">SYNTAX</span></span>

### <span data-ttu-id="7929c-105">SetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7929c-105">SetByName (Default)</span></span>
```
Set-AzSynapsePipeline -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7929c-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="7929c-106">SetByObject</span></span>
```
Set-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7929c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7929c-107">DESCRIPTION</span></span>
<span data-ttu-id="7929c-108">O cmdlet **Set-AzSynapsePipeline** cria um pipeline no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7929c-108">The **Set-AzSynapsePipeline** cmdlet creates a pipeline in workspace.</span></span>

## <span data-ttu-id="7929c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7929c-109">EXAMPLES</span></span>

### <span data-ttu-id="7929c-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7929c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="7929c-111">Este comando cria um pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7929c-111">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="7929c-112">O comando baseia o pipeline em informações no arquivo pipeline.json.</span><span class="sxs-lookup"><span data-stu-id="7929c-112">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="7929c-113">Esse arquivo inclui informações sobre atividades.</span><span class="sxs-lookup"><span data-stu-id="7929c-113">This file includes information about activities.</span></span>

### <span data-ttu-id="7929c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7929c-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapsePipeline -Name ContosoPipeline -DefinitionFile "C:\pipeline.json"
```

<span data-ttu-id="7929c-115">Este comando cria um pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="7929c-115">This command creates a pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>
<span data-ttu-id="7929c-116">O comando baseia o pipeline em informações no arquivo pipeline.json.</span><span class="sxs-lookup"><span data-stu-id="7929c-116">The command bases the pipeline on information in the pipeline.json file.</span></span>
<span data-ttu-id="7929c-117">Esse arquivo inclui informações sobre atividades.</span><span class="sxs-lookup"><span data-stu-id="7929c-117">This file includes information about activities.</span></span>

## <span data-ttu-id="7929c-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7929c-118">PARAMETERS</span></span>

### <span data-ttu-id="7929c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7929c-119">-AsJob</span></span>
<span data-ttu-id="7929c-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7929c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7929c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7929c-121">-DefaultProfile</span></span>
<span data-ttu-id="7929c-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7929c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7929c-123">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7929c-123">-DefinitionFile</span></span>
<span data-ttu-id="7929c-124">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="7929c-124">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7929c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7929c-125">-Name</span></span>
<span data-ttu-id="7929c-126">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="7929c-126">The pipeline name.</span></span>

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

### <span data-ttu-id="7929c-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7929c-127">-WorkspaceName</span></span>
<span data-ttu-id="7929c-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="7929c-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7929c-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7929c-129">-WorkspaceObject</span></span>
<span data-ttu-id="7929c-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7929c-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7929c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7929c-131">-Confirm</span></span>
<span data-ttu-id="7929c-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7929c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7929c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7929c-133">-WhatIf</span></span>
<span data-ttu-id="7929c-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7929c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7929c-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7929c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7929c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7929c-136">CommonParameters</span></span>
<span data-ttu-id="7929c-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7929c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7929c-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7929c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7929c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7929c-139">INPUTS</span></span>

### <span data-ttu-id="7929c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7929c-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7929c-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7929c-141">OUTPUTS</span></span>

### <span data-ttu-id="7929c-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="7929c-142">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="7929c-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="7929c-143">NOTES</span></span>

## <span data-ttu-id="7929c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7929c-144">RELATED LINKS</span></span>
