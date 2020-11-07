---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955970"
---
# <span data-ttu-id="b2be8-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="b2be8-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="b2be8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2be8-102">SYNOPSIS</span></span>
<span data-ttu-id="b2be8-103">Cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="b2be8-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="b2be8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2be8-104">SYNTAX</span></span>

```
New-AzSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-HyperVGeneration <String>] [-Incremental] [-Tag <Hashtable>] [-CreateOption <String>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DiskEncryptionSetId <String>] [-EncryptionType <String>] [DiskAccessId <String>]
 [-NetworkAccessPolicy <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2be8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2be8-105">DESCRIPTION</span></span>
<span data-ttu-id="b2be8-106">O cmdlet **New-AzSnapshotConfig** cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="b2be8-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="b2be8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2be8-107">EXAMPLES</span></span>

### <span data-ttu-id="b2be8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2be8-108">Example 1</span></span>
```powershell
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="b2be8-109">O primeiro comando cria um objeto de instantâneo vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2be8-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="b2be8-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b2be8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b2be8-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b2be8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="b2be8-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b2be8-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b2be8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b2be8-113">Example 2</span></span>

<span data-ttu-id="b2be8-114">Cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="b2be8-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="b2be8-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="b2be8-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="b2be8-116">OS</span><span class="sxs-lookup"><span data-stu-id="b2be8-116">PARAMETERS</span></span>

### <span data-ttu-id="b2be8-117">-Createoption</span><span class="sxs-lookup"><span data-stu-id="b2be8-117">-CreateOption</span></span>
<span data-ttu-id="b2be8-118">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="b2be8-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="b2be8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2be8-119">-DefaultProfile</span></span>
<span data-ttu-id="b2be8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2be8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2be8-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b2be8-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="b2be8-122">Especifica o objeto da chave de criptografia do disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b2be8-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="b2be8-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="b2be8-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="b2be8-124">Especifica a ID do recurso do conjunto de criptografia de disco a ser usado para habilitar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="b2be8-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="b2be8-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b2be8-125">-DiskSizeGB</span></span>
<span data-ttu-id="b2be8-126">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="b2be8-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b2be8-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="b2be8-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b2be8-128">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b2be8-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="b2be8-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="b2be8-129">-EncryptionType</span></span>
<span data-ttu-id="b2be8-130">O tipo de chave usado para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="b2be8-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="b2be8-131">Os valores disponíveis são: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="b2be8-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="b2be8-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="b2be8-132">-DiskAccessId</span></span>
<span data-ttu-id="b2be8-133">Obtém ou define a ID de braço do recurso DiskAccess para uso de pontos de extremidade privados em.</span><span class="sxs-lookup"><span data-stu-id="b2be8-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="b2be8-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b2be8-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="b2be8-135">A política de acesso à rede define a política de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="b2be8-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="b2be8-136">Os valores possíveis incluem: ' AllowAll ', ' AllowPrivate ', ' DenyAll '</span><span class="sxs-lookup"><span data-stu-id="b2be8-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="b2be8-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="b2be8-137">-HyperVGeneration</span></span>
<span data-ttu-id="b2be8-138">A geração de hipervisor da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b2be8-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="b2be8-139">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b2be8-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="b2be8-140">Os valores permitidos são v1 e v2.</span><span class="sxs-lookup"><span data-stu-id="b2be8-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="b2be8-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="b2be8-141">-ImageReference</span></span>
<span data-ttu-id="b2be8-142">Especifica a referência de imagem em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b2be8-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="b2be8-143">-Incremental</span><span class="sxs-lookup"><span data-stu-id="b2be8-143">-Incremental</span></span>
<span data-ttu-id="b2be8-144">Especifica um instantâneo incremental.</span><span class="sxs-lookup"><span data-stu-id="b2be8-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="b2be8-145">Instantâneos incrementais no mesmo disco ocupam menos espaço do que os instantâneos completos e podem ser diferenciados.</span><span class="sxs-lookup"><span data-stu-id="b2be8-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2be8-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b2be8-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="b2be8-147">Especifica a chave de criptografia da chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b2be8-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="b2be8-148">-Local</span><span class="sxs-lookup"><span data-stu-id="b2be8-148">-Location</span></span>
<span data-ttu-id="b2be8-149">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="b2be8-149">Specifies a location.</span></span>

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

### <span data-ttu-id="b2be8-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="b2be8-150">-OsType</span></span>
<span data-ttu-id="b2be8-151">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b2be8-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="b2be8-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b2be8-152">-SkuName</span></span>
<span data-ttu-id="b2be8-153">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2be8-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="b2be8-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b2be8-154">-SourceResourceId</span></span>
<span data-ttu-id="b2be8-155">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="b2be8-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="b2be8-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="b2be8-156">-SourceUri</span></span>
<span data-ttu-id="b2be8-157">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="b2be8-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="b2be8-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b2be8-158">-StorageAccountId</span></span>
<span data-ttu-id="b2be8-159">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2be8-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="b2be8-160">-Marca</span><span class="sxs-lookup"><span data-stu-id="b2be8-160">-Tag</span></span>
<span data-ttu-id="b2be8-161">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b2be8-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b2be8-162">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b2be8-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b2be8-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2be8-163">-Confirm</span></span>
<span data-ttu-id="b2be8-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2be8-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2be8-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2be8-165">-WhatIf</span></span>
<span data-ttu-id="b2be8-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2be8-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2be8-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2be8-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2be8-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2be8-168">CommonParameters</span></span>
<span data-ttu-id="b2be8-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2be8-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2be8-170">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2be8-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2be8-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2be8-171">INPUTS</span></span>

### <span data-ttu-id="b2be8-172">System. String</span><span class="sxs-lookup"><span data-stu-id="b2be8-172">System.String</span></span>

### <span data-ttu-id="b2be8-173">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b2be8-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="b2be8-174">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b2be8-174">System.Int32</span></span>

### <span data-ttu-id="b2be8-175">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b2be8-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b2be8-176">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="b2be8-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="b2be8-177">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b2be8-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b2be8-178">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="b2be8-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="b2be8-179">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="b2be8-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="b2be8-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2be8-180">OUTPUTS</span></span>

### <span data-ttu-id="b2be8-181">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b2be8-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b2be8-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2be8-182">NOTES</span></span>

## <span data-ttu-id="b2be8-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2be8-183">RELATED LINKS</span></span>
