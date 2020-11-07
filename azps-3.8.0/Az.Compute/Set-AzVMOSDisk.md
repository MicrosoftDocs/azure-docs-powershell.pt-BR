---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944625"
---
# <span data-ttu-id="52a77-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="52a77-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="52a77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52a77-102">SYNOPSIS</span></span>
<span data-ttu-id="52a77-103">Define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52a77-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="52a77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52a77-104">SYNTAX</span></span>

### <span data-ttu-id="52a77-105">Defaultparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="52a77-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a77-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="52a77-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a77-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a77-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a77-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="52a77-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52a77-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="52a77-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a77-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52a77-110">DESCRIPTION</span></span>
<span data-ttu-id="52a77-111">O cmdlet **set-AzVMOSDisk** define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52a77-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="52a77-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52a77-112">EXAMPLES</span></span>

### <span data-ttu-id="52a77-113">Exemplo 1: definir propriedades em uma máquina virtual a partir da imagem da plataforma</span><span class="sxs-lookup"><span data-stu-id="52a77-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="52a77-114">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet13 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="52a77-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="52a77-115">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="52a77-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="52a77-116">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52a77-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="52a77-117">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="52a77-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="52a77-118">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="52a77-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="52a77-119">Exemplo 2: define propriedades em uma máquina virtual a partir de uma imagem generalizada do usuário</span><span class="sxs-lookup"><span data-stu-id="52a77-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="52a77-120">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="52a77-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="52a77-121">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="52a77-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="52a77-122">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52a77-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="52a77-123">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="52a77-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="52a77-124">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="52a77-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="52a77-125">Exemplo 3: define propriedades em uma máquina virtual a partir de uma imagem de usuário especializada</span><span class="sxs-lookup"><span data-stu-id="52a77-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="52a77-126">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="52a77-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="52a77-127">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="52a77-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="52a77-128">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52a77-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="52a77-129">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="52a77-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="52a77-130">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="52a77-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="52a77-131">Exemplo 4: definir as configurações de criptografia de disco em um disco do sistema operacional da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="52a77-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="52a77-132">Este exemplo define as configurações de criptografia de disco em um disco do sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52a77-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="52a77-133">OS</span><span class="sxs-lookup"><span data-stu-id="52a77-133">PARAMETERS</span></span>

