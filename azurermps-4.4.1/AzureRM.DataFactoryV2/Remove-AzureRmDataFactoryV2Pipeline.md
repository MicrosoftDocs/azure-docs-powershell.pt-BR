---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2Pipeline.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: cc43b2982ff2269a1e0e72da065a806895cc798e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441575"
---
# <span data-ttu-id="4ce4d-101">Remove-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4ce4d-101">Remove-AzureRmDataFactoryV2Pipeline</span></span>

## <span data-ttu-id="4ce4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ce4d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ce4d-103">Remove um pipeline da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-103">Removes a pipeline from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ce4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ce4d-104">SYNTAX</span></span>

### <span data-ttu-id="4ce4d-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ce4d-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4ce4d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4ce4d-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-InputObject] <PSPipeline> [-Force] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4ce4d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce4d-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2Pipeline [-ResourceId] <String> [-Force] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4ce4d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ce4d-108">DESCRIPTION</span></span>
<span data-ttu-id="4ce4d-109">O cmdlet Remove-AzureRmDataFactoryV2Pipeline remove um pipeline do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-109">The Remove-AzureRmDataFactoryV2Pipeline cmdlet removes a pipeline from Azure Data Factory.</span></span>

## <span data-ttu-id="4ce4d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ce4d-110">EXAMPLES</span></span>

### <span data-ttu-id="4ce4d-111">Exemplo 1: remover um pipeline</span><span class="sxs-lookup"><span data-stu-id="4ce4d-111">Example 1: Remove a pipeline</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2Pipeline -ResourceGroupName "ADF" -Name "DPWikisample" -DataFactoryName "WikiADF"
          Confirm
          Are you sure you want to remove pipeline 'DPWikisample' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="4ce4d-112">Esse cmdlet Remove o pipeline chamado DPWikisample da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-112">This cmdlet removes the pipeline named DPWikisample from the data factory named WikiADF.</span></span>
<span data-ttu-id="4ce4d-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="4ce4d-114">OS</span><span class="sxs-lookup"><span data-stu-id="4ce4d-114">PARAMETERS</span></span>

### <span data-ttu-id="4ce4d-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ce4d-115">-Confirm</span></span>
<span data-ttu-id="4ce4d-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ce4d-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4ce4d-117">-DataFactoryName</span></span>
<span data-ttu-id="4ce4d-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4ce4d-119">Esse cmdlet Remove um pipeline da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-119">This cmdlet removes a pipeline from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ce4d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4ce4d-120">-Force</span></span>
<span data-ttu-id="4ce4d-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4ce4d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ce4d-122">-Name</span></span>
<span data-ttu-id="4ce4d-123">Especifica o nome do pipeline a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-123">Specifies the name of the pipeline to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: PipelineName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ce4d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ce4d-124">-InputObject</span></span>
<span data-ttu-id="4ce4d-125">Especifica um objeto de pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-125">Specifies a Pipeline object.</span></span>
<span data-ttu-id="4ce4d-126">Esse cmdlet Remove o pipeline que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-126">This cmdlet removes the pipeline that this parameter specifies.</span></span>

```yaml
Type: PSPipeline
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ce4d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ce4d-127">-ResourceGroupName</span></span>
<span data-ttu-id="4ce4d-128">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4ce4d-129">Esse cmdlet Remove um pipeline do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-129">This cmdlet removes a pipeline from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4ce4d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ce4d-130">-ResourceId</span></span>
<span data-ttu-id="4ce4d-131">A ID de recurso do Azure do pipeline a ser removida.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-131">The Azure resource ID of the pipeline to remove.</span></span>

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

### <span data-ttu-id="4ce4d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ce4d-132">-WhatIf</span></span>
<span data-ttu-id="4ce4d-133">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ce4d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="4ce4d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ce4d-134">INPUTS</span></span>

### <span data-ttu-id="4ce4d-135">Microsoft. Azure. Commands. DataFactoryV2. Models. PSPipeline</span><span class="sxs-lookup"><span data-stu-id="4ce4d-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>
<span data-ttu-id="4ce4d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4ce4d-136">System.String</span></span>


## <span data-ttu-id="4ce4d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ce4d-137">OUTPUTS</span></span>

### <span data-ttu-id="4ce4d-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="4ce4d-138">System.Object</span></span>

## <span data-ttu-id="4ce4d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ce4d-139">NOTES</span></span>
<span data-ttu-id="4ce4d-140">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="4ce4d-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4ce4d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ce4d-141">RELATED LINKS</span></span>
[<span data-ttu-id="4ce4d-142">Get-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4ce4d-142">Get-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4ce4d-143">Set-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4ce4d-143">Set-AzureRmDataFactoryV2Pipeline</span></span>]()

[<span data-ttu-id="4ce4d-144">Invoke-AzureRmDataFactoryV2Pipeline</span><span class="sxs-lookup"><span data-stu-id="4ce4d-144">Invoke-AzureRmDataFactoryV2Pipeline</span></span>]()

