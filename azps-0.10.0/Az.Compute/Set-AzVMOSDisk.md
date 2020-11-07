---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 378d0d33d6cc1ceb2eca4773d93f76afbf75cf4b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776826"
---
# <span data-ttu-id="dd392-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="dd392-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="dd392-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd392-102">SYNOPSIS</span></span>
<span data-ttu-id="dd392-103">Define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd392-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="dd392-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd392-104">SYNTAX</span></span>

### <span data-ttu-id="dd392-105">Defaultparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="dd392-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd392-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="dd392-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd392-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd392-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dd392-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="dd392-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd392-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd392-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd392-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd392-110">DESCRIPTION</span></span>
<span data-ttu-id="dd392-111">O cmdlet **set-AzVMOSDisk** define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd392-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="dd392-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd392-112">EXAMPLES</span></span>

### <span data-ttu-id="dd392-113">Exemplo 1: definir propriedades em uma máquina virtual a partir da imagem da plataforma</span><span class="sxs-lookup"><span data-stu-id="dd392-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="dd392-114">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet13 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dd392-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="dd392-115">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dd392-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dd392-116">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd392-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="dd392-117">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dd392-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="dd392-118">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dd392-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="dd392-119">Exemplo 2: define propriedades em uma máquina virtual a partir de uma imagem generalizada do usuário</span><span class="sxs-lookup"><span data-stu-id="dd392-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="dd392-120">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dd392-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="dd392-121">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dd392-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dd392-122">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd392-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="dd392-123">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dd392-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="dd392-124">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dd392-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="dd392-125">Exemplo 3: define propriedades em uma máquina virtual a partir de uma imagem de usuário especializada</span><span class="sxs-lookup"><span data-stu-id="dd392-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="dd392-126">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dd392-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="dd392-127">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dd392-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="dd392-128">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd392-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="dd392-129">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="dd392-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="dd392-130">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="dd392-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="dd392-131">Exemplo 4: definir as configurações de criptografia de disco em um disco do sistema operacional da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="dd392-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="dd392-132">Este exemplo define as configurações de criptografia de disco em um disco do sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd392-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="dd392-133">OS</span><span class="sxs-lookup"><span data-stu-id="dd392-133">PARAMETERS</span></span>

### <span data-ttu-id="dd392-134">-Cache</span><span class="sxs-lookup"><span data-stu-id="dd392-134">-Caching</span></span>
<span data-ttu-id="dd392-135">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dd392-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="dd392-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dd392-136">Valid values are:</span></span> 

- <span data-ttu-id="dd392-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="dd392-137">ReadOnly</span></span>
- <span data-ttu-id="dd392-138">Leitura</span><span class="sxs-lookup"><span data-stu-id="dd392-138">ReadWrite</span></span>

<span data-ttu-id="dd392-139">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="dd392-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="dd392-140">Alterar o valor de cache faz com que a máquina virtual reinicie.</span><span class="sxs-lookup"><span data-stu-id="dd392-140">Changing the caching value causes the virtual machine to restart.</span></span>

<span data-ttu-id="dd392-141">Essa configuração afeta o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="dd392-141">This setting affects the performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-142">-Createoption</span><span class="sxs-lookup"><span data-stu-id="dd392-142">-CreateOption</span></span>
<span data-ttu-id="dd392-143">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="dd392-143">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="dd392-144">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="dd392-144">Valid values are:</span></span> 

