---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 5af8053f3d504cfc3eb28a2f8ad71f83492f0e3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117749"
---
# <span data-ttu-id="efc0a-101">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="efc0a-101">Get-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="efc0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="efc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="efc0a-103">Obtém informações sobre conjuntos de dados no Data Factory.</span><span class="sxs-lookup"><span data-stu-id="efc0a-103">Gets information about datasets in Data Factory.</span></span>

## <span data-ttu-id="efc0a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efc0a-104">SYNTAX</span></span>

### <span data-ttu-id="efc0a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="efc0a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efc0a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="efc0a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2Dataset [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efc0a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="efc0a-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2Dataset [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efc0a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="efc0a-108">DESCRIPTION</span></span>
<span data-ttu-id="efc0a-109">O Get-AzDataFactoryV2Dataset cmdlet obtém informações sobre conjuntos de dados no Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="efc0a-109">The Get-AzDataFactoryV2Dataset cmdlet gets information about datasets in Azure Data Factory.</span></span>
<span data-ttu-id="efc0a-110">Se você especificar o nome de um conjuntos de dados, esse cmdlet obterá informações sobre esse conjuntos de dados.</span><span class="sxs-lookup"><span data-stu-id="efc0a-110">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="efc0a-111">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os conjuntos de dados no fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="efc0a-111">If you do not specify a name, this cmdlet gets information about all the datasets in the data factory.</span></span>

## <span data-ttu-id="efc0a-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="efc0a-112">EXAMPLES</span></span>

### <span data-ttu-id="efc0a-113">Exemplo 1: Obter informações sobre todos os conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="efc0a-113">Example 1: Get information about all datasets</span></span>
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

<span data-ttu-id="efc0a-114">Esse comando obtém informações sobre todos os conjuntos de dados no fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="efc0a-114">This command gets information about all datasets in the data factory named WikiADF.</span></span>

### <span data-ttu-id="efc0a-115">Exemplo 2: Obter informações sobre um determinado conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="efc0a-115">Example 2: Get information about a specific dataset</span></span>
```
PS C:\> Get-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset
```

<span data-ttu-id="efc0a-116">Este comando obtém informações sobre o conjuntos de dados chamado DAWikipediaClickEvents na fábrica de dados chamada WikiADF.</span><span class="sxs-lookup"><span data-stu-id="efc0a-116">This command gets information about the dataset named DAWikipediaClickEvents in the data factory named WikiADF.</span></span>

## <span data-ttu-id="efc0a-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efc0a-117">PARAMETERS</span></span>

### <span data-ttu-id="efc0a-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="efc0a-118">-DataFactory</span></span>
<span data-ttu-id="efc0a-119">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="efc0a-119">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="efc0a-120">Este cmdlet obtém conjuntos de dados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="efc0a-120">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="efc0a-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="efc0a-121">-DataFactoryName</span></span>
<span data-ttu-id="efc0a-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="efc0a-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="efc0a-123">Este cmdlet obtém conjuntos de dados que pertencem ao fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="efc0a-123">This cmdlet gets datasets that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="efc0a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc0a-124">-DefaultProfile</span></span>
<span data-ttu-id="efc0a-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="efc0a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efc0a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="efc0a-126">-Name</span></span>
<span data-ttu-id="efc0a-127">Especifica o nome do conjuntos de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="efc0a-127">Specifies the name of the dataset about which to get information.</span></span>

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

### <span data-ttu-id="efc0a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc0a-128">-ResourceGroupName</span></span>
<span data-ttu-id="efc0a-129">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="efc0a-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="efc0a-130">Este cmdlet obtém conjuntos de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="efc0a-130">This cmdlet gets datasets that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="efc0a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="efc0a-131">-ResourceId</span></span>
<span data-ttu-id="efc0a-132">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="efc0a-132">The Azure resource ID.</span></span>

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

### <span data-ttu-id="efc0a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc0a-133">CommonParameters</span></span>
<span data-ttu-id="efc0a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc0a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc0a-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc0a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc0a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="efc0a-136">INPUTS</span></span>

### <span data-ttu-id="efc0a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="efc0a-137">System.String</span></span>

### <span data-ttu-id="efc0a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="efc0a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="efc0a-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="efc0a-139">OUTPUTS</span></span>

### <span data-ttu-id="efc0a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="efc0a-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

## <span data-ttu-id="efc0a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="efc0a-141">NOTES</span></span>
<span data-ttu-id="efc0a-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="efc0a-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="efc0a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="efc0a-143">RELATED LINKS</span></span>

[<span data-ttu-id="efc0a-144">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="efc0a-144">Set-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="efc0a-145">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="efc0a-145">Remove-AzDataFactoryV2Dataset</span></span>]()
