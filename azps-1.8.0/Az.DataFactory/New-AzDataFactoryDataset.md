---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 352A4B94-E433-413B-91D1-6AA347563959
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryDataset.md
ms.openlocfilehash: 1d03ba1e4b025be933fd9cd409270d8deb93d1d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601144"
---
# <span data-ttu-id="559dc-101">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="559dc-101">New-AzDataFactoryDataset</span></span>

## <span data-ttu-id="559dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="559dc-102">SYNOPSIS</span></span>
<span data-ttu-id="559dc-103">Cria um conjunto de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="559dc-103">Creates a dataset in Data Factory.</span></span>

## <span data-ttu-id="559dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="559dc-104">SYNTAX</span></span>

### <span data-ttu-id="559dc-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="559dc-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="559dc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="559dc-106">ByFactoryObject</span></span>
```
New-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>] [-File] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="559dc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="559dc-107">DESCRIPTION</span></span>
<span data-ttu-id="559dc-108">O cmdlet **New-AzDataFactoryDataset** cria um conjunto de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="559dc-108">The **New-AzDataFactoryDataset** cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="559dc-109">Se você especificar um nome para um DataSet que já existe, esse cmdlet solicitará confirmação antes de substituir o DataSet.</span><span class="sxs-lookup"><span data-stu-id="559dc-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="559dc-110">Se você especificar o parâmetro *Force* , o cmdlet substituirá o DataSet existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="559dc-110">If you specify the *Force* parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>
<span data-ttu-id="559dc-111">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="559dc-111">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="559dc-112">Criar uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="559dc-112">Create a data factory.</span></span> 
- <span data-ttu-id="559dc-113">Criar serviços vinculados.</span><span class="sxs-lookup"><span data-stu-id="559dc-113">Create linked services.</span></span> 
- <span data-ttu-id="559dc-114">Criar conjuntos de valores de valores.</span><span class="sxs-lookup"><span data-stu-id="559dc-114">Create datasets.</span></span> 
- <span data-ttu-id="559dc-115">Crie um pipeline.</span><span class="sxs-lookup"><span data-stu-id="559dc-115">Create a pipeline.</span></span>
<span data-ttu-id="559dc-116">Se um conjunto de dados com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deseja substituir o conjunto de dados existente pelo novo conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="559dc-116">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="559dc-117">Se você confirmar para substituir o conjunto de um conjunto de um existente, a definição de DataSet também será substituída.</span><span class="sxs-lookup"><span data-stu-id="559dc-117">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="559dc-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="559dc-118">EXAMPLES</span></span>

### <span data-ttu-id="559dc-119">Exemplo 1: criar um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="559dc-119">Example 1: Create a dataset</span></span>
```
PS C:\>New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
DatasetName         : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="559dc-120">Esse comando cria um conjunto de dados chamado DA_WikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="559dc-120">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="559dc-121">O comando baseia o DataSet nas informações do DAWikipediaClickEvents.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="559dc-121">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

### <span data-ttu-id="559dc-122">Exemplo 2: exibir a disponibilidade de um novo conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="559dc-122">Example 2: View availability for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Availability
AnchorDateTime : 
Frequency      : Hour
Interval       : 1
Offset         : 
WaitOnExternal : Microsoft.DataFactories.WaitOnExternal
```

<span data-ttu-id="559dc-123">O primeiro comando cria um DataSet chamado DA_WikipediaClickEvents, como em um exemplo anterior, e, em seguida, atribui esse conjunto de DataSet à variável $Dataset.</span><span class="sxs-lookup"><span data-stu-id="559dc-123">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="559dc-124">O segundo comando usa a notação de ponto padrão para exibir detalhes sobre a propriedade Availability do conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="559dc-124">The second command uses standard dot notation to display details about the Availability property of the dataset.</span></span>

### <span data-ttu-id="559dc-125">Exemplo 3: Exibir local para um novo conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="559dc-125">Example 3: View location for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="559dc-126">O primeiro comando cria um DataSet chamado DA_WikipediaClickEvents, como em um exemplo anterior, e, em seguida, atribui esse conjunto de DataSet à variável $Dataset.</span><span class="sxs-lookup"><span data-stu-id="559dc-126">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="559dc-127">O segundo comando exibe detalhes sobre a propriedade Location do DataSet.</span><span class="sxs-lookup"><span data-stu-id="559dc-127">The second command displays details about the Location property of the dataset.</span></span>

### <span data-ttu-id="559dc-128">Exemplo 4: Exibir regras de validação para um novo conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="559dc-128">Example 4: View validation rules for a new dataset</span></span>
```
PS C:\>$Dataset = New-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -File "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"
PS C:\> $Dataset.Policy.Validation | Format-List $dataset.Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}

