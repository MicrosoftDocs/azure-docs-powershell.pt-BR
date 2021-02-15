---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeering.md
ms.openlocfilehash: 58ba131ab0bebc65d8fd5259d24b2846da229721
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114063"
---
# <span data-ttu-id="9dd1b-101">Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="9dd1b-101">Get-AzPeering</span></span>

## <span data-ttu-id="9dd1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9dd1b-102">SYNOPSIS</span></span>
<span data-ttu-id="9dd1b-103">Obtém os Recursos de Parimento de uma assinatura</span><span class="sxs-lookup"><span data-stu-id="9dd1b-103">Gets the Peering Resources for a subscription</span></span>

## <span data-ttu-id="9dd1b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9dd1b-104">SYNTAX</span></span>

### <span data-ttu-id="9dd1b-105">BySubscription (Default)</span><span class="sxs-lookup"><span data-stu-id="9dd1b-105">BySubscription (Default)</span></span>
```
Get-AzPeering [-Kind <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dd1b-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="9dd1b-106">ByResourceGroupAndName</span></span>
```
Get-AzPeering [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9dd1b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd1b-107">ByResourceId</span></span>
```
Get-AzPeering [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dd1b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9dd1b-108">DESCRIPTION</span></span>
<span data-ttu-id="9dd1b-109">Obtém os Pares de uma assinatura, grupo de recursos ou por nome.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-109">Gets the Peerings from a subscription, resource group, or by name.</span></span>

## <span data-ttu-id="9dd1b-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9dd1b-110">EXAMPLES</span></span>

### <span data-ttu-id="9dd1b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9dd1b-111">Example 1</span></span>
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

<span data-ttu-id="9dd1b-112">Obtém todos os recursos da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-112">Gets all the resources for the subscription.</span></span>

### <span data-ttu-id="9dd1b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9dd1b-113">Example 2</span></span>
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

<span data-ttu-id="9dd1b-114">Nomeia o peering do Exchange `myExchangePeering1`</span><span class="sxs-lookup"><span data-stu-id="9dd1b-114">Gets the Exchange peering named `myExchangePeering1`</span></span>

### <span data-ttu-id="9dd1b-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9dd1b-115">Example 2</span></span>
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

<span data-ttu-id="9dd1b-116">Recebe o peering do Exchange `myExchangePeering1` nomeado com base na ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-116">Gets the Exchange peering named `myExchangePeering1` based on the resource id.</span></span>

## <span data-ttu-id="9dd1b-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9dd1b-117">PARAMETERS</span></span>

### <span data-ttu-id="9dd1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dd1b-118">-DefaultProfile</span></span>
<span data-ttu-id="9dd1b-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dd1b-120">-Tipo</span><span class="sxs-lookup"><span data-stu-id="9dd1b-120">-Kind</span></span>
<span data-ttu-id="9dd1b-121">Mostra todos os recursos de Peering por Tipo.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-121">Shows all Peering resource by Kind.</span></span>

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

### <span data-ttu-id="9dd1b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9dd1b-122">-Name</span></span>
<span data-ttu-id="9dd1b-123">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="9dd1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dd1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9dd1b-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-125">The resource group name.</span></span>

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

### <span data-ttu-id="9dd1b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dd1b-126">-ResourceId</span></span>
<span data-ttu-id="9dd1b-127">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-127">The resource id string name.</span></span>

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

### <span data-ttu-id="9dd1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dd1b-128">CommonParameters</span></span>
<span data-ttu-id="9dd1b-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dd1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dd1b-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dd1b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dd1b-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="9dd1b-131">INPUTS</span></span>

### <span data-ttu-id="9dd1b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9dd1b-132">System.String</span></span>

## <span data-ttu-id="9dd1b-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="9dd1b-133">OUTPUTS</span></span>

### <span data-ttu-id="9dd1b-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="9dd1b-134">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

## <span data-ttu-id="9dd1b-135">Notas</span><span class="sxs-lookup"><span data-stu-id="9dd1b-135">NOTES</span></span>

## <span data-ttu-id="9dd1b-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9dd1b-136">RELATED LINKS</span></span>
