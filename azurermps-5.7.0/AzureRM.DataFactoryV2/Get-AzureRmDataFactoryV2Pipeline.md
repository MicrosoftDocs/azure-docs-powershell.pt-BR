---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2pipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Pipeline.md
ms.openlocfilehash: bce1969ed951f196b1ff2c6d5bcc359ee68bc3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440483"
---
# <span data-ttu-id="7eabf-101">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7eabf-101">Get-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="7eabf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7eabf-102">SYNOPSIS</span></span>
<span data-ttu-id="7eabf-103">Obtém informações sobre pipelines na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7eabf-103">Gets information about pipelines in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eabf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7eabf-104">SYNTAX</span></span>

### <span data-ttu-id="7eabf-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7eabf-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eabf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7eabf-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Pipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7eabf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7eabf-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Pipeline -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eabf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7eabf-108">DESCRIPTION</span></span>
<span data-ttu-id="7eabf-109">O cmdlet Get-AzureRmDataFactoryV2Pipeline Obtém informações sobre pipelines no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="7eabf-109">The Get-AzureRmDataFactoryV2Pipeline cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="7eabf-110">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="7eabf-110">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="7eabf-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as tubulações na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7eabf-111">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="7eabf-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7eabf-112">EXAMPLES</span></span>

### <span data-ttu-id="7eabf-113">Exemplo 1: obter informações sobre todas as tubulações</span><span class="sxs-lookup"><span data-stu-id="7eabf-113">Example 1: Get information about all pipelines</span></span>
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

<span data-ttu-id="7eabf-114">Esse comando obtém informações sobre todos os pipelines no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7eabf-114">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="7eabf-115">Você pode usar qualquer um dos comandos de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7eabf-115">You can use either one of the following example commands.</span></span>
<span data-ttu-id="7eabf-116">O segundo usa um objeto datafactory como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7eabf-116">The second one uses a DataFactory object as a parameter.</span></span>

### <span data-ttu-id="7eabf-117">Exemplo 2: obter informações sobre um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="7eabf-117">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List

    PipelineName      : DPWikisample
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Activities        : {MyCopyActivity_0_0, MyCopyActivity_1_0}
    Parameters        : {[OutputBlobName, Microsoft.Azure.Management.DataFactory.Models.ParameterSpecification]}
```

<span data-ttu-id="7eabf-118">Esse comando obtém informações sobre o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="7eabf-118">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="7eabf-119">O comando transmite essas informações para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="7eabf-119">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7eabf-120">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="7eabf-120">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="7eabf-121">Para obter mais informações, digite Get-Help formato-List.</span><span class="sxs-lookup"><span data-stu-id="7eabf-121">For more information, type Get-Help Format-List.</span></span>

### <span data-ttu-id="7eabf-122">Exemplo 3: obter as propriedades para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="7eabf-122">Example 3: Get the properties for a specific pipeline</span></span>
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

<span data-ttu-id="7eabf-123">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="7eabf-123">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>

### <span data-ttu-id="7eabf-124">Exemplo 6: obter informações sobre as entradas para a primeira atividade</span><span class="sxs-lookup"><span data-stu-id="7eabf-124">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\> (Get-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Activities[0].Inputs | Format-List

    ReferenceName : dsIn
    Parameters    :
```

<span data-ttu-id="7eabf-125">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade Activities associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="7eabf-125">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the Activities property associated with that pipeline.</span></span>
<span data-ttu-id="7eabf-126">O comando exibe a propriedade inputs do primeiro elemento da matriz Activities usando o cmdlet Format-List.</span><span class="sxs-lookup"><span data-stu-id="7eabf-126">The command displays the Inputs property of the first element of the Activities array by using the Format-List cmdlet.</span></span>

## <span data-ttu-id="7eabf-127">OS</span><span class="sxs-lookup"><span data-stu-id="7eabf-127">PARAMETERS</span></span>

### <span data-ttu-id="7eabf-128">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="7eabf-128">-DataFactory</span></span>
<span data-ttu-id="7eabf-129">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="7eabf-129">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="7eabf-130">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7eabf-130">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7eabf-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7eabf-131">-DataFactoryName</span></span>
<span data-ttu-id="7eabf-132">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="7eabf-132">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7eabf-133">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7eabf-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="7eabf-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eabf-134">-DefaultProfile</span></span>
<span data-ttu-id="7eabf-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7eabf-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eabf-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="7eabf-136">-Name</span></span>
<span data-ttu-id="7eabf-137">Especifica o nome do pipeline sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="7eabf-137">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: PipelineName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eabf-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eabf-138">-ResourceGroupName</span></span>
<span data-ttu-id="7eabf-139">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="7eabf-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7eabf-140">Esse cmdlet obtém pipelines que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7eabf-140">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="7eabf-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7eabf-141">-ResourceId</span></span>
<span data-ttu-id="7eabf-142">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="7eabf-142">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eabf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eabf-143">CommonParameters</span></span>
<span data-ttu-id="7eabf-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eabf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eabf-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eabf-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eabf-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7eabf-146">INPUTS</span></span>

### <span data-ttu-id="7eabf-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7eabf-147">System.String</span></span>
<span data-ttu-id="7eabf-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="7eabf-148">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7eabf-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7eabf-149">OUTPUTS</span></span>

### <span data-ttu-id="7eabf-150">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7eabf-150">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="7eabf-151">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="7eabf-151">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="7eabf-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7eabf-152">NOTES</span></span>
<span data-ttu-id="7eabf-153">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="7eabf-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7eabf-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7eabf-154">RELATED LINKS</span></span>

[<span data-ttu-id="7eabf-155">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7eabf-155">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7eabf-156">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7eabf-156">Remove-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="7eabf-157">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="7eabf-157">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()
