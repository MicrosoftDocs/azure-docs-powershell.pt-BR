---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssrollingupgradepolicy
schema: 2.0.0
ms.openlocfilehash: 4abdef2109b9591b6eaa0643e5e871518bd53b22
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785787"
---
# <span data-ttu-id="99481-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="99481-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="99481-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99481-102">SYNOPSIS</span></span>
<span data-ttu-id="99481-103">Define as propriedades da política de atualização sem interrupção do VMSS.</span><span class="sxs-lookup"><span data-stu-id="99481-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99481-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99481-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99481-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99481-105">DESCRIPTION</span></span>
<span data-ttu-id="99481-106">Define as propriedades da política de atualização sem interrupção do VMSS.</span><span class="sxs-lookup"><span data-stu-id="99481-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="99481-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99481-107">EXAMPLES</span></span>

### <span data-ttu-id="99481-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99481-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="99481-109">Este comando define 40% para MaxBatchInstance, 35% para MaxUnhealthyInstance, 30% para MaxUnhealthyUpgradedInstance e 30 segundos de tempo de pausa entre lotes para VMSS $vmss de objeto local.</span><span class="sxs-lookup"><span data-stu-id="99481-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="99481-110">OS</span><span class="sxs-lookup"><span data-stu-id="99481-110">PARAMETERS</span></span>

### <span data-ttu-id="99481-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99481-111">-DefaultProfile</span></span>
<span data-ttu-id="99481-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99481-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99481-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="99481-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="99481-114">A porcentagem máxima do total de instâncias da máquina virtual que serão atualizadas simultaneamente pela atualização sem interrupção em um lote.</span><span class="sxs-lookup"><span data-stu-id="99481-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="99481-115">Como se trata de um valor máximo, instâncias não íntegras em lotes anteriores ou futuros podem fazer com que a porcentagem de instâncias em um lote seja reduzida para garantir maior confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="99481-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="99481-116">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="99481-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99481-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="99481-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="99481-118">A porcentagem máxima do total de instâncias da máquina virtual no conjunto de escala que podem ser simultaneamente não íntegras, como resultado da atualização ou por estar em um estado não íntegro pelas verificações de integridade da máquina virtual antes de anular a atualização sem interrupção.</span><span class="sxs-lookup"><span data-stu-id="99481-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="99481-119">Esta restrição será verificada antes de iniciar qualquer lote.</span><span class="sxs-lookup"><span data-stu-id="99481-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="99481-120">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="99481-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99481-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="99481-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="99481-122">A porcentagem máxima de instâncias da máquina virtual atualizadas que podem ser encontradas em um estado não íntegro.</span><span class="sxs-lookup"><span data-stu-id="99481-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="99481-123">Essa verificação ocorrerá após a atualização de cada lote.</span><span class="sxs-lookup"><span data-stu-id="99481-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="99481-124">Se essa porcentagem já tiver sido excedida, a atualização sem interrupção será anulada.</span><span class="sxs-lookup"><span data-stu-id="99481-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="99481-125">Se o valor não for especificado, será definido como 20.</span><span class="sxs-lookup"><span data-stu-id="99481-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99481-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="99481-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="99481-127">O tempo de espera entre concluir a atualização de todas as máquinas virtuais em um lote e iniciar o próximo lote.</span><span class="sxs-lookup"><span data-stu-id="99481-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="99481-128">A duração do tempo deve ser especificada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="99481-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="99481-129">O valor padrão é 0 segundos (PT0S).</span><span class="sxs-lookup"><span data-stu-id="99481-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99481-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99481-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="99481-131">Especifica o objeto VMSS.</span><span class="sxs-lookup"><span data-stu-id="99481-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="99481-132">Você pode usar o cmdlet New-AzureRmVmssConfig para criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="99481-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99481-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99481-133">-Confirm</span></span>
<span data-ttu-id="99481-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99481-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99481-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99481-135">-WhatIf</span></span>
<span data-ttu-id="99481-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99481-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99481-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99481-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99481-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99481-138">CommonParameters</span></span>
<span data-ttu-id="99481-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99481-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99481-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99481-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99481-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99481-141">INPUTS</span></span>

### <span data-ttu-id="99481-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99481-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="99481-143">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String</span><span class="sxs-lookup"><span data-stu-id="99481-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String</span></span>

## <span data-ttu-id="99481-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99481-144">OUTPUTS</span></span>

### <span data-ttu-id="99481-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99481-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="99481-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99481-146">NOTES</span></span>

## <span data-ttu-id="99481-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99481-147">RELATED LINKS</span></span>

