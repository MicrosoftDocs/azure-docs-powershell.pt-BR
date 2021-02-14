---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115490"
---
# <span data-ttu-id="91eca-101">Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="91eca-101">Add-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="91eca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91eca-102">SYNOPSIS</span></span>
<span data-ttu-id="91eca-103">Adiciona um disco de dados a um VMSS.</span><span class="sxs-lookup"><span data-stu-id="91eca-103">Adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="91eca-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91eca-104">SYNTAX</span></span>

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91eca-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="91eca-105">DESCRIPTION</span></span>
<span data-ttu-id="91eca-106">O cmdlet **Add-AzVmsSVMDataDisk** adiciona um disco de dados a um VMSS.</span><span class="sxs-lookup"><span data-stu-id="91eca-106">The **Add-AzVmssVMDataDisk** cmdlet adds a data disk to a Vmss VM.</span></span>

## <span data-ttu-id="91eca-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91eca-107">EXAMPLES</span></span>

### <span data-ttu-id="91eca-108">Exemplo 1: Adicionar um disco de dados gerenciado a um VM VMSS.</span><span class="sxs-lookup"><span data-stu-id="91eca-108">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="91eca-109">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="91eca-109">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="91eca-110">O próximo comando obtém um VM Vmss existente dado pelo nome do grupo de recursos, pelo nome do vmss e pela ID da instância.</span><span class="sxs-lookup"><span data-stu-id="91eca-110">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="91eca-111">O próximo comando adiciona o disco gerenciado ao VM Vmss armazenado localmente no $VmssVM.</span><span class="sxs-lookup"><span data-stu-id="91eca-111">The next command adds the managed disk to the Vmss VM stored locally in $VmssVM.</span></span>
<span data-ttu-id="91eca-112">O comando final atualiza o VMSS com disco de dados adicionado.</span><span class="sxs-lookup"><span data-stu-id="91eca-112">The final command updates the Vmss VM with added data disk.</span></span>

## <span data-ttu-id="91eca-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91eca-113">PARAMETERS</span></span>

### <span data-ttu-id="91eca-114">-Cache</span><span class="sxs-lookup"><span data-stu-id="91eca-114">-Caching</span></span>
<span data-ttu-id="91eca-115">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="91eca-115">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="91eca-116">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="91eca-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91eca-117">Readonly</span><span class="sxs-lookup"><span data-stu-id="91eca-117">ReadOnly</span></span>
- <span data-ttu-id="91eca-118">Readwrite</span><span class="sxs-lookup"><span data-stu-id="91eca-118">ReadWrite</span></span>
- <span data-ttu-id="91eca-119">Nenhum O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="91eca-119">None The default value is ReadWrite.</span></span>
<span data-ttu-id="91eca-120">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="91eca-120">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="91eca-121">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="91eca-121">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="91eca-122">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="91eca-122">-CreateOption</span></span>
<span data-ttu-id="91eca-123">Especifica se esse cmdlet cria um disco no computador virtual a partir de uma plataforma ou imagem do usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="91eca-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="91eca-124">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="91eca-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91eca-125">Anexar.</span><span class="sxs-lookup"><span data-stu-id="91eca-125">Attach.</span></span>
<span data-ttu-id="91eca-126">Especifique essa opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="91eca-126">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="91eca-127">Quando você especificar essa opção, não especifique o parâmetro *SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="91eca-127">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="91eca-128">O *LtdadUri* é tudo o que é necessário para dizer à plataforma do Azure o local do disco rígido virtual (TEMD) a ser anexado como um disco de dados à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91eca-128">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="91eca-129">Vazio.</span><span class="sxs-lookup"><span data-stu-id="91eca-129">Empty.</span></span>
<span data-ttu-id="91eca-130">Especifique isso para criar um disco de dados vazio.</span><span class="sxs-lookup"><span data-stu-id="91eca-130">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="91eca-131">Fromimage.</span><span class="sxs-lookup"><span data-stu-id="91eca-131">FromImage.</span></span>
<span data-ttu-id="91eca-132">Especifique essa opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.</span><span class="sxs-lookup"><span data-stu-id="91eca-132">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="91eca-133">Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para dizer à plataforma do Azure o local da d'água para anexar como um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="91eca-133">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="91eca-134">O *parâmetro LtdadUri* é usado como o local que identifica onde o disco de dados SERÁ armazenado quando for usado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91eca-134">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="91eca-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91eca-135">-DefaultProfile</span></span>
<span data-ttu-id="91eca-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91eca-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91eca-137">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="91eca-137">-DiskEncryptionSetId</span></span>
<span data-ttu-id="91eca-138">Especifica a ID de recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="91eca-138">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="91eca-139">Isso só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="91eca-139">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="91eca-140">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="91eca-140">-DiskSizeInGB</span></span>
<span data-ttu-id="91eca-141">Especifica o tamanho, em gigabytes, de um disco vazio a ser anexado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91eca-141">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="91eca-142">-Ltda</span><span class="sxs-lookup"><span data-stu-id="91eca-142">-Lun</span></span>
<span data-ttu-id="91eca-143">Especifica o número de unidade lógica (NUMD) de um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="91eca-143">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="91eca-144">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="91eca-144">-ManagedDiskId</span></span>
<span data-ttu-id="91eca-145">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="91eca-145">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="91eca-146">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="91eca-146">-StorageAccountType</span></span>
<span data-ttu-id="91eca-147">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="91eca-147">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="91eca-148">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="91eca-148">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="91eca-149">Especifica o objeto VM definido em escala de máquina virtual local ao qual adicionar um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="91eca-149">Specifies the local virtual machine scale set VM object to which to add a data disk.</span></span>
<span data-ttu-id="91eca-150">Você pode usar o **cmdlet Get-AzVmsVM para** obter um objeto VM de conjunto de escala de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91eca-150">You can use the **Get-AzVmssVM** cmdlet to obtain a virtual machine scale set VM object.</span></span>

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

### <span data-ttu-id="91eca-151">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="91eca-151">-WriteAccelerator</span></span>
<span data-ttu-id="91eca-152">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="91eca-152">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="91eca-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91eca-153">CommonParameters</span></span>
<span data-ttu-id="91eca-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91eca-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91eca-155">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91eca-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91eca-156">Entradas</span><span class="sxs-lookup"><span data-stu-id="91eca-156">INPUTS</span></span>

### <span data-ttu-id="91eca-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="91eca-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

### <span data-ttu-id="91eca-158">System.Int32</span><span class="sxs-lookup"><span data-stu-id="91eca-158">System.Int32</span></span>

### <span data-ttu-id="91eca-159">System.String</span><span class="sxs-lookup"><span data-stu-id="91eca-159">System.String</span></span>

### <span data-ttu-id="91eca-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="91eca-160">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

## <span data-ttu-id="91eca-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="91eca-161">OUTPUTS</span></span>

### <span data-ttu-id="91eca-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="91eca-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="91eca-163">Notas</span><span class="sxs-lookup"><span data-stu-id="91eca-163">NOTES</span></span>

## <span data-ttu-id="91eca-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91eca-164">RELATED LINKS</span></span>
