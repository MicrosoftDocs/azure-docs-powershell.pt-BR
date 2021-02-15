---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: ce52463e9e983f3ad2483262775f5d4114370aa8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114568"
---
# <span data-ttu-id="276a0-101">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="276a0-101">Get-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="276a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="276a0-102">SYNOPSIS</span></span>
<span data-ttu-id="276a0-103">Obtém os detalhes de uma Capacidade Inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="276a0-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="276a0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="276a0-104">SYNTAX</span></span>

### <span data-ttu-id="276a0-105">ByCapacityOrResourceGroupOrSubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="276a0-105">ByCapacityOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzPowerBIEmbeddedCapacity [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="276a0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="276a0-106">ByResourceId</span></span>
```
Get-AzPowerBIEmbeddedCapacity -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="276a0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="276a0-107">DESCRIPTION</span></span>
<span data-ttu-id="276a0-108">O Get-AzPowerBIEmbeddedCapacity cmdlet obtém os detalhes de uma Capacidade Inserida do PowerBI.</span><span class="sxs-lookup"><span data-stu-id="276a0-108">The Get-AzPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="276a0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="276a0-109">EXAMPLES</span></span>

### <span data-ttu-id="276a0-110">Exemplo 1: Obter capacidades de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="276a0-110">Example 1: Get resource group capacities</span></span>
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

<span data-ttu-id="276a0-111">Esse comando obtém toda a Capacidade Inserida do Azure PowerBI no grupo de recursos chamado testRG</span><span class="sxs-lookup"><span data-stu-id="276a0-111">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="276a0-112">Exemplo 2: Obter uma capacidade</span><span class="sxs-lookup"><span data-stu-id="276a0-112">Example 2: Get a capacity</span></span>
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

<span data-ttu-id="276a0-113">Esse comando obtém a Capacidade Inserida do Azure PowerBI nomeada testcapacity no grupo de recursos chamado testRG.</span><span class="sxs-lookup"><span data-stu-id="276a0-113">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="276a0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="276a0-114">PARAMETERS</span></span>

### <span data-ttu-id="276a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="276a0-115">-DefaultProfile</span></span>
<span data-ttu-id="276a0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="276a0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="276a0-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="276a0-117">-Name</span></span>
<span data-ttu-id="276a0-118">Nome da Capacidade Inserida do PowerBI</span><span class="sxs-lookup"><span data-stu-id="276a0-118">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="276a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="276a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="276a0-120">Nome do grupo de recursos do Azure ao qual a capacidade pertence</span><span class="sxs-lookup"><span data-stu-id="276a0-120">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="276a0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="276a0-121">-ResourceId</span></span>
<span data-ttu-id="276a0-122">ID de recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="276a0-122">Azure resource ID</span></span>

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

### <span data-ttu-id="276a0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276a0-123">CommonParameters</span></span>
<span data-ttu-id="276a0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="276a0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276a0-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276a0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276a0-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="276a0-126">INPUTS</span></span>

### <span data-ttu-id="276a0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="276a0-127">System.String</span></span>

## <span data-ttu-id="276a0-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="276a0-128">OUTPUTS</span></span>

### <span data-ttu-id="276a0-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="276a0-129">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="276a0-130">Notas</span><span class="sxs-lookup"><span data-stu-id="276a0-130">NOTES</span></span>

## <span data-ttu-id="276a0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="276a0-131">RELATED LINKS</span></span>

[<span data-ttu-id="276a0-132">New-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="276a0-132">New-AzPowerBIEmbeddedCapacity </span></span>](./New-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="276a0-133">Remove-AzPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="276a0-133">Remove-AzPowerBIEmbeddedCapacity </span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
