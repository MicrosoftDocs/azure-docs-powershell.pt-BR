---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 56f78fe75ab01db70fb7af1fe2eba98003387342
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771249"
---
# <span data-ttu-id="ca39c-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ca39c-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="ca39c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca39c-102">SYNOPSIS</span></span>
<span data-ttu-id="ca39c-103">Adiciona um disco de dados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="ca39c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca39c-104">SYNTAX</span></span>

### <span data-ttu-id="ca39c-105">VmNormalDiskParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca39c-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca39c-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ca39c-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca39c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca39c-107">DESCRIPTION</span></span>
<span data-ttu-id="ca39c-108">O cmdlet **Add-AzVMDataDisk** adiciona um disco de dados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="ca39c-109">Você pode adicionar um disco de dados quando cria uma máquina virtual ou pode adicionar um disco de dados a uma máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="ca39c-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="ca39c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca39c-110">EXAMPLES</span></span>

### <span data-ttu-id="ca39c-111">Exemplo 1: adicionar discos de dados a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="ca39c-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="ca39c-112">O primeiro comando cria um objeto de máquina virtual e, em seguida, armazena-o na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ca39c-113">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ca39c-114">Os próximos três comandos atribuem caminhos de três discos de dados às variáveis $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="ca39c-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="ca39c-115">Essa abordagem só tem a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca39c-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="ca39c-116">Os três comandos finais adicionam um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ca39c-117">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="ca39c-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="ca39c-118">O URI de cada disco é armazenado no $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="ca39c-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="ca39c-119">Exemplo 2: adicionar um disco de dados a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="ca39c-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="ca39c-120">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="ca39c-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="ca39c-121">O comando armazena a máquina virtual na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ca39c-122">O segundo comando adiciona um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ca39c-123">O comando final atualiza o estado da máquina virtual armazenada em $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ca39c-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="ca39c-124">Exemplo 3: adicionar um disco de dados a uma nova máquina virtual a partir de uma imagem geral do usuário</span><span class="sxs-lookup"><span data-stu-id="ca39c-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="ca39c-125">O primeiro comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ca39c-126">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ca39c-127">Os próximos dois comandos atribuem caminhos para a imagem de dados e discos de dados às variáveis $DataImageUri e $DataDiskUri, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ca39c-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="ca39c-128">Essa abordagem é usada para melhorar a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca39c-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="ca39c-129">Os comandos finais adicionam um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ca39c-130">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="ca39c-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="ca39c-131">Exemplo 4: adicionar discos de dados a uma nova máquina virtual a partir de uma imagem de usuário especializada</span><span class="sxs-lookup"><span data-stu-id="ca39c-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="ca39c-132">O primeiro comando cria um objeto de máquina virtual e o armazena na variável $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ca39c-133">O comando atribui um nome e um tamanho para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ca39c-134">Os comandos a seguir atribuirão caminhos do disco de dados à variável $DataDiskUri.</span><span class="sxs-lookup"><span data-stu-id="ca39c-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="ca39c-135">Essa abordagem é usada para melhorar a legibilidade dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca39c-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="ca39c-136">O comando final adicionar um disco de dados à máquina virtual armazenada em $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ca39c-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ca39c-137">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="ca39c-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="ca39c-138">OS</span><span class="sxs-lookup"><span data-stu-id="ca39c-138">PARAMETERS</span></span>

