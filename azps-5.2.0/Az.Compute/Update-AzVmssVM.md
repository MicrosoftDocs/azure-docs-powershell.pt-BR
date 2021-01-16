---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssVM.md
ms.openlocfilehash: e97c52e8bc22f1eff42a4ffade598fb28c2aff36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262745"
---
# <span data-ttu-id="07304-101">Update-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="07304-101">Update-AzVmssVM</span></span>

## <span data-ttu-id="07304-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07304-102">SYNOPSIS</span></span>
<span data-ttu-id="07304-103">Atualiza o estado de uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="07304-103">Updates the state of a Vmss VM.</span></span>

## <span data-ttu-id="07304-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07304-104">SYNTAX</span></span>

### <span data-ttu-id="07304-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="07304-105">DefaultParameter (Default)</span></span>
```
Update-AzVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07304-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="07304-106">ResourceIdParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07304-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="07304-107">ObjectParameter</span></span>
```
Update-AzVmssVM [-DataDisk <PSVirtualMachineDataDisk[]>] [-ProtectFromScaleIn <Boolean>]
 [-ProtectFromScaleSetAction <Boolean>] [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07304-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07304-108">DESCRIPTION</span></span>
<span data-ttu-id="07304-109">Atualiza o estado de uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="07304-109">Updates the state of a Vmss VM.</span></span>  <span data-ttu-id="07304-110">Por enquanto, a única atualização permitida está adicionando um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="07304-110">For now, the only allowed update is adding a managed data disk.</span></span>

## <span data-ttu-id="07304-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07304-111">EXAMPLES</span></span>

### <span data-ttu-id="07304-112">Exemplo 1: adicionar um disco de dados gerenciado a uma VM do Vmss usando New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="07304-112">Example 1: Add a managed data disk to a Vmss VM using New-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="07304-113">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="07304-113">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="07304-114">O próximo comando cria um objeto de disco de dados com o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="07304-114">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="07304-115">O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="07304-115">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="07304-116">O comando final atualiza a VM Vmss adicionando um novo disco de dados.</span><span class="sxs-lookup"><span data-stu-id="07304-116">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="07304-117">Exemplo 2: adicionar um disco de dados gerenciado a uma VM do Vmss usando Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="07304-117">Example 2: Add a managed data disk to a Vmss VM using Add-AzVMDataDisk</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="07304-118">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="07304-118">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="07304-119">O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="07304-119">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="07304-120">O próximo comando adiciona o disco gerenciado à VM Vmss armazenada localmente em $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="07304-120">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="07304-121">O comando final atualiza a VM Vmss com o disco de dados adicionado.</span><span class="sxs-lookup"><span data-stu-id="07304-121">The final command updates the Vmss VM with added data disk.</span></span>

### <span data-ttu-id="07304-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="07304-122">Example 3</span></span>

<span data-ttu-id="07304-123">Atualiza o estado de uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="07304-123">Updates the state of a Vmss VM.</span></span> <span data-ttu-id="07304-124">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="07304-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzVmssVM -InstanceId 0 -ProtectFromScaleIn $false -ProtectFromScaleSetAction $false -ResourceGroupName 'myrg' -VMScaleSetName 'myvmss'
```

## <span data-ttu-id="07304-125">OS</span><span class="sxs-lookup"><span data-stu-id="07304-125">PARAMETERS</span></span>

### <span data-ttu-id="07304-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07304-126">-AsJob</span></span>
<span data-ttu-id="07304-127">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="07304-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07304-128">-Datadisk</span><span class="sxs-lookup"><span data-stu-id="07304-128">-DataDisk</span></span>

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

### <span data-ttu-id="07304-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07304-129">-DefaultProfile</span></span>
<span data-ttu-id="07304-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07304-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07304-131">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="07304-131">-InstanceId</span></span>
<span data-ttu-id="07304-132">Especifica a ID de instância de uma VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="07304-132">Specifies the instance ID of a VMSS VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07304-133">-ProtectFromScaleIn</span><span class="sxs-lookup"><span data-stu-id="07304-133">-ProtectFromScaleIn</span></span>
<span data-ttu-id="07304-134">Indica que o conjunto de dimensionamento de escala da máquina virtual não deve ser considerado para exclusão durante uma operação de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="07304-134">Indicates that the virtual machine scale set VM shouldn't be considered for deletion during a scale-in operation.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-135">-ProtectFromScaleSetAction</span><span class="sxs-lookup"><span data-stu-id="07304-135">-ProtectFromScaleSetAction</span></span>
<span data-ttu-id="07304-136">Indica que as atualizações de modelo ou as ações (incluindo a escala de escala) iniciadas no VMSS não devem ser aplicadas à VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="07304-136">Indicates that model updates or actions (including scale-in) initiated on the VMSS should not be applied to the VMSS VM.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07304-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07304-137">-ResourceGroupName</span></span>
<span data-ttu-id="07304-138">Especifica o nome do grupo de recursos do VMSS.</span><span class="sxs-lookup"><span data-stu-id="07304-138">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07304-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07304-139">-ResourceId</span></span>
<span data-ttu-id="07304-140">A ID do recurso para a VM do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="07304-140">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="07304-141">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="07304-141">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="07304-142">Objeto VM do conjunto de escala da máquina virtual local</span><span class="sxs-lookup"><span data-stu-id="07304-142">Local virtual machine scale set VM object</span></span>

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

### <span data-ttu-id="07304-143">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="07304-143">-VMScaleSetName</span></span>
<span data-ttu-id="07304-144">O nome do conjunto de escala da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="07304-144">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07304-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07304-145">-Confirm</span></span>
<span data-ttu-id="07304-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07304-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07304-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07304-147">-WhatIf</span></span>
<span data-ttu-id="07304-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07304-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07304-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07304-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07304-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07304-150">CommonParameters</span></span>
<span data-ttu-id="07304-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07304-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07304-152">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07304-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07304-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07304-153">INPUTS</span></span>

### <span data-ttu-id="07304-154">System. String</span><span class="sxs-lookup"><span data-stu-id="07304-154">System.String</span></span>

### <span data-ttu-id="07304-155">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk []</span><span class="sxs-lookup"><span data-stu-id="07304-155">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk[]</span></span>

### <span data-ttu-id="07304-156">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="07304-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="07304-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07304-157">OUTPUTS</span></span>

### <span data-ttu-id="07304-158">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="07304-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="07304-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07304-159">NOTES</span></span>

## <span data-ttu-id="07304-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07304-160">RELATED LINKS</span></span>
