---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: b8065c3b4aa958c9138316488b7ca8a9b982d97c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441130"
---
# <span data-ttu-id="ca875-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ca875-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="ca875-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca875-102">SYNOPSIS</span></span>
<span data-ttu-id="ca875-103">Obtém informações sobre pipelines na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ca875-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca875-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca875-104">SYNTAX</span></span>

### <span data-ttu-id="ca875-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca875-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="ca875-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ca875-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="ca875-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca875-107">DESCRIPTION</span></span>
<span data-ttu-id="ca875-108">O cmdlet Get-AzureRmDataFactoryV2Pipeline Obtém informações sobre pipelines no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="ca875-108">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="ca875-109">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca875-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="ca875-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as tubulações na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ca875-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="ca875-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca875-111">EXAMPLES</span></span>

### <span data-ttu-id="ca875-112">Exemplo 1: obter informações sobre todas as tubulações</span><span class="sxs-lookup"><span data-stu-id="ca875-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyWebActivity}
    Parameters        : {[url, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

    PipelineName      : DPTwittersample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}

```

<span data-ttu-id="ca875-113">Esse comando obtém informações sobre todos os pipelines no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ca875-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="ca875-114">Você pode usar qualquer um dos comandos de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca875-114">You can use either one of the following example commands.</span></span>
<span data-ttu-id="ca875-115">O segundo usa um objeto datafactory como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ca875-115">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="ca875-116">Exemplo 2: obter informações sobre um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="ca875-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="ca875-117">Esse comando obtém informações sobre o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ca875-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="ca875-118">O comando transmite essas informações para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca875-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ca875-119">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="ca875-119">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="ca875-120">Para obter mais informações, digite Get-Help formato-List.</span><span class="sxs-lookup"><span data-stu-id="ca875-120">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="ca875-121">Exemplo 3: obter as propriedades para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="ca875-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_0_0
    Description                     :
    DependsOn                       :

    Source                          : Microsoft.Azure.Management.DataFactory.Models.BlobSource
    Sink                            : Microsoft.Azure.Management.DataFactory.Models.BlobSink
    Translator                      :
    EnableStaging                   :
    StagingSettings                 :
    ParallelCopies                  :
    CloudDataMovementUnits          :
    EnableSkipIncompatibleRow       :
    RedirectIncompatibleRowSettings :
    Inputs                          : {}
    Outputs                         : {}
    LinkedServiceName               :
    Policy                          :
    Name                            : MyCopyActivity_1_0
    Description                     :
    DependsOn                       : {Microsoft.Azure.Management.DataFactory.Models.ActivityDependency}

```

<span data-ttu-id="ca875-122">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca875-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="ca875-123">Exemplo 6: obter informações sobre as entradas para a primeira atividade</span><span class="sxs-lookup"><span data-stu-id="ca875-123">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :

```

<span data-ttu-id="ca875-124">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca875-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="ca875-125">O comando exibe a propriedade inputs do primeiro elemento da matriz Activities usando o cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="ca875-125">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="ca875-126">OS</span><span class="sxs-lookup"><span data-stu-id="ca875-126">PARAMETERS</span></span>

### <span data-ttu-id="ca875-127">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="ca875-127">-DataFactory</span></span>
<span data-ttu-id="ca875-128">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="ca875-128">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="ca875-129">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca875-129">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca875-130">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ca875-130">-DataFactoryName</span></span>
<span data-ttu-id="ca875-131">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ca875-131">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ca875-132">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca875-132">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca875-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca875-133">-Name</span></span>
<span data-ttu-id="ca875-134">Especifica o nome do pipeline sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="ca875-134">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca875-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca875-135">-ResourceGroupName</span></span>
<span data-ttu-id="ca875-136">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca875-136">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ca875-137">Esse cmdlet obtém pipelines que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ca875-137">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="ca875-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca875-138">INPUTS</span></span>

### <span data-ttu-id="ca875-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ca875-139">System.String</span></span>
<span data-ttu-id="ca875-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ca875-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="ca875-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca875-141">OUTPUTS</span></span>

### <span data-ttu-id="ca875-142">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ca875-142">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ca875-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ca875-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>


## <span data-ttu-id="ca875-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca875-144">NOTES</span></span>
<span data-ttu-id="ca875-145">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="ca875-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ca875-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca875-146">RELATED LINKS</span></span>
[<span data-ttu-id="ca875-147">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ca875-147">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ca875-148">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ca875-148">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="ca875-149">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="ca875-149">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
