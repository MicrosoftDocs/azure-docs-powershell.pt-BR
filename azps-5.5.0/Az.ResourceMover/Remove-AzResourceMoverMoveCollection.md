---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112643"
---
# <span data-ttu-id="33c32-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="33c32-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="33c32-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33c32-102">SYNOPSIS</span></span>
<span data-ttu-id="33c32-103">Exclui uma coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="33c32-103">Deletes a move collection.</span></span>

## <span data-ttu-id="33c32-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33c32-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33c32-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="33c32-105">DESCRIPTION</span></span>
<span data-ttu-id="33c32-106">Exclui uma coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="33c32-106">Deletes a move collection.</span></span>

## <span data-ttu-id="33c32-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33c32-107">EXAMPLES</span></span>

### <span data-ttu-id="33c32-108">Exemplo 1: Remover o Conjunto de Movimentações da assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="33c32-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="33c32-109">Remova a coleção Mover da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="33c32-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="33c32-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33c32-110">PARAMETERS</span></span>

### <span data-ttu-id="33c32-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33c32-111">-AsJob</span></span>
<span data-ttu-id="33c32-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="33c32-112">Run the command as a job</span></span>

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

### <span data-ttu-id="33c32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c32-113">-DefaultProfile</span></span>
<span data-ttu-id="33c32-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33c32-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c32-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="33c32-115">-Name</span></span>
<span data-ttu-id="33c32-116">O nome mover coleção.</span><span class="sxs-lookup"><span data-stu-id="33c32-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="33c32-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33c32-117">-NoWait</span></span>
<span data-ttu-id="33c32-118">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="33c32-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33c32-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33c32-119">-PassThru</span></span>
<span data-ttu-id="33c32-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="33c32-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="33c32-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c32-121">-ResourceGroupName</span></span>
<span data-ttu-id="33c32-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33c32-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="33c32-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33c32-123">-SubscriptionId</span></span>
<span data-ttu-id="33c32-124">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="33c32-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="33c32-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="33c32-125">-Confirm</span></span>
<span data-ttu-id="33c32-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c32-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c32-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c32-127">-WhatIf</span></span>
<span data-ttu-id="33c32-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="33c32-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33c32-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33c32-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c32-130">CommonParameters</span></span>
<span data-ttu-id="33c32-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c32-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33c32-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c32-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="33c32-133">INPUTS</span></span>

## <span data-ttu-id="33c32-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="33c32-134">OUTPUTS</span></span>

### <span data-ttu-id="33c32-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="33c32-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="33c32-136">Notas</span><span class="sxs-lookup"><span data-stu-id="33c32-136">NOTES</span></span>

<span data-ttu-id="33c32-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="33c32-137">ALIASES</span></span>

## <span data-ttu-id="33c32-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33c32-138">RELATED LINKS</span></span>

