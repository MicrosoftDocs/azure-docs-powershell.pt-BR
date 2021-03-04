---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890164"
---
# <span data-ttu-id="f1a1d-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="f1a1d-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="f1a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a1d-103">Obter uma lista de objetos de serviço de paração de um único objeto.</span><span class="sxs-lookup"><span data-stu-id="f1a1d-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="f1a1d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f1a1d-104">SYNTAX</span></span>

### <span data-ttu-id="f1a1d-105">ByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f1a1d-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1a1d-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="f1a1d-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1a1d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a1d-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1a1d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f1a1d-108">DESCRIPTION</span></span>
<span data-ttu-id="f1a1d-109">Obtém serviços de paring para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="f1a1d-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="f1a1d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1a1d-110">EXAMPLES</span></span>

### <span data-ttu-id="f1a1d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1a1d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="f1a1d-112">Obtém um serviço de peering para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f1a1d-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="f1a1d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f1a1d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="f1a1d-114">Obtém um serviço de peering para um grupo de recursos e nome</span><span class="sxs-lookup"><span data-stu-id="f1a1d-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="f1a1d-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f1a1d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="f1a1d-116">Obtém um serviço de paração por id de recurso</span><span class="sxs-lookup"><span data-stu-id="f1a1d-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="f1a1d-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f1a1d-117">PARAMETERS</span></span>

### <span data-ttu-id="f1a1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a1d-118">-DefaultProfile</span></span>
<span data-ttu-id="f1a1d-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1a1d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a1d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f1a1d-120">-Name</span></span>
<span data-ttu-id="f1a1d-121">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f1a1d-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1a1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1a1d-123">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="f1a1d-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="f1a1d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a1d-124">-ResourceId</span></span>
<span data-ttu-id="f1a1d-125">O nome da cadeia de caracteres de id de recurso.</span><span class="sxs-lookup"><span data-stu-id="f1a1d-125">The resource id string name.</span></span>

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

### <span data-ttu-id="f1a1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a1d-126">CommonParameters</span></span>
<span data-ttu-id="f1a1d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1a1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a1d-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1a1d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a1d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f1a1d-129">INPUTS</span></span>

### <span data-ttu-id="f1a1d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f1a1d-130">System.String</span></span>

## <span data-ttu-id="f1a1d-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f1a1d-131">OUTPUTS</span></span>

### <span data-ttu-id="f1a1d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="f1a1d-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="f1a1d-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="f1a1d-133">NOTES</span></span>

## <span data-ttu-id="f1a1d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1a1d-134">RELATED LINKS</span></span>
