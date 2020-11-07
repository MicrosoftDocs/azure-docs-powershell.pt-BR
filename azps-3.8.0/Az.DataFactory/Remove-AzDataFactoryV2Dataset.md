---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2dataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2Dataset.md
ms.openlocfilehash: 7db88488ccf60865654169233bb19025eae080d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940469"
---
# <span data-ttu-id="88df6-101">Remove-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="88df6-101">Remove-AzDataFactoryV2Dataset</span></span>

## <span data-ttu-id="88df6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88df6-102">SYNOPSIS</span></span>
<span data-ttu-id="88df6-103">Remove um conjunto de dados da fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="88df6-103">Removes a dataset from Data Factory.</span></span>

## <span data-ttu-id="88df6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88df6-104">SYNTAX</span></span>

### <span data-ttu-id="88df6-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="88df6-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2Dataset [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88df6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="88df6-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2Dataset [-InputObject] <PSDataset> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88df6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="88df6-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2Dataset [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88df6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88df6-108">DESCRIPTION</span></span>
<span data-ttu-id="88df6-109">O cmdlet Remove-AzDataFactoryV2Dataset remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="88df6-109">The Remove-AzDataFactoryV2Dataset cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="88df6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88df6-110">EXAMPLES</span></span>

### <span data-ttu-id="88df6-111">Exemplo 1: remover um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="88df6-111">Example 1: Remove a dataset</span></span>
```
PS C:\> Remove-AzDataFactoryV2Dataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
          Confirm
          Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
          True
```

<span data-ttu-id="88df6-112">Esse comando Remove o conjunto de dados chamado DAWikiAggregatedData da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="88df6-112">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="88df6-113">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="88df6-113">The command returns a value of $True.</span></span>

## <span data-ttu-id="88df6-114">OS</span><span class="sxs-lookup"><span data-stu-id="88df6-114">PARAMETERS</span></span>

### <span data-ttu-id="88df6-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="88df6-115">-DataFactoryName</span></span>
<span data-ttu-id="88df6-116">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="88df6-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="88df6-117">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="88df6-117">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="88df6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88df6-118">-DefaultProfile</span></span>
<span data-ttu-id="88df6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88df6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88df6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="88df6-120">-Force</span></span>
<span data-ttu-id="88df6-121">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="88df6-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="88df6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88df6-122">-InputObject</span></span>
<span data-ttu-id="88df6-123">Especifica um objeto DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="88df6-123">Specifies a Dataset object to remove.</span></span>

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

### <span data-ttu-id="88df6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="88df6-124">-Name</span></span>
<span data-ttu-id="88df6-125">Especifica o nome do DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="88df6-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="88df6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88df6-126">-ResourceGroupName</span></span>
<span data-ttu-id="88df6-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="88df6-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="88df6-128">Esse cmdlet Remove um DataSet do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="88df6-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="88df6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88df6-129">-ResourceId</span></span>
<span data-ttu-id="88df6-130">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="88df6-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="88df6-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88df6-131">-Confirm</span></span>
<span data-ttu-id="88df6-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88df6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88df6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88df6-133">-WhatIf</span></span>
<span data-ttu-id="88df6-134">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88df6-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="88df6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88df6-135">CommonParameters</span></span>
<span data-ttu-id="88df6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88df6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88df6-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88df6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88df6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88df6-138">INPUTS</span></span>

### <span data-ttu-id="88df6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span><span class="sxs-lookup"><span data-stu-id="88df6-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataset</span></span>

### <span data-ttu-id="88df6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="88df6-140">System.String</span></span>

## <span data-ttu-id="88df6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88df6-141">OUTPUTS</span></span>

### <span data-ttu-id="88df6-142">System. void</span><span class="sxs-lookup"><span data-stu-id="88df6-142">System.Void</span></span>

## <span data-ttu-id="88df6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88df6-143">NOTES</span></span>
<span data-ttu-id="88df6-144">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="88df6-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="88df6-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88df6-145">RELATED LINKS</span></span>

[<span data-ttu-id="88df6-146">Get-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="88df6-146">Get-AzDataFactoryV2Dataset</span></span>]()

[<span data-ttu-id="88df6-147">Set-AzDataFactoryV2Dataset</span><span class="sxs-lookup"><span data-stu-id="88df6-147">Set-AzDataFactoryV2Dataset</span></span>]()
