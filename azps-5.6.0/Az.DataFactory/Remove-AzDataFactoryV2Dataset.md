---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: a5c7ca7a651510d8b417beedc28cbd5ba26e6fe1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885728"
---
# <span data-ttu-id="09d60-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="09d60-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="09d60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d60-102">SYNOPSIS</span></span>
<span data-ttu-id="09d60-103">Remove um conjuntos de dados do Data Factory.</span><span class="sxs-lookup"><span data-stu-id="09d60-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="09d60-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="09d60-104">SYNTAX</span></span>

### <span data-ttu-id="09d60-105">ByFactoryName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09d60-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d60-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="09d60-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09d60-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="09d60-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09d60-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="09d60-108">DESCRIPTION</span></span>
<span data-ttu-id="09d60-109">O Remove-AzDataFactoryV2Dataset cmdlet remove um conjuntos de dados do Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="09d60-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="09d60-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09d60-110">EXAMPLES</span></span>

### <span data-ttu-id="09d60-111">Exemplo 1: Remover um conjuntos de dados</span><span class="sxs-lookup"><span data-stu-id="09d60-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="09d60-112">Este comando remove o conjuntos de dados chamado DAWikiAggregatedData do fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="09d60-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="09d60-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="09d60-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="09d60-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="09d60-114">PARAMETERS</span></span>

### <span data-ttu-id="09d60-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="09d60-115">-DataFactoryName</span></span>
<span data-ttu-id="09d60-116">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="09d60-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="09d60-117">Este cmdlet remove um conjuntos de dados do fábrica de dados especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="09d60-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="09d60-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d60-118">-DefaultProfile</span></span>
<span data-ttu-id="09d60-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="09d60-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09d60-120">-Force</span><span class="sxs-lookup"><span data-stu-id="09d60-120">-Force</span></span>
<span data-ttu-id="09d60-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="09d60-121">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d60-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09d60-122">-InputObject</span></span>
<span data-ttu-id="09d60-123">Especifica um objeto Dataset a ser removido.</span><span class="sxs-lookup"><span data-stu-id="09d60-123">Specifies a Dataset object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d60-124">-Name</span><span class="sxs-lookup"><span data-stu-id="09d60-124">-Name</span></span>
<span data-ttu-id="09d60-125">Especifica o nome do conjuntos de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="09d60-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d60-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09d60-126">-ResourceGroupName</span></span>
<span data-ttu-id="09d60-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="09d60-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="09d60-128">Este cmdlet remove um conjunto de dados do grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="09d60-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="09d60-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09d60-129">-ResourceId</span></span>
<span data-ttu-id="09d60-130">A ID de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="09d60-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="09d60-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09d60-131">-Confirm</span></span>
<span data-ttu-id="09d60-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09d60-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d60-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09d60-133">-WhatIf</span></span>
<span data-ttu-id="09d60-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09d60-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d60-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d60-135">CommonParameters</span></span>
<span data-ttu-id="09d60-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09d60-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d60-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09d60-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d60-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09d60-138">INPUTS</span></span>

### <span data-ttu-id="09d60-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="09d60-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="09d60-140">System.String</span><span class="sxs-lookup"><span data-stu-id="09d60-140">System.String</span></span>

## <span data-ttu-id="09d60-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="09d60-141">OUTPUTS</span></span>

### <span data-ttu-id="09d60-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="09d60-142">System.Void</span></span>

## <span data-ttu-id="09d60-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="09d60-143">NOTES</span></span>
<span data-ttu-id="09d60-144">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="09d60-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="09d60-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09d60-145">RELATED LINKS</span></span>

[<span data-ttu-id="09d60-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="09d60-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="09d60-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="09d60-147">Set-AzDataFactoryV2Dataset</span></span>]()
