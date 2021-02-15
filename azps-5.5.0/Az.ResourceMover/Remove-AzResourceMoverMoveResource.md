---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112642"
---
# <span data-ttu-id="e147b-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="e147b-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="e147b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e147b-102">SYNOPSIS</span></span>
<span data-ttu-id="e147b-103">Exclui um Recurso de Movimentação da coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="e147b-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="e147b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e147b-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e147b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e147b-105">DESCRIPTION</span></span>
<span data-ttu-id="e147b-106">Exclui um Recurso de Movimentação da coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="e147b-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="e147b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e147b-107">EXAMPLES</span></span>

### <span data-ttu-id="e147b-108">Exemplo 1: Remover o recurso da coleção Mover</span><span class="sxs-lookup"><span data-stu-id="e147b-108">Example 1: Remove the resource from the Move collection</span></span>
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

<span data-ttu-id="e147b-109">Remova o recurso da coleção Mover dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e147b-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="e147b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e147b-110">PARAMETERS</span></span>

### <span data-ttu-id="e147b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e147b-111">-AsJob</span></span>
<span data-ttu-id="e147b-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e147b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e147b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e147b-113">-DefaultProfile</span></span>
<span data-ttu-id="e147b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e147b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e147b-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="e147b-115">-MoveCollectionName</span></span>
<span data-ttu-id="e147b-116">O nome mover coleção.</span><span class="sxs-lookup"><span data-stu-id="e147b-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="e147b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e147b-117">-Name</span></span>
<span data-ttu-id="e147b-118">O nome mover recurso.</span><span class="sxs-lookup"><span data-stu-id="e147b-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="e147b-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e147b-119">-NoWait</span></span>
<span data-ttu-id="e147b-120">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="e147b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e147b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e147b-121">-PassThru</span></span>
<span data-ttu-id="e147b-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e147b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e147b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e147b-123">-ResourceGroupName</span></span>
<span data-ttu-id="e147b-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e147b-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="e147b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e147b-125">-SubscriptionId</span></span>
<span data-ttu-id="e147b-126">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="e147b-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="e147b-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e147b-127">-Confirm</span></span>
<span data-ttu-id="e147b-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e147b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e147b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e147b-129">-WhatIf</span></span>
<span data-ttu-id="e147b-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e147b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e147b-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e147b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e147b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e147b-132">CommonParameters</span></span>
<span data-ttu-id="e147b-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e147b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e147b-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e147b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e147b-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="e147b-135">INPUTS</span></span>

## <span data-ttu-id="e147b-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="e147b-136">OUTPUTS</span></span>

### <span data-ttu-id="e147b-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="e147b-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="e147b-138">Notas</span><span class="sxs-lookup"><span data-stu-id="e147b-138">NOTES</span></span>

<span data-ttu-id="e147b-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="e147b-139">ALIASES</span></span>

## <span data-ttu-id="e147b-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e147b-140">RELATED LINKS</span></span>

