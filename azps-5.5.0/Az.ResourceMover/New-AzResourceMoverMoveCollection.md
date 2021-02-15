---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112645"
---
# <span data-ttu-id="48b2f-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="48b2f-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="48b2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="48b2f-103">Cria ou atualiza uma coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="48b2f-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="48b2f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48b2f-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="48b2f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="48b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="48b2f-106">Cria ou atualiza uma coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="48b2f-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="48b2f-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="48b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="48b2f-108">Exemplo 1: Criar uma nova coleção Mover.</span><span class="sxs-lookup"><span data-stu-id="48b2f-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="48b2f-109">Crie uma nova coleção Mover dentro de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="48b2f-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="48b2f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="48b2f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b2f-111">-DefaultProfile</span></span>
<span data-ttu-id="48b2f-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48b2f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48b2f-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="48b2f-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="48b2f-114">Obtém ou define a ID principal.</span><span class="sxs-lookup"><span data-stu-id="48b2f-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="48b2f-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="48b2f-115">-IdentityTenantId</span></span>
<span data-ttu-id="48b2f-116">Obtém ou define a ID do locatário.</span><span class="sxs-lookup"><span data-stu-id="48b2f-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="48b2f-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="48b2f-117">-IdentityType</span></span>
<span data-ttu-id="48b2f-118">O tipo de identidade usado para o serviço de movimentação de região.</span><span class="sxs-lookup"><span data-stu-id="48b2f-118">The type of identity used for the region move service.</span></span>

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

### <span data-ttu-id="48b2f-119">-Local</span><span class="sxs-lookup"><span data-stu-id="48b2f-119">-Location</span></span>
<span data-ttu-id="48b2f-120">A localização geográfica onde o recurso reside.</span><span class="sxs-lookup"><span data-stu-id="48b2f-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="48b2f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="48b2f-121">-Name</span></span>
<span data-ttu-id="48b2f-122">O nome mover coleção.</span><span class="sxs-lookup"><span data-stu-id="48b2f-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="48b2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="48b2f-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="48b2f-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="48b2f-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="48b2f-125">-SourceRegion</span></span>
<span data-ttu-id="48b2f-126">Obtém ou define a região de origem.</span><span class="sxs-lookup"><span data-stu-id="48b2f-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="48b2f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48b2f-127">-SubscriptionId</span></span>
<span data-ttu-id="48b2f-128">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="48b2f-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="48b2f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="48b2f-129">-Tag</span></span>
<span data-ttu-id="48b2f-130">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="48b2f-130">Resource tags.</span></span>

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

### <span data-ttu-id="48b2f-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="48b2f-131">-TargetRegion</span></span>
<span data-ttu-id="48b2f-132">Obtém ou define a região de destino.</span><span class="sxs-lookup"><span data-stu-id="48b2f-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="48b2f-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="48b2f-133">-Confirm</span></span>
<span data-ttu-id="48b2f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b2f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48b2f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b2f-135">-WhatIf</span></span>
<span data-ttu-id="48b2f-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="48b2f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48b2f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48b2f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48b2f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b2f-138">CommonParameters</span></span>
<span data-ttu-id="48b2f-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b2f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b2f-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48b2f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b2f-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="48b2f-141">INPUTS</span></span>

## <span data-ttu-id="48b2f-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="48b2f-142">OUTPUTS</span></span>

### <span data-ttu-id="48b2f-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="48b2f-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="48b2f-144">Notas</span><span class="sxs-lookup"><span data-stu-id="48b2f-144">NOTES</span></span>

<span data-ttu-id="48b2f-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="48b2f-145">ALIASES</span></span>

## <span data-ttu-id="48b2f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48b2f-146">RELATED LINKS</span></span>

