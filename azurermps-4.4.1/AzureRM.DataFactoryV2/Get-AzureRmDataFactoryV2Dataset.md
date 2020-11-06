---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: ec66f865c4a511935599b81b672cd60d6da78485
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441135"
---
# <span data-ttu-id="fdeed-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fdeed-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="fdeed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fdeed-102">SYNOPSIS</span></span>
<span data-ttu-id="fdeed-103">Obtém informações sobre conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="fdeed-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdeed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fdeed-104">SYNTAX</span></span>

### <span data-ttu-id="fdeed-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fdeed-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
```

### <span data-ttu-id="fdeed-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fdeed-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
```

## <span data-ttu-id="fdeed-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fdeed-107">DESCRIPTION</span></span>
<span data-ttu-id="fdeed-108">O cmdlet Get-AzureRmDataFactoryV2Dataset Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="fdeed-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="fdeed-109">Se você especificar o nome de um conjunto de dados, esse cmdlet obterá informações sobre esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="fdeed-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="fdeed-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="fdeed-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="fdeed-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fdeed-111">EXAMPLES</span></span>

### <span data-ttu-id="fdeed-112">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="fdeed-112">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

    DatasetName       : DACuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

    DatasetName       : DAWikiAggregatedData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="fdeed-113">Esse comando obtém informações sobre todos os conjuntos de dados no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="fdeed-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="fdeed-114">Exemplo 2: obter informações sobre um conjunto de dados específico</span><span class="sxs-lookup"><span data-stu-id="fdeed-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="fdeed-115">Esse comando obtém informações sobre o conjunto de dados chamado DAWikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="fdeed-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="fdeed-116">OS</span><span class="sxs-lookup"><span data-stu-id="fdeed-116">PARAMETERS</span></span>

### <span data-ttu-id="fdeed-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="fdeed-117">-DataFactory</span></span>
<span data-ttu-id="fdeed-118">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="fdeed-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="fdeed-119">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="fdeed-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="fdeed-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="fdeed-120">-DataFactoryName</span></span>
<span data-ttu-id="fdeed-121">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="fdeed-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="fdeed-122">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="fdeed-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="fdeed-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdeed-123">-Name</span></span>
<span data-ttu-id="fdeed-124">Especifica o nome do conjunto de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="fdeed-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdeed-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdeed-125">-ResourceGroupName</span></span>
<span data-ttu-id="fdeed-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="fdeed-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fdeed-127">Esse cmdlet obtém DataSets que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="fdeed-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="fdeed-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fdeed-128">INPUTS</span></span>

### <span data-ttu-id="fdeed-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fdeed-129">System.String</span></span>
<span data-ttu-id="fdeed-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fdeed-130">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="fdeed-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fdeed-131">OUTPUTS</span></span>

### <span data-ttu-id="fdeed-132">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="fdeed-132">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fdeed-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="fdeed-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="fdeed-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fdeed-134">NOTES</span></span>
<span data-ttu-id="fdeed-135">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="fdeed-135">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fdeed-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fdeed-136">RELATED LINKS</span></span>
[<span data-ttu-id="fdeed-137">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fdeed-137">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="fdeed-138">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="fdeed-138">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
