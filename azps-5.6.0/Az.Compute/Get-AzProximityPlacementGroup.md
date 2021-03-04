---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: 7a69b47cef0d1f2ad11dcbe1c2bd191149d127df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893396"
---
# <span data-ttu-id="555c1-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="555c1-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="555c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="555c1-102">SYNOPSIS</span></span>
<span data-ttu-id="555c1-103">Obter ou listar recursos do Grupo de Posicionamento de Proximidade.</span><span class="sxs-lookup"><span data-stu-id="555c1-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="555c1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="555c1-104">SYNTAX</span></span>

### <span data-ttu-id="555c1-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="555c1-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="555c1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="555c1-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="555c1-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="555c1-107">DESCRIPTION</span></span>
<span data-ttu-id="555c1-108">Este cmdlet receberá ou lista os recursos do Grupo de Posicionamento de Proximidade.</span><span class="sxs-lookup"><span data-stu-id="555c1-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="555c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="555c1-109">EXAMPLES</span></span>

### <span data-ttu-id="555c1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="555c1-110">Example 1</span></span>
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

<span data-ttu-id="555c1-111">Este comando obtém o grupo de posicionamento de proximidade</span><span class="sxs-lookup"><span data-stu-id="555c1-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="555c1-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="555c1-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="555c1-113">Este comando lista todos os grupos de posicionamento de proximidade no grupo de recursos determinado.</span><span class="sxs-lookup"><span data-stu-id="555c1-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="555c1-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="555c1-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="555c1-115">Este comando lista todos os grupos de posicionamento de proximidade sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="555c1-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="555c1-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="555c1-116">PARAMETERS</span></span>

### <span data-ttu-id="555c1-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="555c1-117">-ColocationStatus</span></span>
<span data-ttu-id="555c1-118">Mostra o status de colocação de um recurso no grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="555c1-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

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

### <span data-ttu-id="555c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="555c1-119">-DefaultProfile</span></span>
<span data-ttu-id="555c1-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="555c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="555c1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="555c1-121">-Name</span></span>
<span data-ttu-id="555c1-122">O nome do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="555c1-122">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="555c1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="555c1-123">-ResourceGroupName</span></span>
<span data-ttu-id="555c1-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="555c1-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="555c1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="555c1-125">-ResourceId</span></span>
<span data-ttu-id="555c1-126">A ID do recurso para o grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="555c1-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="555c1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="555c1-127">CommonParameters</span></span>
<span data-ttu-id="555c1-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="555c1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="555c1-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="555c1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="555c1-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="555c1-130">INPUTS</span></span>

### <span data-ttu-id="555c1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="555c1-131">System.String</span></span>

## <span data-ttu-id="555c1-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="555c1-132">OUTPUTS</span></span>

### <span data-ttu-id="555c1-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="555c1-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="555c1-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="555c1-134">NOTES</span></span>

## <span data-ttu-id="555c1-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="555c1-135">RELATED LINKS</span></span>
