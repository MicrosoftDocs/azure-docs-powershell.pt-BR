---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283779"
---
# <span data-ttu-id="93eb6-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="93eb6-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="93eb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93eb6-102">SYNOPSIS</span></span>
<span data-ttu-id="93eb6-103">Obtém uma lista de dependências não resolvidas.</span><span class="sxs-lookup"><span data-stu-id="93eb6-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="93eb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93eb6-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="93eb6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93eb6-105">DESCRIPTION</span></span>
<span data-ttu-id="93eb6-106">Obtém uma lista de dependências não resolvidas.</span><span class="sxs-lookup"><span data-stu-id="93eb6-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="93eb6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93eb6-107">EXAMPLES</span></span>

### <span data-ttu-id="93eb6-108">Exemplo 1: obter a lista de recursos dependentes não resolvidos</span><span class="sxs-lookup"><span data-stu-id="93eb6-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="93eb6-109">Obter uma lista de recursos dependentes não resolvidos para uma coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="93eb6-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="93eb6-110">OS</span><span class="sxs-lookup"><span data-stu-id="93eb6-110">PARAMETERS</span></span>

### <span data-ttu-id="93eb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93eb6-111">-DefaultProfile</span></span>
<span data-ttu-id="93eb6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93eb6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93eb6-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="93eb6-113">-MoveCollectionName</span></span>
<span data-ttu-id="93eb6-114">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="93eb6-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="93eb6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93eb6-115">-ResourceGroupName</span></span>
<span data-ttu-id="93eb6-116">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93eb6-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="93eb6-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93eb6-117">-SubscriptionId</span></span>
<span data-ttu-id="93eb6-118">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="93eb6-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="93eb6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93eb6-119">CommonParameters</span></span>
<span data-ttu-id="93eb6-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93eb6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93eb6-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93eb6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93eb6-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93eb6-122">INPUTS</span></span>

## <span data-ttu-id="93eb6-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93eb6-123">OUTPUTS</span></span>

### <span data-ttu-id="93eb6-124">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="93eb6-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="93eb6-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93eb6-125">NOTES</span></span>

<span data-ttu-id="93eb6-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="93eb6-126">ALIASES</span></span>

## <span data-ttu-id="93eb6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93eb6-127">RELATED LINKS</span></span>

