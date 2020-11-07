---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzProximityPlacementGroup.md
ms.openlocfilehash: cf8c4867fcc623065cce73fa392cb78d513200fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941452"
---
# <span data-ttu-id="37fa4-101">New-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="37fa4-101">New-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="37fa4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="37fa4-103">Crie um recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="37fa4-103">Create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="37fa4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37fa4-104">SYNTAX</span></span>

```
New-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-ProximityPlacementGroupType <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37fa4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="37fa4-106">Este cmdlet criará o recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="37fa4-106">This cmdlet will create Proximity Placement Group resource.</span></span>

## <span data-ttu-id="37fa4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37fa4-107">EXAMPLES</span></span>

### <span data-ttu-id="37fa4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37fa4-108">Example 1</span></span>
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

<span data-ttu-id="37fa4-109">Esse comando cria um grupo local de proximidade no local indicado.</span><span class="sxs-lookup"><span data-stu-id="37fa4-109">This command creates a proximity place group in the given location.</span></span>

## <span data-ttu-id="37fa4-110">OS</span><span class="sxs-lookup"><span data-stu-id="37fa4-110">PARAMETERS</span></span>

### <span data-ttu-id="37fa4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37fa4-111">-AsJob</span></span>
<span data-ttu-id="37fa4-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="37fa4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37fa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37fa4-113">-DefaultProfile</span></span>
<span data-ttu-id="37fa4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37fa4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37fa4-115">-Local</span><span class="sxs-lookup"><span data-stu-id="37fa4-115">-Location</span></span>
<span data-ttu-id="37fa4-116">Local do recurso</span><span class="sxs-lookup"><span data-stu-id="37fa4-116">Resource location</span></span>

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

### <span data-ttu-id="37fa4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="37fa4-117">-Name</span></span>
<span data-ttu-id="37fa4-118">O nome do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="37fa4-118">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="37fa4-119">-ProximityPlacementGroupType</span><span class="sxs-lookup"><span data-stu-id="37fa4-119">-ProximityPlacementGroupType</span></span>
<span data-ttu-id="37fa4-120">Especifica o tipo do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="37fa4-120">Specifies the type of the proximity placement group.</span></span>  <span data-ttu-id="37fa4-121">Os valores possíveis são: Standard ou ultra</span><span class="sxs-lookup"><span data-stu-id="37fa4-121">Possible values are: Standard or Ultra</span></span>

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

### <span data-ttu-id="37fa4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37fa4-122">-ResourceGroupName</span></span>
<span data-ttu-id="37fa4-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="37fa4-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="37fa4-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="37fa4-124">-Tag</span></span>
<span data-ttu-id="37fa4-125">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="37fa4-125">Resource tags</span></span>

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

### <span data-ttu-id="37fa4-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37fa4-126">-Confirm</span></span>
<span data-ttu-id="37fa4-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37fa4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37fa4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37fa4-128">-WhatIf</span></span>
<span data-ttu-id="37fa4-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37fa4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37fa4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37fa4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37fa4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37fa4-131">CommonParameters</span></span>
<span data-ttu-id="37fa4-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37fa4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37fa4-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37fa4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37fa4-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37fa4-134">INPUTS</span></span>

### <span data-ttu-id="37fa4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="37fa4-135">System.String</span></span>

## <span data-ttu-id="37fa4-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37fa4-136">OUTPUTS</span></span>

### <span data-ttu-id="37fa4-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="37fa4-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="37fa4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37fa4-138">NOTES</span></span>

## <span data-ttu-id="37fa4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37fa4-139">RELATED LINKS</span></span>
