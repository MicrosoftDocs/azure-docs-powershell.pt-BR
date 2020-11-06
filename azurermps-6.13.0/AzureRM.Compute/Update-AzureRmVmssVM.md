---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmssVM.md
ms.openlocfilehash: 3003387b0d989d01231e7be549727ebc88158723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610098"
---
# <span data-ttu-id="1ed3d-101">Update-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="1ed3d-101">Update-AzureRmVmssVM</span></span>

## <span data-ttu-id="1ed3d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ed3d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed3d-103">Atualiza o estado de uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-103">Updates the state of a Vmss VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ed3d-104">SYNTAX</span></span>

### <span data-ttu-id="1ed3d-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ed3d-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ed3d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1ed3d-106">ResourceIdParameter</span></span>
```
Update-AzureRmVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ed3d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1ed3d-107">ObjectParameter</span></span>
```
Update-AzureRmVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ed3d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ed3d-108">DESCRIPTION</span></span>
<span data-ttu-id="1ed3d-109">Atualiza o estado de uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="1ed3d-110">Por enquanto, a única atualização permitida está adicionando um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="1ed3d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ed3d-111">EXAMPLES</span></span>

### <span data-ttu-id="1ed3d-112">Exemplo 1: adicionar um disco de dados gerenciado a uma VM do Vmss usando New-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1ed3d-112">Example 1: Add a managed data disk to a Vmss VM using New-AzureRmVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzureRmVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="1ed3d-113">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="1ed3d-114">O próximo comando cria um objeto de disco de dados com o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="1ed3d-115">O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="1ed3d-116">O comando final atualiza a VM Vmss adicionando um novo disco de dados.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="1ed3d-117">Exemplo 2: adicionar um disco de dados gerenciado a uma VM do Vmss usando Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1ed3d-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzureRmVMDataDisk</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzureRmVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzureRmVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzureRmVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="1ed3d-118">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="1ed3d-119">O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="1ed3d-120">O próximo comando adiciona o disco gerenciado à VM Vmss armazenada localmente em $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="1ed3d-121">O comando final atualiza a VM Vmss com o disco de dados adicionado.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-121">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="1ed3d-122">OS</span><span class="sxs-lookup"><span data-stu-id="1ed3d-122">PARAMETERS</span></span>

### <span data-ttu-id="1ed3d-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ed3d-123">-AsJob</span></span>
<span data-ttu-id="1ed3d-124">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1ed3d-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ed3d-125">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="1ed3d-125">-DataDisk</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ed3d-126">-DefaultProfile</span></span>
<span data-ttu-id="1ed3d-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3d-128">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1ed3d-128">-InstanceId</span></span>
<span data-ttu-id="1ed3d-129">Especifica a ID de instância de uma VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-129">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ed3d-130">-ResourceGroupName</span></span>
<span data-ttu-id="1ed3d-131">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ed3d-132">-ResourceId</span></span>
<span data-ttu-id="1ed3d-133">A ID do recurso para a VM do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="1ed3d-133">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="1ed3d-134">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1ed3d-134">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="1ed3d-135">Objeto VM do conjunto de escala da máquina virtual local</span><span class="sxs-lookup"><span data-stu-id="1ed3d-135">Local virtual machine scale set VM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3d-136">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1ed3d-136">-VMScaleSetName</span></span>
<span data-ttu-id="1ed3d-137">O nome do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="1ed3d-137">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ed3d-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ed3d-138">-Confirm</span></span>
<span data-ttu-id="1ed3d-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ed3d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ed3d-140">-WhatIf</span></span>
<span data-ttu-id="1ed3d-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ed3d-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ed3d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed3d-143">CommonParameters</span></span>
<span data-ttu-id="1ed3d-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ed3d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed3d-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed3d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed3d-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ed3d-146">INPUTS</span></span>

### <span data-ttu-id="1ed3d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="1ed3d-147">System.String</span></span>

### <span data-ttu-id="1ed3d-148">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="1ed3d-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>
<span data-ttu-id="1ed3d-149">Parâmetros: datadisk (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ed3d-149">Parameters: DataDisk (ByValue)</span></span>

### <span data-ttu-id="1ed3d-150">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1ed3d-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>
<span data-ttu-id="1ed3d-151">Parâmetros: VirtualMachineScaleSetVM (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1ed3d-151">Parameters: VirtualMachineScaleSetVM (ByValue)</span></span>

## <span data-ttu-id="1ed3d-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ed3d-152">OUTPUTS</span></span>

### <span data-ttu-id="1ed3d-153">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="1ed3d-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="1ed3d-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ed3d-154">NOTES</span></span>

## <span data-ttu-id="1ed3d-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ed3d-155">RELATED LINKS</span></span>
