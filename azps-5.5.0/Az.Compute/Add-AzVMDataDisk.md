---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMDataDisk.md
ms.openlocfilehash: 29233b0bdce273205acffcb87dbf3a8adb1d4a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116559"
---
# <span data-ttu-id="9495d-101">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9495d-101">Add-AzVMDataDisk</span></span>

## <span data-ttu-id="9495d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9495d-102">SYNOPSIS</span></span>
<span data-ttu-id="9495d-103">Adiciona um disco de dados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="9495d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9495d-104">SYNTAX</span></span>

### <span data-ttu-id="9495d-105">VmNormalDiskParameterSetName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9495d-105">VmNormalDiskParameterSetName (Default)</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-SourceImageUri] <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9495d-106">VmManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9495d-106">VmManagedDiskParameterSetName</span></span>
```
Add-AzVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <String> [[-ManagedDiskId] <String>]
 [[-StorageAccountType] <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9495d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9495d-107">DESCRIPTION</span></span>
<span data-ttu-id="9495d-108">O **cmdlet Add-AzVMDataDisk** adiciona um disco de dados a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-108">The **Add-AzVMDataDisk** cmdlet adds a data disk to a virtual machine.</span></span>
<span data-ttu-id="9495d-109">Você pode adicionar um disco de dados ao criar uma máquina virtual ou pode adicionar um disco de dados a uma máquina virtual existente.</span><span class="sxs-lookup"><span data-stu-id="9495d-109">You can add a data disk when you create a virtual machine, or you can add a data disk to an existing virtual machine.</span></span>

## <span data-ttu-id="9495d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9495d-110">EXAMPLES</span></span>

### <span data-ttu-id="9495d-111">Exemplo 1: Adicionar discos de dados a uma nova máquina virtual</span><span class="sxs-lookup"><span data-stu-id="9495d-111">Example 1: Add data disks to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

<span data-ttu-id="9495d-112">O primeiro comando cria um objeto virtual de máquina e, em seguida, o armazena na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="9495d-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9495d-113">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9495d-114">Os três comandos a seguir atribuem caminhos de três discos de dados às variáveis $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="9495d-114">The next three commands assign paths of three data disks to the $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03 variables.</span></span>
<span data-ttu-id="9495d-115">Esta abordagem é apenas para a capacidade de leitura dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9495d-115">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="9495d-116">Os três comandos finais adicionam um disco de dados à máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9495d-116">The final three commands each adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="9495d-117">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="9495d-117">The command specifies the name and location for the disk, and other properties of the disk.</span></span>
<span data-ttu-id="9495d-118">O URI de cada disco é armazenado em $DataDiskVhdUri 01, $DataDiskVhdUri 02 e $DataDiskVhdUri 03.</span><span class="sxs-lookup"><span data-stu-id="9495d-118">The URI of each disk is stored in $DataDiskVhdUri01, $DataDiskVhdUri02, and $DataDiskVhdUri03.</span></span>

### <span data-ttu-id="9495d-119">Exemplo 2: Adicionar um disco de dados a uma máquina virtual existente</span><span class="sxs-lookup"><span data-stu-id="9495d-119">Example 2: Add a data disk to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="9495d-120">O primeiro comando obtém a máquina virtual chamada VirtualMachine07 usando o cmdlet [Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="9495d-120">The first command gets the virtual machine named VirtualMachine07 by using the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="9495d-121">O comando armazena a máquina virtual na variável $VirtualMachine dados.</span><span class="sxs-lookup"><span data-stu-id="9495d-121">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9495d-122">O segundo comando adiciona um disco de dados à máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9495d-122">The second command adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="9495d-123">O comando final atualiza o estado da máquina virtual armazenada $VirtualMachine no ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9495d-123">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

### <span data-ttu-id="9495d-124">Exemplo 3: Adicionar um disco de dados a uma nova máquina virtual a partir de uma imagem de usuário generalizada</span><span class="sxs-lookup"><span data-stu-id="9495d-124">Example 3: Add a data disk to a new virtual machine from a generalized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

<span data-ttu-id="9495d-125">O primeiro comando cria um objeto virtual de máquina e o armazena na $VirtualMachine variável.</span><span class="sxs-lookup"><span data-stu-id="9495d-125">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9495d-126">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-126">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9495d-127">Os próximos dois comandos atribuem caminhos para a imagem de dados e discos de dados para as variáveis $DataImageUri e $DataDiskUri, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9495d-127">The next two commands assign paths for the data image and data disks to the $DataImageUri and $DataDiskUri variables respectively.</span></span>
<span data-ttu-id="9495d-128">Essa abordagem é usada para melhorar a capacidade de leitura dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9495d-128">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="9495d-129">Os comandos finais adicionam um disco de dados à máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9495d-129">The final commands adds a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="9495d-130">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="9495d-130">The command specifies the name and location for the disk and other properties of the disk.</span></span>

### <span data-ttu-id="9495d-131">Exemplo 4: Adicionar discos de dados a uma nova máquina virtual a partir de uma imagem de usuário especializada</span><span class="sxs-lookup"><span data-stu-id="9495d-131">Example 4: Add data disks to a new virtual machine from a specialized user image</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

<span data-ttu-id="9495d-132">O primeiro comando cria um objeto virtual de máquina e o armazena na $VirtualMachine variável.</span><span class="sxs-lookup"><span data-stu-id="9495d-132">The first command creates a virtual machine object and stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9495d-133">O comando atribui um nome e um tamanho à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-133">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="9495d-134">Os próximos comandos atribuem caminhos do disco de dados à variável $DataDiskUri dados.</span><span class="sxs-lookup"><span data-stu-id="9495d-134">The next commands assigns paths of the data disk to the $DataDiskUri variable.</span></span>
<span data-ttu-id="9495d-135">Essa abordagem é usada para melhorar a capacidade de leitura dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="9495d-135">This approach is used to improve the readability of the following commands.</span></span>
<span data-ttu-id="9495d-136">O comando final adiciona um disco de dados à máquina virtual armazenada $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9495d-136">The final command add a data disk to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="9495d-137">O comando especifica o nome e o local do disco e outras propriedades do disco.</span><span class="sxs-lookup"><span data-stu-id="9495d-137">The command specifies the name and location for the disk, and other properties of the disk.</span></span>

## <span data-ttu-id="9495d-138">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9495d-138">PARAMETERS</span></span>

### <span data-ttu-id="9495d-139">-Cache</span><span class="sxs-lookup"><span data-stu-id="9495d-139">-Caching</span></span>
<span data-ttu-id="9495d-140">Especifica o modo de cache do disco.</span><span class="sxs-lookup"><span data-stu-id="9495d-140">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="9495d-141">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9495d-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9495d-142">Readonly</span><span class="sxs-lookup"><span data-stu-id="9495d-142">ReadOnly</span></span>
- <span data-ttu-id="9495d-143">Readwrite</span><span class="sxs-lookup"><span data-stu-id="9495d-143">ReadWrite</span></span>
- <span data-ttu-id="9495d-144">Nenhum O valor padrão é ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="9495d-144">None The default value is ReadWrite.</span></span>
<span data-ttu-id="9495d-145">Alterar esse valor faz com que a máquina virtual seja reiniciada.</span><span class="sxs-lookup"><span data-stu-id="9495d-145">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="9495d-146">Essa configuração afeta a consistência e o desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="9495d-146">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="9495d-147">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="9495d-147">-CreateOption</span></span>
<span data-ttu-id="9495d-148">Especifica se esse cmdlet cria um disco no computador virtual a partir de uma plataforma ou imagem do usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="9495d-148">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>
<span data-ttu-id="9495d-149">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9495d-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9495d-150">Anexar.</span><span class="sxs-lookup"><span data-stu-id="9495d-150">Attach.</span></span>
<span data-ttu-id="9495d-151">Especifique essa opção para criar uma máquina virtual a partir de um disco especializado.</span><span class="sxs-lookup"><span data-stu-id="9495d-151">Specify this option to create a virtual machine from a specialized disk.</span></span>
<span data-ttu-id="9495d-152">Quando você especificar essa opção, não especifique o parâmetro *SourceImageUri.*</span><span class="sxs-lookup"><span data-stu-id="9495d-152">When you specify this option, do not specify the *SourceImageUri* parameter.</span></span>
<span data-ttu-id="9495d-153">O *LtdadUri* é tudo o que é necessário para dizer à plataforma do Azure o local do disco rígido virtual (TEMD) a ser anexado como um disco de dados à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-153">The *VhdUri* is all that is needed in order to tell the Azure platform the location of the virtual hard disk (VHD) to attach as a data disk to the virtual machine.</span></span>
- <span data-ttu-id="9495d-154">Vazio.</span><span class="sxs-lookup"><span data-stu-id="9495d-154">Empty.</span></span>
<span data-ttu-id="9495d-155">Especifique isso para criar um disco de dados vazio.</span><span class="sxs-lookup"><span data-stu-id="9495d-155">Specify this to create an empty data disk.</span></span>
- <span data-ttu-id="9495d-156">Fromimage.</span><span class="sxs-lookup"><span data-stu-id="9495d-156">FromImage.</span></span>
<span data-ttu-id="9495d-157">Especifique essa opção para criar uma máquina virtual a partir de uma imagem ou disco generalizado.</span><span class="sxs-lookup"><span data-stu-id="9495d-157">Specify this option to create a virtual machine from a generalized image or disk.</span></span>
<span data-ttu-id="9495d-158">Ao especificar essa opção, você deve especificar o parâmetro *SourceImageUri* também para dizer à plataforma do Azure o local da d'água para anexar como um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9495d-158">When you specify this option, you must specify the *SourceImageUri* parameter also in order to tell the Azure platform the location of the VHD to attach as a data disk.</span></span>
<span data-ttu-id="9495d-159">O *parâmetro LtdadUri* é usado como o local que identifica onde o disco de dados TEMD será armazenado quando for usado pela máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-159">The *VhdUri* parameter is used as the location identifying where the data disk VHD will be stored when it is used by the virtual machine.</span></span>

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

### <span data-ttu-id="9495d-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9495d-160">-DefaultProfile</span></span>
<span data-ttu-id="9495d-161">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9495d-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9495d-162">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="9495d-162">-DiskEncryptionSetId</span></span>
<span data-ttu-id="9495d-163">Especifica a ID de recurso do conjunto de criptografia de disco gerenciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="9495d-163">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="9495d-164">Isso só pode ser especificado para disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9495d-164">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="9495d-165">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9495d-165">-DiskSizeInGB</span></span>
<span data-ttu-id="9495d-166">Especifica o tamanho, em gigabytes, de um disco vazio a ser anexado a uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-166">Specifies the size, in gigabytes, of an empty disk to attach to a virtual machine.</span></span>

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

### <span data-ttu-id="9495d-167">-Ltda</span><span class="sxs-lookup"><span data-stu-id="9495d-167">-Lun</span></span>
<span data-ttu-id="9495d-168">Especifica o número de unidade lógica (NUMD) de um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9495d-168">Specifies the logical unit number (LUN) for a data disk.</span></span>

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

### <span data-ttu-id="9495d-169">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="9495d-169">-ManagedDiskId</span></span>
<span data-ttu-id="9495d-170">Especifica a ID de um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9495d-170">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="9495d-171">-Nome</span><span class="sxs-lookup"><span data-stu-id="9495d-171">-Name</span></span>
<span data-ttu-id="9495d-172">Especifica o nome do disco de dados a ser acrescentado.</span><span class="sxs-lookup"><span data-stu-id="9495d-172">Specifies the name of the data disk to add.</span></span>

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

### <span data-ttu-id="9495d-173">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="9495d-173">-SourceImageUri</span></span>
<span data-ttu-id="9495d-174">Especifica o URI de origem do disco que este cmdlet anexa.</span><span class="sxs-lookup"><span data-stu-id="9495d-174">Specifies the source URI of the disk that this cmdlet attaches.</span></span>

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

### <span data-ttu-id="9495d-175">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9495d-175">-StorageAccountType</span></span>
<span data-ttu-id="9495d-176">Especifica o tipo de conta de armazenamento do disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9495d-176">Specifies the storage account type of managed disk.</span></span>

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

### <span data-ttu-id="9495d-177">-HighdUri</span><span class="sxs-lookup"><span data-stu-id="9495d-177">-VhdUri</span></span>
<span data-ttu-id="9495d-178">Especifica o URI (Uniform Resource Identifier) do arquivo de disco rígido virtual (PGD) a ser criado quando uma imagem de usuário ou imagem de plataforma é usada.</span><span class="sxs-lookup"><span data-stu-id="9495d-178">Specifies the Uniform Resource Identifier (URI) for the virtual hard disk (VHD) file to create when a platform image or user image is used.</span></span>
<span data-ttu-id="9495d-179">Este cmdlet copia o objeto binário de imagem grande (blob) para esse local.</span><span class="sxs-lookup"><span data-stu-id="9495d-179">This cmdlet copies the image binary large object (blob) to this location.</span></span>
<span data-ttu-id="9495d-180">Este é o local de onde iniciar a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-180">This is the location from which to start the virtual machine.</span></span>

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

### <span data-ttu-id="9495d-181">-VM</span><span class="sxs-lookup"><span data-stu-id="9495d-181">-VM</span></span>
<span data-ttu-id="9495d-182">Especifica o objeto de máquina virtual local ao qual adicionar um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="9495d-182">Specifies the local virtual machine object to which to add a data disk.</span></span>
<span data-ttu-id="9495d-183">Você pode usar o **cmdlet Get-AzVM** para obter um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-183">You can use the **Get-AzVM** cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="9495d-184">Você pode usar o **cmdlet New-AzVMConfig** para criar um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9495d-184">You can use the **New-AzVMConfig** cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="9495d-185">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9495d-185">-WriteAccelerator</span></span>
<span data-ttu-id="9495d-186">Especifica se o WriteAccelerator deve ser habilitado ou desabilitado em um disco de dados gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9495d-186">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

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

### <span data-ttu-id="9495d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9495d-187">CommonParameters</span></span>
<span data-ttu-id="9495d-188">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9495d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9495d-189">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9495d-189">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9495d-190">Entradas</span><span class="sxs-lookup"><span data-stu-id="9495d-190">INPUTS</span></span>

### <span data-ttu-id="9495d-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9495d-191">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9495d-192">System.String</span><span class="sxs-lookup"><span data-stu-id="9495d-192">System.String</span></span>

### <span data-ttu-id="9495d-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span><span class="sxs-lookup"><span data-stu-id="9495d-193">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="9495d-194">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9495d-194">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9495d-195">Saídas</span><span class="sxs-lookup"><span data-stu-id="9495d-195">OUTPUTS</span></span>

### <span data-ttu-id="9495d-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9495d-196">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9495d-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="9495d-197">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="9495d-198">Notas</span><span class="sxs-lookup"><span data-stu-id="9495d-198">NOTES</span></span>

## <span data-ttu-id="9495d-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9495d-199">RELATED LINKS</span></span>

[<span data-ttu-id="9495d-200">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9495d-200">Remove-AzVMDataDisk</span></span>](./Remove-AzVMDataDisk.md)

[<span data-ttu-id="9495d-201">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9495d-201">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9495d-202">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9495d-202">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
