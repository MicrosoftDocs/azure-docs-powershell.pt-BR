---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: fe5359740975776e5796dce2a6d4959ed289cae6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597087"
---
# <span data-ttu-id="3837f-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3837f-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="3837f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3837f-102">SYNOPSIS</span></span>
<span data-ttu-id="3837f-103">Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="3837f-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="3837f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3837f-104">SYNTAX</span></span>

### <span data-ttu-id="3837f-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3837f-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3837f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3837f-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3837f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3837f-107">DESCRIPTION</span></span>
<span data-ttu-id="3837f-108">O cmdlet **Get-AzDataFactoryDataset** Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="3837f-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="3837f-109">Se você especificar o nome de um conjunto de dados, esse cmdlet obterá informações sobre esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="3837f-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="3837f-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3837f-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="3837f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3837f-111">EXAMPLES</span></span>

### <span data-ttu-id="3837f-112">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="3837f-112">Example 1: Get information about all datasets</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" 
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

<span data-ttu-id="3837f-113">Esse comando obtém informações sobre todos os conjuntos de dados no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3837f-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="3837f-114">Exemplo 2: obter informações sobre um conjunto de dados específico</span><span class="sxs-lookup"><span data-stu-id="3837f-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\>Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" 
DatasetName       : DAWikipediaClickEvents
ResourceGroupName : ADF
DataFactoryName   : WikiADF
Availability      : Microsoft.DataFactories.Availability
Location          : Microsoft.DataFactories.AzureBlobLocation
Policy            : Microsoft.DataFactories.Policy
Structure         : {}
```

<span data-ttu-id="3837f-115">Esse comando obtém informações sobre o conjunto de dados chamado DAWikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="3837f-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="3837f-116">Exemplo 3: obter o local de um conjunto de um conjunto de um específico</span><span class="sxs-lookup"><span data-stu-id="3837f-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="3837f-117">Esse comando obtém informações para o conjunto de dados chamado DAWikipediaClickEvents na fábrica de dados chamado WikiADF e, em seguida, usa a notação de ponto padrão para exibir o **local** associado a esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="3837f-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="3837f-118">Como alternativa, atribua a saída do cmdlet **Get-AzDataFactoryDataset** a uma variável e, em seguida, use a notação de ponto para exibir a propriedade Location associada ao objeto DataSet armazenado nessa variável.</span><span class="sxs-lookup"><span data-stu-id="3837f-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="3837f-119">OS</span><span class="sxs-lookup"><span data-stu-id="3837f-119">PARAMETERS</span></span>

### <span data-ttu-id="3837f-120">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="3837f-120">-DataFactory</span></span>
<span data-ttu-id="3837f-121">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="3837f-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="3837f-122">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3837f-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3837f-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3837f-123">-DataFactoryName</span></span>
<span data-ttu-id="3837f-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="3837f-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="3837f-125">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3837f-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="3837f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3837f-126">-DefaultProfile</span></span>
<span data-ttu-id="3837f-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3837f-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3837f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="3837f-128">-Name</span></span>
<span data-ttu-id="3837f-129">Especifica o nome do conjunto de dados sobre o qual esse cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="3837f-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="3837f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3837f-130">-ResourceGroupName</span></span>
<span data-ttu-id="3837f-131">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="3837f-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3837f-132">Esse cmdlet obtém DataSets que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3837f-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3837f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3837f-133">CommonParameters</span></span>
<span data-ttu-id="3837f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3837f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3837f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3837f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3837f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3837f-136">INPUTS</span></span>

### <span data-ttu-id="3837f-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3837f-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3837f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3837f-138">System.String</span></span>

## <span data-ttu-id="3837f-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3837f-139">OUTPUTS</span></span>

### <span data-ttu-id="3837f-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="3837f-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="3837f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3837f-141">NOTES</span></span>
* <span data-ttu-id="3837f-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="3837f-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3837f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3837f-143">RELATED LINKS</span></span>

[<span data-ttu-id="3837f-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3837f-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="3837f-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="3837f-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


