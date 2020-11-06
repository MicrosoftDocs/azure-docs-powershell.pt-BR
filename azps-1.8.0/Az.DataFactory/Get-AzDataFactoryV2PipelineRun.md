---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2PipelineRun.md
ms.openlocfilehash: eba11e68d23c852426a7d4541359874bd813fc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601150"
---
# <span data-ttu-id="96c07-101">Get-AzDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="96c07-101">Get-AzDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="96c07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96c07-102">SYNOPSIS</span></span>
<span data-ttu-id="96c07-103">Obtém informações sobre execuções de pipeline.</span><span class="sxs-lookup"><span data-stu-id="96c07-103">Gets information about pipeline runs.</span></span>

## <span data-ttu-id="96c07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96c07-104">SYNTAX</span></span>

### <span data-ttu-id="96c07-105">ByFactoryNameByRunId (padrão)</span><span class="sxs-lookup"><span data-stu-id="96c07-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c07-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="96c07-106">ByFactoryObjectByRunId</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96c07-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="96c07-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96c07-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="96c07-108">ByFactoryNameByPipeline</span></span>
```
Get-AzDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c07-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96c07-109">DESCRIPTION</span></span>
<span data-ttu-id="96c07-110">O comando **Get-AzDataFactoryV2PipelineRun** retorna informações sobre execuções para o pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="96c07-110">The **Get-AzDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="96c07-111">Se PipelineRunId for especificado, exibirá detalhes para a execução com essa ID.</span><span class="sxs-lookup"><span data-stu-id="96c07-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="96c07-112">Se o PipelineRunId não for especificado, ele exibirá informações sobre todas as execuções para o pipeline especificado que aconteceu entre os valores de LastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="96c07-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="96c07-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96c07-113">EXAMPLES</span></span>

### <span data-ttu-id="96c07-114">Exemplo 1: obter informações para uma execução do pipline</span><span class="sxs-lookup"><span data-stu-id="96c07-114">Example 1: Get information for a pipline run</span></span>
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

<span data-ttu-id="96c07-115">Esse comando obtém detalhes sobre o pipeline executado com ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="96c07-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="96c07-116">OS</span><span class="sxs-lookup"><span data-stu-id="96c07-116">PARAMETERS</span></span>

### <span data-ttu-id="96c07-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="96c07-117">-DataFactory</span></span>
<span data-ttu-id="96c07-118">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="96c07-118">The data factory object.</span></span>

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

### <span data-ttu-id="96c07-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="96c07-119">-DataFactoryName</span></span>
<span data-ttu-id="96c07-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="96c07-120">The data factory name.</span></span>

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

### <span data-ttu-id="96c07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c07-121">-DefaultProfile</span></span>
<span data-ttu-id="96c07-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96c07-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c07-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="96c07-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="96c07-124">O horário em que a execução do pipeline foi atualizada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="96c07-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="96c07-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="96c07-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="96c07-126">O horário em ou antes do qual a execução do pipeline foi atualizada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="96c07-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

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

### <span data-ttu-id="96c07-127">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="96c07-127">-PipelineName</span></span>
<span data-ttu-id="96c07-128">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="96c07-128">The pipeline name.</span></span>

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

### <span data-ttu-id="96c07-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="96c07-129">-PipelineRunId</span></span>
<span data-ttu-id="96c07-130">A ID de execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="96c07-130">The Run ID of the pipeline.</span></span>

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

### <span data-ttu-id="96c07-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c07-131">-ResourceGroupName</span></span>
<span data-ttu-id="96c07-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="96c07-132">The resource group name.</span></span>

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

### <span data-ttu-id="96c07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c07-133">CommonParameters</span></span>
<span data-ttu-id="96c07-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c07-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96c07-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c07-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96c07-136">INPUTS</span></span>

### <span data-ttu-id="96c07-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="96c07-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="96c07-138">System. String</span><span class="sxs-lookup"><span data-stu-id="96c07-138">System.String</span></span>

## <span data-ttu-id="96c07-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96c07-139">OUTPUTS</span></span>

### <span data-ttu-id="96c07-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="96c07-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="96c07-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96c07-141">NOTES</span></span>

## <span data-ttu-id="96c07-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96c07-142">RELATED LINKS</span></span>

[<span data-ttu-id="96c07-143">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="96c07-143">Invoke-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="96c07-144">Get-AzDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="96c07-144">Get-AzDataFactoryV2ActivityRun</span></span>]()

