---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: 85e9e96db366adcb30494ac22e7d1b73bbff9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427977"
---
# <span data-ttu-id="64104-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="64104-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="64104-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64104-102">SYNOPSIS</span></span>
<span data-ttu-id="64104-103">Remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="64104-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64104-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64104-104">SYNTAX</span></span>

### <span data-ttu-id="64104-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="64104-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64104-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="64104-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64104-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64104-107">DESCRIPTION</span></span>
<span data-ttu-id="64104-108">O cmdlet **Remove-AzureRmDataFactoryDataset** remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="64104-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="64104-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64104-109">EXAMPLES</span></span>

### <span data-ttu-id="64104-110">Exemplo 1: remover um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="64104-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="64104-111">Esse comando Remove o conjunto de dados chamado DAWikiAggregatedData da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="64104-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="64104-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="64104-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="64104-113">OS</span><span class="sxs-lookup"><span data-stu-id="64104-113">PARAMETERS</span></span>

### <span data-ttu-id="64104-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="64104-114">-DataFactory</span></span>
<span data-ttu-id="64104-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="64104-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="64104-116">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="64104-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="64104-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="64104-117">-DataFactoryName</span></span>
<span data-ttu-id="64104-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="64104-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="64104-119">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="64104-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="64104-120">-Force</span><span class="sxs-lookup"><span data-stu-id="64104-120">-Force</span></span>
<span data-ttu-id="64104-121">Indica que esse cmdlet Remove um DataSet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="64104-121">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="64104-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="64104-122">-Name</span></span>
<span data-ttu-id="64104-123">Especifica o nome do DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="64104-123">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="64104-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64104-124">-ResourceGroupName</span></span>
<span data-ttu-id="64104-125">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="64104-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="64104-126">Esse cmdlet Remove um DataSet do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="64104-126">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="64104-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64104-127">-Confirm</span></span>
<span data-ttu-id="64104-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64104-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64104-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64104-129">-WhatIf</span></span>
<span data-ttu-id="64104-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64104-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64104-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64104-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64104-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64104-132">-DefaultProfile</span></span>
<span data-ttu-id="64104-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64104-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64104-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64104-134">CommonParameters</span></span>
<span data-ttu-id="64104-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64104-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64104-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64104-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64104-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64104-137">INPUTS</span></span>

## <span data-ttu-id="64104-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64104-138">OUTPUTS</span></span>

### <span data-ttu-id="64104-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="64104-139">System.Boolean</span></span>

## <span data-ttu-id="64104-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64104-140">NOTES</span></span>
* <span data-ttu-id="64104-141">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="64104-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="64104-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64104-142">RELATED LINKS</span></span>

[<span data-ttu-id="64104-143">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="64104-143">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="64104-144">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="64104-144">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)

