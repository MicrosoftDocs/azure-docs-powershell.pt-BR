---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipeline.md
ms.openlocfilehash: 6224a871aebff834693c8eed3026a75f22879ffa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118553"
---
# <span data-ttu-id="a2a3c-101">Get-AzSynapsePipeline</span><span class="sxs-lookup"><span data-stu-id="a2a3c-101">Get-AzSynapsePipeline</span></span>

## <span data-ttu-id="a2a3c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a2a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="a2a3c-103">Obtém informações sobre pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-103">Gets information about pipelines in workspace.</span></span>

## <span data-ttu-id="a2a3c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2a3c-104">SYNTAX</span></span>

### <span data-ttu-id="a2a3c-105">GetByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a2a3c-105">GetByName (Default)</span></span>
```
Get-AzSynapsePipeline -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2a3c-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="a2a3c-106">GetByObject</span></span>
```
Get-AzSynapsePipeline -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2a3c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2a3c-107">DESCRIPTION</span></span>
<span data-ttu-id="a2a3c-108">O cmdlet **Get-AzSynapse Pipelineline** obtém informações sobre pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-108">The **Get-AzSynapsePipeline** cmdlet gets information about pipelines in workspace.</span></span> <span data-ttu-id="a2a3c-109">Se você especificar o nome de um pipeline, este cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span> <span data-ttu-id="a2a3c-110">Se você não especificar um nome, este cmdlet obterá informações sobre todos os pipelines no espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the workspace.</span></span>

## <span data-ttu-id="a2a3c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a2a3c-111">EXAMPLES</span></span>

### <span data-ttu-id="a2a3c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2a3c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="a2a3c-113">Esse comando obtém informações sobre todos os pipelines no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-113">This command gets information about all pipelines in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a2a3c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a2a3c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapsePipeline -WorkspaceName ContosoWorkspace -Name ContosoPipeline
```

<span data-ttu-id="a2a3c-115">Este comando obtém informações sobre o pipeline chamado Contoso Pipeline no espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-115">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="a2a3c-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a2a3c-116">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapsePipeline -Name ContosoPipeline
```

<span data-ttu-id="a2a3c-117">Este comando obtém informações sobre o pipeline chamado Contoso Pipeline no espaço de trabalho chamado ContosoWorkspace por meio de pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-117">This command gets information about the pipeline named ContosoPipeline in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="a2a3c-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2a3c-118">PARAMETERS</span></span>

### <span data-ttu-id="a2a3c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2a3c-119">-DefaultProfile</span></span>
<span data-ttu-id="a2a3c-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2a3c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2a3c-121">-Name</span></span>
<span data-ttu-id="a2a3c-122">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-122">The pipeline name.</span></span>

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

### <span data-ttu-id="a2a3c-123">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="a2a3c-123">-WorkspaceName</span></span>
<span data-ttu-id="a2a3c-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a2a3c-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a2a3c-125">-WorkspaceObject</span></span>
<span data-ttu-id="a2a3c-126">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a2a3c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2a3c-127">CommonParameters</span></span>
<span data-ttu-id="a2a3c-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2a3c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2a3c-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2a3c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2a3c-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="a2a3c-130">INPUTS</span></span>

### <span data-ttu-id="a2a3c-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a2a3c-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a2a3c-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="a2a3c-132">OUTPUTS</span></span>

### <span data-ttu-id="a2a3c-133">Microsoft.Azure.Commands.Synapse.Models.PS ElelineResource</span><span class="sxs-lookup"><span data-stu-id="a2a3c-133">Microsoft.Azure.Commands.Synapse.Models.PSPipelineResource</span></span>

## <span data-ttu-id="a2a3c-134">Notas</span><span class="sxs-lookup"><span data-stu-id="a2a3c-134">NOTES</span></span>

## <span data-ttu-id="a2a3c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2a3c-135">RELATED LINKS</span></span>
