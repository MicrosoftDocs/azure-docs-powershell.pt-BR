---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
gitcommit: https://github.com/Azure/azure-powershell/blob/7fe7039e96038b4a91513dfda26026ad8e0a352b
ms.openlocfilehash: 8742babd73e28e28797db75952d7eb9e9c8dc4a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431766"
---
# <span data-ttu-id="c08d2-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c08d2-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="c08d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c08d2-102">SYNOPSIS</span></span>
<span data-ttu-id="c08d2-103">Obtém informações sobre a fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c08d2-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c08d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c08d2-104">SYNTAX</span></span>

```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
```

## <span data-ttu-id="c08d2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c08d2-105">DESCRIPTION</span></span>
<span data-ttu-id="c08d2-106">O cmdlet Get-AzureRmDataFactoryV2 Obtém informações sobre as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c08d2-106">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="c08d2-107">Se você especificar o nome de uma fábrica de dados, esse cmdlet obterá informações sobre essa fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="c08d2-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="c08d2-108">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c08d2-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>


## <span data-ttu-id="c08d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c08d2-109">EXAMPLES</span></span>

### <span data-ttu-id="c08d2-110">Exemplo 1: obter todas as fábricas de dados</span><span class="sxs-lookup"><span data-stu-id="c08d2-110">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded

```

<span data-ttu-id="c08d2-111">Exibe informações sobre todas as fábricas de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c08d2-111">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="c08d2-112">Exemplo 2: obter uma fábrica de dados específica</span><span class="sxs-lookup"><span data-stu-id="c08d2-112">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

```

<span data-ttu-id="c08d2-113">Esse comando exibe informações sobre o realocador de dados chamado WikiADF na assinatura do grupo de recursos chamado ADF e, em seguida, armazena-o na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="c08d2-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="c08d2-114">Especifique o parâmetro datafactory em cmdlets subsequentes para usar o data Factory armazenado no $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="c08d2-114">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="c08d2-115">OS</span><span class="sxs-lookup"><span data-stu-id="c08d2-115">PARAMETERS</span></span>

### <span data-ttu-id="c08d2-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c08d2-116">-Name</span></span>
<span data-ttu-id="c08d2-117">Especifica o nome do alocador de dados sobre o qual obterá informações.</span><span class="sxs-lookup"><span data-stu-id="c08d2-117">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c08d2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c08d2-118">-ResourceGroupName</span></span>
<span data-ttu-id="c08d2-119">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c08d2-119">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c08d2-120">Esse cmdlet obtém informações sobre as fábricas de dados que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c08d2-120">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="c08d2-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c08d2-121">INPUTS</span></span>

### <span data-ttu-id="c08d2-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c08d2-122">System.String</span></span>


## <span data-ttu-id="c08d2-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c08d2-123">OUTPUTS</span></span>

### <span data-ttu-id="c08d2-124">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c08d2-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="c08d2-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c08d2-125">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>


## <span data-ttu-id="c08d2-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c08d2-126">NOTES</span></span>
<span data-ttu-id="c08d2-127">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="c08d2-127">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c08d2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c08d2-128">RELATED LINKS</span></span>
[<span data-ttu-id="c08d2-129">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c08d2-129">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="c08d2-130">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c08d2-130">Remove-AzureRmDataFactoryV2</span></span>]()

