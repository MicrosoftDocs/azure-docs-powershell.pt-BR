---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891649"
---
# <span data-ttu-id="8851d-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="8851d-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="8851d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8851d-102">SYNOPSIS</span></span>
<span data-ttu-id="8851d-103">Confirma o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="8851d-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="8851d-104">A operação de confirmação é disparada no moveResources no moveState 'CommitPending' ou 'CommitFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para Committed.</span><span class="sxs-lookup"><span data-stu-id="8851d-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="8851d-105">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="8851d-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8851d-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8851d-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8851d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8851d-107">DESCRIPTION</span></span>
<span data-ttu-id="8851d-108">Confirma o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="8851d-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="8851d-109">A operação de confirmação é disparada no moveResources no moveState 'CommitPending' ou 'CommitFailed', em uma conclusão bem-sucedida, moveResource moveState faz uma transição para Committed.</span><span class="sxs-lookup"><span data-stu-id="8851d-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="8851d-110">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="8851d-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8851d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8851d-111">EXAMPLES</span></span>

### <span data-ttu-id="8851d-112">Exemplo 1: Validar as dependeções antes da confirmação dos recursos.</span><span class="sxs-lookup"><span data-stu-id="8851d-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="8851d-113">Valide as dependeções antes da confirmação dos recursos.</span><span class="sxs-lookup"><span data-stu-id="8851d-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="8851d-114">Exemplo 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span><span class="sxs-lookup"><span data-stu-id="8851d-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="8851d-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span><span class="sxs-lookup"><span data-stu-id="8851d-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="8851d-116">Exemplo 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span><span class="sxs-lookup"><span data-stu-id="8851d-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="8851d-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span><span class="sxs-lookup"><span data-stu-id="8851d-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="8851d-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8851d-118">PARAMETERS</span></span>

### <span data-ttu-id="8851d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8851d-119">-AsJob</span></span>
<span data-ttu-id="8851d-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8851d-120">Run the command as a job</span></span>

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

### <span data-ttu-id="8851d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8851d-121">-DefaultProfile</span></span>
<span data-ttu-id="8851d-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8851d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8851d-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="8851d-123">-MoveCollectionName</span></span>
<span data-ttu-id="8851d-124">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="8851d-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8851d-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="8851d-125">-MoveResource</span></span>
<span data-ttu-id="8851d-126">Obtém ou define a lista de IDs de recursos, por padrão, aceita mover ids de recurso, a menos que o tipo de entrada seja comutado por meio da propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="8851d-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="8851d-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="8851d-127">-MoveResourceInputType</span></span>
<span data-ttu-id="8851d-128">Define o tipo de entrada de recurso move.</span><span class="sxs-lookup"><span data-stu-id="8851d-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="8851d-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8851d-129">-NoWait</span></span>
<span data-ttu-id="8851d-130">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8851d-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8851d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8851d-131">-ResourceGroupName</span></span>
<span data-ttu-id="8851d-132">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8851d-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8851d-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8851d-133">-SubscriptionId</span></span>
<span data-ttu-id="8851d-134">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="8851d-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="8851d-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="8851d-135">-ValidateOnly</span></span>
<span data-ttu-id="8851d-136">Obtém ou define um valor que indica se a operação precisa executar somente pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="8851d-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="8851d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8851d-137">-Confirm</span></span>
<span data-ttu-id="8851d-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8851d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8851d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8851d-139">-WhatIf</span></span>
<span data-ttu-id="8851d-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8851d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8851d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8851d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8851d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8851d-142">CommonParameters</span></span>
<span data-ttu-id="8851d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8851d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8851d-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8851d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8851d-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8851d-145">INPUTS</span></span>

## <span data-ttu-id="8851d-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8851d-146">OUTPUTS</span></span>

### <span data-ttu-id="8851d-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8851d-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="8851d-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="8851d-148">NOTES</span></span>

<span data-ttu-id="8851d-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8851d-149">ALIASES</span></span>

## <span data-ttu-id="8851d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8851d-150">RELATED LINKS</span></span>

