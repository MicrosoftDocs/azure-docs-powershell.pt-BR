---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: a738ec606fc982573c4062879e9da4becee43df2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116244"
---
# <span data-ttu-id="5967c-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="5967c-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="5967c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5967c-102">SYNOPSIS</span></span>
<span data-ttu-id="5967c-103">Cria um objeto de atualização de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="5967c-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="5967c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5967c-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5967c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5967c-105">DESCRIPTION</span></span>
<span data-ttu-id="5967c-106">O cmdlet **New-AzDiskUpdateConfig** cria um objeto de atualização de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="5967c-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="5967c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5967c-107">EXAMPLES</span></span>

### <span data-ttu-id="5967c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5967c-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="5967c-109">O primeiro comando cria um objeto de atualização de disco vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5967c-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="5967c-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5967c-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="5967c-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="5967c-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="5967c-112">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5967c-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="5967c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5967c-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="5967c-114">Este comando atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="5967c-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="5967c-115">OS</span><span class="sxs-lookup"><span data-stu-id="5967c-115">PARAMETERS</span></span>

### <span data-ttu-id="5967c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5967c-116">-DefaultProfile</span></span>
<span data-ttu-id="5967c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5967c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5967c-118">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="5967c-118">-DiskAccessId</span></span>
<span data-ttu-id="5967c-119">{{Fill DiskAccessId descrição}}</span><span class="sxs-lookup"><span data-stu-id="5967c-119">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="5967c-120">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5967c-120">-DiskEncryptionKey</span></span>
<span data-ttu-id="5967c-121">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="5967c-121">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="5967c-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="5967c-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="5967c-123">Especifica a ID do recurso do conjunto de criptografia de disco a ser usado para habilitar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="5967c-123">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="5967c-124">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="5967c-124">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="5967c-125">O número total de IOPS que serão permitidas em todas as VMs montando o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="5967c-125">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5967c-126">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="5967c-126">One operation can transfer between 4k and 256k bytes.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5967c-127">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="5967c-127">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="5967c-128">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="5967c-128">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5967c-129">Uma operação pode ser transferida entre 4K e 256K de bytes.</span><span class="sxs-lookup"><span data-stu-id="5967c-129">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="5967c-130">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="5967c-130">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="5967c-131">A taxa de transferência total (MBps) que será permitida em todas as VMs montando o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="5967c-131">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="5967c-132">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="5967c-132">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5967c-133">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="5967c-133">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="5967c-134">A largura de banda permitida para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="5967c-134">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="5967c-135">MBps significa milhões de bytes por segundo-MB aqui usa a notação ISO, das potências de 10.</span><span class="sxs-lookup"><span data-stu-id="5967c-135">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="5967c-136">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="5967c-136">-DiskSizeGB</span></span>
<span data-ttu-id="5967c-137">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="5967c-137">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="5967c-138">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="5967c-138">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="5967c-139">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5967c-139">Enable encryption settings.</span></span>

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

### <span data-ttu-id="5967c-140">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="5967c-140">-EncryptionType</span></span>
<span data-ttu-id="5967c-141">O tipo de chave usado para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="5967c-141">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="5967c-142">Os valores disponíveis são: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="5967c-142">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="5967c-143">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5967c-143">-KeyEncryptionKey</span></span>
<span data-ttu-id="5967c-144">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="5967c-144">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="5967c-145">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="5967c-145">-MaxSharesCount</span></span>
<span data-ttu-id="5967c-146">O número máximo de VMs que podem ser anexadas ao disco ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="5967c-146">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="5967c-147">O valor maior que um indica um disco que pode ser montado em várias VMs ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="5967c-147">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5967c-148">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5967c-148">-NetworkAccessPolicy</span></span>
<span data-ttu-id="5967c-149">{{Fill NetworkAccessPolicy descrição}}</span><span class="sxs-lookup"><span data-stu-id="5967c-149">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="5967c-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="5967c-150">-OsType</span></span>
<span data-ttu-id="5967c-151">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5967c-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="5967c-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="5967c-152">-SkuName</span></span>
<span data-ttu-id="5967c-153">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5967c-153">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="5967c-154">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="5967c-154">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="5967c-155">UltraSSD_LRS só pode ser usado com um valor vazio para o parâmetro createoption.</span><span class="sxs-lookup"><span data-stu-id="5967c-155">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="5967c-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="5967c-156">-Tag</span></span>
<span data-ttu-id="5967c-157">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5967c-157">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5967c-158">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5967c-158">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5967c-159">-Tier</span><span class="sxs-lookup"><span data-stu-id="5967c-159">-Tier</span></span>
<span data-ttu-id="5967c-160">Camada de desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="5967c-160">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="5967c-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5967c-161">-Confirm</span></span>
<span data-ttu-id="5967c-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5967c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5967c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5967c-163">-WhatIf</span></span>
<span data-ttu-id="5967c-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5967c-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5967c-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5967c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5967c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5967c-166">CommonParameters</span></span>
<span data-ttu-id="5967c-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5967c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5967c-168">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5967c-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5967c-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5967c-169">INPUTS</span></span>

### <span data-ttu-id="5967c-170">System. String</span><span class="sxs-lookup"><span data-stu-id="5967c-170">System.String</span></span>

### <span data-ttu-id="5967c-171">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5967c-171">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5967c-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5967c-172">System.Int32</span></span>

### <span data-ttu-id="5967c-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5967c-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5967c-174">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5967c-174">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5967c-175">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="5967c-175">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="5967c-176">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="5967c-176">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="5967c-177">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5967c-177">OUTPUTS</span></span>

### <span data-ttu-id="5967c-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="5967c-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="5967c-179">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5967c-179">NOTES</span></span>

## <span data-ttu-id="5967c-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5967c-180">RELATED LINKS</span></span>
