---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
ms.openlocfilehash: c92f3bf2a124d5fc533fa86914cd218052e71e57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427576"
---
# <span data-ttu-id="b0504-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b0504-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="b0504-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0504-102">SYNOPSIS</span></span>
<span data-ttu-id="b0504-103">Obtém informações sobre a fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0504-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0504-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0504-104">SYNTAX</span></span>

### <span data-ttu-id="b0504-105">BySubscriptionId (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0504-105">BySubscriptionId (Default)</span></span>
```
Get-AzureRmDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0504-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="b0504-106">ByFactoryName</span></span>
```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0504-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0504-107">DESCRIPTION</span></span>
<span data-ttu-id="b0504-108">O cmdlet Get-AzureRmDataFactoryV2 Obtém informações sobre as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0504-108">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="b0504-109">Se você especificar o nome de uma fábrica de dados, esse cmdlet obterá informações sobre essa fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="b0504-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="b0504-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0504-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="b0504-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0504-111">EXAMPLES</span></span>

### <span data-ttu-id="b0504-112">Exemplo 1: obter todas as fábricas de dados</span><span class="sxs-lookup"><span data-stu-id="b0504-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="b0504-113">Exibe informações sobre todas as fábricas de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0504-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="b0504-114">Exemplo 2: obter uma fábrica de dados específica</span><span class="sxs-lookup"><span data-stu-id="b0504-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="b0504-115">Esse comando exibe informações sobre o realocador de dados chamado WikiADF na assinatura do grupo de recursos chamado ADF e, em seguida, armazena-o na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b0504-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="b0504-116">Especifique o parâmetro datafactory em cmdlets subsequentes para usar o data Factory armazenado no $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="b0504-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="b0504-117">OS</span><span class="sxs-lookup"><span data-stu-id="b0504-117">PARAMETERS</span></span>

### <span data-ttu-id="b0504-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0504-118">-DefaultProfile</span></span>
<span data-ttu-id="b0504-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b0504-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0504-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0504-120">-Name</span></span>
<span data-ttu-id="b0504-121">Especifica o nome do alocador de dados sobre o qual obterá informações.</span><span class="sxs-lookup"><span data-stu-id="b0504-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0504-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0504-122">-ResourceGroupName</span></span>
<span data-ttu-id="b0504-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="b0504-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b0504-124">Esse cmdlet obtém informações sobre as fábricas de dados que pertencem ao grupo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b0504-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="b0504-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0504-125">CommonParameters</span></span>
<span data-ttu-id="b0504-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0504-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0504-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0504-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0504-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0504-128">INPUTS</span></span>

### <span data-ttu-id="b0504-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b0504-129">System.String</span></span>

## <span data-ttu-id="b0504-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0504-130">OUTPUTS</span></span>

### <span data-ttu-id="b0504-131">System. Collections. Generic. List ' 1 [[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft. Azure. Commands. DataFactoryV2, Version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b0504-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b0504-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b0504-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b0504-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0504-133">NOTES</span></span>
<span data-ttu-id="b0504-134">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="b0504-134">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b0504-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0504-135">RELATED LINKS</span></span>

[<span data-ttu-id="b0504-136">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b0504-136">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="b0504-137">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b0504-137">Remove-AzureRmDataFactoryV2</span></span>]()

