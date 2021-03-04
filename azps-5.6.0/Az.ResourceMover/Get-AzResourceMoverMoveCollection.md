---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveCollection.md
ms.openlocfilehash: a10ac77515b225c5e5ef06335f9cee1e99ecd3b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891657"
---
# <span data-ttu-id="76175-101">Get-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="76175-101">Get-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="76175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76175-102">SYNOPSIS</span></span>
<span data-ttu-id="76175-103">Obtém a coleção move.</span><span class="sxs-lookup"><span data-stu-id="76175-103">Gets the move collection.</span></span>

## <span data-ttu-id="76175-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="76175-104">SYNTAX</span></span>

### <span data-ttu-id="76175-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="76175-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveCollection [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="76175-106">Obter</span><span class="sxs-lookup"><span data-stu-id="76175-106">Get</span></span>
```
Get-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="76175-107">List1</span><span class="sxs-lookup"><span data-stu-id="76175-107">List1</span></span>
```
Get-AzResourceMoverMoveCollection -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="76175-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="76175-108">DESCRIPTION</span></span>
<span data-ttu-id="76175-109">Obtém a coleção move.</span><span class="sxs-lookup"><span data-stu-id="76175-109">Gets the move collection.</span></span>

## <span data-ttu-id="76175-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76175-110">EXAMPLES</span></span>

### <span data-ttu-id="76175-111">Exemplo 1: Obter detalhes de todas as coleções Move na assinatura</span><span class="sxs-lookup"><span data-stu-id="76175-111">Example 1:  Get details of all the Move collections in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection  -SubscriptionId "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"270119e0-0000-0c00-0000-5f5c94940000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"39015ed4-0000-0c00-0000-5f5ce2760000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections
"1000b505-0000-0c00-0000-5f69db6e0000" centraluseuap MoveCollection-cus-eus-ccy         Microsoft.Migrate/moveCollections


```

<span data-ttu-id="76175-112">Obter detalhes de todas as coleções Move na assinatura.</span><span class="sxs-lookup"><span data-stu-id="76175-112">Get details of all the Move collections in the subscription.</span></span>

### <span data-ttu-id="76175-113">Exemplo 2: Obter detalhes da coleção Move com um nome de coleção de movimentação especificado na assinatura</span><span class="sxs-lookup"><span data-stu-id="76175-113">Example 2: Get details of the Move collection with a specified move collection name in the subscription</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -Name "PS-centralus-westcentralus-demoRMS"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="76175-114">Obter detalhes da coleção Move com um nome de coleção de movimentação especificado na assinatura.</span><span class="sxs-lookup"><span data-stu-id="76175-114">Get details of the Move collection with a specified move collection name in the subscription.</span></span>

### <span data-ttu-id="76175-115">Exemplo 3: Obter detalhes da coleção Move com um nome de grupo de recursos especificado na assinatura</span><span class="sxs-lookup"><span data-stu-id="76175-115">Example 3: Get details of the Move collection with a specified resource group name in the subscription</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" 

Location    Name                               Type
--------    ----                               ----
eastus2     PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
Etag                                   Location      Name                                Type                             
----                                   --------      ----                                ----                             
"22006609-0000-3300-0000-602169590000" centraluseuap PS-centralus-westcentralus-demoRMS  Microsoft.Migrate/moveCollections
"4e02b0a9-0000-0c00-0000-5fd101cc0000" centraluseuap PS-centralus-westcentralus-demo2RMS Microsoft.Migrate/moveCollections

```

<span data-ttu-id="76175-116">Obter detalhes da Coleção Move com um nome de grupo de recursos especificado na assinatura.</span><span class="sxs-lookup"><span data-stu-id="76175-116">Get details of the Move Collection with a specified resource group name in the subscription.</span></span>

## <span data-ttu-id="76175-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="76175-117">PARAMETERS</span></span>

### <span data-ttu-id="76175-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76175-118">-DefaultProfile</span></span>
<span data-ttu-id="76175-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76175-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76175-120">-Name</span><span class="sxs-lookup"><span data-stu-id="76175-120">-Name</span></span>
<span data-ttu-id="76175-121">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="76175-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="76175-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76175-122">-ResourceGroupName</span></span>
<span data-ttu-id="76175-123">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="76175-123">The Resource Group Name.</span></span>

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

### <span data-ttu-id="76175-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="76175-124">-SubscriptionId</span></span>
<span data-ttu-id="76175-125">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="76175-125">The Subscription ID.</span></span>

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

### <span data-ttu-id="76175-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76175-126">CommonParameters</span></span>
<span data-ttu-id="76175-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76175-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76175-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76175-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76175-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76175-129">INPUTS</span></span>

## <span data-ttu-id="76175-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="76175-130">OUTPUTS</span></span>

### <span data-ttu-id="76175-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="76175-131">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="76175-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="76175-132">NOTES</span></span>

<span data-ttu-id="76175-133">ALIASES</span><span class="sxs-lookup"><span data-stu-id="76175-133">ALIASES</span></span>

## <span data-ttu-id="76175-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76175-134">RELATED LINKS</span></span>

