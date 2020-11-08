---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110992"
---
# <span data-ttu-id="bbc09-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="bbc09-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="bbc09-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bbc09-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc09-103">Exclui um recurso de movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="bbc09-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="bbc09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bbc09-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bbc09-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bbc09-105">DESCRIPTION</span></span>
<span data-ttu-id="bbc09-106">Exclui um recurso de movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="bbc09-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="bbc09-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bbc09-107">EXAMPLES</span></span>

### <span data-ttu-id="bbc09-108">Exemplo 1: remover o recurso da coleção mover</span><span class="sxs-lookup"><span data-stu-id="bbc09-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="bbc09-109">Remover o recurso da coleção mover na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="bbc09-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="bbc09-110">OS</span><span class="sxs-lookup"><span data-stu-id="bbc09-110">PARAMETERS</span></span>

### <span data-ttu-id="bbc09-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbc09-111">-AsJob</span></span>
<span data-ttu-id="bbc09-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="bbc09-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc09-113">-DefaultProfile</span></span>
<span data-ttu-id="bbc09-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bbc09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbc09-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="bbc09-115">-MoveCollectionName</span></span>
<span data-ttu-id="bbc09-116">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="bbc09-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="bbc09-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbc09-117">-Name</span></span>
<span data-ttu-id="bbc09-118">O nome do recurso de movimento.</span><span class="sxs-lookup"><span data-stu-id="bbc09-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc09-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="bbc09-119">-NoWait</span></span>
<span data-ttu-id="bbc09-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="bbc09-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc09-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbc09-121">-PassThru</span></span>
<span data-ttu-id="bbc09-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="bbc09-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc09-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc09-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbc09-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bbc09-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="bbc09-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbc09-125">-SubscriptionId</span></span>
<span data-ttu-id="bbc09-126">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="bbc09-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="bbc09-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bbc09-127">-Confirm</span></span>
<span data-ttu-id="bbc09-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbc09-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc09-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc09-129">-WhatIf</span></span>
<span data-ttu-id="bbc09-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bbc09-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc09-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bbc09-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc09-132">CommonParameters</span></span>
<span data-ttu-id="bbc09-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbc09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc09-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbc09-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc09-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bbc09-135">INPUTS</span></span>

## <span data-ttu-id="bbc09-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bbc09-136">OUTPUTS</span></span>

### <span data-ttu-id="bbc09-137">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="bbc09-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="bbc09-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bbc09-138">NOTES</span></span>

<span data-ttu-id="bbc09-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bbc09-139">ALIASES</span></span>

## <span data-ttu-id="bbc09-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bbc09-140">RELATED LINKS</span></span>

