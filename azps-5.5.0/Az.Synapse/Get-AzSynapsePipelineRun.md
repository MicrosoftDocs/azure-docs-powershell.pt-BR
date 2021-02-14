---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsepipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapsePipelineRun.md
ms.openlocfilehash: 365311b156b8bd6f2c61da760c6b82a3b2d5dfb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116061"
---
# <span data-ttu-id="4c838-101">Get-AzSynapsePipelineRun</span><span class="sxs-lookup"><span data-stu-id="4c838-101">Get-AzSynapsePipelineRun</span></span>

## <span data-ttu-id="4c838-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c838-102">SYNOPSIS</span></span>
<span data-ttu-id="4c838-103">Obtém informações sobre o pipeline executado.</span><span class="sxs-lookup"><span data-stu-id="4c838-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="4c838-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c838-104">SYNTAX</span></span>

### <span data-ttu-id="4c838-105">GetByNameAndId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4c838-105">GetByNameAndId (Default)</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c838-106">GetByNameAndTime</span><span class="sxs-lookup"><span data-stu-id="4c838-106">GetByNameAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceName <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c838-107">GetByObjectAndId</span><span class="sxs-lookup"><span data-stu-id="4c838-107">GetByObjectAndId</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -PipelineRunId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c838-108">GetByObjectAndTime</span><span class="sxs-lookup"><span data-stu-id="4c838-108">GetByObjectAndTime</span></span>
```
Get-AzSynapsePipelineRun -WorkspaceObject <PSSynapseWorkspace> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-PipelineName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c838-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c838-109">DESCRIPTION</span></span>
<span data-ttu-id="4c838-110">O **comando Get-AzSynapse PipelineRun retorna** informações sobre as executados para o pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="4c838-110">The **Get-AzSynapsePipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="4c838-111">Se PipelineRunId for especificado, ele mostrará detalhes para a executar com essa ID.</span><span class="sxs-lookup"><span data-stu-id="4c838-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="4c838-112">Se o PipelineRunId não for especificado, ele mostrará informações sobre todas as executados para os pipelines que aconteceram entre os valores de RunStartedAfter e RunStartedBefore.</span><span class="sxs-lookup"><span data-stu-id="4c838-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of RunStartedAfter and RunStartedBefore.</span></span>

## <span data-ttu-id="4c838-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c838-113">EXAMPLES</span></span>

### <span data-ttu-id="4c838-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c838-114">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapsePipelineRun -WorkspaceName ContosoWorkspace -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"
```

<span data-ttu-id="4c838-115">Este comando obtém detalhes sobre o pipeline executado com a ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="4c838-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="4c838-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c838-116">PARAMETERS</span></span>

### <span data-ttu-id="4c838-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c838-117">-DefaultProfile</span></span>
<span data-ttu-id="4c838-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c838-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c838-119">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="4c838-119">-PipelineName</span></span>
<span data-ttu-id="4c838-120">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c838-120">The pipeline name.</span></span>

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

### <span data-ttu-id="4c838-121">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4c838-121">-PipelineRunId</span></span>
<span data-ttu-id="4c838-122">O identificador de executar pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c838-122">The pipeline run identifier.</span></span>

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

### <span data-ttu-id="4c838-123">-ExecutarStartedAfter</span><span class="sxs-lookup"><span data-stu-id="4c838-123">-RunStartedAfter</span></span>
<span data-ttu-id="4c838-124">O horário em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="4c838-124">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="4c838-125">-ExecutarStartedBefore</span><span class="sxs-lookup"><span data-stu-id="4c838-125">-RunStartedBefore</span></span>
<span data-ttu-id="4c838-126">O horário em que o evento de executar foi atualizado no formato 'ISO 8601'.</span><span class="sxs-lookup"><span data-stu-id="4c838-126">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="4c838-127">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="4c838-127">-WorkspaceName</span></span>
<span data-ttu-id="4c838-128">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="4c838-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4c838-129">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4c838-129">-WorkspaceObject</span></span>
<span data-ttu-id="4c838-130">objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c838-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4c838-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c838-131">CommonParameters</span></span>
<span data-ttu-id="4c838-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c838-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c838-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c838-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c838-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c838-134">INPUTS</span></span>

### <span data-ttu-id="4c838-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4c838-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4c838-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c838-136">OUTPUTS</span></span>

### <span data-ttu-id="4c838-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="4c838-137">Microsoft.Azure.Commands.Synapse.Models.PSPipelineRun</span></span>

## <span data-ttu-id="4c838-138">Notas</span><span class="sxs-lookup"><span data-stu-id="4c838-138">NOTES</span></span>

## <span data-ttu-id="4c838-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c838-139">RELATED LINKS</span></span>
