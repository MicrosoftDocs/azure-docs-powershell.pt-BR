---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 98c0f5ed1dee4c5cd25c69a1a88e596a2f99a7c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890339"
---
# <span data-ttu-id="4bae7-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="4bae7-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="4bae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bae7-102">SYNOPSIS</span></span>
<span data-ttu-id="4bae7-103">Obtém informações sobre as executações de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bae7-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="4bae7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4bae7-104">SYNTAX</span></span>

### <span data-ttu-id="4bae7-105">GetByNameAndId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4bae7-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bae7-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="4bae7-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bae7-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="4bae7-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bae7-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="4bae7-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bae7-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4bae7-109">DESCRIPTION</span></span>
<span data-ttu-id="4bae7-110">O **comando Get-AzSynapsePipelineRun** retorna informações sobre as executações para o pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="4bae7-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="4bae7-111">Se PipelineRunId for especificado, ele mostrará detalhes para a executar com essa ID.</span><span class="sxs-lookup"><span data-stu-id="4bae7-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="4bae7-112">Se PipelineRunId não for especificado, ele mostrará informações sobre todas as executações para os pipelines que aconteceram entre os valores de RunStartedAfter e RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="4bae7-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="4bae7-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4bae7-113">EXAMPLES</span></span>

### <span data-ttu-id="4bae7-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4bae7-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="4bae7-115">Este comando obtém detalhes sobre o pipeline executado com a ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="4bae7-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="4bae7-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4bae7-116">PARAMETERS</span></span>

### <span data-ttu-id="4bae7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bae7-117">-DefaultProfile</span></span>
<span data-ttu-id="4bae7-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4bae7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bae7-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4bae7-119">-PipelineName</span></span>
<span data-ttu-id="4bae7-120">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bae7-120">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bae7-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4bae7-121">-PipelineRunId</span></span>
<span data-ttu-id="4bae7-122">O identificador de executar pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bae7-122">The pipeline run identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByObjectAndId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bae7-123">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="4bae7-123">-RunStartedAfter</span></span>
<span data-ttu-id="4bae7-124">A hora em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="4bae7-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bae7-125">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="4bae7-125">-RunStartedBefore</span></span>
<span data-ttu-id="4bae7-126">A hora em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="4bae7-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: GetByNameAndTime, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bae7-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4bae7-127">-WorkspaceName</span></span>
<span data-ttu-id="4bae7-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4bae7-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndId, GetByNameAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bae7-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4bae7-129">-WorkspaceObject</span></span>
<span data-ttu-id="4bae7-130">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4bae7-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObjectAndId, GetByObjectAndTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bae7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bae7-131">CommonParameters</span></span>
<span data-ttu-id="4bae7-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bae7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bae7-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bae7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bae7-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bae7-134">INPUTS</span></span>

### <span data-ttu-id="4bae7-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4bae7-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4bae7-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4bae7-136">OUTPUTS</span></span>

### <span data-ttu-id="4bae7-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="4bae7-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="4bae7-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="4bae7-138">NOTES</span></span>

## <span data-ttu-id="4bae7-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4bae7-139">RELATED LINKS</span></span>
