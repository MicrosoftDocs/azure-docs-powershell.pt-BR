---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzProximityPlacementGroup.md
ms.openlocfilehash: a6308120303684a8e87280ef903056361fbaf848
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117866"
---
# <span data-ttu-id="e9330-101">Get-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e9330-101">Get-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="e9330-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9330-102">SYNOPSIS</span></span>
<span data-ttu-id="e9330-103">Obter ou listar recursos de Grupo de Posicionamento de Proximidade.</span><span class="sxs-lookup"><span data-stu-id="e9330-103">Get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="e9330-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9330-104">SYNTAX</span></span>

### <span data-ttu-id="e9330-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e9330-105">DefaultParameter (Default)</span></span>
```
Get-AzProximityPlacementGroup [[-ResourceGroupName] <String>] [[-Name] <String>] [-ColocationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9330-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e9330-106">ResourceIdParameter</span></span>
```
Get-AzProximityPlacementGroup [-ColocationStatus] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9330-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e9330-107">DESCRIPTION</span></span>
<span data-ttu-id="e9330-108">Este cmdlet receberá ou lista os recursos do Grupo de Posicionamento de Proximidade.</span><span class="sxs-lookup"><span data-stu-id="e9330-108">This cmdlet will get or list Proximity Placement Group resource(s).</span></span>

## <span data-ttu-id="e9330-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e9330-109">EXAMPLES</span></span>

### <span data-ttu-id="e9330-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e9330-110">Example 1</span></span>
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

<span data-ttu-id="e9330-111">Este comando obtém o grupo de posicionamento de proximidade</span><span class="sxs-lookup"><span data-stu-id="e9330-111">This command gets the proximity placement group</span></span>

### <span data-ttu-id="e9330-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e9330-112">Example 2</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
```

<span data-ttu-id="e9330-113">Este comando lista todos os grupos de posicionamento de proximidade sob determinado grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9330-113">This command list all proximity placement groups under the given resource group.</span></span>

### <span data-ttu-id="e9330-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e9330-114">Example 3</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup

ResourceGroupName            Name      Location     Type
-----------------            ----      --------     ----
rg0                          ppg0 westcentralus Standard
rg0                          ppg1 westcentralus Standard
rg1                          ppg2     centralus Standard
```

<span data-ttu-id="e9330-115">Esta lista de comandos lista todos os grupos de posicionamento de proximidade sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e9330-115">This command list all proximity placement groups under the subscription.</span></span>

## <span data-ttu-id="e9330-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9330-116">PARAMETERS</span></span>

### <span data-ttu-id="e9330-117">-ColocationStatus</span><span class="sxs-lookup"><span data-stu-id="e9330-117">-ColocationStatus</span></span>
<span data-ttu-id="e9330-118">Mostra o status de colocação de um recurso no grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e9330-118">Shows the colocation status of a resource in the proximity placement group.</span></span>

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

### <span data-ttu-id="e9330-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9330-119">-DefaultProfile</span></span>
<span data-ttu-id="e9330-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e9330-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9330-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9330-121">-Name</span></span>
<span data-ttu-id="e9330-122">O nome do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e9330-122">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="e9330-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9330-123">-ResourceGroupName</span></span>
<span data-ttu-id="e9330-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9330-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9330-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9330-125">-ResourceId</span></span>
<span data-ttu-id="e9330-126">A ID do recurso para o grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e9330-126">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="e9330-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9330-127">CommonParameters</span></span>
<span data-ttu-id="e9330-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9330-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9330-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9330-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9330-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="e9330-130">INPUTS</span></span>

### <span data-ttu-id="e9330-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e9330-131">System.String</span></span>

## <span data-ttu-id="e9330-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="e9330-132">OUTPUTS</span></span>

### <span data-ttu-id="e9330-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e9330-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="e9330-134">Notas</span><span class="sxs-lookup"><span data-stu-id="e9330-134">NOTES</span></span>

## <span data-ttu-id="e9330-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9330-135">RELATED LINKS</span></span>
