---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127089"
---
# <span data-ttu-id="97dfb-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="97dfb-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="97dfb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="97dfb-103">Cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="97dfb-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="97dfb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97dfb-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97dfb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="97dfb-105">DESCRIPTION</span></span>
<span data-ttu-id="97dfb-106">O **cmdlet New-AzSnapshotUpdateConfig** cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="97dfb-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="97dfb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97dfb-107">EXAMPLES</span></span>

### <span data-ttu-id="97dfb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97dfb-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="97dfb-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com tamanho de 10 GB Premium_LRS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="97dfb-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="97dfb-110">Ele também define o tipo do sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="97dfb-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="97dfb-111">O segundo e o terceiro comandos configuram a chave de criptografia de disco e as configurações da chave de criptografia para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="97dfb-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="97dfb-112">O último comando leva o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="97dfb-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="97dfb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="97dfb-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="97dfb-114">Esse comando atualiza um instantâneo existente com o nome "Instantâneo01" no grupo de recursos 'ResourceGroup01' para o tamanho do disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="97dfb-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="97dfb-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97dfb-115">PARAMETERS</span></span>

### <span data-ttu-id="97dfb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97dfb-116">-DefaultProfile</span></span>
<span data-ttu-id="97dfb-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="97dfb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97dfb-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="97dfb-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="97dfb-119">Especifica o objeto da chave de criptografia de disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="97dfb-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="97dfb-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="97dfb-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="97dfb-121">Especifica a ID de recurso do conjunto de criptografia de disco que deve ser usado para habilenciar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="97dfb-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="97dfb-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="97dfb-122">-DiskSizeGB</span></span>
<span data-ttu-id="97dfb-123">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="97dfb-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="97dfb-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="97dfb-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="97dfb-125">Habilitar configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="97dfb-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="97dfb-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="97dfb-126">-EncryptionType</span></span>
<span data-ttu-id="97dfb-127">O tipo de chave usada para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="97dfb-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="97dfb-128">Os valores disponíveis são: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span><span class="sxs-lookup"><span data-stu-id="97dfb-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="97dfb-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="97dfb-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="97dfb-130">Especifica a chave de criptografia chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="97dfb-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="97dfb-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="97dfb-131">-OsType</span></span>
<span data-ttu-id="97dfb-132">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="97dfb-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="97dfb-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="97dfb-133">-SkuName</span></span>
<span data-ttu-id="97dfb-134">Especifica o nome SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="97dfb-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="97dfb-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="97dfb-135">-Tag</span></span>
<span data-ttu-id="97dfb-136">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="97dfb-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="97dfb-137">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="97dfb-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="97dfb-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="97dfb-138">-Confirm</span></span>
<span data-ttu-id="97dfb-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97dfb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97dfb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97dfb-140">-WhatIf</span></span>
<span data-ttu-id="97dfb-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="97dfb-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97dfb-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97dfb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97dfb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97dfb-143">CommonParameters</span></span>
<span data-ttu-id="97dfb-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97dfb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97dfb-145">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97dfb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97dfb-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="97dfb-146">INPUTS</span></span>

### <span data-ttu-id="97dfb-147">System.String</span><span class="sxs-lookup"><span data-stu-id="97dfb-147">System.String</span></span>

### <span data-ttu-id="97dfb-148">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="97dfb-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="97dfb-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="97dfb-149">System.Int32</span></span>

### <span data-ttu-id="97dfb-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="97dfb-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="97dfb-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="97dfb-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="97dfb-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSeciliReference</span><span class="sxs-lookup"><span data-stu-id="97dfb-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="97dfb-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="97dfb-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="97dfb-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="97dfb-154">OUTPUTS</span></span>

### <span data-ttu-id="97dfb-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="97dfb-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="97dfb-156">Notas</span><span class="sxs-lookup"><span data-stu-id="97dfb-156">NOTES</span></span>

## <span data-ttu-id="97dfb-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97dfb-157">RELATED LINKS</span></span>
