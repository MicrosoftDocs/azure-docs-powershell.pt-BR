---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 35810cf1d190f9ee8ada758fbd2e52fe41ca2455
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426736"
---
# <span data-ttu-id="de46b-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="de46b-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="de46b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de46b-102">SYNOPSIS</span></span>
<span data-ttu-id="de46b-103">Remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="de46b-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de46b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de46b-104">SYNTAX</span></span>

### <span data-ttu-id="de46b-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="de46b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de46b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="de46b-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de46b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de46b-107">DESCRIPTION</span></span>
<span data-ttu-id="de46b-108">O cmdlet **Remove-AzureRmDataFactoryDataset** remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="de46b-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="de46b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de46b-109">EXAMPLES</span></span>

### <span data-ttu-id="de46b-110">Exemplo 1: remover um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="de46b-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="de46b-111">Esse comando Remove o conjunto de dados chamado DAWikiAggregatedData da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="de46b-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="de46b-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="de46b-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="de46b-113">OS</span><span class="sxs-lookup"><span data-stu-id="de46b-113">PARAMETERS</span></span>

### <span data-ttu-id="de46b-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="de46b-114">-DataFactory</span></span>
<span data-ttu-id="de46b-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="de46b-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="de46b-116">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="de46b-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de46b-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="de46b-117">-DataFactoryName</span></span>
<span data-ttu-id="de46b-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="de46b-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="de46b-119">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="de46b-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="de46b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de46b-120">-DefaultProfile</span></span>
<span data-ttu-id="de46b-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="de46b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de46b-122">-Force</span><span class="sxs-lookup"><span data-stu-id="de46b-122">-Force</span></span>
<span data-ttu-id="de46b-123">Indica que esse cmdlet Remove um DataSet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="de46b-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="de46b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="de46b-124">-Name</span></span>
<span data-ttu-id="de46b-125">Especifica o nome do DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="de46b-125">Specifies the name of the dataset to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de46b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de46b-126">-ResourceGroupName</span></span>
<span data-ttu-id="de46b-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="de46b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="de46b-128">Esse cmdlet Remove um DataSet do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="de46b-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="de46b-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="de46b-129">-Confirm</span></span>
<span data-ttu-id="de46b-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de46b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de46b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de46b-131">-WhatIf</span></span>
<span data-ttu-id="de46b-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de46b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de46b-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de46b-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de46b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de46b-134">CommonParameters</span></span>
<span data-ttu-id="de46b-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de46b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de46b-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de46b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de46b-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de46b-137">INPUTS</span></span>

### <span data-ttu-id="de46b-138">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="de46b-138">None</span></span>
<span data-ttu-id="de46b-139">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="de46b-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de46b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de46b-140">OUTPUTS</span></span>

### <span data-ttu-id="de46b-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de46b-141">System.Boolean</span></span>

## <span data-ttu-id="de46b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de46b-142">NOTES</span></span>
* <span data-ttu-id="de46b-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="de46b-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="de46b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de46b-144">RELATED LINKS</span></span>

[<span data-ttu-id="de46b-145">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="de46b-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="de46b-146">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="de46b-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


