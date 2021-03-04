---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891644"
---
# <span data-ttu-id="b36e4-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="b36e4-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="b36e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b36e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b36e4-103">Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="b36e4-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="b36e4-104">A operação de preparação está no moveResources que estão no moveState 'PreparePending' ou 'PrepareFailed', em uma conclusão bem-sucedida, moveResource moveState fazer uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="b36e4-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b36e4-105">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="b36e4-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b36e4-106">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b36e4-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b36e4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b36e4-107">DESCRIPTION</span></span>
<span data-ttu-id="b36e4-108">Inicia a preparação para o conjunto de recursos incluídos no corpo da solicitação.</span><span class="sxs-lookup"><span data-stu-id="b36e4-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="b36e4-109">A operação de preparação está no moveResources que estão no moveState 'PreparePending' ou 'PrepareFailed', em uma conclusão bem-sucedida, moveResource moveState fazer uma transição para MovePending.</span><span class="sxs-lookup"><span data-stu-id="b36e4-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="b36e4-110">Para ajudar o usuário a pré-requisito da operação que o cliente pode chamar operação com a propriedade validateOnly definida como true.</span><span class="sxs-lookup"><span data-stu-id="b36e4-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b36e4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b36e4-111">EXAMPLES</span></span>

### <span data-ttu-id="b36e4-112">Exemplo 1: Validar as dependeções antes de preparar os recursos.</span><span class="sxs-lookup"><span data-stu-id="b36e4-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="b36e4-113">Obter os recursos dependentes necessários que também precisam ser preparados.</span><span class="sxs-lookup"><span data-stu-id="b36e4-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="b36e4-114">Valide as dependeções antes de preparar os recursos.</span><span class="sxs-lookup"><span data-stu-id="b36e4-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="b36e4-115">Obter os recursos dependentes necessários que também precisam ser preparados.</span><span class="sxs-lookup"><span data-stu-id="b36e4-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="b36e4-116">Exemplo 2: Inicie a preparação para o conjunto de recursos na Coleção Move usando "MoveResource Name" como entrada.</span><span class="sxs-lookup"><span data-stu-id="b36e4-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="b36e4-117">Inicie a preparação para o conjunto de recursos na Coleção Move usando "MoveResource Name" como entrada.</span><span class="sxs-lookup"><span data-stu-id="b36e4-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="b36e4-118">Exemplo 3: Inicie a preparação para o conjunto de recursos na Coleção Move usando "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="b36e4-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="b36e4-119">Inicie a preparação para o conjunto de recursos na Coleção Move usando "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="b36e4-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="b36e4-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b36e4-120">PARAMETERS</span></span>

### <span data-ttu-id="b36e4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b36e4-121">-AsJob</span></span>
<span data-ttu-id="b36e4-122">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b36e4-122">Run the command as a job</span></span>

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

### <span data-ttu-id="b36e4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36e4-123">-DefaultProfile</span></span>
<span data-ttu-id="b36e4-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b36e4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b36e4-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="b36e4-125">-MoveCollectionName</span></span>
<span data-ttu-id="b36e4-126">O nome da coleção Move.</span><span class="sxs-lookup"><span data-stu-id="b36e4-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="b36e4-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="b36e4-127">-MoveResource</span></span>
<span data-ttu-id="b36e4-128">Obtém ou define a lista de IDs de recursos, por padrão, aceita mover ids de recurso, a menos que o tipo de entrada seja comutado por meio da propriedade moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="b36e4-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="b36e4-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="b36e4-129">-MoveResourceInputType</span></span>
<span data-ttu-id="b36e4-130">Define o tipo de entrada de recurso move.</span><span class="sxs-lookup"><span data-stu-id="b36e4-130">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="b36e4-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b36e4-131">-NoWait</span></span>
<span data-ttu-id="b36e4-132">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b36e4-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b36e4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b36e4-133">-ResourceGroupName</span></span>
<span data-ttu-id="b36e4-134">O Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b36e4-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="b36e4-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b36e4-135">-SubscriptionId</span></span>
<span data-ttu-id="b36e4-136">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="b36e4-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="b36e4-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="b36e4-137">-ValidateOnly</span></span>
<span data-ttu-id="b36e4-138">Obtém ou define um valor que indica se a operação precisa executar somente pré-requisito.</span><span class="sxs-lookup"><span data-stu-id="b36e4-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="b36e4-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b36e4-139">-Confirm</span></span>
<span data-ttu-id="b36e4-140">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b36e4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b36e4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b36e4-141">-WhatIf</span></span>
<span data-ttu-id="b36e4-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b36e4-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b36e4-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b36e4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b36e4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36e4-144">CommonParameters</span></span>
<span data-ttu-id="b36e4-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b36e4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36e4-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b36e4-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36e4-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b36e4-147">INPUTS</span></span>

## <span data-ttu-id="b36e4-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b36e4-148">OUTPUTS</span></span>

### <span data-ttu-id="b36e4-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b36e4-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="b36e4-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="b36e4-150">NOTES</span></span>

<span data-ttu-id="b36e4-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b36e4-151">ALIASES</span></span>

## <span data-ttu-id="b36e4-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b36e4-152">RELATED LINKS</span></span>

