---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotConfig.md
ms.openlocfilehash: 8407cb1f8968d1e7d9e469b4ca3ccd1cb49742a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892540"
---
# <span data-ttu-id="30183-101">New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="30183-101">New-AzSnapshotConfig</span></span>

## <span data-ttu-id="30183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30183-102">SYNOPSIS</span></span>
<span data-ttu-id="30183-103">Cria um objeto instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="30183-103">Creates a configurable snapshot object.</span></span>

## <span data-ttu-id="30183-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="30183-104">SYNTAX</span></span>

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

## <span data-ttu-id="30183-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="30183-105">DESCRIPTION</span></span>
<span data-ttu-id="30183-106">O cmdlet **New-AzSnapshotConfig** cria um objeto instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="30183-106">The **New-AzSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="30183-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30183-107">EXAMPLES</span></span>

### <span data-ttu-id="30183-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="30183-108">Example 1</span></span>
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

<span data-ttu-id="30183-109">O primeiro comando cria um objeto instantâneo vazio local com tamanho de 5 GB Standard_LRS de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30183-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="30183-110">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="30183-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="30183-111">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto instantâneo.</span><span class="sxs-lookup"><span data-stu-id="30183-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="30183-112">O último comando pega o objeto instantâneo e cria um instantâneo com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="30183-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="30183-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="30183-113">Example 2</span></span>

