---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 12028dfd15ca27f7d57f2ffa55e473c835e0391f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771062"
---
# <span data-ttu-id="e3f86-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3f86-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="e3f86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3f86-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f86-103">Obtém informações sobre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="e3f86-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="e3f86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3f86-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3f86-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3f86-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f86-106">O cmdlet **Get-AzDataFactory** Obtém informações sobre as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f86-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="e3f86-107">Se você especificar o nome de uma fábrica de dados, esse cmdlet obterá informações sobre essa fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="e3f86-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="e3f86-108">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f86-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="e3f86-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3f86-109">EXAMPLES</span></span>

### <span data-ttu-id="e3f86-110">Exemplo 1: obter todas as fábricas de dados</span><span class="sxs-lookup"><span data-stu-id="e3f86-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="e3f86-111">Esse comando exibe informações sobre todas as fábricas de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f86-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="e3f86-112">Exemplo 2: obter uma fábrica de dados específica</span><span class="sxs-lookup"><span data-stu-id="e3f86-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="e3f86-113">Esse comando exibe informações sobre o realocador de dados chamado WikiADF na assinatura do grupo de recursos chamado ADF e, em seguida, armazena-o na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="e3f86-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="e3f86-114">Especifique o parâmetro *DataFactory* em cmdlets subsequentes para usar o data Factory armazenado no $datafactory.</span><span class="sxs-lookup"><span data-stu-id="e3f86-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="e3f86-115">OS</span><span class="sxs-lookup"><span data-stu-id="e3f86-115">PARAMETERS</span></span>

### <span data-ttu-id="e3f86-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f86-116">-DefaultProfile</span></span>
<span data-ttu-id="e3f86-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e3f86-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3f86-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3f86-118">-Name</span></span>
<span data-ttu-id="e3f86-119">Especifica o nome do alocador de dados sobre o qual obterá informações.</span><span class="sxs-lookup"><span data-stu-id="e3f86-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="e3f86-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f86-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3f86-121">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3f86-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="e3f86-122">Esse cmdlet obtém informações sobre as fábricas de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e3f86-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="e3f86-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f86-123">CommonParameters</span></span>
<span data-ttu-id="e3f86-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f86-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f86-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f86-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f86-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3f86-126">INPUTS</span></span>

### <span data-ttu-id="e3f86-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e3f86-127">System.String</span></span>

## <span data-ttu-id="e3f86-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3f86-128">OUTPUTS</span></span>

### <span data-ttu-id="e3f86-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3f86-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="e3f86-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3f86-130">NOTES</span></span>
* <span data-ttu-id="e3f86-131">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="e3f86-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="e3f86-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3f86-132">RELATED LINKS</span></span>

[<span data-ttu-id="e3f86-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3f86-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="e3f86-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="e3f86-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


