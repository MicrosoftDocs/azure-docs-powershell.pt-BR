---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: 313fcacf071dcee53c5141fe97c33bc1a477fe69
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778358"
---
# <span data-ttu-id="d8442-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d8442-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="d8442-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8442-102">SYNOPSIS</span></span>
<span data-ttu-id="d8442-103">Obtém informações sobre pipelines na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d8442-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="d8442-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8442-104">SYNTAX</span></span>

### <span data-ttu-id="d8442-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d8442-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8442-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d8442-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8442-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8442-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8442-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8442-108">DESCRIPTION</span></span>
<span data-ttu-id="d8442-109">O cmdlet Get-AzDataFactoryV2Pipeline Obtém informações sobre pipelines no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="d8442-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="d8442-110">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8442-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="d8442-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as tubulações na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d8442-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="d8442-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8442-112">EXAMPLES</span></span>

### <span data-ttu-id="d8442-113">Exemplo 1: obter informações sobre todas as tubulações</span><span class="sxs-lookup"><span data-stu-id="d8442-113">Example 1: Get information about all pipelines</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 

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

<span data-ttu-id="d8442-114">Esse comando obtém informações sobre todos os pipelines no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d8442-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="d8442-115">Você pode usar qualquer um dos comandos de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8442-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="d8442-116">O segundo usa um objeto datafactory como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d8442-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="d8442-117">Exemplo 2: obter informações sobre um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="d8442-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="d8442-118">Esse comando obtém informações sobre o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d8442-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="d8442-119">O comando transmite essas informações para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8442-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d8442-120">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="d8442-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="d8442-121">Para obter mais informações, digite Get-Help formato-List.</span><span class="sxs-lookup"><span data-stu-id="d8442-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="d8442-122">Exemplo 3: obter as propriedades para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="d8442-122">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Activities

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

<span data-ttu-id="d8442-123">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8442-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="d8442-124">Exemplo 6: obter informações sobre as entradas para a primeira atividade</span><span class="sxs-lookup"><span data-stu-id="d8442-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="d8442-125">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8442-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="d8442-126">O comando exibe a propriedade inputs do primeiro elemento da matriz Activities usando o cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="d8442-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="d8442-127">OS</span><span class="sxs-lookup"><span data-stu-id="d8442-127">PARAMETERS</span></span>

### <span data-ttu-id="d8442-128">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="d8442-128">-DataFactory</span></span>
<span data-ttu-id="d8442-129">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="d8442-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="d8442-130">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d8442-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8442-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d8442-131">-DataFactoryName</span></span>
<span data-ttu-id="d8442-132">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d8442-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d8442-133">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d8442-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8442-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8442-134">-DefaultProfile</span></span>
<span data-ttu-id="d8442-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8442-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8442-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8442-136">-Name</span></span>
<span data-ttu-id="d8442-137">Especifica o nome do pipeline sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="d8442-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8442-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8442-138">-ResourceGroupName</span></span>
<span data-ttu-id="d8442-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8442-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d8442-140">Esse cmdlet obtém pipelines que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d8442-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8442-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8442-141">-ResourceId</span></span>
<span data-ttu-id="d8442-142">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="d8442-142">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8442-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8442-143">CommonParameters</span></span>
<span data-ttu-id="d8442-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8442-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8442-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8442-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8442-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8442-146">INPUTS</span></span>

### <span data-ttu-id="d8442-147">System. String</span><span class="sxs-lookup"><span data-stu-id="d8442-147">System.String</span></span>

### <span data-ttu-id="d8442-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d8442-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d8442-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8442-149">OUTPUTS</span></span>

### <span data-ttu-id="d8442-150">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="d8442-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="d8442-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8442-151">NOTES</span></span>
<span data-ttu-id="d8442-152">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="d8442-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d8442-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8442-153">RELATED LINKS</span></span>

[<span data-ttu-id="d8442-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d8442-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d8442-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d8442-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="d8442-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="d8442-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
