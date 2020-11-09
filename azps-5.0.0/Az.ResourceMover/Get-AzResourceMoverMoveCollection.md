---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 73bb67577a9160440c2e42e1e5b3259ad8435c5c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283791"
---
# <span data-ttu-id="fe1d8-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="fe1d8-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="fe1d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1d8-103">Obtém a coleção mover.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-103">Gets the move collection.</span></span>

## <span data-ttu-id="fe1d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe1d8-104">SYNTAX</span></span>

### <span data-ttu-id="fe1d8-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe1d8-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe1d8-106">Obter</span><span class="sxs-lookup"><span data-stu-id="fe1d8-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fe1d8-107">List1</span><span class="sxs-lookup"><span data-stu-id="fe1d8-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fe1d8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe1d8-108">DESCRIPTION</span></span>
<span data-ttu-id="fe1d8-109">Obtém a coleção mover.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-109">Gets the move collection.</span></span>

## <span data-ttu-id="fe1d8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe1d8-110">EXAMPLES</span></span>

### <span data-ttu-id="fe1d8-111">Exemplo 1: obter detalhes de todas as coleções de movimentação na assinatura</span><span class="sxs-lookup"><span data-stu-id="fe1d8-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId e80eb9fa-c996-4435-aa32-5af6f3d3077c

Location    Name                                            Type
--------    ----                                            ----
eastus2     mvcolle2e07001                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e34745                                  Microsoft.Migrate/moveCollections
eastus2     mvcolle2e56720                                  Microsoft.Migrate/moveCollections


```

<span data-ttu-id="fe1d8-112">Obter detalhes de todas as coleções de movimentação na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="fe1d8-113">Exemplo 2: obter detalhes da coleção move com um nome de conjunto de movimento especificado na assinatura</span><span class="sxs-lookup"><span data-stu-id="fe1d8-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM -Name PS-centralus-westcentralus-demoRM

Location    Name                              Type
--------    ----                              ----
eastus2     PS-centralus-westcentralus-demoRM Microsoft.Migrate/moveCollections

```

<span data-ttu-id="fe1d8-114">Obter detalhes da coleção move com um nome de conjunto de movimento especificado na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="fe1d8-115">Exemplo 3: obter detalhes da coleção move com um nome de grupo de recursos especificado na assinatura</span><span class="sxs-lookup"><span data-stu-id="fe1d8-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName RG-MoveCollection-demoRM 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
eastus2euap PS-centralus-westcentralus-demoRM2 Microsoft.Migrate/moveCollections


```

<span data-ttu-id="fe1d8-116">Obter detalhes da coleção move com um nome de grupo de recursos especificado na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="fe1d8-117">OS</span><span class="sxs-lookup"><span data-stu-id="fe1d8-117">PARAMETERS</span></span>

### <span data-ttu-id="fe1d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1d8-118">-DefaultProfile</span></span>
<span data-ttu-id="fe1d8-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe1d8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe1d8-120">-Name</span></span>
<span data-ttu-id="fe1d8-121">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-121">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1d8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1d8-122">-ResourceGroupName</span></span>
<span data-ttu-id="fe1d8-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-123">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1d8-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe1d8-124">-SubscriptionId</span></span>
<span data-ttu-id="fe1d8-125">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="fe1d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1d8-126">CommonParameters</span></span>
<span data-ttu-id="fe1d8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1d8-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe1d8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1d8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe1d8-129">INPUTS</span></span>

## <span data-ttu-id="fe1d8-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe1d8-130">OUTPUTS</span></span>

### <span data-ttu-id="fe1d8-131">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="fe1d8-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="fe1d8-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe1d8-132">NOTES</span></span>

<span data-ttu-id="fe1d8-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fe1d8-133">ALIASES</span></span>

## <span data-ttu-id="fe1d8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe1d8-134">RELATED LINKS</span></span>

