---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433921"
---
# <span data-ttu-id="2a8ec-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2a8ec-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="2a8ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2a8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8ec-103">Obtém informações sobre conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="2a8ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a8ec-104">SYNTAX</span></span>

### <span data-ttu-id="2a8ec-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2a8ec-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a8ec-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2a8ec-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a8ec-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a8ec-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a8ec-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2a8ec-108">DESCRIPTION</span></span>
<span data-ttu-id="2a8ec-109">O cmdlet Get-AzDataFactoryV2Dataset Obtém informações sobre conjuntos de dados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="2a8ec-110">Se você especificar o nome de um conjunto de dados, esse cmdlet obterá informações sobre esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="2a8ec-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="2a8ec-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2a8ec-112">EXAMPLES</span></span>

### <span data-ttu-id="2a8ec-113">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="2a8ec-113">Example 1: Get information about all datasets</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF"

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

<span data-ttu-id="2a8ec-114">Esse comando obtém informações sobre todos os conjuntos de dados no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="2a8ec-115">Exemplo 2: obter informações sobre um conjunto de dados específico</span><span class="sxs-lookup"><span data-stu-id="2a8ec-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="2a8ec-116">Esse comando obtém informações sobre o conjunto de dados chamado DAWikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="2a8ec-117">OS</span><span class="sxs-lookup"><span data-stu-id="2a8ec-117">PARAMETERS</span></span>

### <span data-ttu-id="2a8ec-118">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="2a8ec-118">-DataFactory</span></span>
<span data-ttu-id="2a8ec-119">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="2a8ec-120">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a8ec-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="2a8ec-121">-DataFactoryName</span></span>
<span data-ttu-id="2a8ec-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2a8ec-123">Esse cmdlet obtém conjuntos de dados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a8ec-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8ec-124">-DefaultProfile</span></span>
<span data-ttu-id="2a8ec-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a8ec-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a8ec-126">-Name</span></span>
<span data-ttu-id="2a8ec-127">Especifica o nome do conjunto de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-127">Specifies the name of the dataset about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases: DatasetName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a8ec-128">-ResourceGroupName</span></span>
<span data-ttu-id="2a8ec-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2a8ec-130">Esse cmdlet obtém DataSets que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a8ec-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a8ec-131">-ResourceId</span></span>
<span data-ttu-id="2a8ec-132">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-132">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a8ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8ec-133">CommonParameters</span></span>
<span data-ttu-id="2a8ec-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8ec-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a8ec-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8ec-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2a8ec-136">INPUTS</span></span>

### <span data-ttu-id="2a8ec-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2a8ec-137">System.String</span></span>

### <span data-ttu-id="2a8ec-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2a8ec-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2a8ec-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2a8ec-139">OUTPUTS</span></span>

### <span data-ttu-id="2a8ec-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="2a8ec-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="2a8ec-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2a8ec-141">NOTES</span></span>
<span data-ttu-id="2a8ec-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="2a8ec-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2a8ec-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2a8ec-143">RELATED LINKS</span></span>

[<span data-ttu-id="2a8ec-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2a8ec-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="2a8ec-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="2a8ec-145">Remove-AzDataFactoryV2Dataset</span></span>]()
