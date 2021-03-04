---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 17d7547daaffdfafc117a250d20c0af1f069b70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885570"
---
# <span data-ttu-id="12269-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="12269-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="12269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12269-102">SYNOPSIS</span></span>
<span data-ttu-id="12269-103">Obtém os detalhes de uma Capacidade Incorporada do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="12269-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="12269-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12269-104">SYNTAX</span></span>

### <span data-ttu-id="12269-105">ByCapacityOrResourceGroupOrSubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12269-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="12269-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12269-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12269-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12269-107">DESCRIPTION</span></span>
<span data-ttu-id="12269-108">O Get-AzPowerBIEmbeddedCapacity cmdlet obtém os detalhes de uma Capacidade Incorporada do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="12269-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="12269-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12269-109">EXAMPLES</span></span>

### <span data-ttu-id="12269-110">Exemplo 1: Obter capacidades de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="12269-110">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
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

<span data-ttu-id="12269-111">Este comando obtém toda a Capacidade Incorporada do Azure PowerBI no grupo de recursos chamado testRG</span><span class="sxs-lookup"><span data-stu-id="12269-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="12269-112">Exemplo 2: obter uma capacidade</span><span class="sxs-lookup"><span data-stu-id="12269-112">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
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

<span data-ttu-id="12269-113">Este comando obtém a Capacidade Incorporada do Azure PowerBI denominada testcapacity no grupo de recursos chamado testRG.</span><span class="sxs-lookup"><span data-stu-id="12269-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="12269-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12269-114">PARAMETERS</span></span>

### <span data-ttu-id="12269-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12269-115">-DefaultProfile</span></span>
<span data-ttu-id="12269-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12269-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12269-117">-Name</span><span class="sxs-lookup"><span data-stu-id="12269-117">-Name</span></span>
<span data-ttu-id="12269-118">Nome da Capacidade Incorporada do PowerBI</span><span class="sxs-lookup"><span data-stu-id="12269-118">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12269-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12269-119">-ResourceGroupName</span></span>
<span data-ttu-id="12269-120">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="12269-120">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByCapacityOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12269-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12269-121">-ResourceId</span></span>
<span data-ttu-id="12269-122">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="12269-122">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12269-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12269-123">CommonParameters</span></span>
<span data-ttu-id="12269-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12269-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12269-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12269-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12269-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12269-126">INPUTS</span></span>

### <span data-ttu-id="12269-127">System.String</span><span class="sxs-lookup"><span data-stu-id="12269-127">System.String</span></span>

## <span data-ttu-id="12269-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12269-128">OUTPUTS</span></span>

### <span data-ttu-id="12269-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="12269-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="12269-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="12269-130">NOTES</span></span>

## <span data-ttu-id="12269-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12269-131">RELATED LINKS</span></span>

[<span data-ttu-id="12269-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="12269-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="12269-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="12269-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
