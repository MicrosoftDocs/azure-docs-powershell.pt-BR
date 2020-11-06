---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Invoke-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 45095fefa0d4866a40b59c61ca02a98c118cf37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610016"
---
# <span data-ttu-id="58ffe-101">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="58ffe-101">Invoke-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="58ffe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58ffe-102">SYNOPSIS</span></span>
  <span data-ttu-id="58ffe-103">Invoca um pipeline para iniciar uma execução para ele.</span><span class="sxs-lookup"><span data-stu-id="58ffe-103">Invokes a pipeline to start a run for it.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58ffe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="58ffe-104">SYNTAX</span></span>

### <span data-ttu-id="58ffe-105">ByFactoryNameByParameterFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="58ffe-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="58ffe-106">ByPipelineObjectByParameterFile</span><span class="sxs-lookup"><span data-stu-id="58ffe-106">ByPipelineObjectByParameterFile</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-ParameterFile] <String>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="58ffe-107">ByPipelineObjectByParameterObject</span><span class="sxs-lookup"><span data-stu-id="58ffe-107">ByPipelineObjectByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="58ffe-108">ByFactoryNameByParameterObject</span><span class="sxs-lookup"><span data-stu-id="58ffe-108">ByFactoryNameByParameterObject</span></span>
```
Invoke-AzureRmDataFactoryV2Pipeline [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-PipelineName] <String> [[-Parameter] <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="58ffe-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="58ffe-109">DESCRIPTION</span></span>
<span data-ttu-id="58ffe-110">O comando **Invoke-AzureRmDataFactoryV2Pipeline** inicia uma execução no pipeline especificado e retorna uma ID para essa execução.</span><span class="sxs-lookup"><span data-stu-id="58ffe-110">The **Invoke-AzureRmDataFactoryV2Pipeline** command starts a run on the specified pipeline and returns a ID for that run.</span></span> <span data-ttu-id="58ffe-111">Esse GUID pode ser passado para **Get-AzureRmDataFactoryV2PipelineRun** ou **Get-AzureRmDataFactoryV2ActivityRun** para obter mais detalhes sobre essa execução.</span><span class="sxs-lookup"><span data-stu-id="58ffe-111">This GUID can be passed to **Get-AzureRmDataFactoryV2PipelineRun** or **Get-AzureRmDataFactoryV2ActivityRun** to obtain further details about this run.</span></span>

## <span data-ttu-id="58ffe-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="58ffe-112">EXAMPLES</span></span>

### <span data-ttu-id="58ffe-113">Exemplo 1: invocar um pipeline para iniciar uma execução</span><span class="sxs-lookup"><span data-stu-id="58ffe-113">Example 1: Invoke a pipeline to start a run</span></span>
```
PS C:\> Invoke-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -PipelineName "DPWikisample"
867d9d9f-1efc-4fee-974d-d8e6320bfbcb
```

<span data-ttu-id="58ffe-114">Esse comando inicia uma execução para o pipeline "DPWikisample" na fábrica "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="58ffe-114">This command starts a run for "DPWikisample" pipeline in the "WikiADF" factory.</span></span>

## <span data-ttu-id="58ffe-115">OS</span><span class="sxs-lookup"><span data-stu-id="58ffe-115">PARAMETERS</span></span>

### <span data-ttu-id="58ffe-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="58ffe-116">-Confirm</span></span>
<span data-ttu-id="58ffe-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58ffe-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ffe-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="58ffe-118">-DataFactoryName</span></span>
<span data-ttu-id="58ffe-119">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="58ffe-119">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ffe-120">-Parameterfile</span><span class="sxs-lookup"><span data-stu-id="58ffe-120">-ParameterFile</span></span>
<span data-ttu-id="58ffe-121">O nome do arquivo com parâmetros para execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="58ffe-121">The name of the file with parameters for pipeline run.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByPipelineObjectByParameterFile
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ffe-122">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="58ffe-122">-Parameter</span></span>
<span data-ttu-id="58ffe-123">Parâmetros para a execução de pipeline.</span><span class="sxs-lookup"><span data-stu-id="58ffe-123">Parameters for pipeline run.</span></span>

```yaml
Type: Hashtable
Parameter Sets: ByPipelineObjectByParameterObject, ByFactoryNameByParameterObject
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ffe-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58ffe-124">-InputObject</span></span>
<span data-ttu-id="58ffe-125">O objeto de fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="58ffe-125">The data factory object.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByPipelineObjectByParameterFile, ByPipelineObjectByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58ffe-126">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="58ffe-126">-PipelineName</span></span>
<span data-ttu-id="58ffe-127">O nome do pipeline.</span><span class="sxs-lookup"><span data-stu-id="58ffe-127">The pipeline name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ffe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ffe-128">-ResourceGroupName</span></span>
<span data-ttu-id="58ffe-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="58ffe-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryNameByParameterFile, ByFactoryNameByParameterObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ffe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ffe-130">-WhatIf</span></span>
<span data-ttu-id="58ffe-131">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58ffe-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="58ffe-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="58ffe-132">INPUTS</span></span>

### <span data-ttu-id="58ffe-133">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="58ffe-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="58ffe-134">System. String System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="58ffe-134">System.String System.Collections.Hashtable</span></span>


## <span data-ttu-id="58ffe-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="58ffe-135">OUTPUTS</span></span>

### <span data-ttu-id="58ffe-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="58ffe-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="58ffe-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="58ffe-137">NOTES</span></span>

## <span data-ttu-id="58ffe-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58ffe-138">RELATED LINKS</span></span>
[<span data-ttu-id="58ffe-139">Get-AzureRmDataFactoryV2PipelineRun</span><span class="sxs-lookup"><span data-stu-id="58ffe-139">Get-AzureRmDataFactoryV2PipelineRun</span></span>]()

[<span data-ttu-id="58ffe-140">Get-AzureRmDataFactoryV2ActivityRun</span><span class="sxs-lookup"><span data-stu-id="58ffe-140">Get-AzureRmDataFactoryV2ActivityRun</span></span>]()

