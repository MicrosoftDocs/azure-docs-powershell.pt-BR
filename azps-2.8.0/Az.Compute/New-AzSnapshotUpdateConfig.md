---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: d2c029b75f5c451a2254b0dcf6b90c907148f8cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597363"
---
# <span data-ttu-id="6d7d3-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="6d7d3-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="6d7d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d7d3-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7d3-103">Cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="6d7d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d7d3-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d7d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d7d3-105">DESCRIPTION</span></span>
<span data-ttu-id="6d7d3-106">O cmdlet **New-AzSnapshotUpdateConfig** cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="6d7d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d7d3-107">EXAMPLES</span></span>

### <span data-ttu-id="6d7d3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6d7d3-108">Example 1</span></span>
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

<span data-ttu-id="6d7d3-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="6d7d3-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="6d7d3-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="6d7d3-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6d7d3-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6d7d3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6d7d3-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="6d7d3-114">Este comando atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="6d7d3-115">OS</span><span class="sxs-lookup"><span data-stu-id="6d7d3-115">PARAMETERS</span></span>

### <span data-ttu-id="6d7d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7d3-116">-DefaultProfile</span></span>
<span data-ttu-id="6d7d3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d7d3-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6d7d3-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="6d7d3-119">Especifica o objeto da chave de criptografia do disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="6d7d3-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6d7d3-120">-DiskSizeGB</span></span>
<span data-ttu-id="6d7d3-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6d7d3-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="6d7d3-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6d7d3-123">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6d7d3-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6d7d3-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="6d7d3-125">Especifica a chave de criptografia da chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-125">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="6d7d3-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="6d7d3-126">-OsType</span></span>
<span data-ttu-id="6d7d3-127">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-127">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6d7d3-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6d7d3-128">-SkuName</span></span>
<span data-ttu-id="6d7d3-129">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-129">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="6d7d3-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="6d7d3-130">-Tag</span></span>
<span data-ttu-id="6d7d3-131">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6d7d3-132">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6d7d3-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6d7d3-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6d7d3-133">-Confirm</span></span>
<span data-ttu-id="6d7d3-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d7d3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d7d3-135">-WhatIf</span></span>
<span data-ttu-id="6d7d3-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d7d3-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d7d3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7d3-138">CommonParameters</span></span>
<span data-ttu-id="6d7d3-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7d3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7d3-140">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d7d3-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7d3-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d7d3-141">INPUTS</span></span>

### <span data-ttu-id="6d7d3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6d7d3-142">System.String</span></span>

### <span data-ttu-id="6d7d3-143">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6d7d3-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6d7d3-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6d7d3-144">System.Int32</span></span>

### <span data-ttu-id="6d7d3-145">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6d7d3-145">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6d7d3-146">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6d7d3-146">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6d7d3-147">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="6d7d3-147">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="6d7d3-148">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="6d7d3-148">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="6d7d3-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d7d3-149">OUTPUTS</span></span>

### <span data-ttu-id="6d7d3-150">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="6d7d3-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="6d7d3-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d7d3-151">NOTES</span></span>

## <span data-ttu-id="6d7d3-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d7d3-152">RELATED LINKS</span></span>
