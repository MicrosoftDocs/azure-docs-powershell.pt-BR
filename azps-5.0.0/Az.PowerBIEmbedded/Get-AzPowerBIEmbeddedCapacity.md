---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124437"
---
# <span data-ttu-id="db829-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="db829-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="db829-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db829-102">SYNOPSIS</span></span>
<span data-ttu-id="db829-103">Obtém os detalhes de uma capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="db829-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="db829-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db829-104">SYNTAX</span></span>

### <span data-ttu-id="db829-105">ByCapacityOrResourceGroupOrSubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="db829-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db829-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db829-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db829-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db829-107">DESCRIPTION</span></span>
<span data-ttu-id="db829-108">O cmdlet Get-AzPowerBIEmbeddedCapacity Obtém os detalhes de uma capacidade inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="db829-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="db829-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db829-109">EXAMPLES</span></span>

### <span data-ttu-id="db829-110">Exemplo 1: obter capacidades do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="db829-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="db829-111">Esse comando obtém toda a capacidade inserida do Azure PowerBI no grupo de recursos chamado testRG</span><span class="sxs-lookup"><span data-stu-id="db829-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="db829-112">Exemplo 2: obter uma capacidade</span><span class="sxs-lookup"><span data-stu-id="db829-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="db829-113">Esse comando obtém a capacidade inserida do Azure PowerBI chamada testcapacity no grupo de recursos chamado testRG.</span><span class="sxs-lookup"><span data-stu-id="db829-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="db829-114">OS</span><span class="sxs-lookup"><span data-stu-id="db829-114">PARAMETERS</span></span>

### <span data-ttu-id="db829-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db829-115">-DefaultProfile</span></span>
<span data-ttu-id="db829-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="db829-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db829-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="db829-117">-Name</span></span>
<span data-ttu-id="db829-118">Nome da capacidade inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="db829-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="db829-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db829-119">-ResourceGroupName</span></span>
<span data-ttu-id="db829-120">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="db829-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="db829-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db829-121">-ResourceId</span></span>
<span data-ttu-id="db829-122">ID do recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="db829-122">Azure resource ID</span></span>

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

### <span data-ttu-id="db829-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db829-123">CommonParameters</span></span>
<span data-ttu-id="db829-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db829-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db829-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db829-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db829-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db829-126">INPUTS</span></span>

### <span data-ttu-id="db829-127">System. String</span><span class="sxs-lookup"><span data-stu-id="db829-127">System.String</span></span>

## <span data-ttu-id="db829-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db829-128">OUTPUTS</span></span>

### <span data-ttu-id="db829-129">Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="db829-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="db829-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db829-130">NOTES</span></span>

## <span data-ttu-id="db829-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db829-131">RELATED LINKS</span></span>

[<span data-ttu-id="db829-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="db829-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="db829-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="db829-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
