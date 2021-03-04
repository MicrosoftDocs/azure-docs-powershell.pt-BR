---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6161a0ca463973fad1ac7bac5df6487cf23cd0e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887285"
---
# <span data-ttu-id="d0cce-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="d0cce-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="d0cce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0cce-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cce-103">Obtém informações sobre pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0cce-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="d0cce-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d0cce-104">SYNTAX</span></span>

### <span data-ttu-id="d0cce-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d0cce-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0cce-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d0cce-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0cce-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d0cce-107">DESCRIPTION</span></span>
<span data-ttu-id="d0cce-108">O cmdlet **Get-AzSynapsePipeline** obtém informações sobre pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0cce-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="d0cce-109">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0cce-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="d0cce-110">Se você não especificar um nome, este cmdlet obterá informações sobre todos os pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d0cce-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="d0cce-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0cce-111">EXAMPLES</span></span>

### <span data-ttu-id="d0cce-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0cce-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d0cce-113">Este comando obtém informações sobre todos os pipelines no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d0cce-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d0cce-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d0cce-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="d0cce-115">Este comando obtém informações sobre o pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="d0cce-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d0cce-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d0cce-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="d0cce-117">Este comando obtém informações sobre o pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace por pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0cce-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d0cce-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d0cce-118">PARAMETERS</span></span>

### <span data-ttu-id="d0cce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cce-119">-DefaultProfile</span></span>
<span data-ttu-id="d0cce-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0cce-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d0cce-121">-Name</span></span>
<span data-ttu-id="d0cce-122">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0cce-122">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cce-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0cce-123">-WorkspaceName</span></span>
<span data-ttu-id="d0cce-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="d0cce-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0cce-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d0cce-125">-WorkspaceObject</span></span>
<span data-ttu-id="d0cce-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="d0cce-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0cce-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cce-127">CommonParameters</span></span>
<span data-ttu-id="d0cce-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0cce-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cce-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0cce-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cce-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0cce-130">INPUTS</span></span>

### <span data-ttu-id="d0cce-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d0cce-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d0cce-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d0cce-132">OUTPUTS</span></span>

### <span data-ttu-id="d0cce-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="d0cce-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="d0cce-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="d0cce-134">NOTES</span></span>

## <span data-ttu-id="d0cce-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0cce-135">RELATED LINKS</span></span>
