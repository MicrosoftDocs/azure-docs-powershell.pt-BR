---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: 2f0f4ea68de5071a860b55a464d339d65ff2882c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426750"
---
# <span data-ttu-id="d1b60-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="d1b60-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="d1b60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1b60-102">SYNOPSIS</span></span>
<span data-ttu-id="d1b60-103">Obtém informações sobre as fábricas de dados.</span><span class="sxs-lookup"><span data-stu-id="d1b60-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1b60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1b60-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1b60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1b60-105">DESCRIPTION</span></span>
<span data-ttu-id="d1b60-106">O cmdlet **Get-AzureRmDataFactory** Obtém informações sobre as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b60-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="d1b60-107">Se você especificar o nome de uma fábrica de dados, esse cmdlet obterá informações sobre essa fábrica de dados.</span><span class="sxs-lookup"><span data-stu-id="d1b60-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="d1b60-108">Se você não especificar um nome, esse cmdlet obterá informações sobre todas as fábricas de dados em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b60-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="d1b60-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1b60-109">EXAMPLES</span></span>

### <span data-ttu-id="d1b60-110">Exemplo 1: obter todas as fábricas de dados</span><span class="sxs-lookup"><span data-stu-id="d1b60-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="d1b60-111">Esse comando exibe informações sobre todas as fábricas de dados na assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b60-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="d1b60-112">Exemplo 2: obter uma fábrica de dados específica</span><span class="sxs-lookup"><span data-stu-id="d1b60-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="d1b60-113">Esse comando exibe informações sobre o realocador de dados chamado WikiADF na assinatura do grupo de recursos chamado ADF e, em seguida, armazena-o na variável $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="d1b60-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="d1b60-114">Especifique o parâmetro *DataFactory* em cmdlets subsequentes para usar o data Factory armazenado no $datafactory.</span><span class="sxs-lookup"><span data-stu-id="d1b60-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="d1b60-115">OS</span><span class="sxs-lookup"><span data-stu-id="d1b60-115">PARAMETERS</span></span>

### <span data-ttu-id="d1b60-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1b60-116">-DefaultProfile</span></span>
<span data-ttu-id="d1b60-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d1b60-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1b60-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1b60-118">-Name</span></span>
<span data-ttu-id="d1b60-119">Especifica o nome do alocador de dados sobre o qual obterá informações.</span><span class="sxs-lookup"><span data-stu-id="d1b60-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1b60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1b60-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1b60-121">Especifica o nome de um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1b60-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d1b60-122">Esse cmdlet obtém informações sobre as fábricas de dados que pertencem ao grupo especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d1b60-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d1b60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1b60-123">CommonParameters</span></span>
<span data-ttu-id="d1b60-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1b60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1b60-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1b60-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1b60-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1b60-126">INPUTS</span></span>

### <span data-ttu-id="d1b60-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d1b60-127">None</span></span>
<span data-ttu-id="d1b60-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d1b60-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1b60-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1b60-129">OUTPUTS</span></span>

### <span data-ttu-id="d1b60-130">System. Collections. Generic. List ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft. WindowsAzure. Commands. Utilities, Version = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d1b60-130">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="d1b60-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1b60-131">NOTES</span></span>
* <span data-ttu-id="d1b60-132">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, dados, fábricas</span><span class="sxs-lookup"><span data-stu-id="d1b60-132">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d1b60-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1b60-133">RELATED LINKS</span></span>

[<span data-ttu-id="d1b60-134">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="d1b60-134">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="d1b60-135">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="d1b60-135">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)

