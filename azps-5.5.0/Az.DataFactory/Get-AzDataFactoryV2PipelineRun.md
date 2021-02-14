---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 889cffd16c836c5f895a9eb587c14cfbe66a45b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116433"
---
# <span data-ttu-id="0b2a6-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="0b2a6-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="0b2a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b2a6-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2a6-103">Obtém informações sobre o pipeline executado.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="0b2a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b2a6-104">SYNTAX</span></span>

### <span data-ttu-id="0b2a6-105">ByFactoryNameByRunId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0b2a6-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b2a6-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="0b2a6-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b2a6-107">ByFactoryObjectByBjectByBjline</span><span class="sxs-lookup"><span data-stu-id="0b2a6-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b2a6-108">ByFactoryNameByNameLine</span><span class="sxs-lookup"><span data-stu-id="0b2a6-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b2a6-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b2a6-109">DESCRIPTION</span></span>
<span data-ttu-id="0b2a6-110">O **comando Get-AzDataFactoryV2 PipelineRun** retorna informações sobre as executados para o pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="0b2a6-111">Se PipelineRunId for especificado, ele mostrará detalhes para a executar com essa ID.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="0b2a6-112">Se o PipelineRunId não for especificado, ele mostrará informações sobre todas as executados para os pipelines que aconteceram entre os valores lastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="0b2a6-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b2a6-113">EXAMPLES</span></span>

### <span data-ttu-id="0b2a6-114">Exemplo 1: Obter informações para uma adoção de pipeline</span><span class="sxs-lookup"><span data-stu-id="0b2a6-114">Example 1: Get information for a pipeline run</span></span>
```
PS C:\> Get-AzDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    RunId             : 61eb095a-fe23-4591-8a97-fade6c65ca72
    PipelineName      : DPWikisample
    LastUpdated       : 9/14/2017 12:21:02 AM
    Parameters        : {[url, http://adfsamplewebapi.azurewebsites.net/api/execute/sample]}
    RunStart          : 9/14/2017 12:20:54 AM
    RunEnd            : 9/14/2017 12:21:02 AM
    DurationInMs      : 8246
    Status            : Succeeded
    Message           :
```

<span data-ttu-id="0b2a6-115">Este comando obtém detalhes sobre o pipeline executado com a ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="0b2a6-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="0b2a6-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b2a6-116">PARAMETERS</span></span>

### <span data-ttu-id="0b2a6-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0b2a6-117">-DataFactory</span></span>
<span data-ttu-id="0b2a6-118">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-118">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a6-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0b2a6-119">-DataFactoryName</span></span>
<span data-ttu-id="0b2a6-120">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-120">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2a6-121">-DefaultProfile</span></span>
<span data-ttu-id="0b2a6-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b2a6-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="0b2a6-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="0b2a6-124">O horário em que o pipeline foi executado ou depois foi atualizado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a6-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="0b2a6-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="0b2a6-126">O momento em que o pipeline foi executado foi atualizado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a6-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="0b2a6-127">-PipelineName</span></span>
<span data-ttu-id="0b2a6-128">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-128">The pipeline name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a6-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="0b2a6-129">-PipelineRunId</span></span>
<span data-ttu-id="0b2a6-130">A ID de Executar do pipeline.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-130">The Run ID of the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2a6-131">-ResourceGroupName</span></span>
<span data-ttu-id="0b2a6-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2a6-133">CommonParameters</span></span>
<span data-ttu-id="0b2a6-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2a6-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2a6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2a6-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b2a6-136">INPUTS</span></span>

### <span data-ttu-id="0b2a6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0b2a6-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="0b2a6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0b2a6-138">System.String</span></span>

## <span data-ttu-id="0b2a6-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b2a6-139">OUTPUTS</span></span>

### <span data-ttu-id="0b2a6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PS Ltd.</span><span class="sxs-lookup"><span data-stu-id="0b2a6-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="0b2a6-141">Notas</span><span class="sxs-lookup"><span data-stu-id="0b2a6-141">NOTES</span></span>

## <span data-ttu-id="0b2a6-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b2a6-142">RELATED LINKS</span></span>

[<span data-ttu-id="0b2a6-143">Invoke-AzDataFactoryV2 Invokeline</span><span class="sxs-lookup"><span data-stu-id="0b2a6-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="0b2a6-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="0b2a6-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

