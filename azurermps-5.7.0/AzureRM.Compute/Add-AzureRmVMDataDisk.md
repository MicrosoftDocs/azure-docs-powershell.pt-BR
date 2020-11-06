---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428987"
---
# <span data-ttu-id="5bfc4-101">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5bfc4-101">Add-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="5bfc4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5bfc4-102">SYNOPSIS</span></span>
<span data-ttu-id="5bfc4-103">Adiciona um disco de dados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-103">Adds a data disk to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bfc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bfc4-104">SYNTAX</span></span>

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## <span data-ttu-id="5bfc4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5bfc4-105">DESCRIPTION</span></span>
<span data-ttu-id="5bfc4-106">O cmdlet **Add-AzureRmVMDataDisk** adiciona um disco de dados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-106">The **Add-AzureRmVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="5bfc4-107">Você pode adicionar um disco de dados quando cria uma máquina virtual ou pode adicionar um disco de dados a uma máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-107">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="5bfc4-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bfc4-108">EXAMPLES</span></span>

### <span data-ttu-id="5bfc4-109">Exemplo 1: adicionar discos de dados a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="5bfc4-109">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="5bfc4-110">O primeiro comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-110">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5bfc4-111">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-111">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="5bfc4-112">Os próximos três comandos atribuem caminhos de três discos de dados às variáveis $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-112">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="5bfc4-113">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-113">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="5bfc4-114">Os três comandos finais adicionam um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-114">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="5bfc4-115">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-115">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="5bfc4-116">O URI de cada disco é armazenado no $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-116">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="5bfc4-117">Exemplo 2: adicionar um disco de dados a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="5bfc4-117">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="5bfc4-118">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="5bfc4-118">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="5bfc4-119">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-119">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="5bfc4-120">O segundo comando adiciona um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-120">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="5bfc4-121">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-121">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="5bfc4-122">Exemplo 3: adicionar um disco de dados a uma nova máquina virtual a partir de uma imagem geral do usuário</span><span class="sxs-lookup"><span data-stu-id="5bfc4-122">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="5bfc4-123">O primeiro comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-123">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5bfc4-124">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-124">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="5bfc4-125">Os próximos dois comandos atribuem caminhos para a imagem de dados e discos de dados às variáveis $DataImageUri e $DataDiskUri, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-125">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="5bfc4-126">Essa abordagem é usada para melhorar a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-126">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="5bfc4-127">Os comandos finais adicionam um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-127">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="5bfc4-128">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-128">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="5bfc4-129">Exemplo 4: adicionar discos de dados a uma nova máquina virtual a partir de uma imagem de usuário especializada</span><span class="sxs-lookup"><span data-stu-id="5bfc4-129">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="5bfc4-130">O primeiro comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-130">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5bfc4-131">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-131">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="5bfc4-132">Os comandos a seguir atribuirão caminhos do disco de dados à variável $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-132">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="5bfc4-133">Essa abordagem é usada para melhorar a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-133">This approach is used to improve the readability of the following commands.</span></span>

<span data-ttu-id="5bfc4-134">O comando final adicionar um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-134">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="5bfc4-135">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-135">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="5bfc4-136">OS</span><span class="sxs-lookup"><span data-stu-id="5bfc4-136">PARAMETERS</span></span>

### <span data-ttu-id="5bfc4-137">-Cache</span><span class="sxs-lookup"><span data-stu-id="5bfc4-137">-Caching</span></span>
<span data-ttu-id="5bfc4-138">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-138">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="5bfc4-139">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5bfc4-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bfc4-140">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="5bfc4-140">ReadOnly</span></span>
- <span data-ttu-id="5bfc4-141">Leitura</span><span class="sxs-lookup"><span data-stu-id="5bfc4-141">ReadWrite</span></span>
- <span data-ttu-id="5bfc4-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5bfc4-142">None</span></span>

