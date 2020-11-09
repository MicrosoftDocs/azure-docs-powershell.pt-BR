---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5224BDF5-D492-4160-893E-4BB5F76C22F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorypipeline
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryPipeline.md
ms.openlocfilehash: 46f32dd48c433e34209b4a661b8c5b770a40db8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281075"
---
# <span data-ttu-id="f1893-101">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f1893-101">Get-AzDataFactoryPipeline</span></span>

## <span data-ttu-id="f1893-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1893-102">SYNOPSIS</span></span>
<span data-ttu-id="f1893-103">Obtém informações sobre pipelines no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="f1893-103">Gets information about pipelines in Azure Data Factory.</span></span>

## <span data-ttu-id="f1893-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1893-104">SYNTAX</span></span>

### <span data-ttu-id="f1893-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f1893-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1893-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f1893-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryPipeline [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1893-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1893-107">DESCRIPTION</span></span>
<span data-ttu-id="f1893-108">O cmdlet **Get-AzDataFactoryPipeline** Obtém informações sobre pipelines no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="f1893-108">The **Get-AzDataFactoryPipeline** cmdlet gets information about pipelines in Azure Data Factory.</span></span>
<span data-ttu-id="f1893-109">Se você especificar o nome de um pipeline, esse cmdlet obterá informações sobre esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1893-109">If you specify the name of a pipeline, this cmdlet gets information about that pipeline.</span></span>
<span data-ttu-id="f1893-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as tubulações na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f1893-110">If you do not specify a name, this cmdlet gets information about all the pipelines in the data factory.</span></span>

## <span data-ttu-id="f1893-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1893-111">EXAMPLES</span></span>

### <span data-ttu-id="f1893-112">Exemplo 1: obter informações sobre todas as tubulações</span><span class="sxs-lookup"><span data-stu-id="f1893-112">Example 1: Get information about all pipelines</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
```

<span data-ttu-id="f1893-113">Esse comando obtém informações sobre todos os pipelines no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f1893-113">This command gets information about all pipelines in the data factory named WikiADF.</span></span>
<span data-ttu-id="f1893-114">Você pode um dos comandos de exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1893-114">You can either one of the following example commands.</span></span>
<span data-ttu-id="f1893-115">O segundo usa um objeto **DataFactory** como parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f1893-115">The second one uses a **DataFactory** object as a parameter.</span></span>

### <span data-ttu-id="f1893-116">Exemplo 2: obter informações sobre um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="f1893-116">Example 2: Get information about a specific pipeline</span></span>
```
PS C:\>Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF" | Format-List
PipelineName      : DPWikisample
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Properties        : Microsoft.DataFactories.PipelineProperties
```

<span data-ttu-id="f1893-117">Esse comando obtém informações sobre o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f1893-117">This command gets information about the pipeline named DPWikisample in the data factory named WikiADF.</span></span>
<span data-ttu-id="f1893-118">O comando transmite essas informações para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1893-118">The command passes that information to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f1893-119">Esse cmdlet formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="f1893-119">That cmdlet formats the results.</span></span>
<span data-ttu-id="f1893-120">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="f1893-120">For more information, type `Get-Help Format-List`.</span></span>

### <span data-ttu-id="f1893-121">Exemplo 3: obter as propriedades para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="f1893-121">Example 3: Get the properties for a specific pipeline</span></span>
```
PS C:\> (Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name DPWikisample -DataFactoryName "WikiADF").Properties
Activities  : {WikiHiveActivity, BlobToSqlCopyActivity}
Description : DP Wikipedia Sample Pipelines
End         : 6/6/2014 8:00:00 AM
IsPaused    : 
RuntimeInfo : Microsoft.DataFactories.PipelineRuntimeInfo
Start       : 6/5/2014 8:00:00 PM
```

<span data-ttu-id="f1893-122">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Properties** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1893-122">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Properties** property associated with that pipeline.</span></span>

### <span data-ttu-id="f1893-123">Exemplo 4: obter as atividades para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="f1893-123">Example 4: Get the activities for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.Activities
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

<span data-ttu-id="f1893-124">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1893-124">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>

### <span data-ttu-id="f1893-125">Exemplo 5: obter as informações de tempo de execução para um pipeline específico</span><span class="sxs-lookup"><span data-stu-id="f1893-125">Example 5: Get the runtime information for a specific pipeline</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF").Properties.RuntimeInfo
DeploymentTime
--------------
6/5/2014 10:36:46 PM
```

