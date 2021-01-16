---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263405"
---
# <span data-ttu-id="e2319-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="e2319-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="e2319-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2319-102">SYNOPSIS</span></span>
<span data-ttu-id="e2319-103">Exclui uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="e2319-103">Deletes a move collection.</span></span>

## <span data-ttu-id="e2319-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2319-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2319-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2319-105">DESCRIPTION</span></span>
<span data-ttu-id="e2319-106">Exclui uma coleção de movimentação.</span><span class="sxs-lookup"><span data-stu-id="e2319-106">Deletes a move collection.</span></span>

## <span data-ttu-id="e2319-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2319-107">EXAMPLES</span></span>

### <span data-ttu-id="e2319-108">Exemplo 1: remover a coleção mover da assinatura especificada</span><span class="sxs-lookup"><span data-stu-id="e2319-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
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

<span data-ttu-id="e2319-109">Remover a coleção de movimentação da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="e2319-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="e2319-110">OS</span><span class="sxs-lookup"><span data-stu-id="e2319-110">PARAMETERS</span></span>

### <span data-ttu-id="e2319-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2319-111">-AsJob</span></span>
<span data-ttu-id="e2319-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="e2319-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e2319-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2319-113">-DefaultProfile</span></span>
<span data-ttu-id="e2319-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2319-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2319-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2319-115">-Name</span></span>
<span data-ttu-id="e2319-116">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="e2319-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="e2319-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e2319-117">-NoWait</span></span>
<span data-ttu-id="e2319-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="e2319-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e2319-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2319-119">-PassThru</span></span>
<span data-ttu-id="e2319-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="e2319-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e2319-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2319-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2319-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e2319-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="e2319-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2319-123">-SubscriptionId</span></span>
<span data-ttu-id="e2319-124">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="e2319-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="e2319-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e2319-125">-Confirm</span></span>
<span data-ttu-id="e2319-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2319-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2319-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2319-127">-WhatIf</span></span>
<span data-ttu-id="e2319-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e2319-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2319-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e2319-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2319-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2319-130">CommonParameters</span></span>
<span data-ttu-id="e2319-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2319-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2319-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2319-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2319-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2319-133">INPUTS</span></span>

## <span data-ttu-id="e2319-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2319-134">OUTPUTS</span></span>

### <span data-ttu-id="e2319-135">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="e2319-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="e2319-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2319-136">NOTES</span></span>

<span data-ttu-id="e2319-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e2319-137">ALIASES</span></span>

## <span data-ttu-id="e2319-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2319-138">RELATED LINKS</span></span>

