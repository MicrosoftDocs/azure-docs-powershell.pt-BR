---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryDataset.md
ms.openlocfilehash: 925362c3f576a9c243b42efc9af421a30c74d0ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257317"
---
# <span data-ttu-id="f2771-101">Remove-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f2771-101">Remove-AzDataFactoryDataset</span></span>

## <span data-ttu-id="f2771-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2771-102">SYNOPSIS</span></span>
<span data-ttu-id="f2771-103">Remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="f2771-103">Removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="f2771-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2771-104">SYNTAX</span></span>

### <span data-ttu-id="f2771-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2771-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2771-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f2771-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2771-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2771-107">DESCRIPTION</span></span>
<span data-ttu-id="f2771-108">O cmdlet **Remove-AzDataFactoryDataset** remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="f2771-108">The **Remove-AzDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="f2771-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2771-109">EXAMPLES</span></span>

### <span data-ttu-id="f2771-110">Exemplo 1: remover um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="f2771-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="f2771-111">Esse comando Remove o conjunto de dados chamado DAWikiAggregatedData da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f2771-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="f2771-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="f2771-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="f2771-113">OS</span><span class="sxs-lookup"><span data-stu-id="f2771-113">PARAMETERS</span></span>

### <span data-ttu-id="f2771-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="f2771-114">-DataFactory</span></span>
<span data-ttu-id="f2771-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="f2771-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f2771-116">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2771-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2771-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f2771-117">-DataFactoryName</span></span>
<span data-ttu-id="f2771-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="f2771-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f2771-119">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2771-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2771-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2771-120">-DefaultProfile</span></span>
<span data-ttu-id="f2771-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f2771-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2771-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f2771-122">-Force</span></span>
<span data-ttu-id="f2771-123">Indica que esse cmdlet Remove um DataSet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f2771-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f2771-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2771-124">-Name</span></span>
<span data-ttu-id="f2771-125">Especifica o nome do DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f2771-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="f2771-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2771-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2771-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2771-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f2771-128">Esse cmdlet Remove um DataSet do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="f2771-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f2771-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2771-129">-Confirm</span></span>
<span data-ttu-id="f2771-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2771-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2771-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2771-131">-WhatIf</span></span>
<span data-ttu-id="f2771-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2771-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2771-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2771-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2771-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2771-134">CommonParameters</span></span>
<span data-ttu-id="f2771-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2771-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2771-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2771-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2771-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2771-137">INPUTS</span></span>

### <span data-ttu-id="f2771-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f2771-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f2771-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f2771-139">System.String</span></span>

## <span data-ttu-id="f2771-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2771-140">OUTPUTS</span></span>

### <span data-ttu-id="f2771-141">System. void</span><span class="sxs-lookup"><span data-stu-id="f2771-141">System.Void</span></span>

## <span data-ttu-id="f2771-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2771-142">NOTES</span></span>
* <span data-ttu-id="f2771-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="f2771-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f2771-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2771-144">RELATED LINKS</span></span>

[<span data-ttu-id="f2771-145">Get-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f2771-145">Get-AzDataFactoryDataset</span></span>](./Get-AzDataFactoryDataset.md)

[<span data-ttu-id="f2771-146">New-AzDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="f2771-146">New-AzDataFactoryDataset</span></span>](./New-AzDataFactoryDataset.md)


