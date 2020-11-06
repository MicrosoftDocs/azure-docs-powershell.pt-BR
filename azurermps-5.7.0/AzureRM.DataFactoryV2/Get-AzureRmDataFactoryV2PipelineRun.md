---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipelinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2PipelineRun.md
ms.openlocfilehash: 05adb3533604188aa5331d0d4b3f41a2aeba292d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440482"
---
# <span data-ttu-id="4908b-101">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="4908b-101">Get-AzureRmDataFactoryV2PipelineRun</span></span>

## <span data-ttu-id="4908b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4908b-102">SYNOPSIS</span></span>
<span data-ttu-id="4908b-103">Obtém informações sobre execuções de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4908b-103">Gets information about pipeline runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4908b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4908b-104">SYNTAX</span></span>

### <span data-ttu-id="4908b-105">ByFactoryNameByRunId (padrão)</span><span class="sxs-lookup"><span data-stu-id="4908b-105">ByFactoryNameByRunId (Default)</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineRunId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4908b-106">ByFactoryObjectByRunId</span><span class="sxs-lookup"><span data-stu-id="4908b-106">ByFactoryObjectByRunId</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-PipelineRunId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4908b-107">ByFactoryObjectByPipeline</span><span class="sxs-lookup"><span data-stu-id="4908b-107">ByFactoryObjectByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-DataFactory] <PSDataFactory> [-LastUpdatedAfter] <DateTime>
 [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4908b-108">ByFactoryNameByPipeline</span><span class="sxs-lookup"><span data-stu-id="4908b-108">ByFactoryNameByPipeline</span></span>
```
Get-AzureRmDataFactoryV2PipelineRun [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-LastUpdatedAfter] <DateTime> [-LastUpdatedBefore] <DateTime> [[-PipelineName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4908b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4908b-109">DESCRIPTION</span></span>
<span data-ttu-id="4908b-110">O comando **Get-AzureRmDataFactoryV2PipelineRun** retorna informações sobre execuções para o pipeline especificado.</span><span class="sxs-lookup"><span data-stu-id="4908b-110">The **Get-AzureRmDataFactoryV2PipelineRun** command returns information about runs for the specified pipeline.</span></span> <span data-ttu-id="4908b-111">Se PipelineRunId for especificado, exibirá detalhes para a execução com essa ID.</span><span class="sxs-lookup"><span data-stu-id="4908b-111">If PipelineRunId is specified, it shows details for the run with that ID.</span></span> <span data-ttu-id="4908b-112">Se o PipelineRunId não for especificado, ele exibirá informações sobre todas as execuções para o pipeline especificado que aconteceu entre os valores de LastUpdatedAfter e LastUpdatedBefore.</span><span class="sxs-lookup"><span data-stu-id="4908b-112">If the PipelineRunId is not specified, then it shows information about all runs for the specified pipeline that happened between the values of LastUpdatedAfter and LastUpdatedBefore.</span></span>

## <span data-ttu-id="4908b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4908b-113">EXAMPLES</span></span>

### <span data-ttu-id="4908b-114">Exemplo 1: obter informações para uma execução do pipline</span><span class="sxs-lookup"><span data-stu-id="4908b-114">Example 1: Get information for a pipline run</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2PipelineRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineRunId "61eb095a-fe23-4591-8a97-fade6c65ca72"

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

<span data-ttu-id="4908b-115">Esse comando obtém detalhes sobre o pipeline executado com ID "61eb095a-FE23-4591-8a97-fade6c65ca72".</span><span class="sxs-lookup"><span data-stu-id="4908b-115">This command gets details about the pipeline run with ID "61eb095a-fe23-4591-8a97-fade6c65ca72".</span></span>

## <span data-ttu-id="4908b-116">OS</span><span class="sxs-lookup"><span data-stu-id="4908b-116">PARAMETERS</span></span>

### <span data-ttu-id="4908b-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="4908b-117">-DataFactory</span></span>
<span data-ttu-id="4908b-118">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4908b-118">The data factory object.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObjectByRunId, ByFactoryObjectByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4908b-119">-DataFactoryName</span></span>
<span data-ttu-id="4908b-120">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="4908b-120">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4908b-121">-DefaultProfile</span></span>
<span data-ttu-id="4908b-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4908b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-123">-LastUpdatedAfter</span><span class="sxs-lookup"><span data-stu-id="4908b-123">-LastUpdatedAfter</span></span>
<span data-ttu-id="4908b-124">O horário em que a execução do pipeline foi atualizada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="4908b-124">The time at or after which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-125">-LastUpdatedBefore</span><span class="sxs-lookup"><span data-stu-id="4908b-125">-LastUpdatedBefore</span></span>
<span data-ttu-id="4908b-126">O horário em ou antes do qual a execução do pipeline foi atualizada no formato ISO8601.</span><span class="sxs-lookup"><span data-stu-id="4908b-126">The time at or before which the pipeline run was updated in ISO8601 format.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-127">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="4908b-127">-PipelineName</span></span>
<span data-ttu-id="4908b-128">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4908b-128">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryObjectByPipeline, ByFactoryNameByPipeline
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-129">-PipelineRunId</span><span class="sxs-lookup"><span data-stu-id="4908b-129">-PipelineRunId</span></span>
<span data-ttu-id="4908b-130">A ID de execução do pipeline.</span><span class="sxs-lookup"><span data-stu-id="4908b-130">The Run ID of the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryObjectByRunId
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4908b-131">-ResourceGroupName</span></span>
<span data-ttu-id="4908b-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4908b-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByRunId, ByFactoryNameByPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4908b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4908b-133">CommonParameters</span></span>
<span data-ttu-id="4908b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4908b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4908b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4908b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4908b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4908b-136">INPUTS</span></span>

### <span data-ttu-id="4908b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4908b-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="4908b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4908b-138">System.String</span></span>

## <span data-ttu-id="4908b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4908b-139">OUTPUTS</span></span>

### <span data-ttu-id="4908b-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4908b-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4908b-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipelineRun</span><span class="sxs-lookup"><span data-stu-id="4908b-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipelineRun</span></span>

## <span data-ttu-id="4908b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4908b-142">NOTES</span></span>

## <span data-ttu-id="4908b-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4908b-143">RELATED LINKS</span></span>

[<span data-ttu-id="4908b-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4908b-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4908b-145">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="4908b-145">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

