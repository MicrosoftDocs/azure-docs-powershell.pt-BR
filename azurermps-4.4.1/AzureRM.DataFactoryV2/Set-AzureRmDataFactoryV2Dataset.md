---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 311073fcd840e9d163c1316019e48569f7e59c81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611131"
---
# <span data-ttu-id="59c17-101">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="59c17-101">Set-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="59c17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59c17-102">SYNOPSIS</span></span>
<span data-ttu-id="59c17-103">Cria um conjunto de dados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="59c17-103">Creates a dataset in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59c17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59c17-104">SYNTAX</span></span>

### <span data-ttu-id="59c17-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="59c17-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="59c17-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59c17-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Dataset [-DefinitionFile] <String> [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="59c17-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59c17-107">DESCRIPTION</span></span>
<span data-ttu-id="59c17-108">O cmdlet Set-AzureRmDataFactoryV2Dataset cria um DataSet no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="59c17-108">The Set-AzureRmDataFactoryV2Dataset cmdlet creates a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="59c17-109">Se você especificar um nome para um DataSet que já existe, esse cmdlet solicitará confirmação antes de substituir o DataSet.</span><span class="sxs-lookup"><span data-stu-id="59c17-109">If you specify a name for a dataset that already exists, this cmdlet prompts you for confirmation before it replaces the dataset.</span></span>
<span data-ttu-id="59c17-110">Se você especificar o parâmetro Force, o cmdlet substituirá o DataSet existente sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="59c17-110">If you specify the Force parameter, the cmdlet replaces the existing dataset without confirmation.</span></span>

<span data-ttu-id="59c17-111">Execute estas operações na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="59c17-111">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

<span data-ttu-id="59c17-112">Se um conjunto de dados com o mesmo nome já existir na fábrica de dados, esse cmdlet solicitará que você confirme se deseja substituir o conjunto de dados existente pelo novo conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="59c17-112">If a dataset with the same name already exists in the data factory, this cmdlet prompts you to confirm whether to overwrite the existing dataset with the new dataset.</span></span>
<span data-ttu-id="59c17-113">Se você confirmar para substituir o conjunto de um conjunto de um existente, a definição de DataSet também será substituída.</span><span class="sxs-lookup"><span data-stu-id="59c17-113">If you confirm to overwrite the existing dataset, the dataset definition is also replaced.</span></span>

## <span data-ttu-id="59c17-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59c17-114">EXAMPLES</span></span>

### <span data-ttu-id="59c17-115">Exemplo 1: criar um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="59c17-115">Example 1: Create a dataset</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikipediaClickEvents" -DefinitionFile "C:\\samples\\WikiSample\\DA_WikipediaClickEvents.json"

    DatasetName       : DAWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Structure         :
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureBlobDataset

```

<span data-ttu-id="59c17-116">Esse comando cria um conjunto de dados chamado DA_WikipediaClickEvents no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="59c17-116">This command creates a dataset named DA_WikipediaClickEvents in the data factory named WikiADF.</span></span>
<span data-ttu-id="59c17-117">O comando baseia o DataSet nas informações do DAWikipediaClickEvents.jsem arquivo.</span><span class="sxs-lookup"><span data-stu-id="59c17-117">The command bases the dataset on information in the DAWikipediaClickEvents.json file.</span></span>

## <span data-ttu-id="59c17-118">OS</span><span class="sxs-lookup"><span data-stu-id="59c17-118">PARAMETERS</span></span>

### <span data-ttu-id="59c17-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="59c17-119">-Confirm</span></span>
<span data-ttu-id="59c17-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59c17-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c17-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="59c17-121">-DataFactoryName</span></span>
<span data-ttu-id="59c17-122">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="59c17-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="59c17-123">Esse cmdlet cria um conjunto de dados na fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="59c17-123">This cmdlet creates a dataset in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="59c17-124">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="59c17-124">-DefinitionFile</span></span>
<span data-ttu-id="59c17-125">O caminho do arquivo JSON.</span><span class="sxs-lookup"><span data-stu-id="59c17-125">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c17-126">-Force</span><span class="sxs-lookup"><span data-stu-id="59c17-126">-Force</span></span>
<span data-ttu-id="59c17-127">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="59c17-127">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59c17-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="59c17-128">-Name</span></span>
<span data-ttu-id="59c17-129">Especifica o nome do DataSet a ser criado.</span><span class="sxs-lookup"><span data-stu-id="59c17-129">Specifies the name of the dataset to create.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c17-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c17-130">-ResourceGroupName</span></span>
<span data-ttu-id="59c17-131">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="59c17-131">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="59c17-132">Esse cmdlet cria um conjunto de um conjunto de um conjunto de um conjunto de um conjunto de um grupo.</span><span class="sxs-lookup"><span data-stu-id="59c17-132">This cmdlet creates a dataset in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="59c17-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59c17-133">-ResourceId</span></span>
<span data-ttu-id="59c17-134">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="59c17-134">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59c17-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c17-135">-WhatIf</span></span>
<span data-ttu-id="59c17-136">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59c17-136">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="59c17-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59c17-137">INPUTS</span></span>

### <span data-ttu-id="59c17-138">System. String</span><span class="sxs-lookup"><span data-stu-id="59c17-138">System.String</span></span>


## <span data-ttu-id="59c17-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59c17-139">OUTPUTS</span></span>

### <span data-ttu-id="59c17-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="59c17-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>


## <span data-ttu-id="59c17-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59c17-141">NOTES</span></span>
<span data-ttu-id="59c17-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="59c17-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="59c17-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59c17-143">RELATED LINKS</span></span>
[<span data-ttu-id="59c17-144">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="59c17-144">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="59c17-145">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="59c17-145">Remove-AzureRmDataFactoryV2Dataset</span></span>]()
