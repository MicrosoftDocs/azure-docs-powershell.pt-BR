---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283772"
---
# <span data-ttu-id="88fed-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="88fed-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="88fed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88fed-102">SYNOPSIS</span></span>
<span data-ttu-id="88fed-103">Exclui um recurso de movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="88fed-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="88fed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88fed-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="88fed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88fed-105">DESCRIPTION</span></span>
<span data-ttu-id="88fed-106">Exclui um recurso de movimentação da coleção move.</span><span class="sxs-lookup"><span data-stu-id="88fed-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="88fed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88fed-107">EXAMPLES</span></span>

### <span data-ttu-id="88fed-108">Exemplo 1: remover o recurso da coleção mover</span><span class="sxs-lookup"><span data-stu-id="88fed-108">Example 1: Remove the resource from the Move collection</span></span>
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

<span data-ttu-id="88fed-109">Remover o recurso da coleção mover na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="88fed-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="88fed-110">OS</span><span class="sxs-lookup"><span data-stu-id="88fed-110">PARAMETERS</span></span>

### <span data-ttu-id="88fed-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88fed-111">-AsJob</span></span>
<span data-ttu-id="88fed-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="88fed-112">Run the command as a job</span></span>

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

### <span data-ttu-id="88fed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88fed-113">-DefaultProfile</span></span>
<span data-ttu-id="88fed-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88fed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88fed-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="88fed-115">-MoveCollectionName</span></span>
<span data-ttu-id="88fed-116">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="88fed-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="88fed-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="88fed-117">-Name</span></span>
<span data-ttu-id="88fed-118">O nome do recurso de movimento.</span><span class="sxs-lookup"><span data-stu-id="88fed-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="88fed-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="88fed-119">-NoWait</span></span>
<span data-ttu-id="88fed-120">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="88fed-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="88fed-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88fed-121">-PassThru</span></span>
<span data-ttu-id="88fed-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="88fed-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="88fed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88fed-123">-ResourceGroupName</span></span>
<span data-ttu-id="88fed-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="88fed-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="88fed-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88fed-125">-SubscriptionId</span></span>
<span data-ttu-id="88fed-126">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="88fed-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="88fed-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88fed-127">-Confirm</span></span>
<span data-ttu-id="88fed-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88fed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88fed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88fed-129">-WhatIf</span></span>
<span data-ttu-id="88fed-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88fed-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88fed-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88fed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88fed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88fed-132">CommonParameters</span></span>
<span data-ttu-id="88fed-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88fed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88fed-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88fed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88fed-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88fed-135">INPUTS</span></span>

## <span data-ttu-id="88fed-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88fed-136">OUTPUTS</span></span>

### <span data-ttu-id="88fed-137">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="88fed-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="88fed-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88fed-138">NOTES</span></span>

<span data-ttu-id="88fed-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="88fed-139">ALIASES</span></span>

## <span data-ttu-id="88fed-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88fed-140">RELATED LINKS</span></span>

