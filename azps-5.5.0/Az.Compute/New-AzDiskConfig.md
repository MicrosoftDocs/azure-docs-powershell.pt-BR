---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 12ebf45a0428b170f40edce6129d76dd7fcbd601
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112127"
---
# <span data-ttu-id="0b895-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="0b895-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="0b895-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b895-102">SYNOPSIS</span></span>
<span data-ttu-id="0b895-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="0b895-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="0b895-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b895-104">SYNTAX</span></span>

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

## <span data-ttu-id="0b895-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b895-105">DESCRIPTION</span></span>
<span data-ttu-id="0b895-106">O **cmdlet New-AzDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="0b895-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="0b895-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0b895-107">EXAMPLES</span></span>

### <span data-ttu-id="0b895-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0b895-108">Example 1</span></span>
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

<span data-ttu-id="0b895-109">O primeiro comando cria um objeto de disco vazio local com tamanho de 5 GB Standard_LRS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b895-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="0b895-110">Ele também define o tipo do sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="0b895-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="0b895-111">O segundo e o terceiro comandos configuram a chave de criptografia de disco e as configurações da chave de criptografia do objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="0b895-112">O último comando assume o objeto de disco e cria um disco com o nome 'Disco01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="0b895-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="0b895-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0b895-113">Example 2</span></span>
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

<span data-ttu-id="0b895-114">O primeiro comando cria um objeto de disco local para Carregar.</span><span class="sxs-lookup"><span data-stu-id="0b895-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="0b895-115">O segundo comando assume o objeto de disco e cria um disco com o nome 'Disco01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="0b895-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="0b895-116">O terceiro comando obtém a Url do SAS para o disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="0b895-117">O quarto comando obtém o estado do disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="0b895-118">Se o estado do disco for 'ReadyToUpload', um usuário poderá carregar um disco do armazenamento de blob para a URL do SAS de disco usando o AzCopy.</span><span class="sxs-lookup"><span data-stu-id="0b895-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="0b895-119">Durante o carregamento, o estado do disco é alterado para "ActiveUpload".</span><span class="sxs-lookup"><span data-stu-id="0b895-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="0b895-120">O último comando revoga o acesso a disco para a URL do SAS.</span><span class="sxs-lookup"><span data-stu-id="0b895-120">The last command revokes the disk access for the SAS Url.</span></span>

### <span data-ttu-id="0b895-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0b895-121">Example 3</span></span>
```
PS C:\> $galleryImageReference = @{Id = '/subscriptions/0296790d-427c-48ca-b204-8b729bbd8670/resourceGroups/swaggertests/providers/Microsoft.Compute/galleries/swaggergallery/images/swaggerimagedef/versions/1.0.0'; Lun=1}
PS C:\> $diskConfig = New-AzDiskConfig -Location 'West US' -CreateOption 'FromImage' -GalleryImageReference $galleryImageReference;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskConfig
```

<span data-ttu-id="0b895-122">Criar um disco a partir de uma Versão de Imagem da Galeria Compartilhada.</span><span class="sxs-lookup"><span data-stu-id="0b895-122">Create a disk from a Shared Gallery Image Version.</span></span>  <span data-ttu-id="0b895-123">A ID é a ID da versão da imagem da galeria compartilhada.</span><span class="sxs-lookup"><span data-stu-id="0b895-123">Id is the id of the shared gallery image version.</span></span> <span data-ttu-id="0b895-124">Só será necessário se a fonte for um disco de dados.</span><span class="sxs-lookup"><span data-stu-id="0b895-124">Lun is needed only if the source is a data disk.</span></span>

## <span data-ttu-id="0b895-125">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b895-125">PARAMETERS</span></span>

### <span data-ttu-id="0b895-126">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="0b895-126">-BurstingEnabled</span></span>
<span data-ttu-id="0b895-127">Habilita o estouro além da meta de desempenho provisionada do disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-127">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="0b895-128">A explosão é desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="0b895-128">Bursting is disabled by default.</span></span> <span data-ttu-id="0b895-129">Não se aplica a discos Ultra.</span><span class="sxs-lookup"><span data-stu-id="0b895-129">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="0b895-130">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="0b895-130">-CreateOption</span></span>
<span data-ttu-id="0b895-131">Especifica se esse cmdlet cria um disco no computador virtual a partir de uma plataforma ou imagem do usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="0b895-131">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="0b895-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b895-132">-DefaultProfile</span></span>
<span data-ttu-id="0b895-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0b895-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b895-134">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="0b895-134">-DiskAccessId</span></span>
<span data-ttu-id="0b895-135">Obtém ou define a ID ARM do recurso DiskAccess para usar pontos de extremidade particulares.</span><span class="sxs-lookup"><span data-stu-id="0b895-135">Gets or sets ARM ID of the DiskAccess resource for using private endpoints on.</span></span>


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

