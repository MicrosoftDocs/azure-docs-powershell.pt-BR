---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: 88cdb68da94f84dc1af977ba5b12b5bfb4d73914
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597368"
---
# <span data-ttu-id="e667b-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e667b-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="e667b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e667b-102">SYNOPSIS</span></span>
<span data-ttu-id="e667b-103">Crie um recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e667b-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="e667b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e667b-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e667b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e667b-105">DESCRIPTION</span></span>
<span data-ttu-id="e667b-106">Este cmdlet criará o recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e667b-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="e667b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e667b-107">EXAMPLES</span></span>

### <span data-ttu-id="e667b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e667b-108">Example 1</span></span>
```
PS C:\> New-AzureRmProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = "val1"}

ResourceGroupName           : rg0
ProximityPlacementGroupType : Standard
Id                          : /subscriptions/5393f919-a68a-43d0-9063-4b2bda6bffdf/resourceGroups/rg0/providers/Microsoft.Compute/proximityPlacementGroups/ppg0
Name                        : ppg0
Type                        : Microsoft.Compute/proximityPlacementGroups
Location                    : westcentralus
Tags                        : {"key1":"val1"}
```

<span data-ttu-id="e667b-109">Esse comando cria um grupo local de proximidade no local indicado.</span><span class="sxs-lookup"><span data-stu-id="e667b-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="e667b-110">OS</span><span class="sxs-lookup"><span data-stu-id="e667b-110">PARAMETERS</span></span>

### <span data-ttu-id="e667b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e667b-111">-AsJob</span></span>
<span data-ttu-id="e667b-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e667b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e667b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e667b-113">-DefaultProfile</span></span>
<span data-ttu-id="e667b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e667b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e667b-115">-Local</span><span class="sxs-lookup"><span data-stu-id="e667b-115">-Location</span></span>
<span data-ttu-id="e667b-116">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="e667b-116">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e667b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e667b-117">-Name</span></span>
<span data-ttu-id="e667b-118">O nome do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e667b-118">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e667b-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="e667b-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="e667b-120">Especifica o tipo do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="e667b-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="e667b-121">Os valores possíveis são: Standard ou ultra</span><span class="sxs-lookup"><span data-stu-id="e667b-121">Possible values are: Standard or Ultra</span></span>

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

### <span data-ttu-id="e667b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e667b-122">-ResourceGroupName</span></span>
<span data-ttu-id="e667b-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e667b-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e667b-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="e667b-124">-Tag</span></span>
<span data-ttu-id="e667b-125">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="e667b-125">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e667b-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e667b-126">-Confirm</span></span>
<span data-ttu-id="e667b-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e667b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e667b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e667b-128">-WhatIf</span></span>
<span data-ttu-id="e667b-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e667b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e667b-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e667b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e667b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e667b-131">CommonParameters</span></span>
<span data-ttu-id="e667b-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e667b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e667b-133">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e667b-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e667b-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e667b-134">INPUTS</span></span>

### <span data-ttu-id="e667b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e667b-135">System.String</span></span>

## <span data-ttu-id="e667b-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e667b-136">OUTPUTS</span></span>

### <span data-ttu-id="e667b-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e667b-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="e667b-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e667b-138">NOTES</span></span>

## <span data-ttu-id="e667b-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e667b-139">RELATED LINKS</span></span>
