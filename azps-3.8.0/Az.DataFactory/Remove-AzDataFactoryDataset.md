---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778322"
---
# <span data-ttu-id="d7f44-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d7f44-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="d7f44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7f44-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f44-103">Remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7f44-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="d7f44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7f44-104">SYNTAX</span></span>

### <span data-ttu-id="d7f44-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d7f44-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7f44-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d7f44-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7f44-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7f44-107">DESCRIPTION</span></span>
<span data-ttu-id="d7f44-108">O cmdlet **Remove-AzDataFactoryDataset** remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="d7f44-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="d7f44-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7f44-109">EXAMPLES</span></span>

### <span data-ttu-id="d7f44-110">Exemplo 1: remover um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="d7f44-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="d7f44-111">Esse comando Remove o conjunto de dados chamado DAWikiAggregatedData da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d7f44-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="d7f44-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="d7f44-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="d7f44-113">OS</span><span class="sxs-lookup"><span data-stu-id="d7f44-113">PARAMETERS</span></span>

### <span data-ttu-id="d7f44-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="d7f44-114">-DataFactory</span></span>
<span data-ttu-id="d7f44-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="d7f44-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d7f44-116">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d7f44-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f44-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="d7f44-117">-DataFactoryName</span></span>
<span data-ttu-id="d7f44-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d7f44-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d7f44-119">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d7f44-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7f44-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f44-120">-DefaultProfile</span></span>
<span data-ttu-id="d7f44-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d7f44-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7f44-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d7f44-122">-Force</span></span>
<span data-ttu-id="d7f44-123">Indica que esse cmdlet Remove um DataSet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="d7f44-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d7f44-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7f44-124">-Name</span></span>
<span data-ttu-id="d7f44-125">Especifica o nome do DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d7f44-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7f44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7f44-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7f44-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f44-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d7f44-128">Esse cmdlet Remove um DataSet do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d7f44-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d7f44-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7f44-129">-Confirm</span></span>
<span data-ttu-id="d7f44-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7f44-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f44-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7f44-131">-WhatIf</span></span>
<span data-ttu-id="d7f44-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7f44-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7f44-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7f44-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7f44-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f44-134">CommonParameters</span></span>
<span data-ttu-id="d7f44-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f44-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f44-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f44-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f44-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7f44-137">INPUTS</span></span>

### <span data-ttu-id="d7f44-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d7f44-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d7f44-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d7f44-139">System.String</span></span>

## <span data-ttu-id="d7f44-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7f44-140">OUTPUTS</span></span>

### <span data-ttu-id="d7f44-141">System. void</span><span class="sxs-lookup"><span data-stu-id="d7f44-141">System.Void</span></span>

## <span data-ttu-id="d7f44-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7f44-142">NOTES</span></span>
* <span data-ttu-id="d7f44-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="d7f44-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d7f44-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7f44-144">RELATED LINKS</span></span>

[<span data-ttu-id="d7f44-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d7f44-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="d7f44-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="d7f44-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


