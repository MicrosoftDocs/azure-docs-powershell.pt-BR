---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118767"
---
# <span data-ttu-id="bc8b1-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="bc8b1-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="bc8b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc8b1-102">SYNOPSIS</span></span>
<span data-ttu-id="bc8b1-103">Calcula, resolve e valida as dependências das moveResources na coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="bc8b1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc8b1-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="bc8b1-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc8b1-105">DESCRIPTION</span></span>
<span data-ttu-id="bc8b1-106">Calcula, resolve e valida as dependências das moveResources na coleção de movimentações.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="bc8b1-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc8b1-107">EXAMPLES</span></span>

### <span data-ttu-id="bc8b1-108">Exemplo 1: calcula, resolve e valida as dependências dos recursos de movimentação na coleção Mover.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="bc8b1-109">Calcula, resolve e valida as dependências das moveresources na coleção Mover.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="bc8b1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc8b1-110">PARAMETERS</span></span>

### <span data-ttu-id="bc8b1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc8b1-111">-AsJob</span></span>
<span data-ttu-id="bc8b1-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="bc8b1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="bc8b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc8b1-113">-DefaultProfile</span></span>
<span data-ttu-id="bc8b1-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc8b1-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="bc8b1-115">-MoveCollectionName</span></span>
<span data-ttu-id="bc8b1-116">O nome mover coleção.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="bc8b1-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bc8b1-117">-NoWait</span></span>
<span data-ttu-id="bc8b1-118">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="bc8b1-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bc8b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc8b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="bc8b1-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="bc8b1-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc8b1-121">-SubscriptionId</span></span>
<span data-ttu-id="bc8b1-122">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="bc8b1-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="bc8b1-123">-Confirm</span></span>
<span data-ttu-id="bc8b1-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc8b1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc8b1-125">-WhatIf</span></span>
<span data-ttu-id="bc8b1-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc8b1-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc8b1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc8b1-128">CommonParameters</span></span>
<span data-ttu-id="bc8b1-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc8b1-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc8b1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc8b1-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="bc8b1-131">INPUTS</span></span>

## <span data-ttu-id="bc8b1-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="bc8b1-132">OUTPUTS</span></span>

### <span data-ttu-id="bc8b1-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="bc8b1-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="bc8b1-134">Notas</span><span class="sxs-lookup"><span data-stu-id="bc8b1-134">NOTES</span></span>

<span data-ttu-id="bc8b1-135">Aliases</span><span class="sxs-lookup"><span data-stu-id="bc8b1-135">ALIASES</span></span>

## <span data-ttu-id="bc8b1-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc8b1-136">RELATED LINKS</span></span>

