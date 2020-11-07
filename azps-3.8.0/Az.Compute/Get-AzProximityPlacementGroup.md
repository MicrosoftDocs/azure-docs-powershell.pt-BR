---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943431"
---
# <span data-ttu-id="69093-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="69093-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="69093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69093-102">SYNOPSIS</span></span>
<span data-ttu-id="69093-103">Obter ou listar os recursos de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="69093-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="69093-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69093-104">SYNTAX</span></span>

### <span data-ttu-id="69093-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="69093-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69093-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="69093-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69093-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69093-107">DESCRIPTION</span></span>
<span data-ttu-id="69093-108">Este cmdlet receberá ou listará os recursos de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="69093-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="69093-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69093-109">EXAMPLES</span></span>

### <span data-ttu-id="69093-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69093-110">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
VirtualMachines             : {}
VirtualMachineScaleSets     : {}
AvailabilitySets            : {}
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {[key1, val1]}
```

<span data-ttu-id="69093-111">Este comando obtém o grupo de posicionamento de proximidade</span><span class="sxs-lookup"><span data-stu-id="69093-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="69093-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="69093-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="69093-113">Este comando lista todos os grupos de posicionamento de proximidade sob o grupo de recursos específico.</span><span class="sxs-lookup"><span data-stu-id="69093-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="69093-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="69093-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="69093-115">Este comando lista todos os grupos de posicionamento de proximidade sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="69093-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="69093-116">OS</span><span class="sxs-lookup"><span data-stu-id="69093-116">PARAMETERS</span></span>

### <span data-ttu-id="69093-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="69093-117">-ColocationStatus</span></span>
<span data-ttu-id="69093-118">Mostra o status de colocalização de um recurso no grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="69093-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69093-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69093-119">-DefaultProfile</span></span>
<span data-ttu-id="69093-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69093-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69093-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="69093-121">-Name</span></span>
<span data-ttu-id="69093-122">O nome do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="69093-122">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="69093-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69093-123">-ResourceGroupName</span></span>
<span data-ttu-id="69093-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69093-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="69093-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69093-125">-ResourceId</span></span>
<span data-ttu-id="69093-126">A ID do recurso para o grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="69093-126">The resource id for the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69093-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69093-127">CommonParameters</span></span>
<span data-ttu-id="69093-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69093-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69093-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69093-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69093-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69093-130">INPUTS</span></span>

### <span data-ttu-id="69093-131">System. String</span><span class="sxs-lookup"><span data-stu-id="69093-131">System.String</span></span>

## <span data-ttu-id="69093-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69093-132">OUTPUTS</span></span>

### <span data-ttu-id="69093-133">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="69093-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="69093-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69093-134">NOTES</span></span>

## <span data-ttu-id="69093-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69093-135">RELATED LINKS</span></span>