### <span data-ttu-id="52a77-134">-Cache</span><span class="sxs-lookup"><span data-stu-id="52a77-134">-Caching</span></span>
<span data-ttu-id="52a77-135">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52a77-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="52a77-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="52a77-136">Valid values are:</span></span> 
- <span data-ttu-id="52a77-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="52a77-137">ReadOnly</span></span>
- <span data-ttu-id="52a77-138">ReadWrite o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="52a77-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="52a77-139">Alterar o valor de cache faz com que a máquina virtual reinicie.</span><span class="sxs-lookup"><span data-stu-id="52a77-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="52a77-140">Essa configuração afeta o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="52a77-140">This setting affects the performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-141">-Createoption</span><span class="sxs-lookup"><span data-stu-id="52a77-141">-CreateOption</span></span>
<span data-ttu-id="52a77-142">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="52a77-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="52a77-143">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="52a77-143">Valid values are:</span></span> 
- <span data-ttu-id="52a77-144">Liga.</span><span class="sxs-lookup"><span data-stu-id="52a77-144">Attach.</span></span>
<span data-ttu-id="52a77-145">Especifique esta opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="52a77-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="52a77-146">Ao especificar essa opção, não especifique o parâmetro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="52a77-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="52a77-147">Em vez disso, use o cmdlet Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="52a77-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="52a77-148">Você também deve usar os parâmetros de usar os *Windows* ou *Linux* para diferenciar a plataforma do Azure o tipo de sistema operacional no VHD.</span><span class="sxs-lookup"><span data-stu-id="52a77-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="52a77-149">O parâmetro *VhdUri* é suficiente para solicitar à plataforma do Azure o local do disco a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="52a77-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="52a77-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="52a77-150">FromImage.</span></span>
<span data-ttu-id="52a77-151">Especifique esta opção para criar uma máquina virtual a partir de uma imagem de plataforma ou uma imagem de usuário generalizada.</span><span class="sxs-lookup"><span data-stu-id="52a77-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="52a77-152">No caso de uma imagem de usuário generalizada, você também precisa especificar o parâmetro *SourceImageUri* e os parâmetros do *Windows* ou *Linux* para dizer à plataforma do Azure o local e o tipo do VHD do disco do sistema operacional, em vez de usar o cmdlet **set-AzVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="52a77-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="52a77-153">No caso de uma imagem de plataforma, o parâmetro *VhdUri* é suficiente.</span><span class="sxs-lookup"><span data-stu-id="52a77-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="52a77-154">Vazia.</span><span class="sxs-lookup"><span data-stu-id="52a77-154">Empty.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a77-155">-DefaultProfile</span></span>
<span data-ttu-id="52a77-156">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="52a77-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a77-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="52a77-157">-DiffDiskSetting</span></span>
<span data-ttu-id="52a77-158">Especifica as configurações de disco diferencial para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52a77-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="52a77-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="52a77-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="52a77-160">Especifica o local da chave de criptografia do disco.</span><span class="sxs-lookup"><span data-stu-id="52a77-160">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="52a77-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="52a77-162">Especifica a ID do recurso do cofre de chaves que contém a chave de criptografia do disco.</span><span class="sxs-lookup"><span data-stu-id="52a77-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="52a77-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="52a77-164">Especifica a ID do recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="52a77-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="52a77-165">Só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="52a77-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="52a77-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="52a77-166">-DiskSizeInGB</span></span>
<span data-ttu-id="52a77-167">Especifica o tamanho, em GB, do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52a77-167">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="52a77-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="52a77-169">Especifica o local da chave de criptografia da chave.</span><span class="sxs-lookup"><span data-stu-id="52a77-169">Specifies the location of the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="52a77-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="52a77-171">Especifica a ID do recurso do cofre de chaves que contém a chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="52a77-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="52a77-172">-Linux</span></span>
<span data-ttu-id="52a77-173">Indica que o sistema operacional na imagem do usuário é o Linux.</span><span class="sxs-lookup"><span data-stu-id="52a77-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="52a77-174">Especifique esse parâmetro para a implantação da máquina virtual baseada em imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="52a77-174">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="52a77-175">-ManagedDiskId</span></span>
<span data-ttu-id="52a77-176">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="52a77-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="52a77-177">-Nome</span><span class="sxs-lookup"><span data-stu-id="52a77-177">-Name</span></span>
<span data-ttu-id="52a77-178">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52a77-178">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="52a77-179">-SourceImageUri</span></span>
<span data-ttu-id="52a77-180">Especifica o URI do VHD para cenários de imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="52a77-180">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="52a77-181">-StorageAccountType</span></span>
<span data-ttu-id="52a77-182">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="52a77-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="52a77-183">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="52a77-183">-VhdUri</span></span>
<span data-ttu-id="52a77-184">Especifica o URI (Uniform Resource Identifier) de um VHD (disco rígido virtual).</span><span class="sxs-lookup"><span data-stu-id="52a77-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="52a77-185">Para uma máquina virtual baseada em imagem, esse parâmetro especifica o arquivo VHD a ser criado quando uma imagem de plataforma ou de usuário é especificada.</span><span class="sxs-lookup"><span data-stu-id="52a77-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="52a77-186">Esse é o local de onde o objeto binário grande (BLOB) da imagem é copiado para iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="52a77-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="52a77-187">Para um cenário de inicialização de máquina virtual baseado em disco, esse parâmetro especifica o arquivo VHD que a máquina virtual usa diretamente para começar.</span><span class="sxs-lookup"><span data-stu-id="52a77-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-188">-VM</span><span class="sxs-lookup"><span data-stu-id="52a77-188">-VM</span></span>
<span data-ttu-id="52a77-189">Especifica o objeto da máquina virtual local no qual definir propriedades de disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52a77-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="52a77-190">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="52a77-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="52a77-191">-Windows</span></span>
<span data-ttu-id="52a77-192">Indica que o sistema operacional na imagem do usuário é o Windows.</span><span class="sxs-lookup"><span data-stu-id="52a77-192">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52a77-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="52a77-193">-WriteAccelerator</span></span>
<span data-ttu-id="52a77-194">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="52a77-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="52a77-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a77-195">CommonParameters</span></span>
<span data-ttu-id="52a77-196">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a77-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a77-197">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52a77-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a77-198">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52a77-198">INPUTS</span></span>

### <span data-ttu-id="52a77-199">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="52a77-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="52a77-200">System. String</span><span class="sxs-lookup"><span data-stu-id="52a77-200">System.String</span></span>

## <span data-ttu-id="52a77-201">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52a77-201">OUTPUTS</span></span>

### <span data-ttu-id="52a77-202">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="52a77-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="52a77-203">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52a77-203">NOTES</span></span>

## <span data-ttu-id="52a77-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52a77-204">RELATED LINKS</span></span>

[<span data-ttu-id="52a77-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="52a77-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="52a77-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="52a77-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="52a77-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="52a77-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


