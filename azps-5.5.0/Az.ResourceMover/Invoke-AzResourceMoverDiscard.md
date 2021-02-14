---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117190"
---
# <span data-ttu-id="74c4b-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="74c4b-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="74c4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="74c4b-103">Descarta o conjunto de recursos incluído no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="74c4b-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="74c4b-104">A operação de descarte é disparada no moveResources no moveState "CommitPending" ou "DiscardFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para Mover Pendente.</span><span class="sxs-lookup"><span data-stu-id="74c4b-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="74c4b-105">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="74c4b-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="74c4b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74c4b-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74c4b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="74c4b-107">DESCRIPTION</span></span>
<span data-ttu-id="74c4b-108">Descarta o conjunto de recursos incluído no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="74c4b-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="74c4b-109">A operação de descarte é disparada no moveResources no moveState "CommitPending" ou "DiscardFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para Mover Pendente.</span><span class="sxs-lookup"><span data-stu-id="74c4b-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="74c4b-110">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="74c4b-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="74c4b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="74c4b-111">EXAMPLES</span></span>

### <span data-ttu-id="74c4b-112">Exemplo 1: Validar as dependeções antes de descartar os recursos.</span><span class="sxs-lookup"><span data-stu-id="74c4b-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="74c4b-113">Valide as dependecies antes de descartar os recursos.</span><span class="sxs-lookup"><span data-stu-id="74c4b-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="74c4b-114">Exemplo 2: descarta a movimentação dos recursos usando "Nome MoveResource" como entrada</span><span class="sxs-lookup"><span data-stu-id="74c4b-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="74c4b-115">Descarta a movimentação dos recursos usando "Nome MoveResource" como entrada.</span><span class="sxs-lookup"><span data-stu-id="74c4b-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="74c4b-116">Exemplo 3: descarta a movimentação dos recursos usando "SourceARMID" como entrada</span><span class="sxs-lookup"><span data-stu-id="74c4b-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="74c4b-117">Descarta a movimentação dos recursos usando "SourceARMID" como entrada.</span><span class="sxs-lookup"><span data-stu-id="74c4b-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="74c4b-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74c4b-118">PARAMETERS</span></span>

### <span data-ttu-id="74c4b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74c4b-119">-AsJob</span></span>
<span data-ttu-id="74c4b-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="74c4b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="74c4b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c4b-121">-DefaultProfile</span></span>
<span data-ttu-id="74c4b-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74c4b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74c4b-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="74c4b-123">-MoveResource</span></span>
<span data-ttu-id="74c4b-124">Obtém ou define a lista de IDs de recurso, por padrão, ela aceita mover as IDs de recurso, a menos que o tipo de entrada seja alternado pela propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="74c4b-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="74c4b-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="74c4b-125">-MoveResourceInputType</span></span>
<span data-ttu-id="74c4b-126">Define o tipo de entrada mover recurso.</span><span class="sxs-lookup"><span data-stu-id="74c4b-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="74c4b-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="74c4b-127">-Name</span></span>
<span data-ttu-id="74c4b-128">O nome mover coleção.</span><span class="sxs-lookup"><span data-stu-id="74c4b-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="74c4b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="74c4b-129">-NoWait</span></span>
<span data-ttu-id="74c4b-130">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="74c4b-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74c4b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74c4b-131">-ResourceGroupName</span></span>
<span data-ttu-id="74c4b-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="74c4b-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="74c4b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74c4b-133">-SubscriptionId</span></span>
<span data-ttu-id="74c4b-134">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="74c4b-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="74c4b-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="74c4b-135">-ValidateOnly</span></span>
<span data-ttu-id="74c4b-136">Obtém ou define um valor que indica se a operação só precisa executar pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="74c4b-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="74c4b-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="74c4b-137">-Confirm</span></span>
<span data-ttu-id="74c4b-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74c4b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c4b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74c4b-139">-WhatIf</span></span>
<span data-ttu-id="74c4b-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="74c4b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c4b-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74c4b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c4b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c4b-142">CommonParameters</span></span>
<span data-ttu-id="74c4b-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c4b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c4b-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74c4b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c4b-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="74c4b-145">INPUTS</span></span>

## <span data-ttu-id="74c4b-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="74c4b-146">OUTPUTS</span></span>

### <span data-ttu-id="74c4b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="74c4b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="74c4b-148">Notas</span><span class="sxs-lookup"><span data-stu-id="74c4b-148">NOTES</span></span>

<span data-ttu-id="74c4b-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="74c4b-149">ALIASES</span></span>

## <span data-ttu-id="74c4b-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74c4b-150">RELATED LINKS</span></span>

