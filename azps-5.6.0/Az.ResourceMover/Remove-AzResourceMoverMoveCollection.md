---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891637"
---
# <span data-ttu-id="12beb-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="12beb-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="12beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12beb-102">SYNOPSIS</span></span>
<span data-ttu-id="12beb-103">Exclui uma coleção move.</span><span class="sxs-lookup"><span data-stu-id="12beb-103">Deletes a move collection.</span></span>

## <span data-ttu-id="12beb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12beb-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12beb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12beb-105">DESCRIPTION</span></span>
<span data-ttu-id="12beb-106">Exclui uma coleção move.</span><span class="sxs-lookup"><span data-stu-id="12beb-106">Deletes a move collection.</span></span>

## <span data-ttu-id="12beb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12beb-107">EXAMPLES</span></span>

### <span data-ttu-id="12beb-108">Exemplo 1: Remover a coleção Move.</span><span class="sxs-lookup"><span data-stu-id="12beb-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="12beb-109">Remova a coleção Move.</span><span class="sxs-lookup"><span data-stu-id="12beb-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="12beb-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12beb-110">PARAMETERS</span></span>

### <span data-ttu-id="12beb-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12beb-111">-AsJob</span></span>
<span data-ttu-id="12beb-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="12beb-112">Run the command as a job</span></span>

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

### <span data-ttu-id="12beb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12beb-113">-DefaultProfile</span></span>
<span data-ttu-id="12beb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12beb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12beb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="12beb-115">-Name</span></span>
<span data-ttu-id="12beb-116">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="12beb-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="12beb-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="12beb-117">-NoWait</span></span>
<span data-ttu-id="12beb-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="12beb-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12beb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12beb-119">-PassThru</span></span>
<span data-ttu-id="12beb-120">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="12beb-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="12beb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12beb-121">-ResourceGroupName</span></span>
<span data-ttu-id="12beb-122">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="12beb-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="12beb-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12beb-123">-SubscriptionId</span></span>
<span data-ttu-id="12beb-124">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="12beb-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="12beb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12beb-125">-Confirm</span></span>
<span data-ttu-id="12beb-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12beb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12beb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12beb-127">-WhatIf</span></span>
<span data-ttu-id="12beb-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12beb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12beb-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12beb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12beb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12beb-130">CommonParameters</span></span>
<span data-ttu-id="12beb-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12beb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12beb-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12beb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12beb-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12beb-133">INPUTS</span></span>

## <span data-ttu-id="12beb-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12beb-134">OUTPUTS</span></span>

### <span data-ttu-id="12beb-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="12beb-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="12beb-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="12beb-136">NOTES</span></span>

<span data-ttu-id="12beb-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="12beb-137">ALIASES</span></span>

## <span data-ttu-id="12beb-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12beb-138">RELATED LINKS</span></span>

