---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111089"
---
# <span data-ttu-id="302ad-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="302ad-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="302ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="302ad-102">SYNOPSIS</span></span>
<span data-ttu-id="302ad-103">Remove um disco de dados de um VM de conjunto de escala de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="302ad-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="302ad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="302ad-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="302ad-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="302ad-105">DESCRIPTION</span></span>
<span data-ttu-id="302ad-106">O cmdlet **Remove-AzVmsSVMDataDisk** remove um disco de dados de um VM definido como VM</span><span class="sxs-lookup"><span data-stu-id="302ad-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="302ad-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="302ad-107">EXAMPLES</span></span>

### <span data-ttu-id="302ad-108">Exemplo 1: Remover um disco de dados de um VM definido como VM</span><span class="sxs-lookup"><span data-stu-id="302ad-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="302ad-109">O primeiro comando recebe vmss VMss existentes dado pelo nome do grupo de recursos, pelo nome do vmss e pela ID da instância.</span><span class="sxs-lookup"><span data-stu-id="302ad-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="302ad-110">O segundo comando remove o disco de dados 0 do VM de conjunto de VMs armazenado no $VmssVM O comando final atualiza o VM VM do Vmss com disco de dados removido.</span><span class="sxs-lookup"><span data-stu-id="302ad-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="302ad-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="302ad-111">PARAMETERS</span></span>

### <span data-ttu-id="302ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302ad-112">-DefaultProfile</span></span>
<span data-ttu-id="302ad-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="302ad-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="302ad-114">-Ltda</span><span class="sxs-lookup"><span data-stu-id="302ad-114">-Lun</span></span>
<span data-ttu-id="302ad-115">Especifica o número da unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="302ad-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="302ad-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="302ad-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="302ad-117">O perfil de VM de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="302ad-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="302ad-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302ad-118">CommonParameters</span></span>
<span data-ttu-id="302ad-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302ad-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302ad-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="302ad-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302ad-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="302ad-121">INPUTS</span></span>

### <span data-ttu-id="302ad-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="302ad-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="302ad-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="302ad-123">OUTPUTS</span></span>

### <span data-ttu-id="302ad-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="302ad-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="302ad-125">Notas</span><span class="sxs-lookup"><span data-stu-id="302ad-125">NOTES</span></span>

## <span data-ttu-id="302ad-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="302ad-126">RELATED LINKS</span></span>
