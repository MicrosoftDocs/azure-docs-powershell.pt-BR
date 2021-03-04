---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 938b51b6025a420570ad62b4e9ce815fe832c4cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888295"
---
# <span data-ttu-id="1b80d-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1b80d-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="1b80d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b80d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b80d-103">Obtém informações sobre conjuntos de dados no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1b80d-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="1b80d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1b80d-104">SYNTAX</span></span>

### <span data-ttu-id="1b80d-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1b80d-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b80d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1b80d-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b80d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1b80d-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b80d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1b80d-108">DESCRIPTION</span></span>
<span data-ttu-id="1b80d-109">O Get-AzDataFactoryV2Dataset cmdlet obtém informações sobre conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="1b80d-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="1b80d-110">Se você especificar o nome de um conjuntos de dados, esse cmdlet obterá informações sobre esse conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="1b80d-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="1b80d-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados no fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1b80d-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="1b80d-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1b80d-112">EXAMPLES</span></span>

### <span data-ttu-id="1b80d-113">Exemplo 1: obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="1b80d-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="1b80d-114">Este comando obtém informações sobre todos os conjuntos de dados no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1b80d-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="1b80d-115">Exemplo 2: obter informações sobre um conjuntos de dados específico</span><span class="sxs-lookup"><span data-stu-id="1b80d-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="1b80d-116">Este comando obtém informações sobre o conjuntos de dados chamado DAWikipediaClickEvents no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1b80d-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="1b80d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1b80d-117">PARAMETERS</span></span>

### <span data-ttu-id="1b80d-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1b80d-118">-DataFactory</span></span>
<span data-ttu-id="1b80d-119">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="1b80d-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="1b80d-120">Este cmdlet obtém conjuntos de dados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1b80d-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b80d-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1b80d-121">-DataFactoryName</span></span>
<span data-ttu-id="1b80d-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1b80d-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1b80d-123">Este cmdlet obtém conjuntos de dados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1b80d-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b80d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b80d-124">-DefaultProfile</span></span>
<span data-ttu-id="1b80d-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1b80d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b80d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1b80d-126">-Name</span></span>
<span data-ttu-id="1b80d-127">Especifica o nome do conjuntos de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="1b80d-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="1b80d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b80d-128">-ResourceGroupName</span></span>
<span data-ttu-id="1b80d-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b80d-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1b80d-130">Este cmdlet obtém conjuntos de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1b80d-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1b80d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b80d-131">-ResourceId</span></span>
<span data-ttu-id="1b80d-132">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1b80d-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1b80d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b80d-133">CommonParameters</span></span>
<span data-ttu-id="1b80d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b80d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b80d-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b80d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b80d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b80d-136">INPUTS</span></span>

### <span data-ttu-id="1b80d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1b80d-137">System.String</span></span>

### <span data-ttu-id="1b80d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b80d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1b80d-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1b80d-139">OUTPUTS</span></span>

### <span data-ttu-id="1b80d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="1b80d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="1b80d-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="1b80d-141">NOTES</span></span>
<span data-ttu-id="1b80d-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="1b80d-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b80d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1b80d-143">RELATED LINKS</span></span>

[<span data-ttu-id="1b80d-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1b80d-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="1b80d-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1b80d-145">Remove-AzDataFactoryV2Dataset</span></span>]()
