---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: ec4d0444ad88fa7536fbf1ee050dc8dcb6a76af3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430197"
---
# <span data-ttu-id="79a83-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="79a83-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="79a83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79a83-102">SYNOPSIS</span></span>
<span data-ttu-id="79a83-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="79a83-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="79a83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79a83-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>]
 [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79a83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79a83-105">DESCRIPTION</span></span>
<span data-ttu-id="79a83-106">O cmdlet **New-AzDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="79a83-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="79a83-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79a83-107">EXAMPLES</span></span>

### <span data-ttu-id="79a83-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="79a83-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="79a83-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="79a83-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="79a83-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="79a83-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="79a83-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="79a83-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="79a83-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="79a83-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="79a83-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
PS C:\> $diskSas = Grant-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DurationInSecond 86400 -Access 'Write'
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ReadyToUpload'
PS C:\> AzCopy /Source:https://myaccount.blob.core.windows.net/mycontainer1 /Dest:$diskSas
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
# $disk.DiskState == 'ActiveUpload'
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="79a83-114">O primeiro comando cria um objeto de disco local para carregamento.</span><span class="sxs-lookup"><span data-stu-id="79a83-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="79a83-115">O segundo comando leva o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="79a83-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="79a83-116">O terceiro comando obtém a URL SAS para o disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="79a83-117">O quarto comando obtém o estado do disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="79a83-118">Se o estado do disco for ' ReadyToUpload ', um usuário pode carregar um disco do armazenamento de BLOB para a URL SAS de disco usando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="79a83-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="79a83-119">Durante o upload, o estado do disco é alterado para ' ActiveUpload '.</span><span class="sxs-lookup"><span data-stu-id="79a83-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="79a83-120">O último comando revoga o acesso ao disco para a URL SAS.</span><span class="sxs-lookup"><span data-stu-id="79a83-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="79a83-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="79a83-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="79a83-122">Crie um disco a partir de uma versão da imagem da Galeria compartilhada.</span><span class="sxs-lookup"><span data-stu-id="79a83-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="79a83-123">ID é a ID da versão da imagem da Galeria compartilhada.</span><span class="sxs-lookup"><span data-stu-id="79a83-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="79a83-124">O LUN é necessário apenas se a origem for um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="79a83-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="79a83-125">OS</span><span class="sxs-lookup"><span data-stu-id="79a83-125">PARAMETERS</span></span>

### <span data-ttu-id="79a83-126">-Createoption</span><span class="sxs-lookup"><span data-stu-id="79a83-126">-CreateOption</span></span>
<span data-ttu-id="79a83-127">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="79a83-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="79a83-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a83-128">-DefaultProfile</span></span>
<span data-ttu-id="79a83-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79a83-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79a83-130">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="79a83-130">-DiskAccessId</span></span>
<span data-ttu-id="79a83-131">Obtém ou define a ID de braço do recurso DiskAccess para uso de pontos de extremidade privados em.</span><span class="sxs-lookup"><span data-stu-id="79a83-131">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="79a83-132">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="79a83-132">-DiskEncryptionKey</span></span>
<span data-ttu-id="79a83-133">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-133">Specifies the disk encryption key object on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-134">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="79a83-134">-DiskEncryptionSetId</span></span>
<span data-ttu-id="79a83-135">Especifica a ID do recurso do conjunto de criptografia de disco a ser usado para habilitar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="79a83-135">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="79a83-136">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="79a83-136">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="79a83-137">O número total de IOPS que serão permitidas em todas as VMs montando o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="79a83-137">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="79a83-138">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="79a83-138">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-139">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="79a83-139">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="79a83-140">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="79a83-140">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="79a83-141">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="79a83-141">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-142">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="79a83-142">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="79a83-143">"Descrição": "a taxa de transferência total (MBps) que será permitida em todas as VMs que montam o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="79a83-143">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="79a83-144">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="79a83-144">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-145">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="79a83-145">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="79a83-146">A largura de banda permitida para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="79a83-146">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="79a83-147">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="79a83-147">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-148">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="79a83-148">-DiskSizeGB</span></span>
<span data-ttu-id="79a83-149">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="79a83-149">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-150">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="79a83-150">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="79a83-151">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="79a83-151">Enable encryption settings.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-152">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="79a83-152">-EncryptionType</span></span>
<span data-ttu-id="79a83-153">O tipo de chave usado para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-153">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="79a83-154">Os valores disponíveis são: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="79a83-154">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="79a83-155">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="79a83-155">-GalleryImageReference</span></span>
<span data-ttu-id="79a83-156">O objeto GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="79a83-156">The GalleryImageReference object.</span></span>  <span data-ttu-id="79a83-157">Obrigatório se estiver criando a partir de uma imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="79a83-157">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="79a83-158">A ID será a ID do braço da versão da imagem de galé compartilhada a partir da qual criar um disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-158">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="79a83-159">Um LUN será necessário se a origem da cópia for um dos discos de dados na imagem da Galeria; Se for NULL, o disco do sistema operacional da imagem será copiado.</span><span class="sxs-lookup"><span data-stu-id="79a83-159">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-160">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="79a83-160">-HyperVGeneration</span></span>
<span data-ttu-id="79a83-161">A geração de hipervisor da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="79a83-161">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="79a83-162">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79a83-162">Applicable to OS disks only.</span></span>  <span data-ttu-id="79a83-163">Os valores permitidos são v1 e v2.</span><span class="sxs-lookup"><span data-stu-id="79a83-163">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="79a83-164">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="79a83-164">-ImageReference</span></span>
<span data-ttu-id="79a83-165">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-165">Specifies the image reference on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDiskReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-166">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="79a83-166">-KeyEncryptionKey</span></span>
<span data-ttu-id="79a83-167">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-167">Specifies the Key encryption key on a disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-168">-Local</span><span class="sxs-lookup"><span data-stu-id="79a83-168">-Location</span></span>
<span data-ttu-id="79a83-169">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="79a83-169">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-170">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="79a83-170">-LogicalSectorSize</span></span>
<span data-ttu-id="79a83-171">O tamanho do setor lógico em bytes para ultra discos.</span><span class="sxs-lookup"><span data-stu-id="79a83-171">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="79a83-172">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="79a83-172">-MaxSharesCount</span></span>
<span data-ttu-id="79a83-173">O número máximo de VMs que podem ser anexadas ao disco ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="79a83-173">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="79a83-174">O valor maior que um indica um disco que pode ser montado em várias VMs ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="79a83-174">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="79a83-175">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="79a83-175">-NetworkAccessPolicy</span></span>
<span data-ttu-id="79a83-176">A política de acesso à rede define a política de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="79a83-176">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="79a83-177">Os valores possíveis incluem: ' AllowAll ', ' AllowPrivate ', ' DenyAll '</span><span class="sxs-lookup"><span data-stu-id="79a83-177">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="79a83-178">-OsType</span><span class="sxs-lookup"><span data-stu-id="79a83-178">-OsType</span></span>
<span data-ttu-id="79a83-179">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79a83-179">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-180">-SkuName</span><span class="sxs-lookup"><span data-stu-id="79a83-180">-SkuName</span></span>
<span data-ttu-id="79a83-181">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="79a83-181">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="79a83-182">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="79a83-182">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="79a83-183">UltraSSD_LRS só pode ser usado com um valor vazio para o parâmetro createoption.</span><span class="sxs-lookup"><span data-stu-id="79a83-183">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountType

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-184">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="79a83-184">-SourceResourceId</span></span>
<span data-ttu-id="79a83-185">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="79a83-185">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="79a83-186">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="79a83-186">-SourceUri</span></span>
<span data-ttu-id="79a83-187">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="79a83-187">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="79a83-188">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="79a83-188">-StorageAccountId</span></span>
<span data-ttu-id="79a83-189">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="79a83-189">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="79a83-190">-Marca</span><span class="sxs-lookup"><span data-stu-id="79a83-190">-Tag</span></span>
<span data-ttu-id="79a83-191">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="79a83-191">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="79a83-192">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="79a83-192">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-193">-Tier</span><span class="sxs-lookup"><span data-stu-id="79a83-193">-Tier</span></span>
<span data-ttu-id="79a83-194">Camada de desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-194">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="79a83-195">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="79a83-195">-UploadSizeInBytes</span></span>
<span data-ttu-id="79a83-196">Especifica o tamanho do conteúdo do carregamento incluindo o rodapé do VHD quando createoption é carregado.</span><span class="sxs-lookup"><span data-stu-id="79a83-196">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="79a83-197">Esse valor deve estar entre 20972032 (20 MiB + 512 bytes para o rodapé VHD) e 35183298347520 bytes (32 TiB + 512 bytes para o rodapé VHD).</span><span class="sxs-lookup"><span data-stu-id="79a83-197">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-198">-Zone</span><span class="sxs-lookup"><span data-stu-id="79a83-198">-Zone</span></span>
<span data-ttu-id="79a83-199">Especifica a lista de zonas lógicas do disco.</span><span class="sxs-lookup"><span data-stu-id="79a83-199">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-200">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79a83-200">-Confirm</span></span>
<span data-ttu-id="79a83-201">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a83-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a83-202">-WhatIf</span></span>
<span data-ttu-id="79a83-203">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="79a83-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79a83-204">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="79a83-204">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a83-205">CommonParameters</span></span>
<span data-ttu-id="79a83-206">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a83-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a83-207">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79a83-207">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a83-208">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79a83-208">INPUTS</span></span>

### <span data-ttu-id="79a83-209">System. String</span><span class="sxs-lookup"><span data-stu-id="79a83-209">System.String</span></span>

### <span data-ttu-id="79a83-210">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="79a83-210">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="79a83-211">System. Int32</span><span class="sxs-lookup"><span data-stu-id="79a83-211">System.Int32</span></span>

### <span data-ttu-id="79a83-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="79a83-212">System.String[]</span></span>

### <span data-ttu-id="79a83-213">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="79a83-213">System.Collections.Hashtable</span></span>

### <span data-ttu-id="79a83-214">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="79a83-214">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="79a83-215">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="79a83-215">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="79a83-216">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="79a83-216">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="79a83-217">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="79a83-217">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="79a83-218">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79a83-218">OUTPUTS</span></span>

### <span data-ttu-id="79a83-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="79a83-219">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="79a83-220">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79a83-220">NOTES</span></span>

## <span data-ttu-id="79a83-221">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79a83-221">RELATED LINKS</span></span>
