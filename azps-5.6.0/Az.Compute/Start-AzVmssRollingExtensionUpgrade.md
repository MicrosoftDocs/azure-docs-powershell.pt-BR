---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: 2816f34c8a6148d67a5bed397e573b07fa2e7004
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889796"
---
# <span data-ttu-id="14733-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="14733-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="14733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14733-102">SYNOPSIS</span></span>
<span data-ttu-id="14733-103">Este cmdlet inicia uma atualização de rolagem para todas as extensões no conjunto de escala de máquina virtual determinado para a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="14733-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="14733-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14733-104">SYNTAX</span></span>

### <span data-ttu-id="14733-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="14733-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14733-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="14733-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14733-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="14733-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14733-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14733-108">DESCRIPTION</span></span>
<span data-ttu-id="14733-109">Inicia uma atualização de rolagem para mover todas as extensões nesta escala de máquina virtual definida para a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="14733-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="14733-110">As extensões que já estão executando a versão mais recente disponível não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="14733-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="14733-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14733-111">EXAMPLES</span></span>

### <span data-ttu-id="14733-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14733-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="14733-113">Este exemplo obtém o conjunto de escala de VM existente "MyVmssName" e adiciona uma extensão a ele.</span><span class="sxs-lookup"><span data-stu-id="14733-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="14733-114">O comando final executa o processo de atualização de rolagem de extensão.</span><span class="sxs-lookup"><span data-stu-id="14733-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="14733-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14733-115">PARAMETERS</span></span>

### <span data-ttu-id="14733-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14733-116">-AsJob</span></span>
<span data-ttu-id="14733-117">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="14733-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14733-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14733-118">-DefaultProfile</span></span>
<span data-ttu-id="14733-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14733-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14733-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14733-120">-ResourceGroupName</span></span>
<span data-ttu-id="14733-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14733-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14733-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14733-122">-ResourceId</span></span>
<span data-ttu-id="14733-123">A ID do recurso do objeto de conjunto de escala VM.</span><span class="sxs-lookup"><span data-stu-id="14733-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14733-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14733-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="14733-125">O objeto de conjunto de escala VM.</span><span class="sxs-lookup"><span data-stu-id="14733-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14733-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="14733-126">-VMScaleSetName</span></span>
<span data-ttu-id="14733-127">O nome do conjunto de escala de VM.</span><span class="sxs-lookup"><span data-stu-id="14733-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14733-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14733-128">-Confirm</span></span>
<span data-ttu-id="14733-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14733-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14733-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14733-130">-WhatIf</span></span>
<span data-ttu-id="14733-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14733-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14733-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14733-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14733-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14733-133">CommonParameters</span></span>
<span data-ttu-id="14733-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14733-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14733-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14733-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14733-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14733-136">INPUTS</span></span>

### <span data-ttu-id="14733-137">System.String</span><span class="sxs-lookup"><span data-stu-id="14733-137">System.String</span></span>

### <span data-ttu-id="14733-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="14733-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="14733-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14733-139">OUTPUTS</span></span>

### <span data-ttu-id="14733-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="14733-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="14733-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="14733-141">NOTES</span></span>

## <span data-ttu-id="14733-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14733-142">RELATED LINKS</span></span>
