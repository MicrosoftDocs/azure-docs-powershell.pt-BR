---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 4e2e09597cc52431657001e20ca34ad6e77aa40f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113104"
---
# <span data-ttu-id="2febd-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="2febd-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="2febd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2febd-102">SYNOPSIS</span></span>
<span data-ttu-id="2febd-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="2febd-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="2febd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2febd-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>]
 [-DiskMBpsReadWrite <Int64>] [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2febd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2febd-105">DESCRIPTION</span></span>
<span data-ttu-id="2febd-106">O cmdlet **New-AzDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="2febd-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="2febd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2febd-107">EXAMPLES</span></span>

### <span data-ttu-id="2febd-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2febd-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="2febd-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2febd-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="2febd-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="2febd-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="2febd-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="2febd-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2febd-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2febd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2febd-113">Example 2</span></span>
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

<span data-ttu-id="2febd-114">O primeiro comando cria um objeto de disco local para carregamento.</span><span class="sxs-lookup"><span data-stu-id="2febd-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="2febd-115">O segundo comando leva o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2febd-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="2febd-116">O terceiro comando obtém a URL SAS para o disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="2febd-117">O quarto comando obtém o estado do disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="2febd-118">Se o estado do disco for ' ReadyToUpload ', um usuário pode carregar um disco do armazenamento de BLOB para a URL SAS de disco usando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="2febd-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="2febd-119">Durante o upload, o estado do disco é alterado para ' ActiveUpload '.</span><span class="sxs-lookup"><span data-stu-id="2febd-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="2febd-120">O último comando revoga o acesso ao disco para a URL SAS.</span><span class="sxs-lookup"><span data-stu-id="2febd-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="2febd-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2febd-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="2febd-122">Crie um disco a partir de uma versão da imagem da Galeria compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2febd-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="2febd-123">ID é a ID da versão da imagem da Galeria compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2febd-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="2febd-124">O LUN é necessário apenas se a origem for um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="2febd-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="2febd-125">OS</span><span class="sxs-lookup"><span data-stu-id="2febd-125">PARAMETERS</span></span>

### <span data-ttu-id="2febd-126">-Createoption</span><span class="sxs-lookup"><span data-stu-id="2febd-126">-CreateOption</span></span>
<span data-ttu-id="2febd-127">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="2febd-127">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="2febd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2febd-128">-DefaultProfile</span></span>
<span data-ttu-id="2febd-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2febd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2febd-130">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2febd-130">-DiskEncryptionKey</span></span>
<span data-ttu-id="2febd-131">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-131">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="2febd-132">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="2febd-132">-DiskEncryptionSetId</span></span>
<span data-ttu-id="2febd-133">Especifica a ID do recurso do conjunto de criptografia de disco a ser usado para habilitar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="2febd-133">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="2febd-134">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="2febd-134">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="2febd-135">O número total de IOPS que serão permitidas em todas as VMs montando o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="2febd-135">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="2febd-136">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="2febd-136">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="2febd-137">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="2febd-137">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="2febd-138">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="2febd-138">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="2febd-139">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="2febd-139">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="2febd-140">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="2febd-140">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="2febd-141">"Descrição": "a taxa de transferência total (MBps) que será permitida em todas as VMs que montam o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="2febd-141">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="2febd-142">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="2febd-142">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="2febd-143">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="2febd-143">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="2febd-144">A largura de banda permitida para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="2febd-144">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="2febd-145">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="2febd-145">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="2febd-146">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2febd-146">-DiskSizeGB</span></span>
<span data-ttu-id="2febd-147">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="2febd-147">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="2febd-148">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="2febd-148">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="2febd-149">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="2febd-149">Enable encryption settings.</span></span>

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

### <span data-ttu-id="2febd-150">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="2febd-150">-DiskAccessId</span></span>
<span data-ttu-id="2febd-151">Obtém ou define a ID de braço do recurso DiskAccess para uso de pontos de extremidade privados em.</span><span class="sxs-lookup"><span data-stu-id="2febd-151">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="2febd-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2febd-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="2febd-153">A política de acesso à rede define a política de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="2febd-153">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="2febd-154">Os valores possíveis incluem: ' AllowAll ', ' AllowPrivate ', ' DenyAll '</span><span class="sxs-lookup"><span data-stu-id="2febd-154">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="2febd-155">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="2febd-155">-EncryptionType</span></span>
<span data-ttu-id="2febd-156">O tipo de chave usado para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-156">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="2febd-157">Os valores disponíveis são: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="2febd-157">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="2febd-158">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="2febd-158">-GalleryImageReference</span></span>
<span data-ttu-id="2febd-159">O objeto GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="2febd-159">The GalleryImageReference object.</span></span>  <span data-ttu-id="2febd-160">Obrigatório se estiver criando a partir de uma imagem de galeria.</span><span class="sxs-lookup"><span data-stu-id="2febd-160">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="2febd-161">A ID será a ID do braço da versão da imagem de galé compartilhada a partir da qual criar um disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-161">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="2febd-162">Um LUN será necessário se a origem da cópia for um dos discos de dados na imagem da Galeria; Se for NULL, o disco do sistema operacional da imagem será copiado.</span><span class="sxs-lookup"><span data-stu-id="2febd-162">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="2febd-163">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="2febd-163">-HyperVGeneration</span></span>
<span data-ttu-id="2febd-164">A geração de hipervisor da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2febd-164">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="2febd-165">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2febd-165">Applicable to OS disks only.</span></span>  <span data-ttu-id="2febd-166">Os valores permitidos são v1 e v2.</span><span class="sxs-lookup"><span data-stu-id="2febd-166">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="2febd-167">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="2febd-167">-ImageReference</span></span>
<span data-ttu-id="2febd-168">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-168">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="2febd-169">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2febd-169">-KeyEncryptionKey</span></span>
<span data-ttu-id="2febd-170">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-170">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="2febd-171">-Local</span><span class="sxs-lookup"><span data-stu-id="2febd-171">-Location</span></span>
<span data-ttu-id="2febd-172">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="2febd-172">Specifies a location.</span></span>

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

### <span data-ttu-id="2febd-173">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="2febd-173">-MaxSharesCount</span></span>
<span data-ttu-id="2febd-174">O número máximo de VMs que podem ser anexadas ao disco ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="2febd-174">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="2febd-175">O valor maior que um indica um disco que pode ser montado em várias VMs ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="2febd-175">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="2febd-176">-OsType</span><span class="sxs-lookup"><span data-stu-id="2febd-176">-OsType</span></span>
<span data-ttu-id="2febd-177">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="2febd-177">Specifies the OS type.</span></span>

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

### <span data-ttu-id="2febd-178">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2febd-178">-SkuName</span></span>
<span data-ttu-id="2febd-179">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2febd-179">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="2febd-180">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="2febd-180">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="2febd-181">UltraSSD_LRS só pode ser usado com um valor vazio para o parâmetro createoption.</span><span class="sxs-lookup"><span data-stu-id="2febd-181">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="2febd-182">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2febd-182">-SourceResourceId</span></span>
<span data-ttu-id="2febd-183">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="2febd-183">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="2febd-184">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="2febd-184">-SourceUri</span></span>
<span data-ttu-id="2febd-185">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="2febd-185">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="2febd-186">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2febd-186">-StorageAccountId</span></span>
<span data-ttu-id="2febd-187">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2febd-187">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="2febd-188">-Marca</span><span class="sxs-lookup"><span data-stu-id="2febd-188">-Tag</span></span>
<span data-ttu-id="2febd-189">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2febd-189">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2febd-190">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2febd-190">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2febd-191">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="2febd-191">-UploadSizeInBytes</span></span>
<span data-ttu-id="2febd-192">Especifica o tamanho do conteúdo do carregamento incluindo o rodapé do VHD quando createoption é carregado.</span><span class="sxs-lookup"><span data-stu-id="2febd-192">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="2febd-193">Esse valor deve estar entre 20972032 (20 MiB + 512 bytes para o rodapé VHD) e 35183298347520 bytes (32 TiB + 512 bytes para o rodapé VHD).</span><span class="sxs-lookup"><span data-stu-id="2febd-193">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="2febd-194">-Zone</span><span class="sxs-lookup"><span data-stu-id="2febd-194">-Zone</span></span>
<span data-ttu-id="2febd-195">Especifica a lista de zonas lógicas do disco.</span><span class="sxs-lookup"><span data-stu-id="2febd-195">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="2febd-196">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2febd-196">-Confirm</span></span>
<span data-ttu-id="2febd-197">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2febd-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2febd-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2febd-198">-WhatIf</span></span>
<span data-ttu-id="2febd-199">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2febd-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2febd-200">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2febd-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2febd-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2febd-201">CommonParameters</span></span>
<span data-ttu-id="2febd-202">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2febd-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2febd-203">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2febd-203">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2febd-204">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2febd-204">INPUTS</span></span>

### <span data-ttu-id="2febd-205">System. String</span><span class="sxs-lookup"><span data-stu-id="2febd-205">System.String</span></span>

### <span data-ttu-id="2febd-206">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2febd-206">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2febd-207">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2febd-207">System.Int32</span></span>

### <span data-ttu-id="2febd-208">System. String []</span><span class="sxs-lookup"><span data-stu-id="2febd-208">System.String[]</span></span>

### <span data-ttu-id="2febd-209">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2febd-209">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2febd-210">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="2febd-210">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="2febd-211">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2febd-211">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2febd-212">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="2febd-212">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="2febd-213">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="2febd-213">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="2febd-214">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2febd-214">OUTPUTS</span></span>

### <span data-ttu-id="2febd-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="2febd-215">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="2febd-216">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2febd-216">NOTES</span></span>

## <span data-ttu-id="2febd-217">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2febd-217">RELATED LINKS</span></span>
