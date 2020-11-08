---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111438"
---
# <span data-ttu-id="3db70-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="3db70-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="3db70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3db70-102">SYNOPSIS</span></span>
<span data-ttu-id="3db70-103">Confirma o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="3db70-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3db70-104">A operação de confirmação é disparada no moveResources em movestate ' CommitPending ' ou ' CommitFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para Committed.</span><span class="sxs-lookup"><span data-stu-id="3db70-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3db70-105">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="3db70-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3db70-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3db70-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3db70-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3db70-107">DESCRIPTION</span></span>
<span data-ttu-id="3db70-108">Confirma o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="3db70-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="3db70-109">A operação de confirmação é disparada no moveResources em movestate ' CommitPending ' ou ' CommitFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para Committed.</span><span class="sxs-lookup"><span data-stu-id="3db70-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="3db70-110">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="3db70-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3db70-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3db70-111">EXAMPLES</span></span>

### <span data-ttu-id="3db70-112">Exemplo 1: validar o dependecies antes da confirmação dos recursos</span><span class="sxs-lookup"><span data-stu-id="3db70-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="3db70-113">Valide o dependecies antes da confirmação dos recursos.</span><span class="sxs-lookup"><span data-stu-id="3db70-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="3db70-114">Exemplo 2: confirmar o conjunto de recursos na coleção move usando "MoveResource Name" como entrada</span><span class="sxs-lookup"><span data-stu-id="3db70-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="3db70-115">Confirme o conjunto de recursos na coleção move usando "MoveResource Name" como entrada</span><span class="sxs-lookup"><span data-stu-id="3db70-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="3db70-116">Exemplo 3: confirmar o conjunto de recursos na coleção move usando "SourceARMID" como entrada</span><span class="sxs-lookup"><span data-stu-id="3db70-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="3db70-117">Confirme o conjunto de recursos na coleção mover usando "SourceARMID" como entrada</span><span class="sxs-lookup"><span data-stu-id="3db70-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="3db70-118">OS</span><span class="sxs-lookup"><span data-stu-id="3db70-118">PARAMETERS</span></span>

### <span data-ttu-id="3db70-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3db70-119">-AsJob</span></span>
<span data-ttu-id="3db70-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3db70-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3db70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db70-121">-DefaultProfile</span></span>
<span data-ttu-id="3db70-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3db70-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3db70-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3db70-123">-MoveCollectionName</span></span>
<span data-ttu-id="3db70-124">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="3db70-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3db70-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="3db70-125">-MoveResource</span></span>
<span data-ttu-id="3db70-126">Obtém ou define a lista de IDs do recurso, por padrão, aceita mover o ID do recurso, a menos que o tipo de entrada seja alternado pela propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="3db70-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db70-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="3db70-127">-MoveResourceInputType</span></span>
<span data-ttu-id="3db70-128">Define o tipo de entrada mover recurso.</span><span class="sxs-lookup"><span data-stu-id="3db70-128">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3db70-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3db70-129">-NoWait</span></span>
<span data-ttu-id="3db70-130">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3db70-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3db70-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3db70-131">-ResourceGroupName</span></span>
<span data-ttu-id="3db70-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3db70-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3db70-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3db70-133">-SubscriptionId</span></span>
<span data-ttu-id="3db70-134">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="3db70-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="3db70-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="3db70-135">-ValidateOnly</span></span>
<span data-ttu-id="3db70-136">Obtém ou define um valor que indica se a operação precisa executar pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="3db70-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="3db70-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3db70-137">-Confirm</span></span>
<span data-ttu-id="3db70-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3db70-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db70-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db70-139">-WhatIf</span></span>
<span data-ttu-id="3db70-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3db70-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db70-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3db70-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db70-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db70-142">CommonParameters</span></span>
<span data-ttu-id="3db70-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3db70-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db70-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3db70-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db70-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3db70-145">INPUTS</span></span>

## <span data-ttu-id="3db70-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3db70-146">OUTPUTS</span></span>

### <span data-ttu-id="3db70-147">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3db70-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="3db70-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3db70-148">NOTES</span></span>

<span data-ttu-id="3db70-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3db70-149">ALIASES</span></span>

## <span data-ttu-id="3db70-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3db70-150">RELATED LINKS</span></span>

