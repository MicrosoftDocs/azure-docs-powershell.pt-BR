---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2Dataset.md
ms.openlocfilehash: 01c2849c69cfbdd785fae092aeed63117a07b1ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428252"
---
# <span data-ttu-id="9550f-101">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9550f-101">Get-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="9550f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9550f-102">SYNOPSIS</span></span>
<span data-ttu-id="9550f-103">Obtém informações sobre conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9550f-103">Gets information about datasets in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9550f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9550f-104">SYNTAX</span></span>

### <span data-ttu-id="9550f-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="9550f-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9550f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9550f-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9550f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9550f-107">DESCRIPTION</span></span>
<span data-ttu-id="9550f-108">O cmdlet Get-AzureRmDataFactoryV2Dataset Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="9550f-108">The Get-AzureRmDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="9550f-109">Se você especificar o nome de um conjunto de dados, esse cmdlet obterá informações sobre esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="9550f-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="9550f-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9550f-110">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="9550f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9550f-111">EXAMPLES</span></span>

### <span data-ttu-id="9550f-112">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="9550f-112">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="9550f-113">Esse comando obtém informações sobre todos os conjuntos de dados no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9550f-113">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="9550f-114">Exemplo 2: obter informações sobre um conjunto de dados específico</span><span class="sxs-lookup"><span data-stu-id="9550f-114">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="9550f-115">Esse comando obtém informações sobre o conjunto de dados chamado DAWikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="9550f-115">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="9550f-116">OS</span><span class="sxs-lookup"><span data-stu-id="9550f-116">PARAMETERS</span></span>

### <span data-ttu-id="9550f-117">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="9550f-117">-DataFactory</span></span>
<span data-ttu-id="9550f-118">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="9550f-118">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="9550f-119">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9550f-119">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>


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

### <span data-ttu-id="9550f-120">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="9550f-120">-DataFactoryName</span></span>
<span data-ttu-id="9550f-121">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="9550f-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9550f-122">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9550f-122">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9550f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="9550f-123">-Name</span></span>
<span data-ttu-id="9550f-124">Especifica o nome do conjunto de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="9550f-124">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9550f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9550f-125">-ResourceGroupName</span></span>
<span data-ttu-id="9550f-126">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="9550f-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9550f-127">Esse cmdlet obtém DataSets que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9550f-127">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9550f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9550f-128">-DefaultProfile</span></span>
<span data-ttu-id="9550f-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9550f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9550f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9550f-130">CommonParameters</span></span>
<span data-ttu-id="9550f-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9550f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9550f-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9550f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9550f-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9550f-133">INPUTS</span></span>

### <span data-ttu-id="9550f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9550f-134">System.String</span></span>
<span data-ttu-id="9550f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9550f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="9550f-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9550f-136">OUTPUTS</span></span>

### <span data-ttu-id="9550f-137">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9550f-137">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9550f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="9550f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="9550f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9550f-139">NOTES</span></span>
<span data-ttu-id="9550f-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="9550f-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9550f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9550f-141">RELATED LINKS</span></span>

[<span data-ttu-id="9550f-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9550f-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="9550f-143">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="9550f-143">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
