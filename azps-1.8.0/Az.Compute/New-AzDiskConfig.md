---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 273a4388665e12cf58d1fe2d7e067648862bf4ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601319"
---
# <span data-ttu-id="c4d8d-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="c4d8d-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="c4d8d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d8d-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="c4d8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4d8d-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-HyperVGeneration <String>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4d8d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4d8d-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d8d-106">O cmdlet **New-AzDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="c4d8d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4d8d-107">EXAMPLES</span></span>

### <span data-ttu-id="c4d8d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c4d8d-108">Example 1</span></span>
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

<span data-ttu-id="c4d8d-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="c4d8d-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="c4d8d-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="c4d8d-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c4d8d-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c4d8d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c4d8d-113">Example 2</span></span>
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

<span data-ttu-id="c4d8d-114">O primeiro comando cria um objeto de disco local para carregamento.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-114">The first command creates a local disk object for Upload.</span></span>
<span data-ttu-id="c4d8d-115">O segundo comando leva o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c4d8d-115">The second command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>
<span data-ttu-id="c4d8d-116">O terceiro comando obtém a URL SAS para o disco.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-116">The third command gets SAS Url for the disk.</span></span>
<span data-ttu-id="c4d8d-117">O quarto comando obtém o estado do disco.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-117">The fourth command gets the state of the disk.</span></span>
<span data-ttu-id="c4d8d-118">Se o estado do disco for ' ReadyToUpload ', um usuário pode carregar um disco do armazenamento de BLOB para a URL SAS de disco usando AzCopy.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-118">If the disk state is 'ReadyToUpload', a user can upload a disk from blob storage to the disk SAS Url using AzCopy.</span></span>
<span data-ttu-id="c4d8d-119">Durante o upload, o estado do disco é alterado para ' ActiveUpload '.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-119">During uploading, the disk state is changed to 'ActiveUpload'.</span></span>
<span data-ttu-id="c4d8d-120">O último comando revoga o acesso ao disco para a URL SAS.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-120">The last command revokes the disk access for the SAS Url.</span></span>

## <span data-ttu-id="c4d8d-121">OS</span><span class="sxs-lookup"><span data-stu-id="c4d8d-121">PARAMETERS</span></span>

### <span data-ttu-id="c4d8d-122">-Createoption</span><span class="sxs-lookup"><span data-stu-id="c4d8d-122">-CreateOption</span></span>
<span data-ttu-id="c4d8d-123">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-123">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="c4d8d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d8d-124">-DefaultProfile</span></span>
<span data-ttu-id="c4d8d-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4d8d-126">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c4d8d-126">-DiskEncryptionKey</span></span>
<span data-ttu-id="c4d8d-127">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-127">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="c4d8d-128">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="c4d8d-128">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="c4d8d-129">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-129">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="c4d8d-130">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="c4d8d-131">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="c4d8d-131">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="c4d8d-132">A largura de banda permitida para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-132">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="c4d8d-133">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-133">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="c4d8d-134">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c4d8d-134">-DiskSizeGB</span></span>
<span data-ttu-id="c4d8d-135">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-135">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="c4d8d-136">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="c4d8d-136">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="c4d8d-137">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-137">Enable encryption settings.</span></span>

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

### <span data-ttu-id="c4d8d-138">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="c4d8d-138">-HyperVGeneration</span></span>
<span data-ttu-id="c4d8d-139">A geração de hipervisor da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-139">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="c4d8d-140">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-140">Applicable to OS disks only.</span></span>  <span data-ttu-id="c4d8d-141">Os valores permitidos são v1 e v2.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-141">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="c4d8d-142">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="c4d8d-142">-ImageReference</span></span>
<span data-ttu-id="c4d8d-143">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-143">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="c4d8d-144">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c4d8d-144">-KeyEncryptionKey</span></span>
<span data-ttu-id="c4d8d-145">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-145">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="c4d8d-146">-Local</span><span class="sxs-lookup"><span data-stu-id="c4d8d-146">-Location</span></span>
<span data-ttu-id="c4d8d-147">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-147">Specifies a location.</span></span>

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

### <span data-ttu-id="c4d8d-148">-OsType</span><span class="sxs-lookup"><span data-stu-id="c4d8d-148">-OsType</span></span>
<span data-ttu-id="c4d8d-149">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-149">Specifies the OS type.</span></span>

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

### <span data-ttu-id="c4d8d-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c4d8d-150">-SkuName</span></span>
<span data-ttu-id="c4d8d-151">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-151">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="c4d8d-152">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-152">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="c4d8d-153">UltraSSD_LRS só pode ser usado com um valor vazio para o parâmetro createoption.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-153">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="c4d8d-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="c4d8d-154">-SourceResourceId</span></span>
<span data-ttu-id="c4d8d-155">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-155">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="c4d8d-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="c4d8d-156">-SourceUri</span></span>
<span data-ttu-id="c4d8d-157">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="c4d8d-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c4d8d-158">-StorageAccountId</span></span>
<span data-ttu-id="c4d8d-159">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="c4d8d-160">-Marca</span><span class="sxs-lookup"><span data-stu-id="c4d8d-160">-Tag</span></span>
<span data-ttu-id="c4d8d-161">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c4d8d-162">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c4d8d-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c4d8d-163">-Zone</span><span class="sxs-lookup"><span data-stu-id="c4d8d-163">-Zone</span></span>
<span data-ttu-id="c4d8d-164">Especifica a lista de zonas lógicas do disco.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-164">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="c4d8d-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4d8d-165">-Confirm</span></span>
<span data-ttu-id="c4d8d-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d8d-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d8d-167">-WhatIf</span></span>
<span data-ttu-id="c4d8d-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4d8d-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d8d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d8d-170">CommonParameters</span></span>
<span data-ttu-id="c4d8d-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d8d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d8d-172">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d8d-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d8d-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4d8d-173">INPUTS</span></span>

### <span data-ttu-id="c4d8d-174">System. String</span><span class="sxs-lookup"><span data-stu-id="c4d8d-174">System.String</span></span>

### <span data-ttu-id="c4d8d-175">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c4d8d-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c4d8d-176">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c4d8d-176">System.Int32</span></span>

### <span data-ttu-id="c4d8d-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="c4d8d-177">System.String[]</span></span>

### <span data-ttu-id="c4d8d-178">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c4d8d-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="c4d8d-179">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="c4d8d-179">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="c4d8d-180">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c4d8d-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c4d8d-181">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="c4d8d-181">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="c4d8d-182">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="c4d8d-182">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="c4d8d-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4d8d-183">OUTPUTS</span></span>

### <span data-ttu-id="c4d8d-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="c4d8d-184">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="c4d8d-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4d8d-185">NOTES</span></span>

## <span data-ttu-id="c4d8d-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4d8d-186">RELATED LINKS</span></span>
