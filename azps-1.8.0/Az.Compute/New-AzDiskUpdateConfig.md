---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: 82bf5729758af61a08863a9eba84e95e54825dd0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771180"
---
# <span data-ttu-id="742ac-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="742ac-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="742ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="742ac-102">SYNOPSIS</span></span>
<span data-ttu-id="742ac-103">Cria um objeto de atualização de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="742ac-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="742ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="742ac-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>] [-DiskMBpsReadWrite <Int32>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="742ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="742ac-105">DESCRIPTION</span></span>
<span data-ttu-id="742ac-106">O cmdlet **New-AzDiskUpdateConfig** cria um objeto de atualização de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="742ac-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="742ac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="742ac-107">EXAMPLES</span></span>

### <span data-ttu-id="742ac-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="742ac-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="742ac-109">O primeiro comando cria um objeto de atualização de disco vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="742ac-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="742ac-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="742ac-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="742ac-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="742ac-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="742ac-112">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="742ac-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="742ac-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="742ac-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="742ac-114">Este comando atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="742ac-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="742ac-115">OS</span><span class="sxs-lookup"><span data-stu-id="742ac-115">PARAMETERS</span></span>

### <span data-ttu-id="742ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742ac-116">-DefaultProfile</span></span>
<span data-ttu-id="742ac-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="742ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="742ac-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="742ac-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="742ac-119">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="742ac-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="742ac-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="742ac-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="742ac-121">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="742ac-121">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="742ac-122">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="742ac-122">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="742ac-123">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="742ac-123">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="742ac-124">A largura de banda permitida para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="742ac-124">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="742ac-125">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="742ac-125">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="742ac-126">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="742ac-126">-DiskSizeGB</span></span>
<span data-ttu-id="742ac-127">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="742ac-127">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="742ac-128">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="742ac-128">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="742ac-129">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="742ac-129">Enable encryption settings.</span></span>

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

### <span data-ttu-id="742ac-130">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="742ac-130">-KeyEncryptionKey</span></span>
<span data-ttu-id="742ac-131">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="742ac-131">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="742ac-132">-OsType</span><span class="sxs-lookup"><span data-stu-id="742ac-132">-OsType</span></span>
<span data-ttu-id="742ac-133">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="742ac-133">Specifies the OS type.</span></span>

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

### <span data-ttu-id="742ac-134">-SkuName</span><span class="sxs-lookup"><span data-stu-id="742ac-134">-SkuName</span></span>
<span data-ttu-id="742ac-135">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="742ac-135">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="742ac-136">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="742ac-136">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="742ac-137">UltraSSD_LRS só pode ser usado com um valor vazio para o parâmetro createoption.</span><span class="sxs-lookup"><span data-stu-id="742ac-137">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="742ac-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="742ac-138">-Tag</span></span>
<span data-ttu-id="742ac-139">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="742ac-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="742ac-140">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="742ac-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="742ac-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="742ac-141">-Confirm</span></span>
<span data-ttu-id="742ac-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="742ac-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="742ac-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="742ac-143">-WhatIf</span></span>
<span data-ttu-id="742ac-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="742ac-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="742ac-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="742ac-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="742ac-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742ac-146">CommonParameters</span></span>
<span data-ttu-id="742ac-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742ac-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742ac-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742ac-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742ac-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="742ac-149">INPUTS</span></span>

### <span data-ttu-id="742ac-150">System. String</span><span class="sxs-lookup"><span data-stu-id="742ac-150">System.String</span></span>

### <span data-ttu-id="742ac-151">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="742ac-151">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="742ac-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="742ac-152">System.Int32</span></span>

### <span data-ttu-id="742ac-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="742ac-153">System.Collections.Hashtable</span></span>

### <span data-ttu-id="742ac-154">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="742ac-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="742ac-155">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="742ac-155">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="742ac-156">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="742ac-156">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="742ac-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="742ac-157">OUTPUTS</span></span>

### <span data-ttu-id="742ac-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="742ac-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="742ac-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="742ac-159">NOTES</span></span>

## <span data-ttu-id="742ac-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="742ac-160">RELATED LINKS</span></span>
