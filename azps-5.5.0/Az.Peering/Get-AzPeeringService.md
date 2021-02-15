---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118220"
---
# <span data-ttu-id="df814-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="df814-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="df814-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df814-102">SYNOPSIS</span></span>
<span data-ttu-id="df814-103">Obter uma lista de objetos de serviço de paração de um único objeto.</span><span class="sxs-lookup"><span data-stu-id="df814-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="df814-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df814-104">SYNTAX</span></span>

### <span data-ttu-id="df814-105">ByResourceGroupName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df814-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df814-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="df814-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df814-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="df814-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df814-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="df814-108">DESCRIPTION</span></span>
<span data-ttu-id="df814-109">Obtém serviços de peering para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="df814-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="df814-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df814-110">EXAMPLES</span></span>

### <span data-ttu-id="df814-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="df814-111">Example 1</span></span>
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

<span data-ttu-id="df814-112">Obtém um serviço de paridade para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="df814-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="df814-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="df814-113">Example 2</span></span>
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

<span data-ttu-id="df814-114">Obtém um serviço de paridade para um grupo de recursos e um nome</span><span class="sxs-lookup"><span data-stu-id="df814-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="df814-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="df814-115">Example 3</span></span>
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

<span data-ttu-id="df814-116">Obtém um serviço de peering por ID de recurso</span><span class="sxs-lookup"><span data-stu-id="df814-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="df814-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df814-117">PARAMETERS</span></span>

### <span data-ttu-id="df814-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df814-118">-DefaultProfile</span></span>
<span data-ttu-id="df814-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df814-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df814-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="df814-120">-Name</span></span>
<span data-ttu-id="df814-121">O nome exclusivo do PSPeering.</span><span class="sxs-lookup"><span data-stu-id="df814-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="df814-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df814-122">-ResourceGroupName</span></span>
<span data-ttu-id="df814-123">Crie ou use um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="df814-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="df814-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df814-124">-ResourceId</span></span>
<span data-ttu-id="df814-125">O nome da cadeia de caracteres de ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="df814-125">The resource id string name.</span></span>

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

### <span data-ttu-id="df814-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df814-126">CommonParameters</span></span>
<span data-ttu-id="df814-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df814-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df814-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="df814-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df814-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="df814-129">INPUTS</span></span>

### <span data-ttu-id="df814-130">System.String</span><span class="sxs-lookup"><span data-stu-id="df814-130">System.String</span></span>

## <span data-ttu-id="df814-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="df814-131">OUTPUTS</span></span>

### <span data-ttu-id="df814-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="df814-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="df814-133">Notas</span><span class="sxs-lookup"><span data-stu-id="df814-133">NOTES</span></span>

## <span data-ttu-id="df814-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df814-134">RELATED LINKS</span></span>
