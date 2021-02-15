---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 5d9a48fbdc323ffdd232d6d961da6564fecc0dff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112122"
---
# <span data-ttu-id="a85ff-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a85ff-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="a85ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a85ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a85ff-103">Cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="a85ff-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a85ff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a85ff-104">SYNTAX</span></span>

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

## <span data-ttu-id="a85ff-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a85ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a85ff-106">O **cmdlet New-AzSnapshotConfig** cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="a85ff-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="a85ff-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a85ff-107">EXAMPLES</span></span>

### <span data-ttu-id="a85ff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a85ff-108">Example 1</span></span>
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

<span data-ttu-id="a85ff-109">O primeiro comando cria um objeto de instantâneo vazio local com tamanho de 5 GB Standard_LRS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a85ff-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="a85ff-110">Ele também define o tipo do sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="a85ff-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="a85ff-111">O segundo e o terceiro comandos configuram a chave de criptografia de disco e as configurações da chave de criptografia para o objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a85ff-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="a85ff-112">O último comando leva o objeto de instantâneo e cria um instantâneo com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="a85ff-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="a85ff-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a85ff-113">Example 2</span></span>

<span data-ttu-id="a85ff-114">Cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="a85ff-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="a85ff-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="a85ff-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="a85ff-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a85ff-116">PARAMETERS</span></span>

### <span data-ttu-id="a85ff-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="a85ff-117">-CreateOption</span></span>
<span data-ttu-id="a85ff-118">Especifica se esse cmdlet cria um disco no computador virtual a partir de uma plataforma ou imagem do usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="a85ff-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="a85ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a85ff-119">-DefaultProfile</span></span>
<span data-ttu-id="a85ff-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a85ff-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a85ff-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a85ff-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="a85ff-122">Especifica o objeto da chave de criptografia de disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a85ff-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="a85ff-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="a85ff-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="a85ff-124">Especifica a ID do recurso do conjunto de criptografia de disco que deve ser usado para habilenciar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="a85ff-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="a85ff-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="a85ff-125">-DiskSizeGB</span></span>
<span data-ttu-id="a85ff-126">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="a85ff-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="a85ff-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="a85ff-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="a85ff-128">Habilitar configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="a85ff-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="a85ff-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="a85ff-129">-EncryptionType</span></span>
<span data-ttu-id="a85ff-130">O tipo de chave usada para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="a85ff-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="a85ff-131">Os valores disponíveis são: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="a85ff-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="a85ff-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="a85ff-132">-DiskAccessId</span></span>
<span data-ttu-id="a85ff-133">Obtém ou define a ID ARM do recurso DiskAccess para usar pontos de extremidade particulares.</span><span class="sxs-lookup"><span data-stu-id="a85ff-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="a85ff-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a85ff-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="a85ff-135">A política de acesso à rede define a política de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="a85ff-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="a85ff-136">Os valores possíveis incluem: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="a85ff-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="a85ff-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="a85ff-137">-HyperVGeneration</span></span>
<span data-ttu-id="a85ff-138">A geração de hipervisor da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="a85ff-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="a85ff-139">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a85ff-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="a85ff-140">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="a85ff-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="a85ff-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="a85ff-141">-ImageReference</span></span>
<span data-ttu-id="a85ff-142">Especifica a referência de imagem em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a85ff-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="a85ff-143">-Incremental</span><span class="sxs-lookup"><span data-stu-id="a85ff-143">-Incremental</span></span>
<span data-ttu-id="a85ff-144">Especifica um instantâneo incremental.</span><span class="sxs-lookup"><span data-stu-id="a85ff-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="a85ff-145">Instantâneos incrementais no mesmo disco ocupam menos espaço do que instantâneos completos e podem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="a85ff-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="a85ff-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="a85ff-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="a85ff-147">Especifica a chave de criptografia chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="a85ff-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="a85ff-148">-Local</span><span class="sxs-lookup"><span data-stu-id="a85ff-148">-Location</span></span>
<span data-ttu-id="a85ff-149">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="a85ff-149">Specifies a location.</span></span>

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

### <span data-ttu-id="a85ff-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="a85ff-150">-OsType</span></span>
<span data-ttu-id="a85ff-151">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a85ff-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="a85ff-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a85ff-152">-SkuName</span></span>
<span data-ttu-id="a85ff-153">Especifica o nome SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a85ff-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="a85ff-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a85ff-154">-SourceResourceId</span></span>
<span data-ttu-id="a85ff-155">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="a85ff-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="a85ff-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="a85ff-156">-SourceUri</span></span>
<span data-ttu-id="a85ff-157">Especifica o Uri de origem.</span><span class="sxs-lookup"><span data-stu-id="a85ff-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="a85ff-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a85ff-158">-StorageAccountId</span></span>
<span data-ttu-id="a85ff-159">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a85ff-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="a85ff-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="a85ff-160">-Tag</span></span>
<span data-ttu-id="a85ff-161">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a85ff-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a85ff-162">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a85ff-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a85ff-163">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a85ff-163">-Confirm</span></span>
<span data-ttu-id="a85ff-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a85ff-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a85ff-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a85ff-165">-WhatIf</span></span>
<span data-ttu-id="a85ff-166">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a85ff-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a85ff-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a85ff-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a85ff-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a85ff-168">CommonParameters</span></span>
<span data-ttu-id="a85ff-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a85ff-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a85ff-170">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a85ff-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a85ff-171">Entradas</span><span class="sxs-lookup"><span data-stu-id="a85ff-171">INPUTS</span></span>

### <span data-ttu-id="a85ff-172">System.String</span><span class="sxs-lookup"><span data-stu-id="a85ff-172">System.String</span></span>

### <span data-ttu-id="a85ff-173">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a85ff-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="a85ff-174">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a85ff-174">System.Int32</span></span>

### <span data-ttu-id="a85ff-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a85ff-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a85ff-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="a85ff-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="a85ff-177">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a85ff-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a85ff-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSeciliReference</span><span class="sxs-lookup"><span data-stu-id="a85ff-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="a85ff-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="a85ff-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="a85ff-180">Saídas</span><span class="sxs-lookup"><span data-stu-id="a85ff-180">OUTPUTS</span></span>

### <span data-ttu-id="a85ff-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="a85ff-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="a85ff-182">Notas</span><span class="sxs-lookup"><span data-stu-id="a85ff-182">NOTES</span></span>

## <span data-ttu-id="a85ff-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a85ff-183">RELATED LINKS</span></span>
