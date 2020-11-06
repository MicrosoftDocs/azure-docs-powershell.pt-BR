---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOSDisk.md
ms.openlocfilehash: 89a45e785252d1351e41e895cc610a75cbf6c5fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430350"
---
# <span data-ttu-id="66023-101">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="66023-101">Set-AzureRmVMOSDisk</span></span>

## <span data-ttu-id="66023-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66023-102">SYNOPSIS</span></span>
<span data-ttu-id="66023-103">Define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66023-103">Sets the operating system disk properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66023-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="66023-104">SYNTAX</span></span>

### <span data-ttu-id="66023-105">Defaultparamset (padrão)</span><span class="sxs-lookup"><span data-stu-id="66023-105">DefaultParamSet (Default)</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66023-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="66023-106">WindowsParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66023-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="66023-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66023-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="66023-108">LinuxParamSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66023-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="66023-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzureRmVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66023-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="66023-110">DESCRIPTION</span></span>
<span data-ttu-id="66023-111">O cmdlet **set-AzureRmVMOSDisk** define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66023-111">The **Set-AzureRmVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="66023-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66023-112">EXAMPLES</span></span>

### <span data-ttu-id="66023-113">Exemplo 1: definir propriedades em uma máquina virtual a partir da imagem da plataforma</span><span class="sxs-lookup"><span data-stu-id="66023-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="66023-114">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet13 no grupo de recursos chamado ResourceGroup11 e, em seguida, armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="66023-114">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="66023-115">O segundo comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="66023-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="66023-116">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66023-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="66023-117">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="66023-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="66023-118">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="66023-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="66023-119">Exemplo 2: define propriedades em uma máquina virtual a partir de uma imagem generalizada do usuário</span><span class="sxs-lookup"><span data-stu-id="66023-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="66023-120">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="66023-120">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="66023-121">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="66023-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="66023-122">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66023-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="66023-123">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="66023-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="66023-124">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="66023-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="66023-125">Exemplo 3: define propriedades em uma máquina virtual a partir de uma imagem de usuário especializada</span><span class="sxs-lookup"><span data-stu-id="66023-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="66023-126">O primeiro comando obtém o conjunto de disponibilidade chamado AvailablitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="66023-126">The first command gets the availability set named AvailablitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="66023-127">O segundo comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="66023-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="66023-128">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66023-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="66023-129">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="66023-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="66023-130">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="66023-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="66023-131">Exemplo 4: definir as configurações de criptografia de disco em um disco do sistema operacional da máquina virtual</span><span class="sxs-lookup"><span data-stu-id="66023-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzureRmVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="66023-132">Este exemplo define as configurações de criptografia de disco em um disco do sistema operacional da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66023-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="66023-133">OS</span><span class="sxs-lookup"><span data-stu-id="66023-133">PARAMETERS</span></span>

### <span data-ttu-id="66023-134">-Cache</span><span class="sxs-lookup"><span data-stu-id="66023-134">-Caching</span></span>
<span data-ttu-id="66023-135">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="66023-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="66023-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="66023-136">Valid values are:</span></span> 
- <span data-ttu-id="66023-137">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="66023-137">ReadOnly</span></span>
- <span data-ttu-id="66023-138">ReadWrite o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="66023-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="66023-139">Alterar o valor de cache faz com que a máquina virtual reinicie.</span><span class="sxs-lookup"><span data-stu-id="66023-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="66023-140">Essa configuração afeta o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="66023-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="66023-141">-Createoption</span><span class="sxs-lookup"><span data-stu-id="66023-141">-CreateOption</span></span>
<span data-ttu-id="66023-142">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="66023-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="66023-143">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="66023-143">Valid values are:</span></span> 
- <span data-ttu-id="66023-144">Liga.</span><span class="sxs-lookup"><span data-stu-id="66023-144">Attach.</span></span>
<span data-ttu-id="66023-145">Especifique esta opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="66023-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="66023-146">Ao especificar essa opção, não especifique o parâmetro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="66023-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="66023-147">Em vez disso, use o cmdlet Set-AzureRmVMSourceImage.</span><span class="sxs-lookup"><span data-stu-id="66023-147">Instead, use the Set-AzureRmVMSourceImage cmdlet.</span></span>
<span data-ttu-id="66023-148">Você também deve usar os parâmetros de usar os *Windows* ou *Linux* para diferenciar a plataforma do Azure o tipo de sistema operacional no VHD.</span><span class="sxs-lookup"><span data-stu-id="66023-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="66023-149">O parâmetro *VhdUri* é suficiente para solicitar à plataforma do Azure o local do disco a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="66023-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="66023-150">FromImage.</span><span class="sxs-lookup"><span data-stu-id="66023-150">FromImage.</span></span>
<span data-ttu-id="66023-151">Especifique esta opção para criar uma máquina virtual a partir de uma imagem de plataforma ou uma imagem de usuário generalizada.</span><span class="sxs-lookup"><span data-stu-id="66023-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="66023-152">No caso de uma imagem de usuário generalizada, você também precisa especificar o parâmetro *SourceImageUri* e os parâmetros do *Windows* ou *Linux* para dizer à plataforma do Azure o local e o tipo do VHD do disco do sistema operacional, em vez de usar o cmdlet **set-AzureRmVMSourceImage** .</span><span class="sxs-lookup"><span data-stu-id="66023-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzureRmVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="66023-153">No caso de uma imagem de plataforma, o parâmetro *VhdUri* é suficiente.</span><span class="sxs-lookup"><span data-stu-id="66023-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="66023-154">Vazia.</span><span class="sxs-lookup"><span data-stu-id="66023-154">Empty.</span></span>

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

