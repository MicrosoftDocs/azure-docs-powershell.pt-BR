---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverMoveResource.md
ms.openlocfilehash: e0ce7e46e8105048d58ee8a4334eaf098b40399c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114916"
---
# <span data-ttu-id="1c207-101">Get-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="1c207-101">Get-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="1c207-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c207-102">SYNOPSIS</span></span>
<span data-ttu-id="1c207-103">Obtém o Recurso de Movimentação.</span><span class="sxs-lookup"><span data-stu-id="1c207-103">Gets the Move Resource.</span></span>

## <span data-ttu-id="1c207-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c207-104">SYNTAX</span></span>

### <span data-ttu-id="1c207-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1c207-105">List (Default)</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1c207-106">Obter</span><span class="sxs-lookup"><span data-stu-id="1c207-106">Get</span></span>
```
Get-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1c207-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c207-107">DESCRIPTION</span></span>
<span data-ttu-id="1c207-108">Obtém o Recurso de Movimentação.</span><span class="sxs-lookup"><span data-stu-id="1c207-108">Gets the Move Resource.</span></span>

## <span data-ttu-id="1c207-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c207-109">EXAMPLES</span></span>

### <span data-ttu-id="1c207-110">Exemplo 1: Obter detalhes de todos os recursos na coleção Mover.</span><span class="sxs-lookup"><span data-stu-id="1c207-110">Example 1: Get details of all the resources in the Move collection.</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM          

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.networ
                                          k/publicipaddresses/psdemovm-ip, /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psd
                                          emorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet, /subscriptions/e80eb9fa-c996-4435-aa32
                                          -5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemovm62
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : MovePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemovm62
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Network/networkInterfaces
ResourceSettingTargetResourceName       : psdemovm62
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network
                                          /networkInterfaces/psdemovm62
SourceResourceSettingResourceType       : Microsoft.Network/networkInterfaces
SourceResourceSettingTargetResourceName : psdemovm62
Target                                  :
TargetId                                :
Type                                    :

Code                                    :
DependsOn                               : {}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/psdemorm
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : CommitPending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : psdemorm
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : resourceGroups
ResourceSettingTargetResourceName       : psdemorm2
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm
SourceResourceSettingResourceType       : resourceGroups
SourceResourceSettingTargetResourceName : psdemorm
Target                                  :
TargetId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/psdemorm2
Type                                    :

```

<span data-ttu-id="1c207-111">Obter detalhes de todos os recursos do conjunto de movimentações.</span><span class="sxs-lookup"><span data-stu-id="1c207-111">Get details of all the resources in the move collection.</span></span>

### <span data-ttu-id="1c207-112">Exemplo 2: Obter detalhes de recursos específicos em um conjunto mover usando o nome do recurso mover.</span><span class="sxs-lookup"><span data-stu-id="1c207-112">Example 2: Get details of a specific resources in a Move collection using move resource name .</span></span>
```powershell
PS C:\> Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Name PSDemoVM   
                                                     
Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="1c207-113">Obter detalhes de recursos específicos em um conjunto de movimentações usando mover o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="1c207-113">Get details of a specific resources in a Move collection using move resource name .</span></span>

### <span data-ttu-id="1c207-114">Exemplo 3: Obter detalhes de recursos específicos em um conjunto mover usando filtros como : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="1c207-114">Example 3:Get details of a specific resources in a Move collection using filters such as : SourceResourceName, SourceId, MoveState, IsResolveRequired, ProvisioningState</span></span>
```powershell
PS C:\>Get-AzResourceMoverMoveResource -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM -Filter "Properties/SourceResourceName eq 'PSDemoVM'"

Code                                    :
DependsOn                               : {/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Networ
                                          k/networkInterfaces/psdemovm62,
                                          /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/PSDemoRM}
DependsOnOverride                       : {}
Detail                                  :
ExistingTargetId                        :
Id                                      : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/M
                                          icrosoft.Migrate/MoveCollections/PS-centralus-westcentralus-demoRM/MoveResources/PSDemoVM
Message                                 :
MoveStatusCode                          :
MoveStatusDetail                        :
MoveStatusJobName                       :
MoveStatusJobProgress                   :
MoveStatusMessage                       :
MoveStatusMoveState                     : PreparePending
MoveStatusTarget                        :
MoveStatusTargetId                      :
Name                                    : PSDemoVM
ProvisioningState                       : Succeeded
ResourceSettingResourceType             : Microsoft.Compute/virtualMachines
ResourceSettingTargetResourceName       : PSDemoVM
SourceId                                : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Compute
                                          /virtualMachines/PSDemoVM
SourceResourceSettingResourceType       : Microsoft.Compute/virtualMachines
SourceResourceSettingTargetResourceName : PSDemoVM
Target                                  :
TargetId                                :
Type                                    :

```

<span data-ttu-id="1c207-115">Obter detalhes de recursos específicos em uma coleção Mover usando filtro como armid, moveStatusMoveState(verificar) etc.</span><span class="sxs-lookup"><span data-stu-id="1c207-115">Get details of a specific resources in a Move collection using filter such as armid ,moveStatusMoveState(verify) etc.</span></span>

## <span data-ttu-id="1c207-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c207-116">PARAMETERS</span></span>

### <span data-ttu-id="1c207-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c207-117">-DefaultProfile</span></span>
<span data-ttu-id="1c207-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c207-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c207-119">-Filtro</span><span class="sxs-lookup"><span data-stu-id="1c207-119">-Filter</span></span>
<span data-ttu-id="1c207-120">O filtro a ser aplicado na operação.</span><span class="sxs-lookup"><span data-stu-id="1c207-120">The filter to apply on the operation.</span></span>
<span data-ttu-id="1c207-121">Por exemplo, você pode usar $filter=Properties/ProvisioningState eq 'Bem-sucedido'.</span><span class="sxs-lookup"><span data-stu-id="1c207-121">For example, you can use $filter=Properties/ProvisioningState eq 'Succeeded'.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c207-122">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1c207-122">-MoveCollectionName</span></span>
<span data-ttu-id="1c207-123">O nome mover coleção.</span><span class="sxs-lookup"><span data-stu-id="1c207-123">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1c207-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c207-124">-Name</span></span>
<span data-ttu-id="1c207-125">O nome mover recurso.</span><span class="sxs-lookup"><span data-stu-id="1c207-125">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c207-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c207-126">-ResourceGroupName</span></span>
<span data-ttu-id="1c207-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c207-127">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1c207-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c207-128">-SubscriptionId</span></span>
<span data-ttu-id="1c207-129">A ID da Assinatura.</span><span class="sxs-lookup"><span data-stu-id="1c207-129">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c207-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c207-130">CommonParameters</span></span>
<span data-ttu-id="1c207-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c207-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c207-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c207-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c207-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="1c207-133">INPUTS</span></span>

## <span data-ttu-id="1c207-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="1c207-134">OUTPUTS</span></span>

### <span data-ttu-id="1c207-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span><span class="sxs-lookup"><span data-stu-id="1c207-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveResource</span></span>

## <span data-ttu-id="1c207-136">Notas</span><span class="sxs-lookup"><span data-stu-id="1c207-136">NOTES</span></span>

<span data-ttu-id="1c207-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="1c207-137">ALIASES</span></span>

## <span data-ttu-id="1c207-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c207-138">RELATED LINKS</span></span>

