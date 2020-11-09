---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283774"
---
# <span data-ttu-id="27c10-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="27c10-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="27c10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27c10-102">SYNOPSIS</span></span>
<span data-ttu-id="27c10-103">Cria ou atualiza uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="27c10-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="27c10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27c10-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="27c10-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27c10-105">DESCRIPTION</span></span>
<span data-ttu-id="27c10-106">Cria ou atualiza uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="27c10-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="27c10-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27c10-107">EXAMPLES</span></span>

### <span data-ttu-id="27c10-108">Exemplo 1: criar uma nova coleção mover.</span><span class="sxs-lookup"><span data-stu-id="27c10-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="27c10-109">Criar uma nova coleção de movimento em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="27c10-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="27c10-110">OS</span><span class="sxs-lookup"><span data-stu-id="27c10-110">PARAMETERS</span></span>

### <span data-ttu-id="27c10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c10-111">-DefaultProfile</span></span>
<span data-ttu-id="27c10-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27c10-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27c10-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="27c10-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="27c10-114">Obtém ou define a ID da entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="27c10-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="27c10-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="27c10-115">-IdentityTenantId</span></span>
<span data-ttu-id="27c10-116">Obtém ou define a ID do locatário.</span><span class="sxs-lookup"><span data-stu-id="27c10-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="27c10-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="27c10-117">-IdentityType</span></span>
<span data-ttu-id="27c10-118">O tipo de identidade usado para o serviço de mudança de região.</span><span class="sxs-lookup"><span data-stu-id="27c10-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c10-119">-Local</span><span class="sxs-lookup"><span data-stu-id="27c10-119">-Location</span></span>
<span data-ttu-id="27c10-120">A localização geográfica onde reside o recurso.</span><span class="sxs-lookup"><span data-stu-id="27c10-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="27c10-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="27c10-121">-Name</span></span>
<span data-ttu-id="27c10-122">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="27c10-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c10-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c10-123">-ResourceGroupName</span></span>
<span data-ttu-id="27c10-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="27c10-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="27c10-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="27c10-125">-SourceRegion</span></span>
<span data-ttu-id="27c10-126">Obtém ou define a região de origem.</span><span class="sxs-lookup"><span data-stu-id="27c10-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="27c10-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27c10-127">-SubscriptionId</span></span>
<span data-ttu-id="27c10-128">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="27c10-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c10-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="27c10-129">-Tag</span></span>
<span data-ttu-id="27c10-130">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="27c10-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c10-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="27c10-131">-TargetRegion</span></span>
<span data-ttu-id="27c10-132">Obtém ou define a região de destino.</span><span class="sxs-lookup"><span data-stu-id="27c10-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="27c10-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27c10-133">-Confirm</span></span>
<span data-ttu-id="27c10-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27c10-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c10-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c10-135">-WhatIf</span></span>
<span data-ttu-id="27c10-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27c10-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27c10-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27c10-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27c10-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c10-138">CommonParameters</span></span>
<span data-ttu-id="27c10-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c10-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c10-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27c10-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c10-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27c10-141">INPUTS</span></span>

## <span data-ttu-id="27c10-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27c10-142">OUTPUTS</span></span>

### <span data-ttu-id="27c10-143">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="27c10-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="27c10-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27c10-144">NOTES</span></span>

<span data-ttu-id="27c10-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="27c10-145">ALIASES</span></span>

## <span data-ttu-id="27c10-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27c10-146">RELATED LINKS</span></span>