### <span data-ttu-id="ca39c-139">-Cache</span><span class="sxs-lookup"><span data-stu-id="ca39c-139">-Caching</span></span>
<span data-ttu-id="ca39c-140">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="ca39c-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="ca39c-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ca39c-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca39c-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ca39c-142">ReadOnly</span></span>
- <span data-ttu-id="ca39c-143">Leitura</span><span class="sxs-lookup"><span data-stu-id="ca39c-143">ReadWrite</span></span>
- <span data-ttu-id="ca39c-144">None o valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ca39c-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="ca39c-145">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="ca39c-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="ca39c-146">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="ca39c-146">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-147">-Createoption</span><span class="sxs-lookup"><span data-stu-id="ca39c-147">-CreateOption</span></span>
<span data-ttu-id="ca39c-148">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="ca39c-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="ca39c-149">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ca39c-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ca39c-150">Liga.</span><span class="sxs-lookup"><span data-stu-id="ca39c-150">Attach.</span></span>
<span data-ttu-id="ca39c-151">Especifique esta opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="ca39c-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="ca39c-152">Ao especificar essa opção, não especifique o parâmetro *SourceImageUri* .</span><span class="sxs-lookup"><span data-stu-id="ca39c-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="ca39c-153">O *VhdUri* é tudo que é necessário para que a plataforma do Azure seja a localização do disco rígido virtual (VHD) a ser anexado como um disco de dados à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="ca39c-154">Vazia.</span><span class="sxs-lookup"><span data-stu-id="ca39c-154">Empty.</span></span>
<span data-ttu-id="ca39c-155">Especifique isso para criar um disco de dados vazio.</span><span class="sxs-lookup"><span data-stu-id="ca39c-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="ca39c-156">FromImage.</span><span class="sxs-lookup"><span data-stu-id="ca39c-156">FromImage.</span></span>
<span data-ttu-id="ca39c-157">Especifique esta opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.</span><span class="sxs-lookup"><span data-stu-id="ca39c-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="ca39c-158">Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para solicitar à plataforma Azure o local do VHD a ser anexado como um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="ca39c-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="ca39c-159">O parâmetro *VhdUri* é usado como a localização que identifica onde o VHD do disco de dados será armazenado quando for usado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca39c-160">-DefaultProfile</span></span>
<span data-ttu-id="ca39c-161">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca39c-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca39c-162">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="ca39c-162">-DiskSizeInGB</span></span>
<span data-ttu-id="ca39c-163">Especifica o tamanho, em gigabytes, de um disco vazio para ser anexado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-163">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-164">-LUN</span><span class="sxs-lookup"><span data-stu-id="ca39c-164">-Lun</span></span>
<span data-ttu-id="ca39c-165">Especifica o número de unidade lógica (LUN) para um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="ca39c-165">Specifies the logical unit number (LUN) for a data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-166">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="ca39c-166">-ManagedDiskId</span></span>
<span data-ttu-id="ca39c-167">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ca39c-167">Specifies the ID of a managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-168">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca39c-168">-Name</span></span>
<span data-ttu-id="ca39c-169">Especifica o nome do disco de dados a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="ca39c-169">Specifies the name of the data disk to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-170">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="ca39c-170">-SourceImageUri</span></span>
<span data-ttu-id="ca39c-171">Especifica o URI de origem do disco que este cmdlet anexa.</span><span class="sxs-lookup"><span data-stu-id="ca39c-171">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-172">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ca39c-172">-StorageAccountType</span></span>
<span data-ttu-id="ca39c-173">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ca39c-173">Specifies the storage account type of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-174">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="ca39c-174">-VhdUri</span></span>
<span data-ttu-id="ca39c-175">Especifica o URI (Uniform Resource Identifier) para o arquivo de disco rígido virtual (VHD) a ser criado quando uma imagem de plataforma ou de usuário é usada.</span><span class="sxs-lookup"><span data-stu-id="ca39c-175">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="ca39c-176">Esse cmdlet copia o blob (objeto grande binário) da imagem para este local.</span><span class="sxs-lookup"><span data-stu-id="ca39c-176">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="ca39c-177">Este é o local de onde deseja iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-177">This is the location from which to start the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: VmNormalDiskParameterSetName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-178">-VM</span><span class="sxs-lookup"><span data-stu-id="ca39c-178">-VM</span></span>
<span data-ttu-id="ca39c-179">Especifica o objeto da máquina virtual local ao qual adicionar um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="ca39c-179">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="ca39c-180">Você pode usar o cmdlet **Get-AzVM** para obter um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-180">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="ca39c-181">Você pode usar o cmdlet **New-AzVMConfig** para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ca39c-181">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-182">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ca39c-182">-WriteAccelerator</span></span>
<span data-ttu-id="ca39c-183">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ca39c-183">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VmManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca39c-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca39c-184">CommonParameters</span></span>
<span data-ttu-id="ca39c-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca39c-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca39c-186">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca39c-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca39c-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca39c-187">INPUTS</span></span>

### <span data-ttu-id="ca39c-188">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ca39c-188">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ca39c-189">System. String</span><span class="sxs-lookup"><span data-stu-id="ca39c-189">System.String</span></span>

### <span data-ttu-id="ca39c-190">Microsoft. Azure. Management. COMPUTE. Models. CachingTypes</span><span class="sxs-lookup"><span data-stu-id="ca39c-190">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="ca39c-191">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ca39c-191">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ca39c-192">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca39c-192">OUTPUTS</span></span>

### <span data-ttu-id="ca39c-193">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ca39c-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ca39c-194">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="ca39c-194">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="ca39c-195">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca39c-195">NOTES</span></span>

## <span data-ttu-id="ca39c-196">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca39c-196">RELATED LINKS</span></span>

[<span data-ttu-id="ca39c-197">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ca39c-197">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="ca39c-198">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ca39c-198">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ca39c-199">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ca39c-199">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
