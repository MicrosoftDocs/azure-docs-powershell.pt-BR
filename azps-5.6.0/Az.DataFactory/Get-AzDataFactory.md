---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: ff47851c998cb88bec7106e8aba6d47d16069321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888531"
---
# <span data-ttu-id="eb597-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb597-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="eb597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb597-102">SYNOPSIS</span></span>
<span data-ttu-id="eb597-103">Obtém informações sobre Fábricas de Dados.</span><span class="sxs-lookup"><span data-stu-id="eb597-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="eb597-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="eb597-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb597-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="eb597-105">DESCRIPTION</span></span>
<span data-ttu-id="eb597-106">O cmdlet **Get-AzDataFactory** obtém informações sobre fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb597-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="eb597-107">Se você especificar o nome de um fábrica de dados, esse cmdlet obterá informações sobre esse fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="eb597-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="eb597-108">Se você não especificar um nome, este cmdlet obterá informações sobre todas as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb597-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="eb597-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb597-109">EXAMPLES</span></span>

### <span data-ttu-id="eb597-110">Exemplo 1: Obter todas as fábricas de dados</span><span class="sxs-lookup"><span data-stu-id="eb597-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="eb597-111">Este comando exibe informações sobre todas as fábricas de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb597-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="eb597-112">Exemplo 2: Obter um fábrica de dados específico</span><span class="sxs-lookup"><span data-stu-id="eb597-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="eb597-113">Este comando exibe informações sobre o fábrica de dados chamado WikiADF na assinatura do grupo de recursos chamado ADF e, em seguida, as armazena na variável $DataFactory de dados.</span><span class="sxs-lookup"><span data-stu-id="eb597-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="eb597-114">*Especifique o parâmetro DataFactory* em cmdlets subsequentes para usar o fábrica de dados armazenado em $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="eb597-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="eb597-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="eb597-115">PARAMETERS</span></span>

### <span data-ttu-id="eb597-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb597-116">-DefaultProfile</span></span>
<span data-ttu-id="eb597-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="eb597-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb597-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eb597-118">-Name</span></span>
<span data-ttu-id="eb597-119">Especifica o nome do fábrica de dados sobre o qual obter informações.</span><span class="sxs-lookup"><span data-stu-id="eb597-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb597-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb597-120">-ResourceGroupName</span></span>
<span data-ttu-id="eb597-121">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb597-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eb597-122">Este cmdlet obtém informações sobre fábricas de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="eb597-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb597-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb597-123">CommonParameters</span></span>
<span data-ttu-id="eb597-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb597-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb597-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb597-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb597-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eb597-126">INPUTS</span></span>

### <span data-ttu-id="eb597-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eb597-127">System.String</span></span>

## <span data-ttu-id="eb597-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="eb597-128">OUTPUTS</span></span>

### <span data-ttu-id="eb597-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb597-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="eb597-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="eb597-130">NOTES</span></span>
* <span data-ttu-id="eb597-131">Palavras-chave: azure, azurerm, arm, resource, management, manager, data, factories</span><span class="sxs-lookup"><span data-stu-id="eb597-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eb597-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb597-132">RELATED LINKS</span></span>

[<span data-ttu-id="eb597-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb597-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="eb597-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb597-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


