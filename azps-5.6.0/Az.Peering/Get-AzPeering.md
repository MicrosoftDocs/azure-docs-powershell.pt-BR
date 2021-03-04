---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: e2827d08d813608dbf3f6f40bc15603d5a5a0d99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890179"
---
# <span data-ttu-id="d0991-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="d0991-101">Get-AzPeering</span></span>

## <span data-ttu-id="d0991-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0991-102">SYNOPSIS</span></span>
<span data-ttu-id="d0991-103">Obtém os recursos de paração para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d0991-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="d0991-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d0991-104">SYNTAX</span></span>

### <span data-ttu-id="d0991-105">BySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d0991-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0991-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="d0991-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0991-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0991-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0991-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d0991-108">DESCRIPTION</span></span>
<span data-ttu-id="d0991-109">Obtém os Peerings de uma assinatura, grupo de recursos ou pelo nome.</span><span class="sxs-lookup"><span data-stu-id="d0991-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="d0991-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0991-110">EXAMPLES</span></span>

### <span data-ttu-id="d0991-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d0991-111">Example 1</span></span>
```powershell
PS C:> Get-AzPeering

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}

Name                 : ContosoSeattlePeering
Sku                  : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringSku
Kind                 : Direct
Connections          : {99999}
UseForPeeringService : False
PeerAsn              : Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSSubResource
PeeringLocation      : Seattle
ProvisioningState    : Succeeded
Location             : centralus
Id                   : /subscriptions/resourceGroups/testCarrier/providers/Microsoft.Peering/peerings/ContosoSeattlePeering
Type                 : Microsoft.Peering/peerings
Tags                 : {}
```

<span data-ttu-id="d0991-112">Obtém todos os recursos da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d0991-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="d0991-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d0991-113">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceGroupName test -Name myExchangePeering1

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="d0991-114">Obtém o peering do Exchange nomeado `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="d0991-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="d0991-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d0991-115">Example 2</span></span>
```powershell
PS C:> Get-AzPeering -ResourceId $resourceId

Name              : myExchangePeering1
Sku.Name          : Basic_Exchange_Free
Kind              : Exchange
Connections       : {99999}
PeerAsn.Id        : /subscriptions/providers/Microsoft.Peering/peerAsns/Contoso
PeeringLocation   : Seattle
ProvisioningState : Succeeded
Location          : centralus
Id                : /subscriptions/resourceGroups/test/providers/Microsoft.Peering/peerings/myExchangePeering1
Type              : Microsoft.Peering/peerings
Tags              : {}
```

<span data-ttu-id="d0991-116">Obtém o peering do Exchange `myExchangePeering1` nomeado com base na id do recurso.</span><span class="sxs-lookup"><span data-stu-id="d0991-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="d0991-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d0991-117">PARAMETERS</span></span>

### <span data-ttu-id="d0991-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0991-118">-DefaultProfile</span></span>
<span data-ttu-id="d0991-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0991-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0991-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="d0991-120">-Kind</span></span>
<span data-ttu-id="d0991-121">Mostra todo o recurso Peering por Tipo.</span><span class="sxs-lookup"><span data-stu-id="d0991-121">Shows all Peering resource by Kind.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0991-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d0991-122">-Name</span></span>
<span data-ttu-id="d0991-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="d0991-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0991-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0991-124">-ResourceGroupName</span></span>
<span data-ttu-id="d0991-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d0991-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0991-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0991-126">-ResourceId</span></span>
<span data-ttu-id="d0991-127">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="d0991-127">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0991-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0991-128">CommonParameters</span></span>
<span data-ttu-id="d0991-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0991-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0991-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0991-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0991-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0991-131">INPUTS</span></span>

### <span data-ttu-id="d0991-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d0991-132">System.String</span></span>

## <span data-ttu-id="d0991-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d0991-133">OUTPUTS</span></span>

### <span data-ttu-id="d0991-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="d0991-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="d0991-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="d0991-135">NOTES</span></span>

## <span data-ttu-id="d0991-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0991-136">RELATED LINKS</span></span>