MinimumRows   : 
MinimumSizeMB : 1
```

<span data-ttu-id="559dc-129">O primeiro comando cria um DataSet chamado DA_WikipediaClickEvents, como em um exemplo anterior, e, em seguida, atribui esse conjunto de DataSet à variável $Dataset.</span><span class="sxs-lookup"><span data-stu-id="559dc-129">The first command creates a dataset named DA_WikipediaClickEvents, as in a previous example, and then assigns that dataset to the $Dataset variable.</span></span>
<span data-ttu-id="559dc-130">O segundo comando obtém detalhes sobre as regras de validação para o conjunto de dados e, em seguida, passa-as para o cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="559dc-130">The second command gets details about the validation rules for the dataset, and then passes them to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="559dc-131">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="559dc-131">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="559dc-132">Para obter mais informações, digite `Get-Help Format-List` .</span><span class="sxs-lookup"><span data-stu-id="559dc-132">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="559dc-133">OS</span><span class="sxs-lookup"><span data-stu-id="559dc-133">PARAMETERS</span></span>

### <span data-ttu-id="559dc-134">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="559dc-134">-DataFactory</span></span>
<span data-ttu-id="559dc-135">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="559dc-135">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="559dc-136">Esse cmdlet cria um conjunto de dados na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="559dc-136">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="559dc-137">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="559dc-137">-DataFactoryName</span></span>
<span data-ttu-id="559dc-138">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="559dc-138">Specifies the name of a data factory.</span></span>
<span data-ttu-id="559dc-139">Esse cmdlet cria um conjunto de dados na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="559dc-139">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="559dc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="559dc-140">-DefaultProfile</span></span>
<span data-ttu-id="559dc-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="559dc-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="559dc-142">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="559dc-142">-File</span></span>
<span data-ttu-id="559dc-143">Especifica o caminho completo do arquivo JSON (JavaScript Object Notation) que contém a descrição do DataSet.</span><span class="sxs-lookup"><span data-stu-id="559dc-143">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the dataset.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559dc-144">-Force</span><span class="sxs-lookup"><span data-stu-id="559dc-144">-Force</span></span>
<span data-ttu-id="559dc-145">Indica que esse cmdlet substitui um DataSet existente sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="559dc-145">Indicates that this cmdlet replaces an existing dataset without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559dc-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="559dc-146">-Name</span></span>
<span data-ttu-id="559dc-147">Especifica o nome do DataSet a ser criado.</span><span class="sxs-lookup"><span data-stu-id="559dc-147">Specifies the name of the dataset to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="559dc-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="559dc-148">-ResourceGroupName</span></span>
<span data-ttu-id="559dc-149">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="559dc-149">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="559dc-150">Esse cmdlet cria um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de um grupo.</span><span class="sxs-lookup"><span data-stu-id="559dc-150">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="559dc-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="559dc-151">-Confirm</span></span>
<span data-ttu-id="559dc-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="559dc-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559dc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="559dc-153">-WhatIf</span></span>
<span data-ttu-id="559dc-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="559dc-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="559dc-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="559dc-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="559dc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="559dc-156">CommonParameters</span></span>
<span data-ttu-id="559dc-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="559dc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="559dc-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="559dc-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="559dc-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="559dc-159">INPUTS</span></span>

### <span data-ttu-id="559dc-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="559dc-160">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="559dc-161">System. String</span><span class="sxs-lookup"><span data-stu-id="559dc-161">System.String</span></span>

## <span data-ttu-id="559dc-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="559dc-162">OUTPUTS</span></span>

### <span data-ttu-id="559dc-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="559dc-163">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="559dc-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="559dc-164">NOTES</span></span>
* <span data-ttu-id="559dc-165">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="559dc-165">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="559dc-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="559dc-166">RELATED LINKS</span></span>

[<span data-ttu-id="559dc-167">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="559dc-167">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="559dc-168">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="559dc-168">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