<span data-ttu-id="f1893-126">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **RuntimeInfo** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1893-126">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **RuntimeInfo** property associated with that pipeline.</span></span>

### <span data-ttu-id="f1893-127">Exemplo 6: obter informações sobre as entradas para a primeira atividade</span><span class="sxs-lookup"><span data-stu-id="f1893-127">Example 6: Get information about inputs for the first activity</span></span>
```
PS C:\>(Get-AzDataFactoryPipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF11").Properties.Activities[0].Inputs | Format-List
EndTime   : 
Length    : 
Name      : DAWikipediaClickEvents
StartTime :
```

<span data-ttu-id="f1893-128">Esse comando obtém informações para o pipeline chamado DPWikisample na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir a propriedade **Activities** associada a esse pipeline.</span><span class="sxs-lookup"><span data-stu-id="f1893-128">This command gets information for the pipeline named DPWikisample in the data factory named WikiADF, and then uses standard dot notation to view the **Activities** property associated with that pipeline.</span></span>
<span data-ttu-id="f1893-129">O comando exibe a propriedade **inputs** do primeiro elemento da matriz **Activities** usando **Format-List**.</span><span class="sxs-lookup"><span data-stu-id="f1893-129">The command displays the **Inputs** property of the first element of the **Activities** array by using **Format-List**.</span></span>

## <span data-ttu-id="f1893-130">OS</span><span class="sxs-lookup"><span data-stu-id="f1893-130">PARAMETERS</span></span>

### <span data-ttu-id="f1893-131">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="f1893-131">-DataFactory</span></span>
<span data-ttu-id="f1893-132">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="f1893-132">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f1893-133">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f1893-133">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1893-134">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f1893-134">-DataFactoryName</span></span>
<span data-ttu-id="f1893-135">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f1893-135">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f1893-136">Esse cmdlet obtém pipelines que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f1893-136">This cmdlet gets pipelines that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f1893-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1893-137">-DefaultProfile</span></span>
<span data-ttu-id="f1893-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f1893-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1893-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="f1893-139">-Name</span></span>
<span data-ttu-id="f1893-140">Especifica o nome do pipeline sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="f1893-140">Specifies the name of the pipeline about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1893-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1893-141">-ResourceGroupName</span></span>
<span data-ttu-id="f1893-142">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1893-142">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f1893-143">Esse cmdlet obtém pipelines que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f1893-143">This cmdlet gets pipelines that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f1893-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1893-144">CommonParameters</span></span>
<span data-ttu-id="f1893-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1893-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1893-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1893-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1893-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1893-147">INPUTS</span></span>

### <span data-ttu-id="f1893-148">System. String</span><span class="sxs-lookup"><span data-stu-id="f1893-148">System.String</span></span>

### <span data-ttu-id="f1893-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f1893-149">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="f1893-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1893-150">OUTPUTS</span></span>

### <span data-ttu-id="f1893-151">Microsoft. Azure. Commands. datafactorings. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="f1893-151">Microsoft.Azure.Commands.DataFactories.Models.PSPipeline</span></span>

## <span data-ttu-id="f1893-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1893-152">NOTES</span></span>
* <span data-ttu-id="f1893-153">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="f1893-153">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f1893-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1893-154">RELATED LINKS</span></span>

[<span data-ttu-id="f1893-155">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f1893-155">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="f1893-156">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f1893-156">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="f1893-157">Currículo-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f1893-157">Resume-AzDataFactoryPipeline</span></span>](./Resume-AzDataFactoryPipeline.md)

[<span data-ttu-id="f1893-158">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="f1893-158">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="f1893-159">Suspender-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="f1893-159">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