<span data-ttu-id="30183-114">Cria um objeto instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="30183-114">Creates a configurable snapshot object.</span></span> <span data-ttu-id="30183-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="30183-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzSnapshotConfig -CreateOption Empty -Location 'Central US' -SourceUri 'https://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd'
```

## <span data-ttu-id="30183-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="30183-116">PARAMETERS</span></span>

### <span data-ttu-id="30183-117">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="30183-117">-CreateOption</span></span>
<span data-ttu-id="30183-118">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="30183-118">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="30183-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30183-119">-DefaultProfile</span></span>
<span data-ttu-id="30183-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="30183-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30183-121">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="30183-121">-DiskEncryptionKey</span></span>
<span data-ttu-id="30183-122">Especifica o objeto chave de criptografia de disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="30183-122">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="30183-123">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="30183-123">-DiskEncryptionSetId</span></span>
<span data-ttu-id="30183-124">Especifica a ID de recurso do conjunto de criptografia de disco a ser usado para habilenciar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="30183-124">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="30183-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="30183-125">-DiskSizeGB</span></span>
<span data-ttu-id="30183-126">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="30183-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="30183-127">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="30183-127">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="30183-128">Habilitar configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="30183-128">Enable encryption settings.</span></span>

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

### <span data-ttu-id="30183-129">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="30183-129">-EncryptionType</span></span>
<span data-ttu-id="30183-130">O tipo de chave usada para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="30183-130">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="30183-131">Os valores disponíveis são: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="30183-131">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="30183-132">-DiskAccessId</span><span class="sxs-lookup"><span data-stu-id="30183-132">-DiskAccessId</span></span>
<span data-ttu-id="30183-133">Obtém ou define ARM id do recurso DiskAccess para usar pontos de extremidade privados.</span><span class="sxs-lookup"><span data-stu-id="30183-133">Gets or sets ARM id of the DiskAccess resource for using private endpoints on.</span></span>

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

### <span data-ttu-id="30183-134">-NetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="30183-134">-NetworkAccessPolicy</span></span>
<span data-ttu-id="30183-135">A política de acesso à rede define a política de acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="30183-135">Network access policy defines the network access policy.</span></span>
<span data-ttu-id="30183-136">Os valores possíveis incluem: 'AllowAll', 'AllowPrivate', 'DenyAll'</span><span class="sxs-lookup"><span data-stu-id="30183-136">Possible values include: 'AllowAll', 'AllowPrivate', 'DenyAll'</span></span>

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

### <span data-ttu-id="30183-137">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="30183-137">-HyperVGeneration</span></span>
<span data-ttu-id="30183-138">A geração do hipervisor da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="30183-138">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="30183-139">Aplicável somente a discos do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="30183-139">Applicable to OS disks only.</span></span>  <span data-ttu-id="30183-140">Os valores permitidos são V1 e V2.</span><span class="sxs-lookup"><span data-stu-id="30183-140">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="30183-141">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="30183-141">-ImageReference</span></span>
<span data-ttu-id="30183-142">Especifica a referência de imagem em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="30183-142">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="30183-143">-Incremental</span><span class="sxs-lookup"><span data-stu-id="30183-143">-Incremental</span></span>
<span data-ttu-id="30183-144">Especifica um instantâneo incremental.</span><span class="sxs-lookup"><span data-stu-id="30183-144">Specifies an incremental snapshot.</span></span> <span data-ttu-id="30183-145">Instantâneos incrementais no mesmo disco ocupam menos espaço que instantâneos completos e podem ser diferentes.</span><span class="sxs-lookup"><span data-stu-id="30183-145">Incremental snapshots on the same disk occupy less space than full snapshots and can be diffed.</span></span>

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

### <span data-ttu-id="30183-146">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="30183-146">-KeyEncryptionKey</span></span>
<span data-ttu-id="30183-147">Especifica a chave de criptografia Key em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="30183-147">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="30183-148">-Location</span><span class="sxs-lookup"><span data-stu-id="30183-148">-Location</span></span>
<span data-ttu-id="30183-149">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="30183-149">Specifies a location.</span></span>

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

### <span data-ttu-id="30183-150">-OsType</span><span class="sxs-lookup"><span data-stu-id="30183-150">-OsType</span></span>
<span data-ttu-id="30183-151">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="30183-151">Specifies the OS type.</span></span>

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

### <span data-ttu-id="30183-152">-SkuName</span><span class="sxs-lookup"><span data-stu-id="30183-152">-SkuName</span></span>
<span data-ttu-id="30183-153">Especifica o nome Sku da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30183-153">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="30183-154">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="30183-154">-SourceResourceId</span></span>
<span data-ttu-id="30183-155">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="30183-155">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="30183-156">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="30183-156">-SourceUri</span></span>
<span data-ttu-id="30183-157">Especifica o Uri de origem.</span><span class="sxs-lookup"><span data-stu-id="30183-157">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="30183-158">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="30183-158">-StorageAccountId</span></span>
<span data-ttu-id="30183-159">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30183-159">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="30183-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="30183-160">-Tag</span></span>
<span data-ttu-id="30183-161">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="30183-161">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="30183-162">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="30183-162">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="30183-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="30183-163">-Confirm</span></span>
<span data-ttu-id="30183-164">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30183-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30183-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30183-165">-WhatIf</span></span>
<span data-ttu-id="30183-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="30183-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30183-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="30183-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30183-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30183-168">CommonParameters</span></span>
<span data-ttu-id="30183-169">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30183-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30183-170">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30183-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30183-171">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30183-171">INPUTS</span></span>

### <span data-ttu-id="30183-172">System.String</span><span class="sxs-lookup"><span data-stu-id="30183-172">System.String</span></span>

### <span data-ttu-id="30183-173">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="30183-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="30183-174">System.Int32</span><span class="sxs-lookup"><span data-stu-id="30183-174">System.Int32</span></span>

### <span data-ttu-id="30183-175">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="30183-175">System.Collections.Hashtable</span></span>

### <span data-ttu-id="30183-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="30183-176">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="30183-177">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="30183-177">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="30183-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="30183-178">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="30183-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="30183-179">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="30183-180">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="30183-180">OUTPUTS</span></span>

### <span data-ttu-id="30183-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="30183-181">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="30183-182">NOTES</span><span class="sxs-lookup"><span data-stu-id="30183-182">NOTES</span></span>

## <span data-ttu-id="30183-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30183-183">RELATED LINKS</span></span>
