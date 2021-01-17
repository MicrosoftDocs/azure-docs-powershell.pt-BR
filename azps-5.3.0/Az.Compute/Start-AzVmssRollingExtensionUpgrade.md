---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430145"
---
# <span data-ttu-id="8ca99-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="8ca99-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="8ca99-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ca99-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca99-103">Este cmdlet inicia uma atualização sem interrupção para todas as extensões em determinado conjunto de escala da máquina virtual para a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8ca99-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="8ca99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ca99-104">SYNTAX</span></span>

### <span data-ttu-id="8ca99-105">Defaultparameter</span><span class="sxs-lookup"><span data-stu-id="8ca99-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca99-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8ca99-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ca99-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8ca99-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ca99-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ca99-108">DESCRIPTION</span></span>
<span data-ttu-id="8ca99-109">Inicia uma atualização sem interrupção para mover todas as extensões neste conjunto de escala de máquinas virtuais para a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8ca99-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="8ca99-110">Extensões que já estão executando a versão mais recente disponível não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="8ca99-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="8ca99-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ca99-111">EXAMPLES</span></span>

### <span data-ttu-id="8ca99-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ca99-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="8ca99-113">Este exemplo obtém o conjunto de dimensionamento de VM existente "MyVmssName" e adiciona uma extensão a ele.</span><span class="sxs-lookup"><span data-stu-id="8ca99-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="8ca99-114">O comando final executa o processo de atualização sem interrupção da extensão.</span><span class="sxs-lookup"><span data-stu-id="8ca99-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="8ca99-115">OS</span><span class="sxs-lookup"><span data-stu-id="8ca99-115">PARAMETERS</span></span>

### <span data-ttu-id="8ca99-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ca99-116">-AsJob</span></span>
<span data-ttu-id="8ca99-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8ca99-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ca99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca99-118">-DefaultProfile</span></span>
<span data-ttu-id="8ca99-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca99-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ca99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca99-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ca99-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ca99-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="8ca99-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ca99-122">-ResourceId</span></span>
<span data-ttu-id="8ca99-123">A ID do recurso do objeto do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="8ca99-123">The resource Id of the VM scale set object.</span></span> 

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

### <span data-ttu-id="8ca99-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ca99-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="8ca99-125">O objeto do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="8ca99-125">The VM scale set object.</span></span>

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

### <span data-ttu-id="8ca99-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8ca99-126">-VMScaleSetName</span></span>
<span data-ttu-id="8ca99-127">O nome do conjunto de escala da VM.</span><span class="sxs-lookup"><span data-stu-id="8ca99-127">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="8ca99-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ca99-128">-Confirm</span></span>
<span data-ttu-id="8ca99-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ca99-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ca99-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ca99-130">-WhatIf</span></span>
<span data-ttu-id="8ca99-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ca99-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ca99-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ca99-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ca99-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca99-133">CommonParameters</span></span>
<span data-ttu-id="8ca99-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca99-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca99-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ca99-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca99-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ca99-136">INPUTS</span></span>

### <span data-ttu-id="8ca99-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca99-137">System.String</span></span>

### <span data-ttu-id="8ca99-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="8ca99-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="8ca99-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ca99-139">OUTPUTS</span></span>

### <span data-ttu-id="8ca99-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8ca99-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8ca99-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ca99-141">NOTES</span></span>

## <span data-ttu-id="8ca99-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ca99-142">RELATED LINKS</span></span>
