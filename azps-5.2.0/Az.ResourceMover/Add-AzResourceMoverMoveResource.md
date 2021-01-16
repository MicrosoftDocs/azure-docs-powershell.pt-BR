---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/add-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Add-AzResourceMoverMoveResource.md
ms.openlocfilehash: bafba030de13cdee2c4b7026f498c07cf4231fdd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262452"
---
# <span data-ttu-id="9787e-101">Add-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="9787e-101">Add-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="9787e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9787e-102">SYNOPSIS</span></span>
<span data-ttu-id="9787e-103">Cria ou atualiza um recurso de movimentação na coleção move.</span><span class="sxs-lookup"><span data-stu-id="9787e-103">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="9787e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9787e-104">SYNTAX</span></span>

```
Add-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DependsOnOverride <IMoveResourceDependencyOverride[]>]
 [-ExistingTargetId <String>] [-ResourceSettingResourceType <String>]
 [-ResourceSettingTargetResourceName <String>] [-SourceId <String>]
 [-SourceResourceSettingResourceType <String>] [-SourceResourceSettingTargetResourceName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9787e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9787e-105">DESCRIPTION</span></span>
<span data-ttu-id="9787e-106">Cria ou atualiza um recurso de movimentação na coleção move.</span><span class="sxs-lookup"><span data-stu-id="9787e-106">Creates or updates a Move Resource in the move collection.</span></span>

## <span data-ttu-id="9787e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9787e-107">EXAMPLES</span></span>

### <span data-ttu-id="9787e-108">Exemplo 1: adicionando um recurso à coleção move.</span><span class="sxs-lookup"><span data-stu-id="9787e-108">Example 1: Adding a resource to the move collection.</span></span>
```powershell
PS C:\> Add-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM" -SourceId "/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM" -Name PSDemoVM -ResourceSettingResourceType "Microsoft.Compute/virtualMachines" -ResourceSettingTargetResourceName PSDemoVM

Output:

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migr
                                          ate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          : DependencyComputationPending
MoveStatusDetail                        : {}
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       : The dependency computation is not completed for resource - /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resou
                                          rceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM.
                                              Possible Causes: Dependency computation is pending for resource.
                                              Recommended Action: Validate dependencies to compute the dependencies.

MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachi
                                          nes/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type          

