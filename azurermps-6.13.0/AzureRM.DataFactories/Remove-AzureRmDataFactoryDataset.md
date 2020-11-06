---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 428BC568-A305-49AD-B6B8-B1BB5E9B822B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorydataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryDataset.md
ms.openlocfilehash: d4bb50dcc9e3f04d69131afbb7ac8b4f85e5070c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440069"
---
# <span data-ttu-id="ffbaa-101">Remove-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ffbaa-101">Remove-AzureRmDataFactoryDataset</span></span>

## <span data-ttu-id="ffbaa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="ffbaa-103">Remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-103">Removes a dataset from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffbaa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffbaa-104">SYNTAX</span></span>

### <span data-ttu-id="ffbaa-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffbaa-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ffbaa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ffbaa-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryDataset [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffbaa-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffbaa-107">DESCRIPTION</span></span>
<span data-ttu-id="ffbaa-108">O cmdlet **Remove-AzureRmDataFactoryDataset** remove um conjunto de dados do Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-108">The **Remove-AzureRmDataFactoryDataset** cmdlet removes a dataset from Azure Data Factory.</span></span>

## <span data-ttu-id="ffbaa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffbaa-109">EXAMPLES</span></span>

### <span data-ttu-id="ffbaa-110">Exemplo 1: remover um conjunto de um conjunto de um</span><span class="sxs-lookup"><span data-stu-id="ffbaa-110">Example 1: Remove a dataset</span></span>
```
PS C:\>Remove-AzureRmDataFactoryDataset -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "DAWikiAggregatedData"
Confirm
Are you sure you want to remove dataset 'DAWikiAggregatedData' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="ffbaa-111">Esse comando Remove o conjunto de dados chamado DAWikiAggregatedData da fábrica de dados chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-111">This command removes the dataset named DAWikiAggregatedData from the data factory named WikiADF.</span></span>
<span data-ttu-id="ffbaa-112">O comando retorna um valor de $True.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-112">The command returns a value of $True.</span></span>

## <span data-ttu-id="ffbaa-113">OS</span><span class="sxs-lookup"><span data-stu-id="ffbaa-113">PARAMETERS</span></span>

### <span data-ttu-id="ffbaa-114">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="ffbaa-114">-DataFactory</span></span>
<span data-ttu-id="ffbaa-115">Especifica um objeto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ffbaa-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="ffbaa-116">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-116">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ffbaa-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ffbaa-117">-DataFactoryName</span></span>
<span data-ttu-id="ffbaa-118">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="ffbaa-119">Esse cmdlet Remove um conjunto de dados da fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-119">This cmdlet removes a dataset from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="ffbaa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffbaa-120">-DefaultProfile</span></span>
<span data-ttu-id="ffbaa-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ffbaa-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffbaa-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ffbaa-122">-Force</span></span>
<span data-ttu-id="ffbaa-123">Indica que esse cmdlet Remove um DataSet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-123">Indicates that this cmdlet removes a dataset without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ffbaa-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffbaa-124">-Name</span></span>
<span data-ttu-id="ffbaa-125">Especifica o nome do DataSet a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-125">Specifies the name of the dataset to remove.</span></span>

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

### <span data-ttu-id="ffbaa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffbaa-126">-ResourceGroupName</span></span>
<span data-ttu-id="ffbaa-127">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ffbaa-128">Esse cmdlet Remove um DataSet do grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-128">This cmdlet removes a dataset from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ffbaa-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffbaa-129">-Confirm</span></span>
<span data-ttu-id="ffbaa-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffbaa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffbaa-131">-WhatIf</span></span>
<span data-ttu-id="ffbaa-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffbaa-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffbaa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffbaa-134">CommonParameters</span></span>
<span data-ttu-id="ffbaa-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffbaa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffbaa-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffbaa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffbaa-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffbaa-137">INPUTS</span></span>

### <span data-ttu-id="ffbaa-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ffbaa-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="ffbaa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ffbaa-139">System.String</span></span>

## <span data-ttu-id="ffbaa-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffbaa-140">OUTPUTS</span></span>

### <span data-ttu-id="ffbaa-141">System. void</span><span class="sxs-lookup"><span data-stu-id="ffbaa-141">System.Void</span></span>

## <span data-ttu-id="ffbaa-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffbaa-142">NOTES</span></span>
* <span data-ttu-id="ffbaa-143">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="ffbaa-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ffbaa-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffbaa-144">RELATED LINKS</span></span>

[<span data-ttu-id="ffbaa-145">Get-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ffbaa-145">Get-AzureRmDataFactoryDataset</span></span>](./Get-AzureRmDataFactoryDataset.md)

[<span data-ttu-id="ffbaa-146">New-AzureRmDataFactoryDataset</span><span class="sxs-lookup"><span data-stu-id="ffbaa-146">New-AzureRmDataFactoryDataset</span></span>](./New-AzureRmDataFactoryDataset.md)


