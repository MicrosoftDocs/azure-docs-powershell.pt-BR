---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: e075da17009c863e8c564eb5379495a1bdaff505
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891645"
---
# <span data-ttu-id="3ac6a-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="3ac6a-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="3ac6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac6a-103">Move o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="3ac6a-104">A operação de movimentação é disparada depois que moveResources estão no moveState 'MovePending' ou 'MoveFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para CommitPending.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="3ac6a-105">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3ac6a-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ac6a-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ac6a-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ac6a-107">DESCRIPTION</span></span>
<span data-ttu-id="3ac6a-108">Move o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="3ac6a-109">A operação de movimentação é disparada depois que moveResources estão no moveState 'MovePending' ou 'MoveFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para CommitPending.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="3ac6a-110">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="3ac6a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-111">EXAMPLES</span></span>

### <span data-ttu-id="3ac6a-112">Exemplo 1: Validar as dependentes antes de iniciar a movimentação para os recursos.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly


AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 9:39:37 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 9:39:37 AM
Status         : Succeeded

```

<span data-ttu-id="3ac6a-113">Valide as dependeções antes de iniciar a movimentação para os recursos.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="3ac6a-114">Exemplo 2: Iniciar a movimentação para o conjunto de recursos na coleção Move usando "MoveResource Name" como entrada.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" 

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 11:56:33 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 11:55:21 AM
Status         : Succeeded

```

<span data-ttu-id="3ac6a-115">Inicie Mover para o conjunto de recursos na coleção Move usando "Nome moveResource" como entrada.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="3ac6a-116">Exemplo 3: Iniciar Movimentação para o conjunto de recursos na Coleção Move usando "SourceARMID" como entrada.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:01:35 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:00:21 PM
Status         : Succeeded

```

<span data-ttu-id="3ac6a-117">Inicie Mover para o conjunto de recursos na coleção Move usando "SourceARMID" como entrada.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="3ac6a-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-118">PARAMETERS</span></span>

### <span data-ttu-id="3ac6a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ac6a-119">-AsJob</span></span>
<span data-ttu-id="3ac6a-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3ac6a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="3ac6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac6a-121">-DefaultProfile</span></span>
<span data-ttu-id="3ac6a-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac6a-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="3ac6a-123">-MoveCollectionName</span></span>
<span data-ttu-id="3ac6a-124">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="3ac6a-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="3ac6a-125">-MoveResource</span></span>
<span data-ttu-id="3ac6a-126">Obtém ou define a lista de IDs de recursos, por padrão, aceita mover ids de recurso, a menos que o tipo de entrada seja comutado por meio da propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="3ac6a-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="3ac6a-127">-MoveResourceInputType</span></span>
<span data-ttu-id="3ac6a-128">Define o tipo de entrada de recurso move.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="3ac6a-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ac6a-129">-NoWait</span></span>
<span data-ttu-id="3ac6a-130">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3ac6a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ac6a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac6a-131">-ResourceGroupName</span></span>
<span data-ttu-id="3ac6a-132">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="3ac6a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ac6a-133">-SubscriptionId</span></span>
<span data-ttu-id="3ac6a-134">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="3ac6a-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="3ac6a-135">-ValidateOnly</span></span>
<span data-ttu-id="3ac6a-136">Obtém ou define um valor que indica se a operação precisa executar somente pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="3ac6a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ac6a-137">-Confirm</span></span>
<span data-ttu-id="3ac6a-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ac6a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac6a-139">-WhatIf</span></span>
<span data-ttu-id="3ac6a-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac6a-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ac6a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac6a-142">CommonParameters</span></span>
<span data-ttu-id="3ac6a-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ac6a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac6a-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ac6a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac6a-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-145">INPUTS</span></span>

## <span data-ttu-id="3ac6a-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-146">OUTPUTS</span></span>

### <span data-ttu-id="3ac6a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="3ac6a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="3ac6a-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ac6a-148">NOTES</span></span>

<span data-ttu-id="3ac6a-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3ac6a-149">ALIASES</span></span>

## <span data-ttu-id="3ac6a-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ac6a-150">RELATED LINKS</span></span>