<span data-ttu-id="5bfc4-143">O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-143">The default value is ReadWrite.</span></span>
<span data-ttu-id="5bfc4-144">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-144">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="5bfc4-145">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-145">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-146">-Createoption</span><span class="sxs-lookup"><span data-stu-id="5bfc4-146">-CreateOption</span></span>
<span data-ttu-id="5bfc4-147">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-147">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="5bfc4-148">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="5bfc4-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bfc4-149">Liga.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-149">Attach.</span></span>
<span data-ttu-id="5bfc4-150">Especifique esta opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-150">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="5bfc4-151">Ao especificar essa opção, não especifique o parâmetro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="5bfc4-151">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="5bfc4-152">O *VhdUri* é tudo que é necessário para que a plataforma do Azure seja a localização do disco rígido virtual (VHD) a ser anexado como um disco de dados à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-152">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="5bfc4-153">Vazia.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-153">Empty.</span></span>
<span data-ttu-id="5bfc4-154">Especifique isso para criar um disco de dados vazio.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-154">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="5bfc4-155">FromImage.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-155">FromImage.</span></span>
<span data-ttu-id="5bfc4-156">Especifique esta opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-156">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="5bfc4-157">Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para solicitar à plataforma Azure o local do VHD a ser anexado como um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-157">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="5bfc4-158">O parâmetro *VhdUri* é usado como a localização que identifica onde o VHD do disco de dados será armazenado quando for usado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-158">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-159">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="5bfc4-159">-DiskSizeInGB</span></span>
<span data-ttu-id="5bfc4-160">Especifica o tamanho, em gigabytes, de um disco vazio para ser anexado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-160">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-161">-LUN</span><span class="sxs-lookup"><span data-stu-id="5bfc4-161">-Lun</span></span>
<span data-ttu-id="5bfc4-162">Especifica o número de unidade lógica (LUN) para um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-162">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-163">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="5bfc4-163">-ManagedDiskId</span></span>
<span data-ttu-id="5bfc4-164">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-164">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-165">-Nome</span><span class="sxs-lookup"><span data-stu-id="5bfc4-165">-Name</span></span>
<span data-ttu-id="5bfc4-166">Especifica o nome do disco de dados a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-166">Specifies the name of the data disk to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-167">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="5bfc4-167">-SourceImageUri</span></span>
<span data-ttu-id="5bfc4-168">Especifica o URI de origem do disco que este cmdlet anexa.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-168">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-169">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="5bfc4-169">-StorageAccountType</span></span>
<span data-ttu-id="5bfc4-170">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-170">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-171">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="5bfc4-171">-VhdUri</span></span>
<span data-ttu-id="5bfc4-172">Especifica o URI (Uniform Resource Identifier) para o arquivo de disco rígido virtual (VHD) a ser criado quando uma imagem de plataforma ou de usuário é usada.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-172">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="5bfc4-173">Esse cmdlet copia o blob (objeto grande binário) da imagem para este local.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-173">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="5bfc4-174">Este é o local de onde deseja iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-174">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-175">-VM</span><span class="sxs-lookup"><span data-stu-id="5bfc4-175">-VM</span></span>
<span data-ttu-id="5bfc4-176">Especifica o objeto da máquina virtual local ao qual adicionar um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-176">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="5bfc4-177">Você pode usar o cmdlet **Get-AzureRmVM** para obter um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-177">You can use the **Get-AzureRmVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="5bfc4-178">Você pode usar o cmdlet **New-AzureRmVMConfig** para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-178">You can use the **New-AzureRmVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bfc4-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bfc4-179">CommonParameters</span></span>
<span data-ttu-id="5bfc4-180">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bfc4-181">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bfc4-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bfc4-182">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5bfc4-182">INPUTS</span></span>

### <span data-ttu-id="5bfc4-183">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5bfc4-183">None</span></span>
<span data-ttu-id="5bfc4-184">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5bfc4-184">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5bfc4-185">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5bfc4-185">OUTPUTS</span></span>

## <span data-ttu-id="5bfc4-186">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5bfc4-186">NOTES</span></span>

## <span data-ttu-id="5bfc4-187">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bfc4-187">RELATED LINKS</span></span>

[<span data-ttu-id="5bfc4-188">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5bfc4-188">Remove-AzureRmVMDataDisk</span></span>](./Remove-AzureRmVMDataDisk.md)

[<span data-ttu-id="5bfc4-189">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5bfc4-189">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5bfc4-190">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5bfc4-190">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
