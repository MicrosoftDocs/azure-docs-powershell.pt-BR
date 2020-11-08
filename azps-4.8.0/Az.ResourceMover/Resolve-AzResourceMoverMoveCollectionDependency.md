---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113347"
---
# <span data-ttu-id="d1d17-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="d1d17-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="d1d17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d1d17-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d17-103">Calcula, resolve e valida as dependências do moveResources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="d1d17-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="d1d17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d1d17-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d1d17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d1d17-105">DESCRIPTION</span></span>
<span data-ttu-id="d1d17-106">Calcula, resolve e valida as dependências do moveResources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="d1d17-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="d1d17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1d17-107">EXAMPLES</span></span>

### <span data-ttu-id="d1d17-108">Exemplo 1: calcula, resolve e valida as dependências do moveresources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="d1d17-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
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

<span data-ttu-id="d1d17-109">Calcula, resolve e valida as dependências do moveresources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="d1d17-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="d1d17-110">OS</span><span class="sxs-lookup"><span data-stu-id="d1d17-110">PARAMETERS</span></span>

### <span data-ttu-id="d1d17-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1d17-111">-AsJob</span></span>
<span data-ttu-id="d1d17-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d1d17-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d1d17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d17-113">-DefaultProfile</span></span>
<span data-ttu-id="d1d17-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1d17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d17-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d1d17-115">-MoveCollectionName</span></span>
<span data-ttu-id="d1d17-116">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="d1d17-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d1d17-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d1d17-117">-NoWait</span></span>
<span data-ttu-id="d1d17-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d1d17-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d1d17-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d17-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1d17-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d1d17-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d1d17-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1d17-121">-SubscriptionId</span></span>
<span data-ttu-id="d1d17-122">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d1d17-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="d1d17-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d1d17-123">-Confirm</span></span>
<span data-ttu-id="d1d17-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1d17-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d17-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d17-125">-WhatIf</span></span>
<span data-ttu-id="d1d17-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1d17-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d17-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1d17-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d17-128">CommonParameters</span></span>
<span data-ttu-id="d1d17-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d17-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1d17-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d17-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d1d17-131">INPUTS</span></span>

## <span data-ttu-id="d1d17-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d1d17-132">OUTPUTS</span></span>

### <span data-ttu-id="d1d17-133">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d1d17-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="d1d17-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d1d17-134">NOTES</span></span>

<span data-ttu-id="d1d17-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d1d17-135">ALIASES</span></span>

## <span data-ttu-id="d1d17-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1d17-136">RELATED LINKS</span></span>

