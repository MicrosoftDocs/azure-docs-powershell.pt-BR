---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: BB18EEF3-570A-4667-AF0E-FCEEE17B4905
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryDataset.md
ms.openlocfilehash: c31a8bb3ef09eb190a7a4c77aef0c44fadbf8960
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890636"
---
# <span data-ttu-id="93c95-101">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="93c95-101">Get-AzDataFactoryDataset</span></span>

## <span data-ttu-id="93c95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93c95-102">SYNOPSIS</span></span>
<span data-ttu-id="93c95-103">Obtém informações sobre conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="93c95-103">Gets information about datasets in Azure Data Factory.</span></span>

## <span data-ttu-id="93c95-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="93c95-104">SYNTAX</span></span>

### <span data-ttu-id="93c95-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="93c95-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryDataset [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93c95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="93c95-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryDataset [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93c95-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93c95-107">DESCRIPTION</span></span>
<span data-ttu-id="93c95-108">O cmdlet **Get-AzDataFactoryDataset** obtém informações sobre conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="93c95-108">The **Get-AzDataFactoryDataset** cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="93c95-109">Se você especificar o nome de um conjuntos de dados, esse cmdlet obterá informações sobre esse conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="93c95-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="93c95-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados no fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="93c95-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="93c95-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93c95-111">EXAMPLES</span></span>

### <span data-ttu-id="93c95-112">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="93c95-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="93c95-113">Este comando obtém informações sobre todos os conjuntos de dados no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="93c95-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="93c95-114">Exemplo 2: obter informações sobre um conjuntos de dados específico</span><span class="sxs-lookup"><span data-stu-id="93c95-114">Example 2: Get information about a specific dataset</span></span>
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

<span data-ttu-id="93c95-115">Este comando obtém informações sobre o conjuntos de dados chamado DAWikipediaClickEvents no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="93c95-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

### <span data-ttu-id="93c95-116">Exemplo 3: Obter o local para um conjuntos de dados específico</span><span class="sxs-lookup"><span data-stu-id="93c95-116">Example 3: Get the location for a specific dataset</span></span>
```
PS C:\>(Get-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents").Location
BlobPath          : wikidatagateway/wikisampledatain/
FilenamePrefix    : 
Format            : 
LinkedServiceName : LinkedServiceWikipediaClickEvents
PartitionBy       : {}
```

<span data-ttu-id="93c95-117">Este comando obtém informações para o grupo de dados chamado DAWikipediaClickEvents no fábrica de dados chamado WikiADF e usa a notação de ponto padrão para exibir o **Local** associado a esse conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="93c95-117">This command gets information for the dataset named DAWikipediaClickEvents in the data factory named WikiADF, and then uses standard dot notation to view the **Location** associated with that dataset.</span></span>
<span data-ttu-id="93c95-118">Como alternativa, atribua a saída do cmdlet **Get-AzDataFactoryDataset** a uma variável e use a notação de ponto para exibir a propriedade Location associada ao objeto dataset armazenado nessa variável.</span><span class="sxs-lookup"><span data-stu-id="93c95-118">Alternatively, assign the output of the **Get-AzDataFactoryDataset** cmdlet to a variable, and then use dot notation to view the Location property associated with the dataset object stored in that variable.</span></span>

## <span data-ttu-id="93c95-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="93c95-119">PARAMETERS</span></span>

### <span data-ttu-id="93c95-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="93c95-120">-DataFactory</span></span>
<span data-ttu-id="93c95-121">Especifica um **objeto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="93c95-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="93c95-122">Este cmdlet obtém conjuntos de dados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="93c95-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="93c95-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="93c95-123">-DataFactoryName</span></span>
<span data-ttu-id="93c95-124">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="93c95-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="93c95-125">Este cmdlet obtém conjuntos de dados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="93c95-125">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="93c95-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c95-126">-DefaultProfile</span></span>
<span data-ttu-id="93c95-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="93c95-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93c95-128">-Name</span><span class="sxs-lookup"><span data-stu-id="93c95-128">-Name</span></span>
<span data-ttu-id="93c95-129">Especifica o nome do conjuntos de dados sobre o qual este cmdlet obtém informações.</span><span class="sxs-lookup"><span data-stu-id="93c95-129">Specifies the name of the dataset about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="93c95-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93c95-130">-ResourceGroupName</span></span>
<span data-ttu-id="93c95-131">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="93c95-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="93c95-132">Este cmdlet obtém conjuntos de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="93c95-132">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="93c95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c95-133">CommonParameters</span></span>
<span data-ttu-id="93c95-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93c95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c95-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93c95-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c95-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93c95-136">INPUTS</span></span>

### <span data-ttu-id="93c95-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="93c95-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="93c95-138">System.String</span><span class="sxs-lookup"><span data-stu-id="93c95-138">System.String</span></span>

## <span data-ttu-id="93c95-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="93c95-139">OUTPUTS</span></span>

### <span data-ttu-id="93c95-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="93c95-140">Microsoft.Azure.Commands.DataFactories.Models.PSDataset</span></span>

## <span data-ttu-id="93c95-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="93c95-141">NOTES</span></span>
* <span data-ttu-id="93c95-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="93c95-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="93c95-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93c95-143">RELATED LINKS</span></span>

[<span data-ttu-id="93c95-144">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="93c95-144">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)

[<span data-ttu-id="93c95-145">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="93c95-145">Remove-AzDataFactoryDataset</span></span>](./Remove-AzDataFactoryDataset.md)


