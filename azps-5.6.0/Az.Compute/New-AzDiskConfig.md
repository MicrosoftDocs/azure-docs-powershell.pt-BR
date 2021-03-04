---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 34caab92645f610ed6ed71d907639060cf0c456a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886088"
---
# <span data-ttu-id="af928-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="af928-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="af928-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af928-102">SYNOPSIS</span></span>
<span data-ttu-id="af928-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="af928-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="af928-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="af928-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [-Tier <String>] [-LogicalSectorSize <Int32>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Location] <String>]
 [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>]
 [-DiskIOPSReadOnly <Int64>] [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-Tag <Hashtable>]
 [-CreateOption <String>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-GalleryImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-UploadSizeInBytes <Int64>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-BurstingEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af928-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="af928-105">DESCRIPTION</span></span>
<span data-ttu-id="af928-106">O cmdlet **New-AzDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="af928-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="af928-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="af928-107">EXAMPLES</span></span>

### <span data-ttu-id="af928-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="af928-108">Example 1</span></span>
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

<span data-ttu-id="af928-109">O primeiro comando cria um objeto de disco vazio local com tamanho de 5 GB Standard_LRS de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="af928-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="af928-110">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="af928-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="af928-111">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="af928-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="af928-112">O último comando pega o objeto de disco e cria um disco com o nome 'Disk01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="af928-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="af928-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="af928-113">Example 2</span></span>
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

<span data-ttu-id="af928-114">O primeiro comando cria um objeto de disco local para Upload.</span><span class="sxs-lookup"><span data-stu-id="af928-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="af928-115">O segundo comando pega o objeto de disco e cria um disco com o nome 'Disk01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="af928-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="af928-116">O terceiro comando obtém a Url do SAS para o disco.</span><span class="sxs-lookup"><span data-stu-id="af928-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="af928-117">O quarto comando obtém o estado do disco.</span><span class="sxs-lookup"><span data-stu-id="af928-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="af928-118">Se o estado do disco for 'ReadyToUpload', um usuário poderá carregar um disco do armazenamento blob na Url do SAS de disco usando o AzCopy.</span><span class="sxs-lookup"><span data-stu-id="af928-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="af928-119">Durante o carregamento, o estado do disco é alterado para 'ActiveUpload'.</span><span class="sxs-lookup"><span data-stu-id="af928-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="af928-120">O último comando revoga o acesso ao disco para a Url do SAS.</span><span class="sxs-lookup"><span data-stu-id="af928-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="af928-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="af928-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="af928-122">Crie um disco a partir de uma Versão de Imagem de Galeria Compartilhada.</span><span class="sxs-lookup"><span data-stu-id="af928-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="af928-123">Id é a id da versão da imagem da galeria compartilhada.</span><span class="sxs-lookup"><span data-stu-id="af928-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="af928-124">Lun só será necessário se a origem for um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="af928-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="af928-125">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="af928-125">PARAMETERS</span></span>

### <span data-ttu-id="af928-126">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="af928-126">-BurstingEnabled</span></span>
<span data-ttu-id="af928-127">Habilita o estouro além do destino de desempenho provisionado do disco.</span><span class="sxs-lookup"><span data-stu-id="af928-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="af928-128">O estouro está desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="af928-128">Bursting is disabled by default.</span></span> <span data-ttu-id="af928-129">Não se aplica a discos Ultra.</span><span class="sxs-lookup"><span data-stu-id="af928-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="af928-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="af928-130">-CreateOption</span></span>
<span data-ttu-id="af928-131">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="af928-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="af928-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af928-132">-DefaultProfile</span></span>
<span data-ttu-id="af928-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="af928-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af928-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="af928-134">-DiskAccessId</span></span>
<span data-ttu-id="af928-135">Obtém ou define ARM ID do recurso DiskAccess para usar pontos de extremidade privados.</span><span class="sxs-lookup"><span data-stu-id="af928-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="af928-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="af928-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="af928-137">Especifica o objeto chave de criptografia de disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="af928-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="af928-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="af928-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="af928-139">Especifica a ID de recurso do conjunto de criptografia de disco a ser usado para habilenciar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="af928-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="af928-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="af928-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="af928-141">O número total de IOPS que será permitido em todas as VMs que montam o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="af928-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="af928-142">Uma operação pode transferir entre 4k e 256 mil bytes.</span><span class="sxs-lookup"><span data-stu-id="af928-142">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="af928-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="af928-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="af928-144">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="af928-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="af928-145">Uma operação pode transferir entre 4k e 256 mil bytes.</span><span class="sxs-lookup"><span data-stu-id="af928-145">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="af928-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="af928-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="af928-147">"description": "A produtividade total (MBps) que será permitida em todas as VMs que montam o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="af928-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="af928-148">MBps significa milhões de bytes por segundo - MB aqui usa a notação ISO, de potências de 10.</span><span class="sxs-lookup"><span data-stu-id="af928-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="af928-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="af928-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="af928-150">A largura de banda permitida para esse disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="af928-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="af928-151">MBps significa milhões de bytes por segundo - MB aqui usa a notação ISO, de potências de 10.</span><span class="sxs-lookup"><span data-stu-id="af928-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="af928-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="af928-152">-DiskSizeGB</span></span>
<span data-ttu-id="af928-153">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="af928-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="af928-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="af928-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="af928-155">Habilitar configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="af928-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="af928-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="af928-156">-EncryptionType</span></span>
<span data-ttu-id="af928-157">O tipo de chave usada para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="af928-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="af928-158">Os valores disponíveis são: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="af928-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="af928-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="af928-159">-GalleryImageReference</span></span>
<span data-ttu-id="af928-160">O objeto GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="af928-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="af928-161">Obrigatório se estiver criando a partir de uma Imagem de Galeria.</span><span class="sxs-lookup"><span data-stu-id="af928-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="af928-162">A id será a ARM id da versão da imagem de galés compartilhada da qual criar um disco.</span><span class="sxs-lookup"><span data-stu-id="af928-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="af928-163">Um lun é necessário se a origem da cópia for um dos discos de dados na imagem da galeria; se nulo, o disco do sistema operacional da imagem será copiado.</span><span class="sxs-lookup"><span data-stu-id="af928-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="af928-164">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="af928-164">-HyperVGeneration</span></span>
<span data-ttu-id="af928-165">A geração do hipervisor da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="af928-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="af928-166">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="af928-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="af928-167">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="af928-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="af928-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="af928-168">-ImageReference</span></span>
<span data-ttu-id="af928-169">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="af928-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="af928-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="af928-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="af928-171">Especifica a chave de criptografia Key em um disco.</span><span class="sxs-lookup"><span data-stu-id="af928-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="af928-172">-Location</span><span class="sxs-lookup"><span data-stu-id="af928-172">-Location</span></span>
<span data-ttu-id="af928-173">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="af928-173">Specifies a location.</span></span>

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

### <span data-ttu-id="af928-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="af928-174">-LogicalSectorSize</span></span>
<span data-ttu-id="af928-175">Tamanho do setor lógico em bytes para discos Ultra.</span><span class="sxs-lookup"><span data-stu-id="af928-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="af928-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="af928-176">-MaxSharesCount</span></span>
<span data-ttu-id="af928-177">O número máximo de VMs que podem ser anexadas ao disco ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="af928-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="af928-178">Valor maior que um indica um disco que pode ser montado em várias VMs ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="af928-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="af928-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="af928-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="af928-180">A política de acesso à rede define a política de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="af928-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="af928-181">Os valores possíveis incluem: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="af928-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="af928-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="af928-182">-OsType</span></span>
<span data-ttu-id="af928-183">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="af928-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="af928-184">-SkuName</span><span class="sxs-lookup"><span data-stu-id="af928-184">-SkuName</span></span>
<span data-ttu-id="af928-185">Especifica o nome Sku da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="af928-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="af928-186">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="af928-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="af928-187">UltraSSD_LRS pode ser usado apenas com valor vazio para o parâmetro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="af928-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="af928-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="af928-188">-SourceResourceId</span></span>
<span data-ttu-id="af928-189">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="af928-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="af928-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="af928-190">-SourceUri</span></span>
<span data-ttu-id="af928-191">Especifica o Uri de origem.</span><span class="sxs-lookup"><span data-stu-id="af928-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="af928-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="af928-192">-StorageAccountId</span></span>
<span data-ttu-id="af928-193">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="af928-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="af928-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="af928-194">-Tag</span></span>
<span data-ttu-id="af928-195">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="af928-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="af928-196">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="af928-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="af928-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="af928-197">-Tier</span></span>
<span data-ttu-id="af928-198">Camada de desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="af928-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="af928-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="af928-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="af928-200">Especifica o tamanho do conteúdo do carregamento, incluindo o rodapé VHD quando CreateOption é Upload.</span><span class="sxs-lookup"><span data-stu-id="af928-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="af928-201">Esse valor deve estar entre 20972032 (20 MiB + 512 bytes para o rodapé VHD) e 35183298347520 bytes (32 TiB + 512 bytes para o rodapé VHD).</span><span class="sxs-lookup"><span data-stu-id="af928-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="af928-202">-Zone</span><span class="sxs-lookup"><span data-stu-id="af928-202">-Zone</span></span>
<span data-ttu-id="af928-203">Especifica a lista de zonas lógicas para Disco.</span><span class="sxs-lookup"><span data-stu-id="af928-203">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="af928-204">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af928-204">-Confirm</span></span>
<span data-ttu-id="af928-205">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af928-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af928-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af928-206">-WhatIf</span></span>
<span data-ttu-id="af928-207">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="af928-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af928-208">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="af928-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af928-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af928-209">CommonParameters</span></span>
<span data-ttu-id="af928-210">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af928-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af928-211">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af928-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af928-212">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af928-212">INPUTS</span></span>

### <span data-ttu-id="af928-213">System.String</span><span class="sxs-lookup"><span data-stu-id="af928-213">System.String</span></span>

### <span data-ttu-id="af928-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="af928-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="af928-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="af928-215">System.Int32</span></span>

### <span data-ttu-id="af928-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="af928-216">System.String[]</span></span>

### <span data-ttu-id="af928-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="af928-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="af928-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="af928-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="af928-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="af928-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="af928-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="af928-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="af928-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="af928-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="af928-222">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="af928-222">OUTPUTS</span></span>

### <span data-ttu-id="af928-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="af928-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="af928-224">NOTES</span><span class="sxs-lookup"><span data-stu-id="af928-224">NOTES</span></span>

## <span data-ttu-id="af928-225">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="af928-225">RELATED LINKS</span></span>
