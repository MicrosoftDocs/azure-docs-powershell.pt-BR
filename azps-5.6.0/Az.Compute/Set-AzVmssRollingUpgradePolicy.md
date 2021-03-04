---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 16ea3a8754ef08e933412582f100296d07fcb430
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886246"
---
# <span data-ttu-id="d324e-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="d324e-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="d324e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d324e-102">SYNOPSIS</span></span>
<span data-ttu-id="d324e-103">Define as propriedades da política de atualização de rolagem do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d324e-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="d324e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d324e-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d324e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d324e-105">DESCRIPTION</span></span>
<span data-ttu-id="d324e-106">Define as propriedades da política de atualização de rolagem do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d324e-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="d324e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d324e-107">EXAMPLES</span></span>

### <span data-ttu-id="d324e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d324e-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="d324e-109">Este comando define 40% para MaxBatchInstance, 35% para MaxUnhealthyInstance, 30% para MaxUnhealthyUpgradedInstance e 30 segundos de pausa entre lotes para o objeto local VMSS $vmss.</span><span class="sxs-lookup"><span data-stu-id="d324e-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="d324e-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d324e-110">PARAMETERS</span></span>

### <span data-ttu-id="d324e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d324e-111">-DefaultProfile</span></span>
<span data-ttu-id="d324e-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d324e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d324e-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d324e-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="d324e-114">A porcentagem máxima do total de instâncias de máquina virtual que serão atualizadas simultaneamente pela atualização de rolagem em um lote.</span><span class="sxs-lookup"><span data-stu-id="d324e-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="d324e-115">Como isso é um máximo, instâncias não salubres em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote diminua para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="d324e-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="d324e-116">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="d324e-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d324e-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d324e-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="d324e-118">A porcentagem máxima do total de instâncias de máquina virtual no conjunto de escala que podem ser simultaneamente não árias, como resultado da atualização ou por serem encontradas em um estado salubressuário pelas verificações de saúde da máquina virtual antes que a atualização de rolagem seja anulada.</span><span class="sxs-lookup"><span data-stu-id="d324e-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="d324e-119">Essa restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="d324e-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="d324e-120">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="d324e-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d324e-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="d324e-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="d324e-122">A porcentagem máxima de instâncias de máquina virtual atualizadas que podem ser encontradas em um estado não alub.</span><span class="sxs-lookup"><span data-stu-id="d324e-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="d324e-123">Essa verificação acontecerá depois que cada lote for atualizado.</span><span class="sxs-lookup"><span data-stu-id="d324e-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="d324e-124">Se essa porcentagem for sempre excedida, a atualização em circulação será anulada.</span><span class="sxs-lookup"><span data-stu-id="d324e-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="d324e-125">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="d324e-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d324e-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="d324e-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="d324e-127">O tempo de espera entre concluir a atualização para todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="d324e-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="d324e-128">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="d324e-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="d324e-129">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="d324e-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d324e-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d324e-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d324e-131">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="d324e-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="d324e-132">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="d324e-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d324e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d324e-133">-Confirm</span></span>
<span data-ttu-id="d324e-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d324e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d324e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d324e-135">-WhatIf</span></span>
<span data-ttu-id="d324e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d324e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d324e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d324e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d324e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d324e-138">CommonParameters</span></span>
<span data-ttu-id="d324e-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d324e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d324e-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d324e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d324e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d324e-141">INPUTS</span></span>

### <span data-ttu-id="d324e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d324e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d324e-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d324e-143">System.Int32</span></span>

### <span data-ttu-id="d324e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d324e-144">System.String</span></span>

## <span data-ttu-id="d324e-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d324e-145">OUTPUTS</span></span>

### <span data-ttu-id="d324e-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d324e-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d324e-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="d324e-147">NOTES</span></span>

## <span data-ttu-id="d324e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d324e-148">RELATED LINKS</span></span>
