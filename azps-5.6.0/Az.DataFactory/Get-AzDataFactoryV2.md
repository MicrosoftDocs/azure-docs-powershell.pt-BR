---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: 05fad970f92d871dafdb7f712eb4227f7ed06eaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888299"
---
# <span data-ttu-id="205cb-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="205cb-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="205cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205cb-102">SYNOPSIS</span></span>
<span data-ttu-id="205cb-103">Obtém informações sobre a Fábrica de Dados.</span><span class="sxs-lookup"><span data-stu-id="205cb-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="205cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="205cb-104">SYNTAX</span></span>

### <span data-ttu-id="205cb-105">BySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="205cb-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="205cb-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="205cb-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="205cb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="205cb-107">DESCRIPTION</span></span>
<span data-ttu-id="205cb-108">O Get-AzDataFactoryV2 cmdlet obtém informações sobre fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="205cb-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="205cb-109">Se você especificar o nome de um fábrica de dados, esse cmdlet obterá informações sobre esse fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="205cb-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="205cb-110">Se você não especificar um nome, este cmdlet obterá informações sobre todas as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="205cb-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="205cb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="205cb-111">EXAMPLES</span></span>

### <span data-ttu-id="205cb-112">Exemplo 1: Obter todas as fábricas de dados</span><span class="sxs-lookup"><span data-stu-id="205cb-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="205cb-113">Exibe informações sobre todas as fábricas de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="205cb-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="205cb-114">Exemplo 2: Obter um fábrica de dados específico</span><span class="sxs-lookup"><span data-stu-id="205cb-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="205cb-115">Este comando exibe informações sobre o fábrica de dados chamado WikiADF na assinatura do grupo de recursos chamado ADF e, em seguida, as armazena na variável $DataFactory de dados.</span><span class="sxs-lookup"><span data-stu-id="205cb-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="205cb-116">Especifique o parâmetro DataFactory em cmdlets subsequentes para usar o fábrica de dados armazenado em $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="205cb-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="205cb-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="205cb-117">PARAMETERS</span></span>

### <span data-ttu-id="205cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205cb-118">-DefaultProfile</span></span>
<span data-ttu-id="205cb-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="205cb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="205cb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="205cb-120">-Name</span></span>
<span data-ttu-id="205cb-121">Especifica o nome do fábrica de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="205cb-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="205cb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205cb-122">-ResourceGroupName</span></span>
<span data-ttu-id="205cb-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="205cb-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="205cb-124">Este cmdlet obtém informações sobre fábricas de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="205cb-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="205cb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205cb-125">CommonParameters</span></span>
<span data-ttu-id="205cb-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="205cb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205cb-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="205cb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205cb-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="205cb-128">INPUTS</span></span>

### <span data-ttu-id="205cb-129">System.String</span><span class="sxs-lookup"><span data-stu-id="205cb-129">System.String</span></span>

## <span data-ttu-id="205cb-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="205cb-130">OUTPUTS</span></span>

### <span data-ttu-id="205cb-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="205cb-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="205cb-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="205cb-132">NOTES</span></span>
<span data-ttu-id="205cb-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="205cb-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="205cb-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="205cb-134">RELATED LINKS</span></span>

[<span data-ttu-id="205cb-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="205cb-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="205cb-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="205cb-136">Remove-AzDataFactoryV2</span></span>]()

