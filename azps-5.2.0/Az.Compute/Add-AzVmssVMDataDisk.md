---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264059"
---
# <span data-ttu-id="51605-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="51605-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="51605-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51605-102">SYNOPSIS</span></span>
<span data-ttu-id="51605-103">Adiciona um disco de dados a uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="51605-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="51605-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51605-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51605-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51605-105">DESCRIPTION</span></span>
<span data-ttu-id="51605-106">O cmdlet **Add-AzVmssVMDataDisk** adiciona um disco de dados a uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="51605-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="51605-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51605-107">EXAMPLES</span></span>

### <span data-ttu-id="51605-108">Exemplo 1: adicionar um disco de dados gerenciado a uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="51605-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="51605-109">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="51605-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="51605-110">O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="51605-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="51605-111">O próximo comando adiciona o disco gerenciado à VM Vmss armazenada localmente em $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="51605-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="51605-112">O comando final atualiza a VM Vmss com o disco de dados adicionado.</span><span class="sxs-lookup"><span data-stu-id="51605-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="51605-113">OS</span><span class="sxs-lookup"><span data-stu-id="51605-113">PARAMETERS</span></span>

### <span data-ttu-id="51605-114">-Cache</span><span class="sxs-lookup"><span data-stu-id="51605-114">-Caching</span></span>
<span data-ttu-id="51605-115">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="51605-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="51605-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="51605-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51605-117">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="51605-117">ReadOnly</span></span>
- <span data-ttu-id="51605-118">Leitura</span><span class="sxs-lookup"><span data-stu-id="51605-118">ReadWrite</span></span>
- <span data-ttu-id="51605-119">None o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="51605-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="51605-120">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="51605-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="51605-121">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="51605-121">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51605-122">-Createoption</span><span class="sxs-lookup"><span data-stu-id="51605-122">-CreateOption</span></span>
<span data-ttu-id="51605-123">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="51605-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="51605-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="51605-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51605-125">Liga.</span><span class="sxs-lookup"><span data-stu-id="51605-125">Attach.</span></span>
<span data-ttu-id="51605-126">Especifique esta opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="51605-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="51605-127">Ao especificar essa opção, não especifique o parâmetro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="51605-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="51605-128">O *VhdUri* é tudo que é necessário para que a plataforma do Azure seja a localização do disco rígido virtual (VHD) a ser anexado como um disco de dados à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51605-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="51605-129">Vazia.</span><span class="sxs-lookup"><span data-stu-id="51605-129">Empty.</span></span>
<span data-ttu-id="51605-130">Especifique isso para criar um disco de dados vazio.</span><span class="sxs-lookup"><span data-stu-id="51605-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="51605-131">FromImage.</span><span class="sxs-lookup"><span data-stu-id="51605-131">FromImage.</span></span>
<span data-ttu-id="51605-132">Especifique esta opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.</span><span class="sxs-lookup"><span data-stu-id="51605-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="51605-133">Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para solicitar à plataforma Azure o local do VHD a ser anexado como um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="51605-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="51605-134">O parâmetro *VhdUri* é usado como a localização que identifica onde o VHD do disco de dados será armazenado quando for usado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51605-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51605-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51605-135">-DefaultProfile</span></span>
<span data-ttu-id="51605-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51605-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51605-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="51605-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="51605-138">Especifica a ID do recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="51605-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="51605-139">Só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="51605-139">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51605-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="51605-140">-DiskSizeInGB</span></span>
<span data-ttu-id="51605-141">Especifica o tamanho, em gigabytes, de um disco vazio para ser anexado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51605-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51605-142">-LUN</span><span class="sxs-lookup"><span data-stu-id="51605-142">-Lun</span></span>
<span data-ttu-id="51605-143">Especifica o número de unidade lógica (LUN) para um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="51605-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51605-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="51605-144">-ManagedDiskId</span></span>
<span data-ttu-id="51605-145">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="51605-145">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51605-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="51605-146">-StorageAccountType</span></span>
<span data-ttu-id="51605-147">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="51605-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="51605-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="51605-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="51605-149">Especifica o objeto VM do conjunto de escalas da máquina virtual local ao qual adicionar um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="51605-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="51605-150">Você pode usar o cmdlet **Get-AzVmssVM** para obter um objeto VM do conjunto de escalas da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="51605-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="51605-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="51605-151">-WriteAccelerator</span></span>
<span data-ttu-id="51605-152">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="51605-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="51605-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51605-153">CommonParameters</span></span>
<span data-ttu-id="51605-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51605-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51605-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51605-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51605-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51605-156">INPUTS</span></span>

### <span data-ttu-id="51605-157">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="51605-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="51605-158">System. Int32</span><span class="sxs-lookup"><span data-stu-id="51605-158">System.Int32</span></span>

### <span data-ttu-id="51605-159">System. String</span><span class="sxs-lookup"><span data-stu-id="51605-159">System.String</span></span>

### <span data-ttu-id="51605-160">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="51605-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="51605-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51605-161">OUTPUTS</span></span>

### <span data-ttu-id="51605-162">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="51605-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="51605-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51605-163">NOTES</span></span>

## <span data-ttu-id="51605-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51605-164">RELATED LINKS</span></span>
