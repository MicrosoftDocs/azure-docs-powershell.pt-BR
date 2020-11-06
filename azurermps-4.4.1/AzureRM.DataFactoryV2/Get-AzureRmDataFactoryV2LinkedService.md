---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2LinkedService.md
gitcommit: https://github.com/Azure/azure-powershell/blob/c396953644d237789e0f4e1f726b553913186d34
ms.openlocfilehash: 7466ad5617fb78d48deb92ac2d623fc05ad90634
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441129"
---
# <span data-ttu-id="0f6d9-101">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6d9-101">Get-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="0f6d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6d9-103">Obtém informações sobre os serviços vinculados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-103">Gets information about linked services in Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f6d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f6d9-104">SYNTAX</span></span>

### <span data-ttu-id="0f6d9-105">ByFactoryName (padrão)</span><span class="sxs-lookup"><span data-stu-id="0f6d9-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="0f6d9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0f6d9-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryV2LinkedService [[-Name] <String>] [-DataFactory] <PSDataFactory>
```
## <span data-ttu-id="0f6d9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f6d9-107">DESCRIPTION</span></span>
<span data-ttu-id="0f6d9-108">O cmdlet Get-AzureRmDataFactoryV2LinkedService Obtém informações sobre serviços vinculados no Azure data Factory.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-108">The Get-AzureRmDataFactoryV2LinkedService cmdlet gets information about linked services in Azure Data Factory.</span></span>
<span data-ttu-id="0f6d9-109">Se você especificar o nome de um serviço vinculado, esse cmdlet obterá informações sobre esse serviço vinculado.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-109">If you specify the name of a linked service, this cmdlet gets information about that linked service.</span></span>
<span data-ttu-id="0f6d9-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os serviços vinculados na fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-110">If you do not specify a name, this cmdlet gets information about all the linked services in the data factory.</span></span>

## <span data-ttu-id="0f6d9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f6d9-111">EXAMPLES</span></span>

### <span data-ttu-id="0f6d9-112">Exemplo 1: obter informações sobre todos os serviços vinculados</span><span class="sxs-lookup"><span data-stu-id="0f6d9-112">Example 1: Get information about all linked services</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" | Format-List

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceHDIStorage
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService

    LinkedServiceName : LinkedServiceWikipediaClickEvents
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="0f6d9-113">Esse comando obtém informações sobre todos os serviços vinculados no data Factory chamado WikiADF e, em seguida, passa os serviços vinculados ao cmdlet Format-List usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-113">This command gets information about all linked services in the data factory named WikiADF, and then passes the linked services to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0f6d9-114">Esse cmdlet do Windows PowerShell formata os resultados.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-114">That Windows PowerShell cmdlet formats the results.</span></span>
<span data-ttu-id="0f6d9-115">Para obter mais informações, digite Get-Help formato-List.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-115">For more information, type Get-Help Format-List.</span></span>

<span data-ttu-id="0f6d9-116">Você pode usar qualquer uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="0f6d9-116">You can use either one of the following ways:</span></span>

### <span data-ttu-id="0f6d9-117">Exemplo 2: obter informações sobre um serviço vinculado específico</span><span class="sxs-lookup"><span data-stu-id="0f6d9-117">Example 2: Get information about a specific linked service</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceCuratedWikiData"

    LinkedServiceName : LinkedServiceCuratedWikiData
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.AzureStorageLinkedService
```

<span data-ttu-id="0f6d9-118">Esse comando obtém informações sobre o serviço vinculado chamado LinkedServiceCuratedWikiData no data Factory chamado WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-118">This command gets information about the linked service named LinkedServiceCuratedWikiData in the data factory named WikiADF.</span></span>

### <span data-ttu-id="0f6d9-119">Exemplo 3: obter informações sobre um serviço específico vinculado especificando o parâmetro datafactory</span><span class="sxs-lookup"><span data-stu-id="0f6d9-119">Example 3: Get information about a specific linked service by specifying the DataFactory parameter</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "ContosoFactory"PS C:\> Get-AzureRmDataFactoryV2LinkedService -DataFactory $DataFactory | Format-Table -Property LinkedServiceName, DataFactoryName, ResourceGroupName
```

<span data-ttu-id="0f6d9-120">O primeiro comando usa o cmdlet Get-AzureRmDataFactoryV2 para obter a fábrica de dados chamada ContosoFactory e, em seguida, armazena-o na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-120">The first command uses the Get-AzureRmDataFactoryV2 cmdlet to get the data factory named ContosoFactory, and then stores it in the $DataFactory variable.</span></span>

<span data-ttu-id="0f6d9-121">O segundo comando obtém informações sobre o serviço vinculado para o realocador de dados armazenado no $DataFactory e, em seguida, passa essas informações para o cmdlet Format-Table usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-121">The second command gets information about the linked service for the data factory stored in $DataFactory, and then passes that information to the Format-Table cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0f6d9-122">O cmdlet Format-Table formata a saída como um DataSet com as propriedades especificadas como colunas do DataSet.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-122">The Format-Table cmdlet formats the output as a dataset with the specified properties as dataset columns.</span></span>

## <span data-ttu-id="0f6d9-123">OS</span><span class="sxs-lookup"><span data-stu-id="0f6d9-123">PARAMETERS</span></span>

### <span data-ttu-id="0f6d9-124">-Datafactory</span><span class="sxs-lookup"><span data-stu-id="0f6d9-124">-DataFactory</span></span>
<span data-ttu-id="0f6d9-125">Especifica um objeto PSDataFactory.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-125">Specifies a PSDataFactory object.</span></span>
<span data-ttu-id="0f6d9-126">Esse cmdlet obtém serviços vinculados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-126">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d9-127">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0f6d9-127">-DataFactoryName</span></span>
<span data-ttu-id="0f6d9-128">Especifica o nome de uma fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-128">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0f6d9-129">Esse cmdlet obtém serviços vinculados que pertencem à fábrica de dados que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-129">This cmdlet gets linked services that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f6d9-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f6d9-130">-Name</span></span>
<span data-ttu-id="0f6d9-131">Especifica o nome do serviço vinculado sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-131">Specifies the name of the linked service about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6d9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f6d9-132">-ResourceGroupName</span></span>
<span data-ttu-id="0f6d9-133">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0f6d9-134">Esse cmdlet obtém serviços vinculados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0f6d9-134">This cmdlet gets linked services that belong to the group that this parameter specifies.</span></span>

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

## <span data-ttu-id="0f6d9-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f6d9-135">INPUTS</span></span>

### <span data-ttu-id="0f6d9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0f6d9-136">System.String</span></span>
<span data-ttu-id="0f6d9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0f6d9-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="0f6d9-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f6d9-138">OUTPUTS</span></span>

### <span data-ttu-id="0f6d9-139">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0f6d9-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0f6d9-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6d9-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>


## <span data-ttu-id="0f6d9-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f6d9-141">NOTES</span></span>
<span data-ttu-id="0f6d9-142">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="0f6d9-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0f6d9-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f6d9-143">RELATED LINKS</span></span>
[<span data-ttu-id="0f6d9-144">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6d9-144">Set-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="0f6d9-145">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="0f6d9-145">Remove-AzureRmDataFactoryV2LinkedService</span></span>]()
