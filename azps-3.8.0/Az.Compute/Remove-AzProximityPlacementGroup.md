---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 07adbff46713136ec412d10bd428765230e1838c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784915"
---
# <span data-ttu-id="c42eb-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c42eb-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="c42eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c42eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c42eb-103">Excluir recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="c42eb-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="c42eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c42eb-104">SYNTAX</span></span>

### <span data-ttu-id="c42eb-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="c42eb-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c42eb-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c42eb-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c42eb-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c42eb-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-Force] [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c42eb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c42eb-108">DESCRIPTION</span></span>
<span data-ttu-id="c42eb-109">Esse cmdlet excluirá o recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="c42eb-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="c42eb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c42eb-110">EXAMPLES</span></span>

### <span data-ttu-id="c42eb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c42eb-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="c42eb-112">Esse comando Remove o grupo de posicionamento de proximidade fornecido.</span><span class="sxs-lookup"><span data-stu-id="c42eb-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="c42eb-113">OS</span><span class="sxs-lookup"><span data-stu-id="c42eb-113">PARAMETERS</span></span>

### <span data-ttu-id="c42eb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c42eb-114">-AsJob</span></span>
<span data-ttu-id="c42eb-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c42eb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c42eb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42eb-116">-DefaultProfile</span></span>
<span data-ttu-id="c42eb-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c42eb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c42eb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c42eb-118">-Force</span></span>
<span data-ttu-id="c42eb-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c42eb-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c42eb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c42eb-120">-InputObject</span></span>
<span data-ttu-id="c42eb-121">O objeto do grupo de posicionamento de proximidade PS</span><span class="sxs-lookup"><span data-stu-id="c42eb-121">The PS Proximity Placement Group Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup
Parameter Sets: ObjectParameter
Aliases: ProximityPlacementGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c42eb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c42eb-122">-Name</span></span>
<span data-ttu-id="c42eb-123">O nome do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="c42eb-123">The name of the proximity placement group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: ProximityPlacementGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c42eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="c42eb-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c42eb-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c42eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c42eb-126">-ResourceId</span></span>
<span data-ttu-id="c42eb-127">A ID do recurso para o grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="c42eb-127">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="c42eb-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c42eb-128">-Confirm</span></span>
<span data-ttu-id="c42eb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c42eb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c42eb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c42eb-130">-WhatIf</span></span>
<span data-ttu-id="c42eb-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c42eb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c42eb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c42eb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c42eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42eb-133">CommonParameters</span></span>
<span data-ttu-id="c42eb-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42eb-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c42eb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42eb-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c42eb-136">INPUTS</span></span>

### <span data-ttu-id="c42eb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c42eb-137">System.String</span></span>

### <span data-ttu-id="c42eb-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="c42eb-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="c42eb-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c42eb-139">OUTPUTS</span></span>

### <span data-ttu-id="c42eb-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c42eb-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c42eb-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c42eb-141">NOTES</span></span>

## <span data-ttu-id="c42eb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c42eb-142">RELATED LINKS</span></span>
