---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azproximityplacementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzProximityPlacementGroup.md
ms.openlocfilehash: 2a3f4a6d386f37334908efde31332ed6137ecb74
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597312"
---
# <span data-ttu-id="f29d2-101">Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f29d2-101">Remove-AzProximityPlacementGroup</span></span>

## <span data-ttu-id="f29d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f29d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f29d2-103">Excluir recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="f29d2-103">Delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="f29d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f29d2-104">SYNTAX</span></span>

### <span data-ttu-id="f29d2-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="f29d2-105">DefaultParameter (Default)</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f29d2-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="f29d2-106">ResourceIdParameter</span></span>
```
Remove-AzProximityPlacementGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f29d2-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f29d2-107">ObjectParameter</span></span>
```
Remove-AzProximityPlacementGroup [-InputObject] <PSProximityPlacementGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f29d2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f29d2-108">DESCRIPTION</span></span>
<span data-ttu-id="f29d2-109">Esse cmdlet excluirá o recurso de grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="f29d2-109">This cmdlet will delete Proximity Placement Group resource.</span></span>

## <span data-ttu-id="f29d2-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f29d2-110">EXAMPLES</span></span>

### <span data-ttu-id="f29d2-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f29d2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmProximityPlacementGroup  -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName  | Remove-AzureRmProximityPlacementGroup
```

<span data-ttu-id="f29d2-112">Esse comando Remove o grupo de posicionamento de proximidade fornecido.</span><span class="sxs-lookup"><span data-stu-id="f29d2-112">This command removes the given proximity placement group.</span></span>

## <span data-ttu-id="f29d2-113">OS</span><span class="sxs-lookup"><span data-stu-id="f29d2-113">PARAMETERS</span></span>

### <span data-ttu-id="f29d2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f29d2-114">-AsJob</span></span>
<span data-ttu-id="f29d2-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f29d2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f29d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f29d2-116">-DefaultProfile</span></span>
<span data-ttu-id="f29d2-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f29d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f29d2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f29d2-118">-Force</span></span>
<span data-ttu-id="f29d2-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f29d2-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f29d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f29d2-120">-InputObject</span></span>
<span data-ttu-id="f29d2-121">O objeto do grupo de posicionamento de proximidade PS</span><span class="sxs-lookup"><span data-stu-id="f29d2-121">The PS Proximity Placement Group Object</span></span>

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

### <span data-ttu-id="f29d2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f29d2-122">-Name</span></span>
<span data-ttu-id="f29d2-123">O nome do grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="f29d2-123">The name of the proximity placement group.</span></span>

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

### <span data-ttu-id="f29d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f29d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="f29d2-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f29d2-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f29d2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f29d2-126">-ResourceId</span></span>
<span data-ttu-id="f29d2-127">A ID do recurso para o grupo de posicionamento de proximidade.</span><span class="sxs-lookup"><span data-stu-id="f29d2-127">The resource id for the proximity placement group.</span></span>

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

### <span data-ttu-id="f29d2-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f29d2-128">-Confirm</span></span>
<span data-ttu-id="f29d2-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f29d2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f29d2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f29d2-130">-WhatIf</span></span>
<span data-ttu-id="f29d2-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f29d2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f29d2-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f29d2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f29d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f29d2-133">CommonParameters</span></span>
<span data-ttu-id="f29d2-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f29d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f29d2-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f29d2-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f29d2-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f29d2-136">INPUTS</span></span>

### <span data-ttu-id="f29d2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f29d2-137">System.String</span></span>

### <span data-ttu-id="f29d2-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="f29d2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup</span></span>

## <span data-ttu-id="f29d2-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f29d2-139">OUTPUTS</span></span>

### <span data-ttu-id="f29d2-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="f29d2-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f29d2-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f29d2-141">NOTES</span></span>

## <span data-ttu-id="f29d2-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f29d2-142">RELATED LINKS</span></span>
