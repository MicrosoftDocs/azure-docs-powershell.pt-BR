---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 4eefa5a0a22b3db0e7ab10085729e1040dbd4e71
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955062"
---
# <span data-ttu-id="e6a0b-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="e6a0b-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="e6a0b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e6a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a0b-103">Cria um objeto de disco de dados local para uma máquina virtual ou uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="e6a0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6a0b-104">SYNTAX</span></span>

### <span data-ttu-id="e6a0b-105">NormalDiskParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e6a0b-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6a0b-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="e6a0b-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6a0b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e6a0b-107">DESCRIPTION</span></span>
<span data-ttu-id="e6a0b-108">O cmdlet **New-AzVMDataDisk** cria um objeto de disco de dados local para uma máquina virtual ou uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="e6a0b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e6a0b-109">EXAMPLES</span></span>

### <span data-ttu-id="e6a0b-110">Exemplo 1: adicionar um disco de dados gerenciado a uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="e6a0b-111">O primeiro comando obtém um disco gerenciado existente.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="e6a0b-112">O próximo comando cria um objeto de disco de dados com o disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="e6a0b-113">O próximo comando obtém uma VM Vmss existente fornecida pelo nome do grupo de recursos, o nome do Vmss e a ID da instância.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="e6a0b-114">O comando final atualiza a VM Vmss adicionando um novo disco de dados.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

### <span data-ttu-id="e6a0b-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e6a0b-115">Example 2</span></span>

<span data-ttu-id="e6a0b-116">Cria um objeto de disco de dados local para uma máquina virtual ou uma VM Vmss.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-116">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span> <span data-ttu-id="e6a0b-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="e6a0b-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzVMDataDisk -Caching None -CreateOption Attach -DiskSizeInGB 1 -Lun 2 -Name 'AgentPool01'
```

## <span data-ttu-id="e6a0b-118">OS</span><span class="sxs-lookup"><span data-stu-id="e6a0b-118">PARAMETERS</span></span>

### <span data-ttu-id="e6a0b-119">-Cache</span><span class="sxs-lookup"><span data-stu-id="e6a0b-119">-Caching</span></span>
<span data-ttu-id="e6a0b-120">O cache do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-120">The virtual machine data disk's caching.</span></span>

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

### <span data-ttu-id="e6a0b-121">-Createoption</span><span class="sxs-lookup"><span data-stu-id="e6a0b-121">-CreateOption</span></span>
<span data-ttu-id="e6a0b-122">A opção de criação do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-122">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a0b-123">-DefaultProfile</span></span>
<span data-ttu-id="e6a0b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6a0b-125">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="e6a0b-125">-DiskEncryptionSetId</span></span>
<span data-ttu-id="e6a0b-126">O ID do conjunto de criptografia de disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-126">The virtual machine managed disk encryption set's Id.</span></span>

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

### <span data-ttu-id="e6a0b-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="e6a0b-127">-DiskSizeInGB</span></span>
<span data-ttu-id="e6a0b-128">O tamanho do disco dos dados da máquina virtual em GB.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-128">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="e6a0b-129">-Lun</span></span>
<span data-ttu-id="e6a0b-130">O LUN do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-130">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="e6a0b-131">-ManagedDiskId</span></span>
<span data-ttu-id="e6a0b-132">A ID do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-132">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6a0b-133">-Name</span></span>
<span data-ttu-id="e6a0b-134">O nome do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-134">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="e6a0b-135">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="e6a0b-135">-SourceImageUri</span></span>
<span data-ttu-id="e6a0b-136">O URI da imagem de origem do disco do so da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-136">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e6a0b-137">-StorageAccountType</span></span>
<span data-ttu-id="e6a0b-138">O tipo de conta do disco gerenciado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-138">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-139">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="e6a0b-139">-VhdUri</span></span>
<span data-ttu-id="e6a0b-140">O URI do VHD do disco de dados da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-140">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-141">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e6a0b-141">-WriteAccelerator</span></span>
<span data-ttu-id="e6a0b-142">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-142">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a0b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a0b-143">CommonParameters</span></span>
<span data-ttu-id="e6a0b-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6a0b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a0b-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6a0b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a0b-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e6a0b-146">INPUTS</span></span>

### <span data-ttu-id="e6a0b-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e6a0b-147">System.Int32</span></span>

### <span data-ttu-id="e6a0b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e6a0b-148">System.String</span></span>

### <span data-ttu-id="e6a0b-149">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="e6a0b-149">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="e6a0b-150">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6a0b-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e6a0b-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e6a0b-151">OUTPUTS</span></span>

### <span data-ttu-id="e6a0b-152">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineDataDisk</span><span class="sxs-lookup"><span data-stu-id="e6a0b-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="e6a0b-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e6a0b-153">NOTES</span></span>

## <span data-ttu-id="e6a0b-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e6a0b-154">RELATED LINKS</span></span>
