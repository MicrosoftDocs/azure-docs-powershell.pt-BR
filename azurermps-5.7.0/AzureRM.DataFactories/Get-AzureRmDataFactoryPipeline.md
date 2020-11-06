---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryPipeline.md
ms.openlocfilehash: 17a6be37e62693f3e6d6e7c9089f72771fc0a9f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426746"
---
# <span data-ttu-id="21b08-101">Get-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="21b08-101">Get-AzureRmDataFactoryPipeline</span></span>

## <span data-ttu-id="21b08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21b08-102">SYNOPSIS</span></span>
<span data-ttu-id="21b08-103">Obtém informações sobre pipelines no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="21b08-103">Gets information about pipelines in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21b08-104">SYNTAX</span></span>

### <span data-ttu-id="21b08-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="21b08-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21b08-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="21b08-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21b08-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21b08-107">DESCRIPTION</span></span>
<span data-ttu-id="21b08-108">O cmdlet **Get-AzureRmDataFactoryPipeline** Obtém informações sobre pipelines no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="21b08-108">The **Get-AzureRmDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="21b08-109">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="21b08-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="21b08-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as tubulações na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="21b08-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="21b08-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21b08-111">EXAMPLES</span></span>

### <span data-ttu-id="21b08-112">Exemplo 1: obter informações sobre todas as tubulações</span><span class="sxs-lookup"><span data-stu-id="21b08-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="21b08-113">Esse comando obtém informações sobre todos os pipelines no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="21b08-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="21b08-114">Você pode um dos comandos de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="21b08-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="21b08-115">O segundo usa um objeto **DataFactory** como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="21b08-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="21b08-116">Exemplo 2: obter informações sobre um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="21b08-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="21b08-117">Esse comando obtém informações sobre o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="21b08-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="21b08-118">O comando transmite essas informações para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="21b08-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="21b08-119">Esse cmdlet formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="21b08-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="21b08-120">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="21b08-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="21b08-121">Exemplo 3: obter as propriedades para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="21b08-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="21b08-122">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Properties** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="21b08-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="21b08-123">Exemplo 4: obter as atividades para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="21b08-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
Transformation    : Microsoft.DataFactories.HDInsightActivityProperties
Description       : 
Inputs            : {DAWikipediaClickEvents}
LinkedServiceName : HDILinkedService
Name              : WikiHiveActivity
Outputs           : {DACuratedWikiData}
Policy            : Microsoft.DataFactories.ActivityPolicy

Transformation    : Microsoft.DataFactories.CopyActivityProperties
Description       : 
Inputs            : {DACuratedWikiData}
LinkedServiceName : HDILinkedService
Name              : BlobToSqlCopyActivity
Outputs           : {DAWikiAggregatedData}
Policy            : Microsoft.DataFactories.ActivityPolicy
```

<span data-ttu-id="21b08-124">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="21b08-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="21b08-125">Exemplo 5: obter as informações de tempo de execução para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="21b08-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="21b08-126">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **RuntimeInfo** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="21b08-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="21b08-127">Exemplo 6: obter informações sobre as entradas para a primeira atividade</span><span class="sxs-lookup"><span data-stu-id="21b08-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzureRmDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="21b08-128">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="21b08-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="21b08-129">O comando exibe a propriedade **inputs** do primeiro elemento da matriz **Activities** usando **Format-List**.</span><span class="sxs-lookup"><span data-stu-id="21b08-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="21b08-130">OS</span><span class="sxs-lookup"><span data-stu-id="21b08-130">PARAMETERS</span></span>

### <span data-ttu-id="21b08-131">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="21b08-131">-DataFactory</span></span>
<span data-ttu-id="21b08-132">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="21b08-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="21b08-133">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21b08-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b08-134">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="21b08-134">-DataFactoryName</span></span>
<span data-ttu-id="21b08-135">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="21b08-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="21b08-136">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21b08-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="21b08-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b08-137">-DefaultProfile</span></span>
<span data-ttu-id="21b08-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="21b08-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21b08-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="21b08-139">-Name</span></span>
<span data-ttu-id="21b08-140">Especifica o nome do pipeline sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="21b08-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b08-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21b08-141">-ResourceGroupName</span></span>
<span data-ttu-id="21b08-142">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="21b08-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="21b08-143">Esse cmdlet obtém pipelines que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="21b08-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="21b08-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b08-144">CommonParameters</span></span>
<span data-ttu-id="21b08-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b08-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b08-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b08-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b08-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21b08-147">INPUTS</span></span>

### <span data-ttu-id="21b08-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="21b08-148">None</span></span>
<span data-ttu-id="21b08-149">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="21b08-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21b08-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21b08-150">OUTPUTS</span></span>

### <span data-ttu-id="21b08-151">System. Collections. Generic. List ' 1 [[Microsoft. WindowsAzure. Commands. Utilities. PSPipeline, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft. WindowsAzure. Commands. Utilities. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="21b08-151">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSPipeline, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSPipeline</span></span>

## <span data-ttu-id="21b08-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21b08-152">NOTES</span></span>
* <span data-ttu-id="21b08-153">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="21b08-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="21b08-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21b08-154">RELATED LINKS</span></span>

[<span data-ttu-id="21b08-155">New-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="21b08-155">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="21b08-156">Remove-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="21b08-156">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="21b08-157">Currículo-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="21b08-157">Resume-AzureRmDataFactoryPipeline</span></span>](./Resume-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="21b08-158">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="21b08-158">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="21b08-159">Suspender-AzureRmDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="21b08-159">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)

