---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: cd41b7f09bbcf972d28aa38e9c1f4eb622e59b2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597271"
---
# <span data-ttu-id="c42a5-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c42a5-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="c42a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c42a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c42a5-103">Remove um disco de dados de uma VM do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="c42a5-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="c42a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c42a5-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c42a5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c42a5-105">DESCRIPTION</span></span>
<span data-ttu-id="c42a5-106">O cmdlet **Remove-AzVmssVMDataDisk** remove um disco de dados de um conjunto de escala VM da VM</span><span class="sxs-lookup"><span data-stu-id="c42a5-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="c42a5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c42a5-107">EXAMPLES</span></span>

### <span data-ttu-id="c42a5-108">Exemplo 1: remover um disco de dados de um conjunto de escala VM VM</span><span class="sxs-lookup"><span data-stu-id="c42a5-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="c42a5-109">O primeiro comando getsan VM existente Vmss fornecido pelo nome do grupo de recursos, o nome da Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="c42a5-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="c42a5-110">O segundo comando Remove o disco de dados LUN 0 do conjunto de dimensionamento VM armazenado no $VmssVM o comando final atualiza a VM Vmss com o disco de dados removidos.</span><span class="sxs-lookup"><span data-stu-id="c42a5-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="c42a5-111">OS</span><span class="sxs-lookup"><span data-stu-id="c42a5-111">PARAMETERS</span></span>

### <span data-ttu-id="c42a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c42a5-112">-DefaultProfile</span></span>
<span data-ttu-id="c42a5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c42a5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c42a5-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="c42a5-114">-Lun</span></span>
<span data-ttu-id="c42a5-115">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="c42a5-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="c42a5-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c42a5-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="c42a5-117">O perfil da máquina virtual do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c42a5-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="c42a5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c42a5-118">CommonParameters</span></span>
<span data-ttu-id="c42a5-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c42a5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c42a5-120">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c42a5-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c42a5-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c42a5-121">INPUTS</span></span>

### <span data-ttu-id="c42a5-122">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c42a5-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="c42a5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c42a5-123">OUTPUTS</span></span>

### <span data-ttu-id="c42a5-124">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="c42a5-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="c42a5-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c42a5-125">NOTES</span></span>

## <span data-ttu-id="c42a5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c42a5-126">RELATED LINKS</span></span>
