---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 317614d67138b185dc58334d398bb368fc85911e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891638"
---
# <span data-ttu-id="4691a-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="4691a-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="4691a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4691a-102">SYNOPSIS</span></span>
<span data-ttu-id="4691a-103">Cria ou atualiza uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="4691a-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="4691a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4691a-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4691a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4691a-105">DESCRIPTION</span></span>
<span data-ttu-id="4691a-106">Cria ou atualiza uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="4691a-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="4691a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4691a-107">EXAMPLES</span></span>

### <span data-ttu-id="4691a-108">Exemplo 1: Criar uma nova coleção Move.</span><span class="sxs-lookup"><span data-stu-id="4691a-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name "PS-centralus-westcentralus-demoRMS"  -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceRegion "centralus" -TargetRegion "westcentralus" -Location "centraluseuap" -IdentityType "SystemAssigned"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"0200d92f-0000-3300-0000-6021e9ec0000" centraluseuap PS-centralus-westcentralus-demoRMs Microsoft.Migrate/moveCollections
```

<span data-ttu-id="4691a-109">Crie uma nova Coleção Move.</span><span class="sxs-lookup"><span data-stu-id="4691a-109">Create a new Move Collection.</span></span>

## <span data-ttu-id="4691a-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4691a-110">PARAMETERS</span></span>

### <span data-ttu-id="4691a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4691a-111">-DefaultProfile</span></span>
<span data-ttu-id="4691a-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4691a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4691a-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="4691a-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="4691a-114">Obtém ou define a ID principal.</span><span class="sxs-lookup"><span data-stu-id="4691a-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="4691a-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="4691a-115">-IdentityTenantId</span></span>
<span data-ttu-id="4691a-116">Obtém ou define a id do locatário.</span><span class="sxs-lookup"><span data-stu-id="4691a-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="4691a-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="4691a-117">-IdentityType</span></span>
<span data-ttu-id="4691a-118">O tipo de identidade usado para o serviço de movimentação de recursos.</span><span class="sxs-lookup"><span data-stu-id="4691a-118">The type of identity used for the resource mover service.</span></span>

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

### <span data-ttu-id="4691a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4691a-119">-Location</span></span>
<span data-ttu-id="4691a-120">A localização geográfica onde o recurso mora.</span><span class="sxs-lookup"><span data-stu-id="4691a-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="4691a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4691a-121">-Name</span></span>
<span data-ttu-id="4691a-122">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="4691a-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="4691a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4691a-123">-ResourceGroupName</span></span>
<span data-ttu-id="4691a-124">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="4691a-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="4691a-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="4691a-125">-SourceRegion</span></span>
<span data-ttu-id="4691a-126">Obtém ou define a região de origem.</span><span class="sxs-lookup"><span data-stu-id="4691a-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="4691a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4691a-127">-SubscriptionId</span></span>
<span data-ttu-id="4691a-128">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="4691a-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="4691a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="4691a-129">-Tag</span></span>
<span data-ttu-id="4691a-130">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="4691a-130">Resource tags.</span></span>

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

### <span data-ttu-id="4691a-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="4691a-131">-TargetRegion</span></span>
<span data-ttu-id="4691a-132">Obtém ou define a região de destino.</span><span class="sxs-lookup"><span data-stu-id="4691a-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="4691a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4691a-133">-Confirm</span></span>
<span data-ttu-id="4691a-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4691a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4691a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4691a-135">-WhatIf</span></span>
<span data-ttu-id="4691a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4691a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4691a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4691a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4691a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4691a-138">CommonParameters</span></span>
<span data-ttu-id="4691a-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4691a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4691a-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4691a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4691a-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4691a-141">INPUTS</span></span>

## <span data-ttu-id="4691a-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4691a-142">OUTPUTS</span></span>

### <span data-ttu-id="4691a-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="4691a-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="4691a-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="4691a-144">NOTES</span></span>

<span data-ttu-id="4691a-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4691a-145">ALIASES</span></span>

## <span data-ttu-id="4691a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4691a-146">RELATED LINKS</span></span>

