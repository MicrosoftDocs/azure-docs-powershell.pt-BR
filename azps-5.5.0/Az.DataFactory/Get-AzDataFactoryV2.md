---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117750"
---
# <span data-ttu-id="8ac00-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ac00-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="8ac00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ac00-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac00-103">Obtém informações sobre o Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8ac00-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="8ac00-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ac00-104">SYNTAX</span></span>

### <span data-ttu-id="8ac00-105">BySubscriptionId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8ac00-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ac00-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="8ac00-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ac00-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ac00-107">DESCRIPTION</span></span>
<span data-ttu-id="8ac00-108">O Get-AzDataFactoryV2 cmdlet obtém informações sobre a coleta de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac00-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="8ac00-109">Se você especificar o nome de uma fábrica de dados, esse cmdlet obterá informações sobre essa fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="8ac00-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="8ac00-110">Se você não especificar um nome, esse cmdlet obterá informações sobre todos os dados que estão disponíveis em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac00-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="8ac00-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ac00-111">EXAMPLES</span></span>

### <span data-ttu-id="8ac00-112">Exemplo 1: Obter todos os dados</span><span class="sxs-lookup"><span data-stu-id="8ac00-112">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="8ac00-113">Exibe informações sobre toda a coleta de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac00-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="8ac00-114">Exemplo 2: Obter uma fábrica de dados específica</span><span class="sxs-lookup"><span data-stu-id="8ac00-114">Example 2: Get a specific data factory</span></span>
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

<span data-ttu-id="8ac00-115">Esse comando exibe informações sobre a fábrica de dados chamada WikiADF na assinatura do grupo de recursos chamado ADF e, em seguida, as armazena na variável $DataFactory dados.</span><span class="sxs-lookup"><span data-stu-id="8ac00-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="8ac00-116">Especifique o parâmetro DataFactory em cmdlets subsequentes para usar o fábrica de dados armazenado em $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="8ac00-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="8ac00-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ac00-117">PARAMETERS</span></span>

### <span data-ttu-id="8ac00-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac00-118">-DefaultProfile</span></span>
<span data-ttu-id="8ac00-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8ac00-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac00-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ac00-120">-Name</span></span>
<span data-ttu-id="8ac00-121">Especifica o nome da fábrica de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="8ac00-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="8ac00-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac00-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ac00-123">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac00-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8ac00-124">Este cmdlet obtém informações sobre a coleta de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8ac00-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="8ac00-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac00-125">CommonParameters</span></span>
<span data-ttu-id="8ac00-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac00-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac00-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ac00-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac00-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="8ac00-128">INPUTS</span></span>

### <span data-ttu-id="8ac00-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8ac00-129">System.String</span></span>

## <span data-ttu-id="8ac00-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="8ac00-130">OUTPUTS</span></span>

### <span data-ttu-id="8ac00-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8ac00-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8ac00-132">Notas</span><span class="sxs-lookup"><span data-stu-id="8ac00-132">NOTES</span></span>
<span data-ttu-id="8ac00-133">Palavras-chave: azure, azurerm, arm, resource, management, manager, data,</span><span class="sxs-lookup"><span data-stu-id="8ac00-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8ac00-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ac00-134">RELATED LINKS</span></span>

[<span data-ttu-id="8ac00-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ac00-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="8ac00-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8ac00-136">Remove-AzDataFactoryV2</span></span>]()