- <span data-ttu-id="dd392-145">Liga.</span><span class="sxs-lookup"><span data-stu-id="dd392-145">Attach.</span></span>
<span data-ttu-id="dd392-146">Especifique esta opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="dd392-146">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="dd392-147">Ao especificar essa opção, não especifique o parâmetro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="dd392-147">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="dd392-148">Em vez disso, use o cmdlet Set-AzVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="dd392-148">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="dd392-149">Você também deve usar os parâmetros de usar os *Windows* ou *Linux* para diferenciar a plataforma azure2 o tipo de sistema operacional no VHD.</span><span class="sxs-lookup"><span data-stu-id="dd392-149">You must also use the use the *Windows* or *Linux* parameters to tell the azure2 platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="dd392-150">O parâmetro *VhdUri* é suficiente para fornecer à plataforma azure2 o local do disco a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="dd392-150">The *VhdUri* parameter is enough to tell the azure2 platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="dd392-151">FromImage.</span><span class="sxs-lookup"><span data-stu-id="dd392-151">FromImage.</span></span>
<span data-ttu-id="dd392-152">Especifique esta opção para criar uma máquina virtual a partir de uma imagem de plataforma ou uma imagem de usuário generalizada.</span><span class="sxs-lookup"><span data-stu-id="dd392-152">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="dd392-153">No caso de uma imagem de usuário generalizada, você também precisa especificar o parâmetro *SourceImageUri* e os parâmetros do *Windows* ou *Linux* para dizer à plataforma do Azure o local e o tipo do VHD do disco do sistema operacional, em vez de usar o cmdlet **set-AzVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="dd392-153">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="dd392-154">No caso de uma imagem de plataforma, o parâmetro *VhdUri* é suficiente.</span><span class="sxs-lookup"><span data-stu-id="dd392-154">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="dd392-155">Vazia.</span><span class="sxs-lookup"><span data-stu-id="dd392-155">Empty.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd392-156">-DefaultProfile</span></span>
<span data-ttu-id="dd392-157">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd392-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-158">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="dd392-158">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="dd392-159">Especifica o local da chave de criptografia do disco.</span><span class="sxs-lookup"><span data-stu-id="dd392-159">Specifies the location of the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-160">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="dd392-160">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="dd392-161">Especifica a ID do recurso do cofre de chaves que contém a chave de criptografia do disco.</span><span class="sxs-lookup"><span data-stu-id="dd392-161">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="dd392-162">-DiskSizeInGB</span></span>
<span data-ttu-id="dd392-163">Especifica o tamanho, em GB, do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dd392-163">Specifies the size, in GB, of the operating system disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-164">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="dd392-164">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="dd392-165">Especifica o local da chave de criptografia da chave.</span><span class="sxs-lookup"><span data-stu-id="dd392-165">Specifies the location of the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-166">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="dd392-166">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="dd392-167">Especifica a ID do recurso do cofre de chaves que contém a chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="dd392-167">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="dd392-168">-Linux</span></span>
<span data-ttu-id="dd392-169">Indica que o sistema operacional na imagem do usuário é o Linux.</span><span class="sxs-lookup"><span data-stu-id="dd392-169">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="dd392-170">Especifique esse parâmetro para a implantação da máquina virtual baseada em imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd392-170">Specify this parameter for user image based virtual machine deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-171">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="dd392-171">-ManagedDiskId</span></span>
<span data-ttu-id="dd392-172">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dd392-172">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-173">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd392-173">-Name</span></span>
<span data-ttu-id="dd392-174">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dd392-174">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-175">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="dd392-175">-SourceImageUri</span></span>
<span data-ttu-id="dd392-176">Especifica o URI do VHD para cenários de imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd392-176">Specifies the URI of the VHD for user image scenarios.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dd392-177">-StorageAccountType</span></span>
<span data-ttu-id="dd392-178">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="dd392-178">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-179">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="dd392-179">-VhdUri</span></span>
<span data-ttu-id="dd392-180">Especifica o URI (Uniform Resource Identifier) de um VHD (disco rígido virtual).</span><span class="sxs-lookup"><span data-stu-id="dd392-180">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>

<span data-ttu-id="dd392-181">Para uma máquina virtual baseada em imagem, esse parâmetro especifica o arquivo VHD a ser criado quando uma imagem de plataforma ou de usuário é especificada.</span><span class="sxs-lookup"><span data-stu-id="dd392-181">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="dd392-182">Esse é o local de onde o objeto binário grande (BLOB) da imagem é copiado para iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="dd392-182">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>

<span data-ttu-id="dd392-183">Para um cenário de inicialização de máquina virtual baseado em disco, esse parâmetro especifica o arquivo VHD que a máquina virtual usa diretamente para começar.</span><span class="sxs-lookup"><span data-stu-id="dd392-183">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-184">-VM</span><span class="sxs-lookup"><span data-stu-id="dd392-184">-VM</span></span>
<span data-ttu-id="dd392-185">Especifica o objeto da máquina virtual local no qual definir propriedades de disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dd392-185">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="dd392-186">Para obter um objeto de máquina virtual, use o cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="dd392-186">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-187">-Windows</span><span class="sxs-lookup"><span data-stu-id="dd392-187">-Windows</span></span>
<span data-ttu-id="dd392-188">Indica que o sistema operacional na imagem do usuário é o Windows.</span><span class="sxs-lookup"><span data-stu-id="dd392-188">Indicates that the operating system on the user image is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-189">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dd392-189">-WriteAccelerator</span></span>
<span data-ttu-id="dd392-190">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dd392-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd392-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd392-191">CommonParameters</span></span>
<span data-ttu-id="dd392-192">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd392-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd392-193">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd392-193">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd392-194">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd392-194">INPUTS</span></span>

### <span data-ttu-id="dd392-195">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dd392-195">PSVirtualMachine</span></span>
<span data-ttu-id="dd392-196">O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="dd392-196">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="dd392-197">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd392-197">OUTPUTS</span></span>

### <span data-ttu-id="dd392-198">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dd392-198">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dd392-199">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd392-199">NOTES</span></span>

## <span data-ttu-id="dd392-200">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd392-200">RELATED LINKS</span></span>

[<span data-ttu-id="dd392-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="dd392-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="dd392-202">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="dd392-202">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="dd392-203">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="dd392-203">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


