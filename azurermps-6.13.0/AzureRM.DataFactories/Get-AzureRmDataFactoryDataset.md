---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 6f6421659f47d2a6d119d5acd8e614765f356298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610090"
---
# <span data-ttu-id="c1141-101">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c1141-101">Get-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="c1141-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c1141-102">SYNOPSIS</span></span>
<span data-ttu-id="c1141-103">Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c1141-103">Gets information about datasets in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1141-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1141-104">SYNTAX</span></span>

### <span data-ttu-id="c1141-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c1141-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1141-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c1141-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1141-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c1141-107">DESCRIPTION</span></span>
<span data-ttu-id="c1141-108">O cmdlet **Get-AzureRmDataFactoryDataset** Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="c1141-108">The **Get-AzureRmDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="c1141-109">Se você especificar o nome de um conjunto de dados, esse cmdlet obterá informações sobre esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="c1141-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="c1141-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c1141-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="c1141-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1141-111">EXAMPLES</span></span>

### <span data-ttu-id="c1141-112">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="c1141-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
DatasetName       : DACuratedWikiData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}

DatasetName         : DAWikiAggregatedData
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : 
Policy            : 
Structure         : {}
```

<span data-ttu-id="c1141-113">Esse comando obtém informações sobre todos os conjuntos de dados no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c1141-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="c1141-114">Exemplo 2: obter informações sobre um conjunto de dados específico</span><span class="sxs-lookup"><span data-stu-id="c1141-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="c1141-115">Esse comando obtém informações sobre o conjunto de dados chamado DAWikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="c1141-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="c1141-116">Exemplo 3: obter o local de um conjunto de um conjunto de um específico</span><span class="sxs-lookup"><span data-stu-id="c1141-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="c1141-117">Esse comando obtém informações para o conjunto de dados chamado DAWikipediaClickEvents na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir o **local** associado a esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="c1141-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="c1141-118">Como alternativa, atribua a saída do cmdlet **Get-AzureRmDataFactoryDataset** a uma variável e, em seguida, use a notação de ponto para exibir a propriedade Location associada ao objeto DataSet armazenado nessa variável.</span><span class="sxs-lookup"><span data-stu-id="c1141-118">Alternatively, assign the output of the **Get-AzureRmDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="c1141-119">OS</span><span class="sxs-lookup"><span data-stu-id="c1141-119">PARAMETERS</span></span>

### <span data-ttu-id="c1141-120">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="c1141-120">-DataFactory</span></span>
<span data-ttu-id="c1141-121">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="c1141-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c1141-122">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c1141-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1141-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c1141-123">-DataFactoryName</span></span>
<span data-ttu-id="c1141-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c1141-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c1141-125">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c1141-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1141-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1141-126">-DefaultProfile</span></span>
<span data-ttu-id="c1141-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c1141-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1141-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1141-128">-Name</span></span>
<span data-ttu-id="c1141-129">Especifica o nome do conjunto de dados sobre o qual esse cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="c1141-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="c1141-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1141-130">-ResourceGroupName</span></span>
<span data-ttu-id="c1141-131">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c1141-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c1141-132">Esse cmdlet obtém DataSets que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c1141-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1141-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1141-133">CommonParameters</span></span>
<span data-ttu-id="c1141-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1141-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1141-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1141-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1141-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c1141-136">INPUTS</span></span>

### <span data-ttu-id="c1141-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c1141-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c1141-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c1141-138">System.String</span></span>

## <span data-ttu-id="c1141-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c1141-139">OUTPUTS</span></span>

### <span data-ttu-id="c1141-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="c1141-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="c1141-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c1141-141">NOTES</span></span>
* <span data-ttu-id="c1141-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c1141-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c1141-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1141-143">RELATED LINKS</span></span>

[<span data-ttu-id="c1141-144">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c1141-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="c1141-145">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="c1141-145">Remove-AzureRmDataFactoryDataset</span></span>](./Remove-AzureRmDataFactoryDataset.md)