```

<span data-ttu-id="9787e-109">Adicionando um recurso à coleção move dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="9787e-109">Adding a resource to the move collection within the specified subscription.</span></span>

## <span data-ttu-id="9787e-110">OS</span><span class="sxs-lookup"><span data-stu-id="9787e-110">PARAMETERS</span></span>

### <span data-ttu-id="9787e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9787e-111">-AsJob</span></span>
<span data-ttu-id="9787e-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9787e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9787e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9787e-113">-DefaultProfile</span></span>
<span data-ttu-id="9787e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9787e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9787e-115">-DependsOnOverride</span><span class="sxs-lookup"><span data-stu-id="9787e-115">-DependsOnOverride</span></span>
<span data-ttu-id="9787e-116">Obtém ou define a substituição das dependências do recurso de movimentação.</span><span class="sxs-lookup"><span data-stu-id="9787e-116">Gets or sets the move resource dependencies overrides.</span></span>
<span data-ttu-id="9787e-117">Para construir, consulte a seção notas para propriedades DEPENDSONOVERRIDE e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9787e-117">To construct, see NOTES section for DEPENDSONOVERRIDE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResourceDependencyOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-118">-ExistingTargetId</span><span class="sxs-lookup"><span data-stu-id="9787e-118">-ExistingTargetId</span></span>
<span data-ttu-id="9787e-119">Obtém ou define a ID do braço de destino existente do recurso.</span><span class="sxs-lookup"><span data-stu-id="9787e-119">Gets or sets the existing target ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-120">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="9787e-120">-MoveCollectionName</span></span>
<span data-ttu-id="9787e-121">O nome da coleção de movimento.</span><span class="sxs-lookup"><span data-stu-id="9787e-121">The Move Collection Name.</span></span>

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

### <span data-ttu-id="9787e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9787e-122">-Name</span></span>
<span data-ttu-id="9787e-123">O nome do recurso de movimento.</span><span class="sxs-lookup"><span data-stu-id="9787e-123">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9787e-124">-NoWait</span></span>
<span data-ttu-id="9787e-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9787e-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9787e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9787e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9787e-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9787e-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="9787e-128">-ResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="9787e-128">-ResourceSettingResourceType</span></span>
<span data-ttu-id="9787e-129">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="9787e-129">The resource type.</span></span>
<span data-ttu-id="9787e-130">Por exemplo, o valor pode ser Microsoft. Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="9787e-130">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-131">-ResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="9787e-131">-ResourceSettingTargetResourceName</span></span>
<span data-ttu-id="9787e-132">Obtém ou define o nome do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="9787e-132">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-133">-SourceID</span><span class="sxs-lookup"><span data-stu-id="9787e-133">-SourceId</span></span>
<span data-ttu-id="9787e-134">Obtém ou define a ID do braço de origem do recurso.</span><span class="sxs-lookup"><span data-stu-id="9787e-134">Gets or sets the Source ARM Id of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-135">-SourceResourceSettingResourceType</span><span class="sxs-lookup"><span data-stu-id="9787e-135">-SourceResourceSettingResourceType</span></span>
<span data-ttu-id="9787e-136">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="9787e-136">The resource type.</span></span>
<span data-ttu-id="9787e-137">Por exemplo, o valor pode ser Microsoft. Compute/virtualMachines.</span><span class="sxs-lookup"><span data-stu-id="9787e-137">For example, the value can be Microsoft.Compute/virtualMachines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-138">-SourceResourceSettingTargetResourceName</span><span class="sxs-lookup"><span data-stu-id="9787e-138">-SourceResourceSettingTargetResourceName</span></span>
<span data-ttu-id="9787e-139">Obtém ou define o nome do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="9787e-139">Gets or sets the target Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9787e-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9787e-140">-SubscriptionId</span></span>
<span data-ttu-id="9787e-141">A ID da assinatura.</span><span class="sxs-lookup"><span data-stu-id="9787e-141">The Subscription ID.</span></span>

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

### <span data-ttu-id="9787e-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9787e-142">-Confirm</span></span>
<span data-ttu-id="9787e-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9787e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9787e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9787e-144">-WhatIf</span></span>
<span data-ttu-id="9787e-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9787e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9787e-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9787e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9787e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9787e-147">CommonParameters</span></span>
<span data-ttu-id="9787e-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9787e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9787e-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9787e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9787e-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9787e-150">INPUTS</span></span>

## <span data-ttu-id="9787e-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9787e-151">OUTPUTS</span></span>

### <span data-ttu-id="9787e-152">Microsoft. Azure. PowerShell. cmdlets. ResourceMover. Models. Api20191001Preview. IMoveResource</span><span class="sxs-lookup"><span data-stu-id="9787e-152">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="9787e-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9787e-153">NOTES</span></span>

<span data-ttu-id="9787e-154">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9787e-154">ALIASES</span></span>

<span data-ttu-id="9787e-155">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="9787e-155">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9787e-156">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9787e-156">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9787e-157">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9787e-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9787e-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride [] >: Obtém ou define a substituição das dependências do recurso de movimentação.</span><span class="sxs-lookup"><span data-stu-id="9787e-158">DEPENDSONOVERRIDE <IMoveResourceDependencyOverride[]>: Gets or sets the move resource dependencies overrides.</span></span>
  - <span data-ttu-id="9787e-159">`[Id <String>]`: Obtém ou define a ID do braço do recurso dependente.</span><span class="sxs-lookup"><span data-stu-id="9787e-159">`[Id <String>]`: Gets or sets the ARM ID of the dependent resource.</span></span>
  - <span data-ttu-id="9787e-160">`[TargetId <String>]`: Obtém ou define a ID do braço do recurso de MoveResource ou a ID do braço do recurso do recurso dependente.</span><span class="sxs-lookup"><span data-stu-id="9787e-160">`[TargetId <String>]`: Gets or sets the resource ARM id of either the MoveResource or the resource ARM ID of         the dependent resource.</span></span>

## <span data-ttu-id="9787e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9787e-161">RELATED LINKS</span></span>

