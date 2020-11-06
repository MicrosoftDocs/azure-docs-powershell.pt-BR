---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602251"
---
# <span data-ttu-id="c966c-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="c966c-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="c966c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c966c-102">SYNOPSIS</span></span>
<span data-ttu-id="c966c-103">Obtém os detalhes de uma capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="c966c-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c966c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c966c-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="c966c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c966c-105">DESCRIPTION</span></span>
<span data-ttu-id="c966c-106">O cmdlet Get-AzureRmPowerBIEmbeddedCapacity Obtém os detalhes de uma capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="c966c-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="c966c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c966c-107">EXAMPLES</span></span>

### <span data-ttu-id="c966c-108">Exemplo 1: obter capacidades do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c966c-108">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="c966c-109">Esse comando obtém toda a capacidade inserida do Azure PowerBI no grupo de recursos chamado testRG</span><span class="sxs-lookup"><span data-stu-id="c966c-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="c966c-110">Exemplo 2: obter uma capacidade</span><span class="sxs-lookup"><span data-stu-id="c966c-110">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="c966c-111">Esse comando obtém a capacidade inserida do Azure PowerBI chamada testcapacity no grupo de recursos chamado testRG.</span><span class="sxs-lookup"><span data-stu-id="c966c-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="c966c-112">OS</span><span class="sxs-lookup"><span data-stu-id="c966c-112">PARAMETERS</span></span>

### <span data-ttu-id="c966c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c966c-113">-ResourceGroupName</span></span>
<span data-ttu-id="c966c-114">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="c966c-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c966c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c966c-115">-Name</span></span>
<span data-ttu-id="c966c-116">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="c966c-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="c966c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c966c-117">-ResourceId</span></span>
<span data-ttu-id="c966c-118">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="c966c-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c966c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c966c-119">CommonParameters</span></span>
<span data-ttu-id="c966c-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c966c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c966c-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c966c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c966c-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c966c-122">INPUTS</span></span>

### <span data-ttu-id="c966c-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c966c-123">None</span></span>
<span data-ttu-id="c966c-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c966c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c966c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c966c-125">OUTPUTS</span></span>

### <span data-ttu-id="c966c-126">List<Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity></span><span class="sxs-lookup"><span data-stu-id="c966c-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="c966c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c966c-127">NOTES</span></span>

## <span data-ttu-id="c966c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c966c-128">RELATED LINKS</span></span>

[<span data-ttu-id="c966c-129">New-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="c966c-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="c966c-130">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="c966c-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
