---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 016701a762a87ec03912cda62dd5f436f1a45950
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116377"
---
# <span data-ttu-id="ab573-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="ab573-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="ab573-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab573-102">SYNOPSIS</span></span>
<span data-ttu-id="ab573-103">Obter uma lista de objetos de serviço de emparelhamento de um único objeto.</span><span class="sxs-lookup"><span data-stu-id="ab573-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="ab573-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab573-104">SYNTAX</span></span>

### <span data-ttu-id="ab573-105">ByResourceGroupName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ab573-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab573-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="ab573-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab573-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab573-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab573-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab573-108">DESCRIPTION</span></span>
<span data-ttu-id="ab573-109">Obtém serviços de emparelhamento para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="ab573-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="ab573-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab573-110">EXAMPLES</span></span>

### <span data-ttu-id="ab573-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab573-111">Example 1</span></span>
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

<span data-ttu-id="ab573-112">Obtém um serviço de emparelhamento para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ab573-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="ab573-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ab573-113">Example 2</span></span>
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

<span data-ttu-id="ab573-114">Obtém um serviço de emparelhamento para um grupo de recursos e nome</span><span class="sxs-lookup"><span data-stu-id="ab573-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="ab573-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ab573-115">Example 3</span></span>
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

<span data-ttu-id="ab573-116">Obtém um serviço de emparelhamento por ID do recurso</span><span class="sxs-lookup"><span data-stu-id="ab573-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="ab573-117">OS</span><span class="sxs-lookup"><span data-stu-id="ab573-117">PARAMETERS</span></span>

### <span data-ttu-id="ab573-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab573-118">-DefaultProfile</span></span>
<span data-ttu-id="ab573-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab573-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab573-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab573-120">-Name</span></span>
<span data-ttu-id="ab573-121">O nome exclusivo da PSPeering.</span><span class="sxs-lookup"><span data-stu-id="ab573-121">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ab573-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab573-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab573-123">Criar ou usar um nome de grupo de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="ab573-123">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ab573-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab573-124">-ResourceId</span></span>
<span data-ttu-id="ab573-125">O nome da cadeia de caracteres da ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="ab573-125">The resource id string name.</span></span>

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

### <span data-ttu-id="ab573-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab573-126">CommonParameters</span></span>
<span data-ttu-id="ab573-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab573-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab573-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab573-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab573-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab573-129">INPUTS</span></span>

### <span data-ttu-id="ab573-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ab573-130">System.String</span></span>

## <span data-ttu-id="ab573-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab573-131">OUTPUTS</span></span>

### <span data-ttu-id="ab573-132">Microsoft. Azure. PowerShell. cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="ab573-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="ab573-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab573-133">NOTES</span></span>

## <span data-ttu-id="ab573-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab573-134">RELATED LINKS</span></span>