### <span data-ttu-id="66023-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66023-155">-DefaultProfile</span></span>
<span data-ttu-id="66023-156">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="66023-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66023-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="66023-157">-DiffDiskSetting</span></span>
<span data-ttu-id="66023-158">Especifica as configurações de disco diferencial para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="66023-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="66023-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="66023-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="66023-160">Especifica o local da chave de criptografia do disco.</span><span class="sxs-lookup"><span data-stu-id="66023-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="66023-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="66023-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="66023-162">Especifica a ID do recurso do cofre de chaves que contém a chave de criptografia do disco.</span><span class="sxs-lookup"><span data-stu-id="66023-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="66023-163">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="66023-163">-DiskSizeInGB</span></span>
<span data-ttu-id="66023-164">Especifica o tamanho, em GB, do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="66023-164">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="66023-165">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="66023-165">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="66023-166">Especifica o local da chave de criptografia da chave.</span><span class="sxs-lookup"><span data-stu-id="66023-166">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="66023-167">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="66023-167">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="66023-168">Especifica a ID do recurso do cofre de chaves que contém a chave de criptografia de chave.</span><span class="sxs-lookup"><span data-stu-id="66023-168">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="66023-169">-Linux</span><span class="sxs-lookup"><span data-stu-id="66023-169">-Linux</span></span>
<span data-ttu-id="66023-170">Indica que o sistema operacional na imagem do usuário é o Linux.</span><span class="sxs-lookup"><span data-stu-id="66023-170">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="66023-171">Especifique esse parâmetro para a implantação da máquina virtual baseada em imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="66023-171">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="66023-172">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="66023-172">-ManagedDiskId</span></span>
<span data-ttu-id="66023-173">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="66023-173">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="66023-174">-Nome</span><span class="sxs-lookup"><span data-stu-id="66023-174">-Name</span></span>
<span data-ttu-id="66023-175">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="66023-175">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="66023-176">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="66023-176">-SourceImageUri</span></span>
<span data-ttu-id="66023-177">Especifica o URI do VHD para cenários de imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="66023-177">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="66023-178">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="66023-178">-StorageAccountType</span></span>
<span data-ttu-id="66023-179">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="66023-179">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="66023-180">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="66023-180">-VhdUri</span></span>
<span data-ttu-id="66023-181">Especifica o URI (Uniform Resource Identifier) de um VHD (disco rígido virtual).</span><span class="sxs-lookup"><span data-stu-id="66023-181">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="66023-182">Para uma máquina virtual baseada em imagem, esse parâmetro especifica o arquivo VHD a ser criado quando uma imagem de plataforma ou de usuário é especificada.</span><span class="sxs-lookup"><span data-stu-id="66023-182">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="66023-183">Esse é o local de onde o objeto binário grande (BLOB) da imagem é copiado para iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="66023-183">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="66023-184">Para um cenário de inicialização de máquina virtual baseado em disco, esse parâmetro especifica o arquivo VHD que a máquina virtual usa diretamente para começar.</span><span class="sxs-lookup"><span data-stu-id="66023-184">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="66023-185">-VM</span><span class="sxs-lookup"><span data-stu-id="66023-185">-VM</span></span>
<span data-ttu-id="66023-186">Especifica o objeto da máquina virtual local no qual definir propriedades de disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="66023-186">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="66023-187">Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="66023-187">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="66023-188">-Windows</span><span class="sxs-lookup"><span data-stu-id="66023-188">-Windows</span></span>
<span data-ttu-id="66023-189">Indica que o sistema operacional na imagem do usuário é o Windows.</span><span class="sxs-lookup"><span data-stu-id="66023-189">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="66023-190">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="66023-190">-WriteAccelerator</span></span>
<span data-ttu-id="66023-191">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="66023-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="66023-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66023-192">CommonParameters</span></span>
<span data-ttu-id="66023-193">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66023-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66023-194">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66023-194">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66023-195">SENSORES</span><span class="sxs-lookup"><span data-stu-id="66023-195">INPUTS</span></span>

### <span data-ttu-id="66023-196">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="66023-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>
<span data-ttu-id="66023-197">Parâmetros: VM (ByValue)</span><span class="sxs-lookup"><span data-stu-id="66023-197">Parameters: VM (ByValue)</span></span>

## <span data-ttu-id="66023-198">EXIBE</span><span class="sxs-lookup"><span data-stu-id="66023-198">OUTPUTS</span></span>

### <span data-ttu-id="66023-199">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="66023-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="66023-200">INFORMA</span><span class="sxs-lookup"><span data-stu-id="66023-200">NOTES</span></span>

## <span data-ttu-id="66023-201">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66023-201">RELATED LINKS</span></span>

[<span data-ttu-id="66023-202">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="66023-202">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="66023-203">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="66023-203">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="66023-204">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="66023-204">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