### <span data-ttu-id="0b895-136">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0b895-136">-DiskEncryptionKey</span></span>
<span data-ttu-id="0b895-137">Especifica o objeto da chave de criptografia de disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-137">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="0b895-138">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="0b895-138">-DiskEncryptionSetId</span></span>
<span data-ttu-id="0b895-139">Especifica a ID de recurso do conjunto de criptografia de disco que deve ser usado para habilenciar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="0b895-139">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="0b895-140">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="0b895-140">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="0b895-141">O número total de IOPS que será permitido em todos os VMs que montarem o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="0b895-141">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="0b895-142">Uma operação pode transferir entre 4k e 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="0b895-142">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="0b895-143">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b895-143">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="0b895-144">O número de IOPS permitido para este disco; somente de tabela definida para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="0b895-144">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="0b895-145">Uma operação pode transferir entre 4k e 256k bytes.</span><span class="sxs-lookup"><span data-stu-id="0b895-145">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="0b895-146">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="0b895-146">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="0b895-147">"descrição": "A produtividade total (MBps) que será permitida em todos os VMs que montarem o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="0b895-147">"description": "The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="0b895-148">MBps significa milhões de bytes por segundo - MB aqui usa a notação ISO, de potências de 10.</span><span class="sxs-lookup"><span data-stu-id="0b895-148">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="0b895-149">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="0b895-149">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="0b895-150">A largura de banda permitida para esse disco; somente de tabela definida para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="0b895-150">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="0b895-151">MBps significa milhões de bytes por segundo - MB aqui usa a notação ISO, de potências de 10.</span><span class="sxs-lookup"><span data-stu-id="0b895-151">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="0b895-152">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0b895-152">-DiskSizeGB</span></span>
<span data-ttu-id="0b895-153">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="0b895-153">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="0b895-154">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="0b895-154">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="0b895-155">Habilitar configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="0b895-155">Enable encryption settings.</span></span>

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

### <span data-ttu-id="0b895-156">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="0b895-156">-EncryptionType</span></span>
<span data-ttu-id="0b895-157">O tipo de chave usada para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-157">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="0b895-158">Os valores disponíveis são: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="0b895-158">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="0b895-159">-GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="0b895-159">-GalleryImageReference</span></span>
<span data-ttu-id="0b895-160">O objeto GalleryImageReference.</span><span class="sxs-lookup"><span data-stu-id="0b895-160">The GalleryImageReference object.</span></span>  <span data-ttu-id="0b895-161">Obrigatório ao criar a partir de uma Imagem da Galeria.</span><span class="sxs-lookup"><span data-stu-id="0b895-161">Required if creating from a Gallery Image.</span></span> <span data-ttu-id="0b895-162">A id será a ID arm da versão de imagem compartilhada da qual se cria um disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-162">The id will be the ARM id of the shared galley image version from which to create a disk.</span></span>
<span data-ttu-id="0b895-163">Um problema será necessário se a origem da cópia for um dos discos de dados na imagem da galeria; se nulo, o disco do sistema operacional da imagem será copiado.</span><span class="sxs-lookup"><span data-stu-id="0b895-163">A lun is needed if the source of the copy is one of the data disks in the gallery image; if null, the OS disk of the image will be copied.</span></span>

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

### <span data-ttu-id="0b895-164">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="0b895-164">-HyperVGeneration</span></span>
<span data-ttu-id="0b895-165">A geração de hipervisor da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="0b895-165">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="0b895-166">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0b895-166">Applicable to OS disks only.</span></span>  <span data-ttu-id="0b895-167">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="0b895-167">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="0b895-168">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="0b895-168">-ImageReference</span></span>
<span data-ttu-id="0b895-169">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-169">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="0b895-170">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0b895-170">-KeyEncryptionKey</span></span>
<span data-ttu-id="0b895-171">Especifica a chave de criptografia chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-171">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="0b895-172">-Local</span><span class="sxs-lookup"><span data-stu-id="0b895-172">-Location</span></span>
<span data-ttu-id="0b895-173">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="0b895-173">Specifies a location.</span></span>

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

### <span data-ttu-id="0b895-174">-LogicalSectorSize</span><span class="sxs-lookup"><span data-stu-id="0b895-174">-LogicalSectorSize</span></span>
<span data-ttu-id="0b895-175">Tamanho do setor lógico em bytes para discos Ultra.</span><span class="sxs-lookup"><span data-stu-id="0b895-175">Logical sector size in bytes for Ultra disks.</span></span> 

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

