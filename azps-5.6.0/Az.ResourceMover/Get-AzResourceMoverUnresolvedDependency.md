---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891651"
---
# <span data-ttu-id="e6510-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="e6510-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="e6510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6510-102">SYNOPSIS</span></span>
<span data-ttu-id="e6510-103">Obtém uma lista de dependências não resolvidas.</span><span class="sxs-lookup"><span data-stu-id="e6510-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="e6510-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e6510-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e6510-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e6510-105">DESCRIPTION</span></span>
<span data-ttu-id="e6510-106">Obtém uma lista de dependências não resolvidas.</span><span class="sxs-lookup"><span data-stu-id="e6510-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="e6510-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6510-107">EXAMPLES</span></span>

### <span data-ttu-id="e6510-108">Exemplo 1: Obter uma lista de recursos dependentes não resolvidos para uma coleção Move.</span><span class="sxs-lookup"><span data-stu-id="e6510-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="e6510-109">Obter uma lista de recursos dependentes não resolvidos para uma Coleção Move.</span><span class="sxs-lookup"><span data-stu-id="e6510-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="e6510-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e6510-110">PARAMETERS</span></span>

### <span data-ttu-id="e6510-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6510-111">-DefaultProfile</span></span>
<span data-ttu-id="e6510-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6510-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6510-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="e6510-113">-DependencyLevel</span></span>
<span data-ttu-id="e6510-114">Define o nível de dependência.</span><span class="sxs-lookup"><span data-stu-id="e6510-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6510-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="e6510-115">-Filter</span></span>
<span data-ttu-id="e6510-116">O filtro a ser aplicado na operação.</span><span class="sxs-lookup"><span data-stu-id="e6510-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="e6510-117">Por exemplo, $apply=filter(count eq 2).</span><span class="sxs-lookup"><span data-stu-id="e6510-117">For example, $apply=filter(count eq 2).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6510-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="e6510-118">-MoveCollectionName</span></span>
<span data-ttu-id="e6510-119">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="e6510-119">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6510-120">-Orderby</span><span class="sxs-lookup"><span data-stu-id="e6510-120">-Orderby</span></span>
<span data-ttu-id="e6510-121">Opção OData order by query.</span><span class="sxs-lookup"><span data-stu-id="e6510-121">OData order by query option.</span></span>
<span data-ttu-id="e6510-122">Por exemplo, você pode usar $orderby=Count desc.</span><span class="sxs-lookup"><span data-stu-id="e6510-122">For example, you can use $orderby=Count desc.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6510-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6510-123">-ResourceGroupName</span></span>
<span data-ttu-id="e6510-124">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="e6510-124">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6510-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6510-125">-SubscriptionId</span></span>
<span data-ttu-id="e6510-126">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="e6510-126">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6510-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6510-127">CommonParameters</span></span>
<span data-ttu-id="e6510-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6510-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6510-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6510-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6510-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6510-130">INPUTS</span></span>

## <span data-ttu-id="e6510-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e6510-131">OUTPUTS</span></span>

### <span data-ttu-id="e6510-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="e6510-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="e6510-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="e6510-133">NOTES</span></span>

<span data-ttu-id="e6510-134">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e6510-134">ALIASES</span></span>

## <span data-ttu-id="e6510-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6510-135">RELATED LINKS</span></span>

