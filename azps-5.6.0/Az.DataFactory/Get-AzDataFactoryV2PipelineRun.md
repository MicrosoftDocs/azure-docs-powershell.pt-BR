---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: 68c524f2c8712b0da0600abda2fa8035dd5a979c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888278"
---
# <span data-ttu-id="564df-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="564df-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="564df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="564df-102">SYNOPSIS</span></span>
<span data-ttu-id="564df-103">Obtém informações sobre as executações de pipeline.</span><span class="sxs-lookup"><span data-stu-id="564df-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="564df-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="564df-104">SYNTAX</span></span>

### <span data-ttu-id="564df-105">ByFactoryNameByRunId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="564df-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564df-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="564df-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="564df-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="564df-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="564df-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="564df-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="564df-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="564df-109">DESCRIPTION</span></span>
<span data-ttu-id="564df-110">O **comando Get-AzDataFactoryV2PipelineRun** retorna informações sobre as executações para o pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="564df-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="564df-111">Se PipelineRunId for especificado, ele mostrará detalhes para a executar com essa ID.</span><span class="sxs-lookup"><span data-stu-id="564df-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="564df-112">Se PipelineRunId não for especificado, ele mostrará informações sobre todas as executações para os pipelines que aconteceram entre os valores de LastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="564df-112">If the PipelineRunId is not specified, then it shows information about all runs for the pipelines that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="564df-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="564df-113">EXAMPLES</span></span>

### <span data-ttu-id="564df-114">Exemplo 1: obter informações para uma corrida de pipeline</span><span class="sxs-lookup"><span data-stu-id="564df-114">Example 1: Get information for a pipeline run</span></span>
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

<span data-ttu-id="564df-115">Este comando obtém detalhes sobre o pipeline executado com a ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="564df-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="564df-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="564df-116">PARAMETERS</span></span>

### <span data-ttu-id="564df-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="564df-117">-DataFactory</span></span>
<span data-ttu-id="564df-118">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="564df-118">The data factory object.</span></span>

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

### <span data-ttu-id="564df-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="564df-119">-DataFactoryName</span></span>
<span data-ttu-id="564df-120">O nome da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="564df-120">The data factory name.</span></span>

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

### <span data-ttu-id="564df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564df-121">-DefaultProfile</span></span>
<span data-ttu-id="564df-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="564df-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="564df-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="564df-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="564df-124">O momento em que o pipeline foi executado foi atualizado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="564df-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="564df-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="564df-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="564df-126">A hora em que o pipeline foi executado foi atualizado no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="564df-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="564df-127">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="564df-127">-PipelineName</span></span>
<span data-ttu-id="564df-128">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="564df-128">The pipeline name.</span></span>

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

### <span data-ttu-id="564df-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="564df-129">-PipelineRunId</span></span>
<span data-ttu-id="564df-130">A ID de executar do pipeline.</span><span class="sxs-lookup"><span data-stu-id="564df-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="564df-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564df-131">-ResourceGroupName</span></span>
<span data-ttu-id="564df-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="564df-132">The resource group name.</span></span>

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

### <span data-ttu-id="564df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564df-133">CommonParameters</span></span>
<span data-ttu-id="564df-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="564df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564df-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="564df-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564df-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="564df-136">INPUTS</span></span>

### <span data-ttu-id="564df-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="564df-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="564df-138">System.String</span><span class="sxs-lookup"><span data-stu-id="564df-138">System.String</span></span>

## <span data-ttu-id="564df-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="564df-139">OUTPUTS</span></span>

### <span data-ttu-id="564df-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="564df-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="564df-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="564df-141">NOTES</span></span>

## <span data-ttu-id="564df-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="564df-142">RELATED LINKS</span></span>

[<span data-ttu-id="564df-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="564df-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="564df-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="564df-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