### <span data-ttu-id="0b895-176">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="0b895-176">-MaxSharesCount</span></span>
<span data-ttu-id="0b895-177">O número máximo de VMs que podem ser anexadas ao disco ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="0b895-177">The maximum number of VMs that can attach to the disk at the same time.</span></span>
<span data-ttu-id="0b895-178">Valor maior que um indica um disco que pode ser montado em várias VMs ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="0b895-178">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="0b895-179">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b895-179">-NetworkAccessPolicy</span></span>
<span data-ttu-id="0b895-180">A política de acesso à rede define a política de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="0b895-180">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="0b895-181">Os valores possíveis incluem: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="0b895-181">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="0b895-182">-OsType</span><span class="sxs-lookup"><span data-stu-id="0b895-182">-OsType</span></span>
<span data-ttu-id="0b895-183">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0b895-183">Specifies the OS type.</span></span>

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

### <span data-ttu-id="0b895-184">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0b895-184">-SkuName</span></span>
<span data-ttu-id="0b895-185">Especifica o nome SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b895-185">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="0b895-186">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="0b895-186">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="0b895-187">UltraSSD_LRS só pode ser usado com valor vazio para o parâmetro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="0b895-187">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="0b895-188">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="0b895-188">-SourceResourceId</span></span>
<span data-ttu-id="0b895-189">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="0b895-189">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="0b895-190">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="0b895-190">-SourceUri</span></span>
<span data-ttu-id="0b895-191">Especifica o Uri de origem.</span><span class="sxs-lookup"><span data-stu-id="0b895-191">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="0b895-192">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0b895-192">-StorageAccountId</span></span>
<span data-ttu-id="0b895-193">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b895-193">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="0b895-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b895-194">-Tag</span></span>
<span data-ttu-id="0b895-195">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="0b895-195">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0b895-196">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0b895-196">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0b895-197">-Tier</span><span class="sxs-lookup"><span data-stu-id="0b895-197">-Tier</span></span>
<span data-ttu-id="0b895-198">Nível de desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-198">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="0b895-199">-UploadSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="0b895-199">-UploadSizeInBytes</span></span>
<span data-ttu-id="0b895-200">Especifica o tamanho do conteúdo do carregamento, incluindo o rodapé DAD quando CreateOption é Carregado.</span><span class="sxs-lookup"><span data-stu-id="0b895-200">Specifies the size of the contents of the upload including the VHD footer when CreateOption is Upload.</span></span>  <span data-ttu-id="0b895-201">Esse valor deve estar entre 20972032 (20 MiB + 512 bytes para o rodapé EMOD) e 35183298347520 bytes (32 TiB + 512 bytes para o rodapé DAD).</span><span class="sxs-lookup"><span data-stu-id="0b895-201">This value should be between 20972032 (20 MiB + 512 bytes for the VHD footer) and 35183298347520 bytes (32 TiB + 512 bytes for the VHD footer).</span></span>

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

### <span data-ttu-id="0b895-202">-Zona</span><span class="sxs-lookup"><span data-stu-id="0b895-202">-Zone</span></span>
<span data-ttu-id="0b895-203">Especifica a lista de zonas lógicas para Disco.</span><span class="sxs-lookup"><span data-stu-id="0b895-203">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="0b895-204">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0b895-204">-Confirm</span></span>
<span data-ttu-id="0b895-205">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b895-205">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b895-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b895-206">-WhatIf</span></span>
<span data-ttu-id="0b895-207">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0b895-207">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b895-208">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0b895-208">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b895-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b895-209">CommonParameters</span></span>
<span data-ttu-id="0b895-210">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b895-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b895-211">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b895-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b895-212">Entradas</span><span class="sxs-lookup"><span data-stu-id="0b895-212">INPUTS</span></span>

### <span data-ttu-id="0b895-213">System.String</span><span class="sxs-lookup"><span data-stu-id="0b895-213">System.String</span></span>

### <span data-ttu-id="0b895-214">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="0b895-214">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="0b895-215">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0b895-215">System.Int32</span></span>

### <span data-ttu-id="0b895-216">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0b895-216">System.String[]</span></span>

### <span data-ttu-id="0b895-217">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b895-217">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0b895-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="0b895-218">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="0b895-219">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0b895-219">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0b895-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSeciliReference</span><span class="sxs-lookup"><span data-stu-id="0b895-220">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="0b895-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="0b895-221">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="0b895-222">Saídas</span><span class="sxs-lookup"><span data-stu-id="0b895-222">OUTPUTS</span></span>

### <span data-ttu-id="0b895-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="0b895-223">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="0b895-224">Notas</span><span class="sxs-lookup"><span data-stu-id="0b895-224">NOTES</span></span>

## <span data-ttu-id="0b895-225">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b895-225">RELATED LINKS</span></span>
