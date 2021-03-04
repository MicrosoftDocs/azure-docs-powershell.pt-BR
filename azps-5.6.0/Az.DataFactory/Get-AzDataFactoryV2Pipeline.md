---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Pipeline.md
ms.openlocfilehash: cd110ebf3b8467e1590ddf52a28d822eebe17092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888280"
---
# <span data-ttu-id="a1dbd-101">Get-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a1dbd-101">Get-AzDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="a1dbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="a1dbd-103">Obtém informações sobre pipelines na Fábrica de Dados.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-103">Gets information about pipelines in Data Factory.</span></span>

## <span data-ttu-id="a1dbd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a1dbd-104">SYNTAX</span></span>

### <span data-ttu-id="a1dbd-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a1dbd-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1dbd-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a1dbd-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1dbd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1dbd-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Pipeline [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1dbd-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a1dbd-108">DESCRIPTION</span></span>
<span data-ttu-id="a1dbd-109">O Get-AzDataFactoryV2Pipeline cmdlet obtém informações sobre pipelines no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-109">The Get-AzDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="a1dbd-110">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="a1dbd-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os pipelines no fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="a1dbd-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1dbd-112">EXAMPLES</span></span>

### <span data-ttu-id="a1dbd-113">Exemplo 1: obter informações sobre todos os pipelines</span><span class="sxs-lookup"><span data-stu-id="a1dbd-113">Example 1: Get information about all pipelines</span></span>
```powershell
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

<span data-ttu-id="a1dbd-114">Este comando obtém informações sobre todos os pipelines no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="a1dbd-115">Você pode usar um dos comandos de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="a1dbd-116">O segundo usa um objeto DataFactory como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="a1dbd-117">Exemplo 2: obter informações sobre um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="a1dbd-117">Example 2: Get information about a specific pipeline</span></span>
```powershell
PS C:\> Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="a1dbd-118">Este comando obtém informações sobre o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="a1dbd-119">O comando passa essas informações para o cmdlet Format-List usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a1dbd-120">Esse Windows PowerShell cmdlet formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="a1dbd-121">Para obter mais informações, digite Get-Help Format-List.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="a1dbd-122">Exemplo 3: Obter as propriedades de um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="a1dbd-122">Example 3: Get the properties for a specific pipeline</span></span>
```powershell
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

<span data-ttu-id="a1dbd-123">Este comando obtém informações para o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF e usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="a1dbd-124">Exemplo 4: obter informações sobre entradas para a primeira atividade</span><span class="sxs-lookup"><span data-stu-id="a1dbd-124">Example 4: Get information about inputs for the first activity</span></span>
```powershell
PS C:\> (Get-AzDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="a1dbd-125">Este comando obtém informações para o pipeline chamado DPWikisample no fábrica de dados chamado WikiADF e usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="a1dbd-126">O comando exibe a propriedade Inputs do primeiro elemento da matriz Activities usando o cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="a1dbd-127">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a1dbd-127">PARAMETERS</span></span>

### <span data-ttu-id="a1dbd-128">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a1dbd-128">-DataFactory</span></span>
<span data-ttu-id="a1dbd-129">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="a1dbd-130">Este cmdlet obtém pipelines que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1dbd-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a1dbd-131">-DataFactoryName</span></span>
<span data-ttu-id="a1dbd-132">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a1dbd-133">Este cmdlet obtém pipelines que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1dbd-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1dbd-134">-DefaultProfile</span></span>
<span data-ttu-id="a1dbd-135">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1dbd-136">-Name</span><span class="sxs-lookup"><span data-stu-id="a1dbd-136">-Name</span></span>
<span data-ttu-id="a1dbd-137">Especifica o nome do pipeline sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-137">Specifies the name of the pipeline about which to get information.</span></span>

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

### <span data-ttu-id="a1dbd-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1dbd-138">-ResourceGroupName</span></span>
<span data-ttu-id="a1dbd-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a1dbd-140">Este cmdlet obtém pipelines que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a1dbd-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1dbd-141">-ResourceId</span></span>
<span data-ttu-id="a1dbd-142">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-142">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a1dbd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1dbd-143">CommonParameters</span></span>
<span data-ttu-id="a1dbd-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1dbd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1dbd-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1dbd-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1dbd-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1dbd-146">INPUTS</span></span>

### <span data-ttu-id="a1dbd-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a1dbd-147">System.String</span></span>

### <span data-ttu-id="a1dbd-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a1dbd-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a1dbd-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a1dbd-149">OUTPUTS</span></span>

### <span data-ttu-id="a1dbd-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="a1dbd-150">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="a1dbd-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="a1dbd-151">NOTES</span></span>
<span data-ttu-id="a1dbd-152">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="a1dbd-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a1dbd-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1dbd-153">RELATED LINKS</span></span>

[<span data-ttu-id="a1dbd-154">Set-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a1dbd-154">Set-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a1dbd-155">Remove-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a1dbd-155">Remove-AzDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="a1dbd-156">Invoke-AzDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="a1dbd-156">Invoke-AzDataFactoryV2Pipeline</span></span>]()
