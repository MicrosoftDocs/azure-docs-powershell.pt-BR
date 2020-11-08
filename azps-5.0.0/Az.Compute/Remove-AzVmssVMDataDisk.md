---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115610"
---
# <span data-ttu-id="fef1a-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="fef1a-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="fef1a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fef1a-102">SYNOPSIS</span></span>
<span data-ttu-id="fef1a-103">Remove um disco de dados de uma VM do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="fef1a-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="fef1a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fef1a-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fef1a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fef1a-105">DESCRIPTION</span></span>
<span data-ttu-id="fef1a-106">O cmdlet **Remove-AzVmssVMDataDisk** remove um disco de dados de um conjunto de escala VM da VM</span><span class="sxs-lookup"><span data-stu-id="fef1a-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="fef1a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fef1a-107">EXAMPLES</span></span>

### <span data-ttu-id="fef1a-108">Exemplo 1: remover um disco de dados de um conjunto de escala VM VM</span><span class="sxs-lookup"><span data-stu-id="fef1a-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="fef1a-109">O primeiro comando getsan VM existente Vmss fornecido pelo nome do grupo de recursos, o nome da Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="fef1a-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="fef1a-110">O segundo comando Remove o disco de dados LUN 0 do conjunto de dimensionamento VM armazenado no $VmssVM o comando final atualiza a VM Vmss com o disco de dados removidos.</span><span class="sxs-lookup"><span data-stu-id="fef1a-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="fef1a-111">OS</span><span class="sxs-lookup"><span data-stu-id="fef1a-111">PARAMETERS</span></span>

### <span data-ttu-id="fef1a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef1a-112">-DefaultProfile</span></span>
<span data-ttu-id="fef1a-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fef1a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fef1a-114">-LUN</span><span class="sxs-lookup"><span data-stu-id="fef1a-114">-Lun</span></span>
<span data-ttu-id="fef1a-115">Especifica o número de unidade lógica do disco.</span><span class="sxs-lookup"><span data-stu-id="fef1a-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="fef1a-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fef1a-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="fef1a-117">O perfil da máquina virtual do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fef1a-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="fef1a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef1a-118">CommonParameters</span></span>
<span data-ttu-id="fef1a-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef1a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef1a-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fef1a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef1a-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fef1a-121">INPUTS</span></span>

### <span data-ttu-id="fef1a-122">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fef1a-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="fef1a-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fef1a-123">OUTPUTS</span></span>

### <span data-ttu-id="fef1a-124">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="fef1a-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="fef1a-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fef1a-125">NOTES</span></span>

## <span data-ttu-id="fef1a-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fef1a-126">RELATED LINKS</span></span>
