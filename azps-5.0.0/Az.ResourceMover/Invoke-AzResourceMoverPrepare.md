---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283775"
---
# <span data-ttu-id="6cd3a-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="6cd3a-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="6cd3a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd3a-103">Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="6cd3a-104">A operação de preparação está em moveResources que estão em movestate ' PreparePending ' ou ' PrepareFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="6cd3a-105">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="6cd3a-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cd3a-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6cd3a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cd3a-107">DESCRIPTION</span></span>
<span data-ttu-id="6cd3a-108">Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="6cd3a-109">A operação de preparação está em moveResources que estão em movestate ' PreparePending ' ou ' PrepareFailed ', em uma conclusão bem-sucedida, o moveResource movestate faz uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="6cd3a-110">Para ajudar o usuário a usar o pré-requisito para a operação, o cliente pode chamar a operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="6cd3a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cd3a-111">EXAMPLES</span></span>

### <span data-ttu-id="6cd3a-112">Exemplo 1: validar o dependecies antes de preparar-se para os recursos</span><span class="sxs-lookup"><span data-stu-id="6cd3a-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="6cd3a-113">Valide o dependecies antes de se preparar para os recursos.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="6cd3a-114">Exemplo 2: iniciar preparação para o conjunto de recursos na coleção move usando "MoveResource Name" como entrada</span><span class="sxs-lookup"><span data-stu-id="6cd3a-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="6cd3a-115">Inicie a preparação para o conjunto de recursos na coleção move usando "MoveResource Name" como entrada.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="6cd3a-116">Exemplo 3: iniciar preparação para o conjunto de recursos na coleção mover usando "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="6cd3a-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="6cd3a-117">Inicie a preparação para o conjunto de recursos na coleção mover usando "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="6cd3a-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="6cd3a-118">OS</span><span class="sxs-lookup"><span data-stu-id="6cd3a-118">PARAMETERS</span></span>

### <span data-ttu-id="6cd3a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cd3a-119">-AsJob</span></span>
<span data-ttu-id="6cd3a-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6cd3a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="6cd3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cd3a-121">-DefaultProfile</span></span>
<span data-ttu-id="6cd3a-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cd3a-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="6cd3a-123">-MoveCollectionName</span></span>
<span data-ttu-id="6cd3a-124">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="6cd3a-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="6cd3a-125">-MoveResource</span></span>
<span data-ttu-id="6cd3a-126">Obtém ou define a lista de IDs do recurso, por padrão, aceita mover o ID do recurso, a menos que o tipo de entrada seja alternado pela propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="6cd3a-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="6cd3a-127">-MoveResourceInputType</span></span>
<span data-ttu-id="6cd3a-128">Define o tipo de entrada mover recurso.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="6cd3a-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6cd3a-129">-NoWait</span></span>
<span data-ttu-id="6cd3a-130">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="6cd3a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6cd3a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cd3a-131">-ResourceGroupName</span></span>
<span data-ttu-id="6cd3a-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="6cd3a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cd3a-133">-SubscriptionId</span></span>
<span data-ttu-id="6cd3a-134">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="6cd3a-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="6cd3a-135">-ValidateOnly</span></span>
<span data-ttu-id="6cd3a-136">Obtém ou define um valor que indica se a operação precisa executar pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="6cd3a-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6cd3a-137">-Confirm</span></span>
<span data-ttu-id="6cd3a-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6cd3a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cd3a-139">-WhatIf</span></span>
<span data-ttu-id="6cd3a-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cd3a-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6cd3a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd3a-142">CommonParameters</span></span>
<span data-ttu-id="6cd3a-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd3a-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cd3a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd3a-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cd3a-145">INPUTS</span></span>

## <span data-ttu-id="6cd3a-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cd3a-146">OUTPUTS</span></span>

### <span data-ttu-id="6cd3a-147">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6cd3a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="6cd3a-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cd3a-148">NOTES</span></span>

<span data-ttu-id="6cd3a-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6cd3a-149">ALIASES</span></span>

## <span data-ttu-id="6cd3a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cd3a-150">RELATED LINKS</span></span>

