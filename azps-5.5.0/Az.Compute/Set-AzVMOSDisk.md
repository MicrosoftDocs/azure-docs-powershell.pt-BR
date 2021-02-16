---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 66bcaab66f6385bdc9f59233054d90932ac6fa33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117815"
---
# <span data-ttu-id="41142-101">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="41142-101">Set-AzVMOSDisk</span></span>

## <span data-ttu-id="41142-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41142-102">SYNOPSIS</span></span>
<span data-ttu-id="41142-103">Define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41142-103">Sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="41142-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41142-104">SYNTAX</span></span>

### <span data-ttu-id="41142-105">DefaultParamSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="41142-105">DefaultParamSet (Default)</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41142-106">WindowsParamSet</span><span class="sxs-lookup"><span data-stu-id="41142-106">WindowsParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41142-107">WindowsDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="41142-107">WindowsDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Windows] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41142-108">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="41142-108">LinuxParamSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskSizeInGB <Int32>]
 [-ManagedDiskId <String>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DiffDiskSetting <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41142-109">LinuxDiskEncryptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="41142-109">LinuxDiskEncryptionParameterSet</span></span>
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-SourceImageUri] <String>] [[-CreateOption] <String>] [-Linux] [-DiskEncryptionKeyUrl] <String>
 [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>] [[-KeyEncryptionKeyVaultId] <String>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-WriteAccelerator] [-DiffDiskSetting <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41142-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="41142-110">DESCRIPTION</span></span>
<span data-ttu-id="41142-111">O **cmdlet Set-AzVMOSDisk** define as propriedades de disco do sistema operacional em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41142-111">The **Set-AzVMOSDisk** cmdlet sets the operating system disk properties on a virtual machine.</span></span>

## <span data-ttu-id="41142-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41142-112">EXAMPLES</span></span>

### <span data-ttu-id="41142-113">Exemplo 1: Definir propriedades em uma máquina virtual a partir da imagem da plataforma</span><span class="sxs-lookup"><span data-stu-id="41142-113">Example 1: Set properties on a virtual machine from platform image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="41142-114">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="41142-114">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="41142-115">O segundo comando cria um objeto virtual de máquina e o armazena na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="41142-115">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="41142-116">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41142-116">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="41142-117">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="41142-117">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="41142-118">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="41142-118">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="41142-119">Exemplo 2: define as propriedades em uma máquina virtual a partir da imagem do usuário generalizado</span><span class="sxs-lookup"><span data-stu-id="41142-119">Example 2: Sets properties on a virtual machine from generalized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="41142-120">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="41142-120">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="41142-121">O segundo comando cria um objeto virtual de máquina e o armazena na $VirtualMachine variável.</span><span class="sxs-lookup"><span data-stu-id="41142-121">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="41142-122">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41142-122">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="41142-123">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="41142-123">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="41142-124">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="41142-124">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="41142-125">Exemplo 3: define propriedades em uma máquina virtual a partir de uma imagem de usuário especializada</span><span class="sxs-lookup"><span data-stu-id="41142-125">Example 3: Sets properties on a virtual machine from specialized user image</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

<span data-ttu-id="41142-126">O primeiro comando obtém o conjunto de disponibilidade chamado AvailabilitySet13 no grupo de recursos chamado ResourceGroup11 e armazena esse objeto na variável $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="41142-126">The first command gets the availability set named AvailabilitySet13 in the resource group named ResourceGroup11 and stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="41142-127">O segundo comando cria um objeto virtual de máquina e o armazena na $VirtualMachine variável.</span><span class="sxs-lookup"><span data-stu-id="41142-127">The second command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="41142-128">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41142-128">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="41142-129">A máquina virtual pertence ao conjunto de disponibilidade armazenado em $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="41142-129">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="41142-130">O comando final define as propriedades na máquina virtual em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="41142-130">The final command sets the properties on the virtual machine in $VirtualMachine.</span></span>

### <span data-ttu-id="41142-131">Exemplo 4: Definir as configurações de criptografia de disco em um disco do sistema operacional de computador virtual</span><span class="sxs-lookup"><span data-stu-id="41142-131">Example 4: Set the disk encryption settings on a virtual machine operating system disk</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

<span data-ttu-id="41142-132">Este exemplo define as configurações de criptografia de disco em um disco do sistema operacional de computador virtual.</span><span class="sxs-lookup"><span data-stu-id="41142-132">This example sets the disk encryption settings on a virtual machine operating system disk.</span></span>

## <span data-ttu-id="41142-133">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41142-133">PARAMETERS</span></span>

### <span data-ttu-id="41142-134">-Cache</span><span class="sxs-lookup"><span data-stu-id="41142-134">-Caching</span></span>
<span data-ttu-id="41142-135">Especifica o modo de cache do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="41142-135">Specifies the caching mode of the operating system disk.</span></span>
<span data-ttu-id="41142-136">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="41142-136">Valid values are:</span></span> 
- <span data-ttu-id="41142-137">Readonly</span><span class="sxs-lookup"><span data-stu-id="41142-137">ReadOnly</span></span>
- <span data-ttu-id="41142-138">ReadWrite O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="41142-138">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="41142-139">Alterar o valor de cache faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="41142-139">Changing the caching value causes the virtual machine to restart.</span></span>
<span data-ttu-id="41142-140">Essa configuração afeta o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="41142-140">This setting affects the performance of the disk.</span></span>

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

### <span data-ttu-id="41142-141">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="41142-141">-CreateOption</span></span>
<span data-ttu-id="41142-142">Especifica se esse cmdlet cria um disco no computador virtual a partir de uma plataforma ou imagem do usuário ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="41142-142">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, or attaches an existing disk.</span></span>
<span data-ttu-id="41142-143">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="41142-143">Valid values are:</span></span> 
- <span data-ttu-id="41142-144">Anexar.</span><span class="sxs-lookup"><span data-stu-id="41142-144">Attach.</span></span>
<span data-ttu-id="41142-145">Especifique essa opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="41142-145">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="41142-146">Quando você especificar essa opção, não especifique o parâmetro *SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="41142-146">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="41142-147">Em vez disso, use Set-AzVMSourceImage cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41142-147">Instead, use the Set-AzVMSourceImage cmdlet.</span></span>
<span data-ttu-id="41142-148">Você também deve usar os parâmetros *do Windows* ou *do Linux* para dizer à plataforma do azure o tipo do sistema operacional no LINUXD.</span><span class="sxs-lookup"><span data-stu-id="41142-148">You must also use the use the *Windows* or *Linux* parameters to tell the azure platform the type of the operating system on the VHD.</span></span>
<span data-ttu-id="41142-149">O *parâmetro LtdadUri* é suficiente para dizer à plataforma do azure o local do disco a ser anexado.</span><span class="sxs-lookup"><span data-stu-id="41142-149">The *VhdUri* parameter is enough to tell the azure platform the location of the disk to attach.</span></span> 
- <span data-ttu-id="41142-150">Fromimage.</span><span class="sxs-lookup"><span data-stu-id="41142-150">FromImage.</span></span>
<span data-ttu-id="41142-151">Especifique essa opção para criar uma máquina virtual a partir de uma imagem de plataforma ou uma imagem de usuário generalizada.</span><span class="sxs-lookup"><span data-stu-id="41142-151">Specify this option to create a virtual machine from a platform image or a generalized user image.</span></span>
<span data-ttu-id="41142-152">No caso de uma imagem de usuário generalizada, você também precisa especificar o parâmetro *SourceImageUri* e os parâmetros *do Windows* ou *do Linux* para dizer à plataforma do Azure o local e o tipo do disco DOD do sistema operacional em vez de usar o cmdlet **Set-AzVMSourceImage.**</span><span class="sxs-lookup"><span data-stu-id="41142-152">In the case of a generalized user image, you also need to specify the *SourceImageUri* parameter and either the *Windows* or *Linux* parameters to tell the Azure platform the location and type of the operating system disk VHD instead of using the **Set-AzVMSourceImage** cmdlet.</span></span>
<span data-ttu-id="41142-153">No caso de uma imagem de plataforma, o parâmetro *HydUri* é suficiente.</span><span class="sxs-lookup"><span data-stu-id="41142-153">In the case of a platform image, the *VhdUri* parameter is sufficient.</span></span> 
- <span data-ttu-id="41142-154">Vazio.</span><span class="sxs-lookup"><span data-stu-id="41142-154">Empty.</span></span>

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

### <span data-ttu-id="41142-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41142-155">-DefaultProfile</span></span>
<span data-ttu-id="41142-156">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="41142-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41142-157">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="41142-157">-DiffDiskSetting</span></span>
<span data-ttu-id="41142-158">Especifica as configurações de disco diferentes para o disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="41142-158">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="41142-159">-DiskEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="41142-159">-DiskEncryptionKeyUrl</span></span>
<span data-ttu-id="41142-160">Especifica o local da chave de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="41142-160">Specifies the location of the disk encryption key.</span></span>

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

### <span data-ttu-id="41142-161">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="41142-161">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="41142-162">Especifica a ID de recurso do Cofre de Teclas que contém a chave de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="41142-162">Specifies the resource ID of the Key Vault containing the disk encryption key.</span></span>

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

### <span data-ttu-id="41142-163">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="41142-163">-DiskEncryptionSetId</span></span>
<span data-ttu-id="41142-164">Especifica a ID de recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="41142-164">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="41142-165">Isso só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="41142-165">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="41142-166">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="41142-166">-DiskSizeInGB</span></span>
<span data-ttu-id="41142-167">Especifica o tamanho, em GB, do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="41142-167">Specifies the size, in GB, of the operating system disk.</span></span>

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

### <span data-ttu-id="41142-168">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="41142-168">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="41142-169">Especifica o local da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="41142-169">Specifies the location of the key encryption key.</span></span>

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

### <span data-ttu-id="41142-170">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="41142-170">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="41142-171">Especifica a ID de recurso do Cofre de Teclas que contém a chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="41142-171">Specifies the resource ID of the Key Vault containing the key encryption key.</span></span>

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

### <span data-ttu-id="41142-172">-Linux</span><span class="sxs-lookup"><span data-stu-id="41142-172">-Linux</span></span>
<span data-ttu-id="41142-173">Indica que o sistema operacional na imagem do usuário é o Linux.</span><span class="sxs-lookup"><span data-stu-id="41142-173">Indicates that the operating system on the user image is Linux.</span></span>
<span data-ttu-id="41142-174">Especifique este parâmetro para a implantação de máquina virtual baseada em imagens do usuário.</span><span class="sxs-lookup"><span data-stu-id="41142-174">Specify this parameter for user image based virtual machine deployment.</span></span>

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

### <span data-ttu-id="41142-175">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="41142-175">-ManagedDiskId</span></span>
<span data-ttu-id="41142-176">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="41142-176">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="41142-177">-Nome</span><span class="sxs-lookup"><span data-stu-id="41142-177">-Name</span></span>
<span data-ttu-id="41142-178">Especifica o nome do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="41142-178">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="41142-179">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="41142-179">-SourceImageUri</span></span>
<span data-ttu-id="41142-180">Especifica o URI do DOMT para cenários de imagem do usuário.</span><span class="sxs-lookup"><span data-stu-id="41142-180">Specifies the URI of the VHD for user image scenarios.</span></span>

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

### <span data-ttu-id="41142-181">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="41142-181">-StorageAccountType</span></span>
<span data-ttu-id="41142-182">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="41142-182">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="41142-183">-HighdUri</span><span class="sxs-lookup"><span data-stu-id="41142-183">-VhdUri</span></span>
<span data-ttu-id="41142-184">Especifica o URI (Uniform Resource Identifier) de um disco rígido virtual (PGD).</span><span class="sxs-lookup"><span data-stu-id="41142-184">Specifies the Uniform Resource Identifier (URI) of a virtual hard disk (VHD).</span></span>
<span data-ttu-id="41142-185">Para uma máquina virtual baseada em imagens, esse parâmetro especifica o arquivo DESMADA a ser criado quando uma imagem de plataforma ou imagem do usuário é especificada.</span><span class="sxs-lookup"><span data-stu-id="41142-185">For an image based virtual machine, this parameter specifies the VHD file to create when a platform image or user image is specified.</span></span>
<span data-ttu-id="41142-186">Esse é o local a partir do qual o objeto binário de imagem grande (BLOB) é copiado para iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="41142-186">This is the location from which the image binary large object (BLOB) is copied to start the virtual machine.</span></span>
<span data-ttu-id="41142-187">Para um cenário de inicialização de computador virtual baseado em disco, este parâmetro especifica o arquivo TEMD que a máquina virtual usa diretamente para iniciar.</span><span class="sxs-lookup"><span data-stu-id="41142-187">For a disk based virtual machine boot scenario, this parameter specifies the VHD file that the virtual machine uses directly for starting up.</span></span>

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

### <span data-ttu-id="41142-188">-VM</span><span class="sxs-lookup"><span data-stu-id="41142-188">-VM</span></span>
<span data-ttu-id="41142-189">Especifica o objeto de máquina virtual local no qual definir as propriedades de disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="41142-189">Specifies the local virtual machine object on which to set operating system disk properties.</span></span>
<span data-ttu-id="41142-190">Para obter um objeto virtual de máquina, use o cmdlet Get-AzVM computador.</span><span class="sxs-lookup"><span data-stu-id="41142-190">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="41142-191">-Windows</span><span class="sxs-lookup"><span data-stu-id="41142-191">-Windows</span></span>
<span data-ttu-id="41142-192">Indica que o sistema operacional na imagem do usuário é o Windows.</span><span class="sxs-lookup"><span data-stu-id="41142-192">Indicates that the operating system on the user image is Windows.</span></span>

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

### <span data-ttu-id="41142-193">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="41142-193">-WriteAccelerator</span></span>
<span data-ttu-id="41142-194">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado no disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="41142-194">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="41142-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41142-195">CommonParameters</span></span>
<span data-ttu-id="41142-196">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41142-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41142-197">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41142-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41142-198">Entradas</span><span class="sxs-lookup"><span data-stu-id="41142-198">INPUTS</span></span>

### <span data-ttu-id="41142-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="41142-199">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="41142-200">System.String</span><span class="sxs-lookup"><span data-stu-id="41142-200">System.String</span></span>

## <span data-ttu-id="41142-201">Saídas</span><span class="sxs-lookup"><span data-stu-id="41142-201">OUTPUTS</span></span>

### <span data-ttu-id="41142-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="41142-202">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="41142-203">Notas</span><span class="sxs-lookup"><span data-stu-id="41142-203">NOTES</span></span>

## <span data-ttu-id="41142-204">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41142-204">RELATED LINKS</span></span>

[<span data-ttu-id="41142-205">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="41142-205">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="41142-206">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="41142-206">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="41142-207">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="41142-207">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


