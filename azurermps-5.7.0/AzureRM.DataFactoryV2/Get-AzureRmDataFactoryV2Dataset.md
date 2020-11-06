---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 171431e317b9edbafe83f7c0c836f5543fcbd65d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430506"
---
# <span data-ttu-id="2fb0c-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2fb0c-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="2fb0c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb0c-103">Obtém informações sobre conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fb0c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fb0c-104">SYNTAX</span></span>

### <span data-ttu-id="2fb0c-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2fb0c-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fb0c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2fb0c-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fb0c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fb0c-107">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2Dataset -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fb0c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2fb0c-108">DESCRIPTION</span></span>
<span data-ttu-id="2fb0c-109">O cmdlet Get-AzureRmDataFactoryV2Dataset Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-109">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="2fb0c-110">Se você especificar o nome de um conjunto de dados, esse cmdlet obterá informações sobre esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="2fb0c-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="2fb0c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fb0c-112">EXAMPLES</span></span>

### <span data-ttu-id="2fb0c-113">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="2fb0c-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="2fb0c-114">Esse comando obtém informações sobre todos os conjuntos de dados no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="2fb0c-115">Exemplo 2: obter informações sobre um conjunto de dados específico</span><span class="sxs-lookup"><span data-stu-id="2fb0c-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="2fb0c-116">Esse comando obtém informações sobre o conjunto de dados chamado DAWikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="2fb0c-117">OS</span><span class="sxs-lookup"><span data-stu-id="2fb0c-117">PARAMETERS</span></span>

### <span data-ttu-id="2fb0c-118">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="2fb0c-118">-DataFactory</span></span>
<span data-ttu-id="2fb0c-119">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="2fb0c-120">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="2fb0c-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2fb0c-121">-DataFactoryName</span></span>
<span data-ttu-id="2fb0c-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2fb0c-123">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2fb0c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb0c-124">-DefaultProfile</span></span>
<span data-ttu-id="2fb0c-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fb0c-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fb0c-126">-Name</span></span>
<span data-ttu-id="2fb0c-127">Especifica o nome do conjunto de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb0c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb0c-128">-ResourceGroupName</span></span>
<span data-ttu-id="2fb0c-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2fb0c-130">Esse cmdlet obtém DataSets que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2fb0c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fb0c-131">-ResourceId</span></span>
<span data-ttu-id="2fb0c-132">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2fb0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb0c-133">CommonParameters</span></span>
<span data-ttu-id="2fb0c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb0c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb0c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb0c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2fb0c-136">INPUTS</span></span>

### <span data-ttu-id="2fb0c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2fb0c-137">System.String</span></span>
<span data-ttu-id="2fb0c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2fb0c-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2fb0c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2fb0c-139">OUTPUTS</span></span>

### <span data-ttu-id="2fb0c-140">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2fb0c-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2fb0c-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="2fb0c-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="2fb0c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2fb0c-142">NOTES</span></span>
<span data-ttu-id="2fb0c-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="2fb0c-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2fb0c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fb0c-144">RELATED LINKS</span></span>

[<span data-ttu-id="2fb0c-145">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2fb0c-145">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="2fb0c-146">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2fb0c-146">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
