---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: 1a90a1ff260d143cf4df52ad160b4c05e781bd2e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115727"
---
# <span data-ttu-id="9c14f-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="9c14f-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="9c14f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c14f-102">SYNOPSIS</span></span>
<span data-ttu-id="9c14f-103">Cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="9c14f-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="9c14f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9c14f-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DiskEncryptionSetId <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c14f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9c14f-105">DESCRIPTION</span></span>
<span data-ttu-id="9c14f-106">O cmdlet **New-AzSnapshotUpdateConfig** cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="9c14f-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="9c14f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9c14f-107">EXAMPLES</span></span>

### <span data-ttu-id="9c14f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c14f-108">Example 1</span></span>
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

<span data-ttu-id="9c14f-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c14f-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="9c14f-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="9c14f-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="9c14f-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9c14f-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="9c14f-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="9c14f-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="9c14f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9c14f-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="9c14f-114">Este comando atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="9c14f-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="9c14f-115">OS</span><span class="sxs-lookup"><span data-stu-id="9c14f-115">PARAMETERS</span></span>

### <span data-ttu-id="9c14f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c14f-116">-DefaultProfile</span></span>
<span data-ttu-id="9c14f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c14f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c14f-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9c14f-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="9c14f-119">Especifica o objeto da chave de criptografia do disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9c14f-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="9c14f-120">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="9c14f-120">-DiskEncryptionSetId</span></span>
<span data-ttu-id="9c14f-121">Especifica a ID do recurso do conjunto de criptografia de disco a ser usado para habilitar a criptografia em repouso.</span><span class="sxs-lookup"><span data-stu-id="9c14f-121">Specifies the resource Id of the disk encryption set to use for enabling encryption at rest.</span></span>

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

### <span data-ttu-id="9c14f-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="9c14f-122">-DiskSizeGB</span></span>
<span data-ttu-id="9c14f-123">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="9c14f-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="9c14f-124">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="9c14f-124">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="9c14f-125">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="9c14f-125">Enable encryption settings.</span></span>

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

### <span data-ttu-id="9c14f-126">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="9c14f-126">-EncryptionType</span></span>
<span data-ttu-id="9c14f-127">O tipo de chave usado para criptografar os dados do disco.</span><span class="sxs-lookup"><span data-stu-id="9c14f-127">The type of key used to encrypt the data of the disk.</span></span>  <span data-ttu-id="9c14f-128">Os valores disponíveis são: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey"</span><span class="sxs-lookup"><span data-stu-id="9c14f-128">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'</span></span>

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

### <span data-ttu-id="9c14f-129">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="9c14f-129">-KeyEncryptionKey</span></span>
<span data-ttu-id="9c14f-130">Especifica a chave de criptografia da chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="9c14f-130">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="9c14f-131">-OsType</span><span class="sxs-lookup"><span data-stu-id="9c14f-131">-OsType</span></span>
<span data-ttu-id="9c14f-132">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9c14f-132">Specifies the OS type.</span></span>

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

### <span data-ttu-id="9c14f-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9c14f-133">-SkuName</span></span>
<span data-ttu-id="9c14f-134">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9c14f-134">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="9c14f-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="9c14f-135">-Tag</span></span>
<span data-ttu-id="9c14f-136">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9c14f-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9c14f-137">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9c14f-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9c14f-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9c14f-138">-Confirm</span></span>
<span data-ttu-id="9c14f-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c14f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c14f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c14f-140">-WhatIf</span></span>
<span data-ttu-id="9c14f-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9c14f-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c14f-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c14f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c14f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c14f-143">CommonParameters</span></span>
<span data-ttu-id="9c14f-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c14f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c14f-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c14f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c14f-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9c14f-146">INPUTS</span></span>

### <span data-ttu-id="9c14f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9c14f-147">System.String</span></span>

### <span data-ttu-id="9c14f-148">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="9c14f-148">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="9c14f-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9c14f-149">System.Int32</span></span>

### <span data-ttu-id="9c14f-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c14f-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9c14f-151">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9c14f-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9c14f-152">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="9c14f-152">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="9c14f-153">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="9c14f-153">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="9c14f-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9c14f-154">OUTPUTS</span></span>

### <span data-ttu-id="9c14f-155">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="9c14f-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="9c14f-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9c14f-156">NOTES</span></span>

## <span data-ttu-id="9c14f-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c14f-157">RELATED LINKS</span></span>
