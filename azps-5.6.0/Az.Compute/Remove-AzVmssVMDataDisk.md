---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: c44369915c38219491bd8dfdc1ca288487da27f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887816"
---
# <span data-ttu-id="cab1d-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cab1d-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="cab1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab1d-102">SYNOPSIS</span></span>
<span data-ttu-id="cab1d-103">Remove um disco de dados de uma VM de conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="cab1d-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="cab1d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cab1d-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab1d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cab1d-105">DESCRIPTION</span></span>
<span data-ttu-id="cab1d-106">O cmdlet **Remove-AzVmssVMDataDisk** remove um disco de dados de uma VM de conjunto de escala de VM</span><span class="sxs-lookup"><span data-stu-id="cab1d-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="cab1d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cab1d-107">EXAMPLES</span></span>

### <span data-ttu-id="cab1d-108">Exemplo 1: Remover um disco de dados de uma VM de conjunto de escala de VM</span><span class="sxs-lookup"><span data-stu-id="cab1d-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="cab1d-109">O primeiro comando getsan Vmss VM existente dado pelo nome do grupo de recursos, o nome do vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="cab1d-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="cab1d-110">O segundo comando remove o lun de disco de dados 0 da VM do conjunto de escala VM armazenado em $VmssVM O comando final atualiza a VM Vmss com o disco de dados removido.</span><span class="sxs-lookup"><span data-stu-id="cab1d-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="cab1d-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cab1d-111">PARAMETERS</span></span>

### <span data-ttu-id="cab1d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab1d-112">-DefaultProfile</span></span>
<span data-ttu-id="cab1d-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cab1d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab1d-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="cab1d-114">-Lun</span></span>
<span data-ttu-id="cab1d-115">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="cab1d-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab1d-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cab1d-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="cab1d-117">A escala da máquina virtual definiu o perfil da VM.</span><span class="sxs-lookup"><span data-stu-id="cab1d-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cab1d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab1d-118">CommonParameters</span></span>
<span data-ttu-id="cab1d-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab1d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab1d-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cab1d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab1d-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cab1d-121">INPUTS</span></span>

### <span data-ttu-id="cab1d-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cab1d-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="cab1d-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cab1d-123">OUTPUTS</span></span>

### <span data-ttu-id="cab1d-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="cab1d-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="cab1d-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="cab1d-125">NOTES</span></span>

## <span data-ttu-id="cab1d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cab1d-126">RELATED LINKS</span></span>
