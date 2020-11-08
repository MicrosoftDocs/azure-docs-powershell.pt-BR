---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118455"
---
# <span data-ttu-id="02a28-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="02a28-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="02a28-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02a28-102">SYNOPSIS</span></span>
<span data-ttu-id="02a28-103">Obtém informações sobre pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="02a28-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="02a28-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02a28-104">SYNTAX</span></span>

### <span data-ttu-id="02a28-105">GetByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="02a28-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02a28-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="02a28-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a28-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02a28-107">DESCRIPTION</span></span>
<span data-ttu-id="02a28-108">O cmdlet **Get-AzSynapsePipeline** Obtém informações sobre pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="02a28-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="02a28-109">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="02a28-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="02a28-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as tubulações no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="02a28-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="02a28-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02a28-111">EXAMPLES</span></span>

### <span data-ttu-id="02a28-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02a28-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="02a28-113">Esse comando obtém informações sobre todos os pipelines no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="02a28-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="02a28-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="02a28-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="02a28-115">Esse comando obtém informações sobre o pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="02a28-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="02a28-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="02a28-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="02a28-117">Esse comando obtém informações sobre o pipeline chamado ContosoPipeline no espaço de trabalho chamado ContosoWorkspace pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="02a28-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="02a28-118">OS</span><span class="sxs-lookup"><span data-stu-id="02a28-118">PARAMETERS</span></span>

### <span data-ttu-id="02a28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a28-119">-DefaultProfile</span></span>
<span data-ttu-id="02a28-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02a28-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a28-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="02a28-121">-Name</span></span>
<span data-ttu-id="02a28-122">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="02a28-122">The pipeline name.</span></span>

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

### <span data-ttu-id="02a28-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02a28-123">-WorkspaceName</span></span>
<span data-ttu-id="02a28-124">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="02a28-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="02a28-125">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="02a28-125">-WorkspaceObject</span></span>
<span data-ttu-id="02a28-126">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="02a28-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="02a28-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a28-127">CommonParameters</span></span>
<span data-ttu-id="02a28-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a28-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a28-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02a28-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a28-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02a28-130">INPUTS</span></span>

### <span data-ttu-id="02a28-131">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="02a28-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="02a28-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02a28-132">OUTPUTS</span></span>

### <span data-ttu-id="02a28-133">Microsoft. Azure. Commands. Synapse. Models. PSPipelineResource</span><span class="sxs-lookup"><span data-stu-id="02a28-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="02a28-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02a28-134">NOTES</span></span>

## <span data-ttu-id="02a28-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02a28-135">RELATED LINKS</span></span>
