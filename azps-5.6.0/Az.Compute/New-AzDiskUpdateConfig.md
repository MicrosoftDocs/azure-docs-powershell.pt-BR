---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskUpdateConfig.md
ms.openlocfilehash: e73a6bc0d1bf1d2930396bce779bcb03f91d9936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886084"
---
# <span data-ttu-id="20098-101">New-AzDiskUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="20098-101">New-AzDiskUpdateConfig</span></span>

## <span data-ttu-id="20098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20098-102">SYNOPSIS</span></span>
<span data-ttu-id="20098-103">Cria um objeto de atualização de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="20098-103">Creates a configurable disk update object.</span></span>

## <span data-ttu-id="20098-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20098-104">SYNTAX</span></span>

```
New-AzDiskUpdateConfig [[-SkuName] <String>] [-Tier <String>] [-DiskIOPSReadOnly <Int64>]
 [-DiskMBpsReadOnly <Int64>] [-MaxSharesCount <Int32>] [-NetworkAccessPolicy <String>] [-DiskAccessId <String>]
 [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-DiskIOPSReadWrite <Int32>]
 [-DiskMBpsReadWrite <Int32>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [-BurstingEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20098-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20098-105">DESCRIPTION</span></span>
<span data-ttu-id="20098-106">O cmdlet **New-AzDiskUpdateConfig** cria um objeto de atualização de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="20098-106">The **New-AzDiskUpdateConfig** cmdlet creates a configurable disk update object.</span></span>

## <span data-ttu-id="20098-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20098-107">EXAMPLES</span></span>

### <span data-ttu-id="20098-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20098-108">Example 1</span></span>
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

<span data-ttu-id="20098-109">O primeiro comando cria um objeto de atualização de disco vazio local com tamanho de 10 GB Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20098-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="20098-110">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="20098-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="20098-111">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="20098-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="20098-112">O último comando pega o objeto de atualização de disco e atualiza um disco existente com o nome 'Disk01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="20098-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="20098-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="20098-113">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="20098-114">Este comando atualiza um disco existente com o nome 'Disk01' no grupo de recursos 'ResourceGroup01' para o tamanho do disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="20098-114">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="20098-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20098-115">PARAMETERS</span></span>

### <span data-ttu-id="20098-116">-BurstingEnabled</span><span class="sxs-lookup"><span data-stu-id="20098-116">-BurstingEnabled</span></span>
<span data-ttu-id="20098-117">Habilita o estouro além do destino de desempenho provisionado do disco.</span><span class="sxs-lookup"><span data-stu-id="20098-117">Enables bursting beyond the provisioned performance target of the disk.</span></span> <span data-ttu-id="20098-118">O estouro está desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="20098-118">Bursting is disabled by default.</span></span> <span data-ttu-id="20098-119">Não se aplica a discos Ultra.</span><span class="sxs-lookup"><span data-stu-id="20098-119">Does not apply to Ultra disks.</span></span>

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

### <span data-ttu-id="20098-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20098-120">-DefaultProfile</span></span>
<span data-ttu-id="20098-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="20098-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20098-122">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="20098-122">-DiskAccessId</span></span>
<span data-ttu-id="20098-123">{{ Fill DiskAccessId Description }}</span><span class="sxs-lookup"><span data-stu-id="20098-123">{{ Fill DiskAccessId Description }}</span></span>

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

### <span data-ttu-id="20098-124">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="20098-124">-DiskEncryptionKey</span></span>
<span data-ttu-id="20098-125">Especifica o objeto chave de criptografia de disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="20098-125">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="20098-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="20098-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="20098-127">Especifica a ID de recurso do conjunto de criptografia de disco a ser usado para habilenciar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="20098-127">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="20098-128">-DiskIOPSReadOnly</span><span class="sxs-lookup"><span data-stu-id="20098-128">-DiskIOPSReadOnly</span></span>
<span data-ttu-id="20098-129">O número total de IOPS que será permitido em todas as VMs que montam o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="20098-129">The total number of IOPS that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="20098-130">Uma operação pode transferir entre 4k e 256 mil bytes.</span><span class="sxs-lookup"><span data-stu-id="20098-130">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="20098-131">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="20098-131">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="20098-132">O número de IOPS permitidos para este disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="20098-132">The number of IOPS allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="20098-133">Uma operação pode transferir entre 4k e 256 mil bytes.</span><span class="sxs-lookup"><span data-stu-id="20098-133">One operation can transfer between 4k and 256k bytes.</span></span>

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

### <span data-ttu-id="20098-134">-DiskMBpsReadOnly</span><span class="sxs-lookup"><span data-stu-id="20098-134">-DiskMBpsReadOnly</span></span>
<span data-ttu-id="20098-135">A produtividade total (MBps) que será permitida em todas as VMs que montam o disco compartilhado como ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="20098-135">The total throughput (MBps) that will be allowed across all VMs mounting the shared disk as ReadOnly.</span></span> <span data-ttu-id="20098-136">MBps significa milhões de bytes por segundo - MB aqui usa a notação ISO, de potências de 10.</span><span class="sxs-lookup"><span data-stu-id="20098-136">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="20098-137">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="20098-137">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="20098-138">A largura de banda permitida para esse disco; somente settable para discos UltraSSD.</span><span class="sxs-lookup"><span data-stu-id="20098-138">The bandwidth allowed for this disk; only settable for UltraSSD disks.</span></span> <span data-ttu-id="20098-139">MBps significa milhões de bytes por segundo - MB aqui usa a notação ISO, de potências de 10.</span><span class="sxs-lookup"><span data-stu-id="20098-139">MBps means millions of bytes per second - MB here uses the ISO notation, of powers of 10.</span></span>

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

### <span data-ttu-id="20098-140">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="20098-140">-DiskSizeGB</span></span>
<span data-ttu-id="20098-141">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="20098-141">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="20098-142">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="20098-142">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="20098-143">Habilitar configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="20098-143">Enable encryption settings.</span></span>

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

### <span data-ttu-id="20098-144">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="20098-144">-EncryptionType</span></span>
<span data-ttu-id="20098-145">O tipo de chave usada para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="20098-145">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="20098-146">Os valores disponíveis são: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="20098-146">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="20098-147">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="20098-147">-KeyEncryptionKey</span></span>
<span data-ttu-id="20098-148">Especifica a chave de criptografia Key em um disco.</span><span class="sxs-lookup"><span data-stu-id="20098-148">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="20098-149">-MaxSharesCount</span><span class="sxs-lookup"><span data-stu-id="20098-149">-MaxSharesCount</span></span>
<span data-ttu-id="20098-150">O número máximo de VMs que podem ser anexadas ao disco ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="20098-150">The maximum number of VMs that can attach to the disk at the same time.</span></span> <span data-ttu-id="20098-151">Valor maior que um indica um disco que pode ser montado em várias VMs ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="20098-151">Value greater than one indicates a disk that can be mounted on multiple VMs at the same time.</span></span>

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

### <span data-ttu-id="20098-152">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="20098-152">-NetworkAccessPolicy</span></span>
<span data-ttu-id="20098-153">{{ Fill NetworkAccessPolicy Description }}</span><span class="sxs-lookup"><span data-stu-id="20098-153">{{ Fill NetworkAccessPolicy Description }}</span></span>

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

### <span data-ttu-id="20098-154">-OsType</span><span class="sxs-lookup"><span data-stu-id="20098-154">-OsType</span></span>
<span data-ttu-id="20098-155">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="20098-155">Specifies the OS type.</span></span>

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

### <span data-ttu-id="20098-156">-SkuName</span><span class="sxs-lookup"><span data-stu-id="20098-156">-SkuName</span></span>
<span data-ttu-id="20098-157">Especifica o nome Sku da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20098-157">Specifies the Sku name of the storage account.</span></span>  <span data-ttu-id="20098-158">Os valores disponíveis são Standard_LRS, Premium_LRS, StandardSSD_LRS e UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="20098-158">Available values are Standard_LRS, Premium_LRS, StandardSSD_LRS, and UltraSSD_LRS.</span></span>  <span data-ttu-id="20098-159">UltraSSD_LRS pode ser usado apenas com valor vazio para o parâmetro CreateOption.</span><span class="sxs-lookup"><span data-stu-id="20098-159">UltraSSD_LRS can only be used with Empty value for CreateOption parameter.</span></span>

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

### <span data-ttu-id="20098-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="20098-160">-Tag</span></span>
<span data-ttu-id="20098-161">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="20098-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="20098-162">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="20098-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="20098-163">-Tier</span><span class="sxs-lookup"><span data-stu-id="20098-163">-Tier</span></span>
<span data-ttu-id="20098-164">Camada de desempenho do disco.</span><span class="sxs-lookup"><span data-stu-id="20098-164">Performance tier of the disk.</span></span>

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

### <span data-ttu-id="20098-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20098-165">-Confirm</span></span>
<span data-ttu-id="20098-166">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20098-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20098-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20098-167">-WhatIf</span></span>
<span data-ttu-id="20098-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20098-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20098-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20098-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20098-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20098-170">CommonParameters</span></span>
<span data-ttu-id="20098-171">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20098-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20098-172">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20098-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20098-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20098-173">INPUTS</span></span>

### <span data-ttu-id="20098-174">System.String</span><span class="sxs-lookup"><span data-stu-id="20098-174">System.String</span></span>

### <span data-ttu-id="20098-175">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="20098-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="20098-176">System.Int32</span><span class="sxs-lookup"><span data-stu-id="20098-176">System.Int32</span></span>

### <span data-ttu-id="20098-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="20098-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="20098-178">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="20098-178">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="20098-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="20098-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="20098-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="20098-180">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="20098-181">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20098-181">OUTPUTS</span></span>

### <span data-ttu-id="20098-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="20098-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="20098-183">NOTES</span><span class="sxs-lookup"><span data-stu-id="20098-183">NOTES</span></span>

## <span data-ttu-id="20098-184">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20098-184">RELATED LINKS</span></span>
