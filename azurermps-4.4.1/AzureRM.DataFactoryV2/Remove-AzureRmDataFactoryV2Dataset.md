---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Dataset.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 77cb56c08e29bd209ccf53fcdee42545b774c650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439957"
---
# <span data-ttu-id="1eaa0-101">Remove-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1eaa0-101">Remove-AzureRmDataFactoryV2Dataset</span></span>

## <span data-ttu-id="1eaa0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1eaa0-102">SYNOPSIS</span></span>
<span data-ttu-id="1eaa0-103">Remove um conjunto de dados da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-103">Removes a dataset from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eaa0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1eaa0-104">SYNTAX</span></span>

### <span data-ttu-id="1eaa0-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1eaa0-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1eaa0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1eaa0-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1eaa0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1eaa0-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1eaa0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1eaa0-108">DESCRIPTION</span></span>
<span data-ttu-id="1eaa0-109">O cmdlet Remove-AzureRmDataFactoryV2Dataset remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-109">The Remove-AzureRmDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="1eaa0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1eaa0-110">EXAMPLES</span></span>

### <span data-ttu-id="1eaa0-111">Exemplo 1: remover um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="1eaa0-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="1eaa0-112">Esse comando Remove o conjunto de dados chamado DAWikiAggregatedData da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="1eaa0-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="1eaa0-114">OS</span><span class="sxs-lookup"><span data-stu-id="1eaa0-114">PARAMETERS</span></span>

### <span data-ttu-id="1eaa0-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1eaa0-115">-Confirm</span></span>
<span data-ttu-id="1eaa0-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eaa0-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1eaa0-117">-DataFactoryName</span></span>
<span data-ttu-id="1eaa0-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="1eaa0-119">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="1eaa0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eaa0-120">-InputObject</span></span>
<span data-ttu-id="1eaa0-121">Especifica um objeto DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-121">Specifies a Dataset object to remove.</span></span>

```yaml
Type: PSDataset
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1eaa0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1eaa0-122">-Force</span></span>
<span data-ttu-id="1eaa0-123">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-123">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1eaa0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eaa0-124">-Name</span></span>
<span data-ttu-id="1eaa0-125">Especifica o nome do DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eaa0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eaa0-126">-ResourceGroupName</span></span>
<span data-ttu-id="1eaa0-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="1eaa0-128">Esse cmdlet Remove um DataSet do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1eaa0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eaa0-129">-ResourceId</span></span>
<span data-ttu-id="1eaa0-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1eaa0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eaa0-131">-WhatIf</span></span>
<span data-ttu-id="1eaa0-132">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eaa0-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="1eaa0-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1eaa0-133">INPUTS</span></span>

### <span data-ttu-id="1eaa0-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="1eaa0-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>
<span data-ttu-id="1eaa0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1eaa0-135">System.String</span></span>


## <span data-ttu-id="1eaa0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1eaa0-136">OUTPUTS</span></span>

### <span data-ttu-id="1eaa0-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="1eaa0-137">System.Object</span></span>

## <span data-ttu-id="1eaa0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1eaa0-138">NOTES</span></span>
<span data-ttu-id="1eaa0-139">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="1eaa0-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1eaa0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1eaa0-140">RELATED LINKS</span></span>
[<span data-ttu-id="1eaa0-141">Get-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1eaa0-141">Get-AzureRmDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="1eaa0-142">Set-AzureRmDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="1eaa0-142">Set-AzureRmDataFactoryV2Dataset</span></span>]()
