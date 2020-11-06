---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 693d121bac5a618c5ad588cf4d34f63d8c6d0fd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603003"
---
# <span data-ttu-id="ff24a-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ff24a-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="ff24a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff24a-102">SYNOPSIS</span></span>
<span data-ttu-id="ff24a-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="ff24a-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff24a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff24a-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Zone <String[]>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff24a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff24a-105">DESCRIPTION</span></span>
<span data-ttu-id="ff24a-106">O cmdlet **New-AzureRmDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="ff24a-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="ff24a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff24a-107">EXAMPLES</span></span>

### <span data-ttu-id="ff24a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ff24a-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ff24a-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff24a-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="ff24a-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ff24a-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="ff24a-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="ff24a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="ff24a-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ff24a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ff24a-113">OS</span><span class="sxs-lookup"><span data-stu-id="ff24a-113">PARAMETERS</span></span>

### <span data-ttu-id="ff24a-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="ff24a-114">-CreateOption</span></span>
<span data-ttu-id="ff24a-115">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="ff24a-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="ff24a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff24a-116">-DefaultProfile</span></span>
<span data-ttu-id="ff24a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff24a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff24a-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ff24a-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="ff24a-119">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="ff24a-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="ff24a-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="ff24a-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="ff24a-121">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="ff24a-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ff24a-122">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="ff24a-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="ff24a-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="ff24a-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="ff24a-124">A largura de banda permitida para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="ff24a-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="ff24a-125">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="ff24a-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="ff24a-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="ff24a-126">-DiskSizeGB</span></span>
<span data-ttu-id="ff24a-127">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="ff24a-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="ff24a-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="ff24a-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="ff24a-129">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ff24a-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="ff24a-130">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="ff24a-130">-ImageReference</span></span>
<span data-ttu-id="ff24a-131">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="ff24a-131">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="ff24a-132">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ff24a-132">-KeyEncryptionKey</span></span>
<span data-ttu-id="ff24a-133">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="ff24a-133">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="ff24a-134">-Local</span><span class="sxs-lookup"><span data-stu-id="ff24a-134">-Location</span></span>
<span data-ttu-id="ff24a-135">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="ff24a-135">Specifies a location.</span></span>

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

### <span data-ttu-id="ff24a-136">-OsType</span><span class="sxs-lookup"><span data-stu-id="ff24a-136">-OsType</span></span>
<span data-ttu-id="ff24a-137">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ff24a-137">Specifies the OS type.</span></span>

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

### <span data-ttu-id="ff24a-138">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ff24a-138">-SkuName</span></span>
<span data-ttu-id="ff24a-139">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff24a-139">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="ff24a-140">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="ff24a-140">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="ff24a-141">UltraSSD_LRS só pode ser usado com um valor vazio para o parâmetro createoption.</span><span class="sxs-lookup"><span data-stu-id="ff24a-141">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="ff24a-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="ff24a-142">-SourceResourceId</span></span>
<span data-ttu-id="ff24a-143">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="ff24a-143">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="ff24a-144">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="ff24a-144">-SourceUri</span></span>
<span data-ttu-id="ff24a-145">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="ff24a-145">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="ff24a-146">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ff24a-146">-StorageAccountId</span></span>
<span data-ttu-id="ff24a-147">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ff24a-147">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="ff24a-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="ff24a-148">-Tag</span></span>
<span data-ttu-id="ff24a-149">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ff24a-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ff24a-150">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ff24a-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ff24a-151">-Zone</span><span class="sxs-lookup"><span data-stu-id="ff24a-151">-Zone</span></span>
<span data-ttu-id="ff24a-152">Especifica a lista de zonas lógicas do disco.</span><span class="sxs-lookup"><span data-stu-id="ff24a-152">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="ff24a-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ff24a-153">-Confirm</span></span>
<span data-ttu-id="ff24a-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff24a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff24a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff24a-155">-WhatIf</span></span>
<span data-ttu-id="ff24a-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ff24a-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff24a-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ff24a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff24a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff24a-158">CommonParameters</span></span>
<span data-ttu-id="ff24a-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff24a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff24a-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff24a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff24a-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff24a-161">INPUTS</span></span>

### <span data-ttu-id="ff24a-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ff24a-162">System.String</span></span>

### <span data-ttu-id="ff24a-163">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="ff24a-163">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="ff24a-164">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ff24a-164">System.Int32</span></span>

### <span data-ttu-id="ff24a-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="ff24a-165">System.String[]</span></span>

### <span data-ttu-id="ff24a-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ff24a-166">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ff24a-167">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="ff24a-167">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="ff24a-168">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ff24a-168">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ff24a-169">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="ff24a-169">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="ff24a-170">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="ff24a-170">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="ff24a-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff24a-171">OUTPUTS</span></span>

### <span data-ttu-id="ff24a-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="ff24a-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ff24a-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff24a-173">NOTES</span></span>

## <span data-ttu-id="ff24a-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff24a-174">RELATED LINKS</span></span>
