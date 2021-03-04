---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: 6812849fc8fe4aa8dab21f9bbcfc13891c45e0ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891633"
---
# <span data-ttu-id="af4f7-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="af4f7-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="af4f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="af4f7-103">Calcula, resolve e valida as dependências do moveResources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="af4f7-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="af4f7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="af4f7-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="af4f7-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="af4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="af4f7-106">Calcula, resolve e valida as dependências do moveResources na coleção move.</span><span class="sxs-lookup"><span data-stu-id="af4f7-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="af4f7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af4f7-107">EXAMPLES</span></span>

### <span data-ttu-id="af4f7-108">Exemplo 1: Calcular, resolver e validar as dependências dos Recursos de Movimentação na coleção Move.</span><span class="sxs-lookup"><span data-stu-id="af4f7-108">Example 1: Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 2/9/2021 2:05:04 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/c2ad006
                 6-6a69-45fe-aa70-193c240a9bc0
Message        : The resolve dependencies operation of one or more resources has failed. Check the move status of the resource for more details.
                     Possible Causes: The resolve dependencies operation of one ore more resources has failed.
                     Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : c2ad0066-6a69-45fe-aa70-193c240a9bc0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 2:05:00 AM
Status         : Succeeded
```

<span data-ttu-id="af4f7-109">Calcular, resolver e validar as dependências dos Recursos de Movimentação na coleção Move.</span><span class="sxs-lookup"><span data-stu-id="af4f7-109">Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>

## <span data-ttu-id="af4f7-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="af4f7-110">PARAMETERS</span></span>

### <span data-ttu-id="af4f7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af4f7-111">-AsJob</span></span>
<span data-ttu-id="af4f7-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="af4f7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="af4f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af4f7-113">-DefaultProfile</span></span>
<span data-ttu-id="af4f7-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="af4f7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af4f7-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="af4f7-115">-MoveCollectionName</span></span>
<span data-ttu-id="af4f7-116">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="af4f7-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="af4f7-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="af4f7-117">-NoWait</span></span>
<span data-ttu-id="af4f7-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="af4f7-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="af4f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af4f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="af4f7-120">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="af4f7-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="af4f7-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af4f7-121">-SubscriptionId</span></span>
<span data-ttu-id="af4f7-122">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="af4f7-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="af4f7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af4f7-123">-Confirm</span></span>
<span data-ttu-id="af4f7-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af4f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af4f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af4f7-125">-WhatIf</span></span>
<span data-ttu-id="af4f7-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af4f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af4f7-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af4f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af4f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af4f7-128">CommonParameters</span></span>
<span data-ttu-id="af4f7-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af4f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af4f7-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af4f7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af4f7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af4f7-131">INPUTS</span></span>

## <span data-ttu-id="af4f7-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="af4f7-132">OUTPUTS</span></span>

### <span data-ttu-id="af4f7-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="af4f7-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="af4f7-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="af4f7-134">NOTES</span></span>

<span data-ttu-id="af4f7-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="af4f7-135">ALIASES</span></span>

## <span data-ttu-id="af4f7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af4f7-136">RELATED LINKS</span></span>

