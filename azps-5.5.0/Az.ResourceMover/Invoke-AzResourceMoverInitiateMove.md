---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113349"
---
# <span data-ttu-id="30f47-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="30f47-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="30f47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30f47-102">SYNOPSIS</span></span>
<span data-ttu-id="30f47-103">Move o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="30f47-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="30f47-104">A operação de movimentação é disparada depois que o moveResources está no moveState "MovePending" ou "MoveFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para CommitPending.</span><span class="sxs-lookup"><span data-stu-id="30f47-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="30f47-105">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="30f47-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="30f47-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30f47-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="30f47-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="30f47-107">DESCRIPTION</span></span>
<span data-ttu-id="30f47-108">Move o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="30f47-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="30f47-109">A operação de movimentação é disparada depois que o moveResources está no moveState "MovePending" ou "MoveFailed", em uma conclusão bem-sucedida, o moveResource moveState faz uma transição para CommitPending.</span><span class="sxs-lookup"><span data-stu-id="30f47-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="30f47-110">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar com a propriedade validateOnly definida como verdadeira.</span><span class="sxs-lookup"><span data-stu-id="30f47-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="30f47-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30f47-111">EXAMPLES</span></span>

### <span data-ttu-id="30f47-112">Exemplo 1: Validar as dependeções antes de iniciar a movimentação para os recursos.</span><span class="sxs-lookup"><span data-stu-id="30f47-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="30f47-113">Valide as dependecies antes de Iniciar Movimentação para os recursos.</span><span class="sxs-lookup"><span data-stu-id="30f47-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="30f47-114">Exemplo 2: Iniciar Mover para o conjunto de recursos na coleção Mover usando "Nome MoveResource" como entrada</span><span class="sxs-lookup"><span data-stu-id="30f47-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="30f47-115">Inicie Mover para o conjunto de recursos na coleção Mover usando "Nome MoveResource" como entrada.</span><span class="sxs-lookup"><span data-stu-id="30f47-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="30f47-116">Exemplo 3: Iniciar Movimentação para o conjunto de recursos no Conjunto de Movimentações usando "SourceARMID" como entrada</span><span class="sxs-lookup"><span data-stu-id="30f47-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="30f47-117">Inicie Mover para o conjunto de recursos na coleção Mover usando "SourceARMID" como entrada.</span><span class="sxs-lookup"><span data-stu-id="30f47-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="30f47-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30f47-118">PARAMETERS</span></span>

### <span data-ttu-id="30f47-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30f47-119">-AsJob</span></span>
<span data-ttu-id="30f47-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="30f47-120">Run the command as a job</span></span>

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

### <span data-ttu-id="30f47-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30f47-121">-DefaultProfile</span></span>
<span data-ttu-id="30f47-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30f47-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30f47-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="30f47-123">-MoveCollectionName</span></span>
<span data-ttu-id="30f47-124">O nome mover coleção.</span><span class="sxs-lookup"><span data-stu-id="30f47-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="30f47-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="30f47-125">-MoveResource</span></span>
<span data-ttu-id="30f47-126">Obtém ou define a lista de IDs de recurso, por padrão, ela aceita mover as IDs de recurso, a menos que o tipo de entrada seja alternado pela propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="30f47-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="30f47-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="30f47-127">-MoveResourceInputType</span></span>
<span data-ttu-id="30f47-128">Define o tipo de entrada mover recurso.</span><span class="sxs-lookup"><span data-stu-id="30f47-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="30f47-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="30f47-129">-NoWait</span></span>
<span data-ttu-id="30f47-130">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="30f47-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="30f47-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30f47-131">-ResourceGroupName</span></span>
<span data-ttu-id="30f47-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="30f47-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="30f47-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="30f47-133">-SubscriptionId</span></span>
<span data-ttu-id="30f47-134">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="30f47-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="30f47-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="30f47-135">-ValidateOnly</span></span>
<span data-ttu-id="30f47-136">Obtém ou define um valor que indica se a operação só precisa executar pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="30f47-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="30f47-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="30f47-137">-Confirm</span></span>
<span data-ttu-id="30f47-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30f47-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30f47-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30f47-139">-WhatIf</span></span>
<span data-ttu-id="30f47-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="30f47-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30f47-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30f47-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30f47-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30f47-142">CommonParameters</span></span>
<span data-ttu-id="30f47-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30f47-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30f47-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30f47-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30f47-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="30f47-145">INPUTS</span></span>

## <span data-ttu-id="30f47-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="30f47-146">OUTPUTS</span></span>

### <span data-ttu-id="30f47-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="30f47-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="30f47-148">Notas</span><span class="sxs-lookup"><span data-stu-id="30f47-148">NOTES</span></span>

<span data-ttu-id="30f47-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="30f47-149">ALIASES</span></span>

## <span data-ttu-id="30f47-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30f47-150">RELATED LINKS</span></span>

