---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: bcf26466c87a98d6a44486c5314c3541a7192a47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772863"
---
# <span data-ttu-id="2fab6-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="2fab6-101">Get-AzPeering</span></span>

## <span data-ttu-id="2fab6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fab6-102">SYNOPSIS</span></span>
<span data-ttu-id="2fab6-103">Obtém os recursos de emparelhamento para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="2fab6-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="2fab6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fab6-104">SYNTAX</span></span>

### <span data-ttu-id="2fab6-105">BySubscription (padrão)</span><span class="sxs-lookup"><span data-stu-id="2fab6-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fab6-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="2fab6-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fab6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fab6-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fab6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2fab6-108">DESCRIPTION</span></span>
<span data-ttu-id="2fab6-109">Obtém os pares de uma assinatura, grupo de recursos ou por nome.</span><span class="sxs-lookup"><span data-stu-id="2fab6-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="2fab6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fab6-110">EXAMPLES</span></span>

### <span data-ttu-id="2fab6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2fab6-111">Example 1</span></span>
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

<span data-ttu-id="2fab6-112">Obtém todos os recursos para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="2fab6-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="2fab6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2fab6-113">Example 2</span></span>
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

<span data-ttu-id="2fab6-114">Obtém o emparelhamento do Exchange chamado `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="2fab6-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="2fab6-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2fab6-115">Example 2</span></span>
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

<span data-ttu-id="2fab6-116">Obtém o emparelhamento do Exchange nomeado `myExchangePeering1` com base na ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2fab6-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="2fab6-117">OS</span><span class="sxs-lookup"><span data-stu-id="2fab6-117">PARAMETERS</span></span>

### <span data-ttu-id="2fab6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fab6-118">-DefaultProfile</span></span>
<span data-ttu-id="2fab6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fab6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fab6-120">-Kind</span><span class="sxs-lookup"><span data-stu-id="2fab6-120">-Kind</span></span>
<span data-ttu-id="2fab6-121">Mostra todos os recursos de emparelhamento por tipo.</span><span class="sxs-lookup"><span data-stu-id="2fab6-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="2fab6-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fab6-122">-Name</span></span>
<span data-ttu-id="2fab6-123">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="2fab6-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="2fab6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fab6-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fab6-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fab6-125">The resource group name.</span></span>

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

### <span data-ttu-id="2fab6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fab6-126">-ResourceId</span></span>
<span data-ttu-id="2fab6-127">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="2fab6-127">The resource id string name.</span></span>

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

### <span data-ttu-id="2fab6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fab6-128">CommonParameters</span></span>
<span data-ttu-id="2fab6-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fab6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fab6-130">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fab6-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fab6-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2fab6-131">INPUTS</span></span>

### <span data-ttu-id="2fab6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2fab6-132">System.String</span></span>

## <span data-ttu-id="2fab6-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2fab6-133">OUTPUTS</span></span>

### <span data-ttu-id="2fab6-134">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="2fab6-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="2fab6-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2fab6-135">NOTES</span></span>

## <span data-ttu-id="2fab6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fab6-136">RELATED LINKS</span></span>