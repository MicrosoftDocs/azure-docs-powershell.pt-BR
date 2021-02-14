---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 7274067b2f8daa916a0021f0ea2fd7985e1914ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115950"
---
# <span data-ttu-id="049dc-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="049dc-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="049dc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="049dc-102">SYNOPSIS</span></span>
<span data-ttu-id="049dc-103">Define as propriedades da política de atualização em implantação do VMSS.</span><span class="sxs-lookup"><span data-stu-id="049dc-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="049dc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="049dc-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="049dc-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="049dc-105">DESCRIPTION</span></span>
<span data-ttu-id="049dc-106">Define as propriedades da política de atualização em implantação do VMSS.</span><span class="sxs-lookup"><span data-stu-id="049dc-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="049dc-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="049dc-107">EXAMPLES</span></span>

### <span data-ttu-id="049dc-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="049dc-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="049dc-109">Esse comando define 40% para MaxBatchInstance, 35% para MaxUnhealthyInstance, 30% para MaxUnhealthyUpgradedInstance e tempo de pausa de 30 segundos entre lotes de objeto local VMSS $vmss.</span><span class="sxs-lookup"><span data-stu-id="049dc-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="049dc-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="049dc-110">PARAMETERS</span></span>

### <span data-ttu-id="049dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049dc-111">-DefaultProfile</span></span>
<span data-ttu-id="049dc-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="049dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="049dc-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="049dc-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="049dc-114">A porcentagem máxima do total de instâncias de máquina virtual que serão atualizadas simultaneamente pela atualização em um lote.</span><span class="sxs-lookup"><span data-stu-id="049dc-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="049dc-115">Como esse é um máximo, instâncias não saudáveis em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote diminua para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="049dc-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="049dc-116">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="049dc-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="049dc-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="049dc-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="049dc-118">A porcentagem máxima do total de instâncias de máquina virtual no conjunto de escalas que pode ser simultaneamente não saudável, seja como resultado da atualização, ou por ser encontrada em um estado insalubre pela saúde da máquina virtual verifica antes que a atualização em implantação seja cancelada.</span><span class="sxs-lookup"><span data-stu-id="049dc-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="049dc-119">Essa restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="049dc-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="049dc-120">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="049dc-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="049dc-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="049dc-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="049dc-122">A porcentagem máxima de instâncias de máquina virtual atualizadas que podem ser encontradas em um estado não saudável.</span><span class="sxs-lookup"><span data-stu-id="049dc-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="049dc-123">Essa verificação acontecerá depois que cada lote for atualizado.</span><span class="sxs-lookup"><span data-stu-id="049dc-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="049dc-124">Se essa porcentagem for excedida, a atualização em circulação será cancelada.</span><span class="sxs-lookup"><span data-stu-id="049dc-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="049dc-125">Se o valor não for especificado, ele será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="049dc-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="049dc-126">-PauseTimeBetweenBat along</span><span class="sxs-lookup"><span data-stu-id="049dc-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="049dc-127">O tempo de espera entre concluir a atualização para todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="049dc-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="049dc-128">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="049dc-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="049dc-129">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="049dc-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="049dc-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="049dc-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="049dc-131">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="049dc-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="049dc-132">Você pode usar o cmdlet New-AzVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="049dc-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="049dc-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="049dc-133">-Confirm</span></span>
<span data-ttu-id="049dc-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="049dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="049dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="049dc-135">-WhatIf</span></span>
<span data-ttu-id="049dc-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="049dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="049dc-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="049dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="049dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049dc-138">CommonParameters</span></span>
<span data-ttu-id="049dc-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049dc-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="049dc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049dc-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="049dc-141">INPUTS</span></span>

### <span data-ttu-id="049dc-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="049dc-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="049dc-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="049dc-143">System.Int32</span></span>

### <span data-ttu-id="049dc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="049dc-144">System.String</span></span>

## <span data-ttu-id="049dc-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="049dc-145">OUTPUTS</span></span>

### <span data-ttu-id="049dc-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="049dc-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="049dc-147">Notas</span><span class="sxs-lookup"><span data-stu-id="049dc-147">NOTES</span></span>

## <span data-ttu-id="049dc-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="049dc-148">RELATED LINKS</span></span>
