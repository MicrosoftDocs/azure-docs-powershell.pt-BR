---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmSnapshotConfig.md
ms.openlocfilehash: 2050536a39c8ebcd5a1269709d25af100cc251b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603002"
---
# <span data-ttu-id="6ab93-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="6ab93-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="6ab93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ab93-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab93-103">Cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="6ab93-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ab93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ab93-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <String>] [[-OsType] <OperatingSystemTypes>] [[-DiskSizeGB] <Int32>]
 [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <String>] [-StorageAccountId <String>]
 [-ImageReference <ImageDiskReference>] [-SourceUri <String>] [-SourceResourceId <String>]
 [-EncryptionSettingsEnabled <Boolean>] [-DiskEncryptionKey <KeyVaultAndSecretReference>]
 [-KeyEncryptionKey <KeyVaultAndKeyReference>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ab93-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ab93-105">DESCRIPTION</span></span>
<span data-ttu-id="6ab93-106">O cmdlet **New-AzureRmSnapshotConfig** cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="6ab93-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="6ab93-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ab93-107">EXAMPLES</span></span>

### <span data-ttu-id="6ab93-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ab93-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="6ab93-109">O primeiro comando cria um objeto de instantâneo vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ab93-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="6ab93-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6ab93-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6ab93-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6ab93-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="6ab93-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6ab93-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6ab93-113">OS</span><span class="sxs-lookup"><span data-stu-id="6ab93-113">PARAMETERS</span></span>

### <span data-ttu-id="6ab93-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="6ab93-114">-CreateOption</span></span>
<span data-ttu-id="6ab93-115">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="6ab93-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="6ab93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab93-116">-DefaultProfile</span></span>
<span data-ttu-id="6ab93-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab93-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab93-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6ab93-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="6ab93-119">Especifica o objeto da chave de criptografia do disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6ab93-119">Specifies the disk encryption key object on a snapshot.</span></span>

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

### <span data-ttu-id="6ab93-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6ab93-120">-DiskSizeGB</span></span>
<span data-ttu-id="6ab93-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="6ab93-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6ab93-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="6ab93-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="6ab93-123">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6ab93-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="6ab93-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="6ab93-124">-ImageReference</span></span>
<span data-ttu-id="6ab93-125">Especifica a referência de imagem em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6ab93-125">Specifies the image reference on a snapshot.</span></span>

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

### <span data-ttu-id="6ab93-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6ab93-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="6ab93-127">Especifica a chave de criptografia da chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="6ab93-127">Specifies the Key encryption key on a snapshot.</span></span>

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

### <span data-ttu-id="6ab93-128">-Local</span><span class="sxs-lookup"><span data-stu-id="6ab93-128">-Location</span></span>
<span data-ttu-id="6ab93-129">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="6ab93-129">Specifies a location.</span></span>

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

### <span data-ttu-id="6ab93-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="6ab93-130">-OsType</span></span>
<span data-ttu-id="6ab93-131">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6ab93-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6ab93-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="6ab93-132">-SkuName</span></span>
<span data-ttu-id="6ab93-133">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ab93-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="6ab93-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab93-134">-SourceResourceId</span></span>
<span data-ttu-id="6ab93-135">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="6ab93-135">Specifies the source resource ID.</span></span>

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

### <span data-ttu-id="6ab93-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="6ab93-136">-SourceUri</span></span>
<span data-ttu-id="6ab93-137">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="6ab93-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="6ab93-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6ab93-138">-StorageAccountId</span></span>
<span data-ttu-id="6ab93-139">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ab93-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="6ab93-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="6ab93-140">-Tag</span></span>
<span data-ttu-id="6ab93-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="6ab93-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ab93-142">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6ab93-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6ab93-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ab93-143">-Confirm</span></span>
<span data-ttu-id="6ab93-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ab93-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ab93-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ab93-145">-WhatIf</span></span>
<span data-ttu-id="6ab93-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ab93-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ab93-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ab93-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ab93-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab93-148">CommonParameters</span></span>
<span data-ttu-id="6ab93-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ab93-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab93-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab93-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab93-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ab93-151">INPUTS</span></span>

### <span data-ttu-id="6ab93-152">System. String</span><span class="sxs-lookup"><span data-stu-id="6ab93-152">System.String</span></span>

### <span data-ttu-id="6ab93-153">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. OperatingSystemTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6ab93-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="6ab93-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6ab93-154">System.Int32</span></span>

### <span data-ttu-id="6ab93-155">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ab93-155">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6ab93-156">Microsoft. Azure. Management. COMPUTE. Models. ImageDiskReference</span><span class="sxs-lookup"><span data-stu-id="6ab93-156">Microsoft.Azure.Management.Compute.Models.ImageDiskReference</span></span>

### <span data-ttu-id="6ab93-157">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6ab93-157">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6ab93-158">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndSecretReference</span><span class="sxs-lookup"><span data-stu-id="6ab93-158">Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference</span></span>

### <span data-ttu-id="6ab93-159">Microsoft. Azure. Management. COMPUTE. Models. KeyVaultAndKeyReference</span><span class="sxs-lookup"><span data-stu-id="6ab93-159">Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="6ab93-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ab93-160">OUTPUTS</span></span>

### <span data-ttu-id="6ab93-161">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="6ab93-161">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="6ab93-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ab93-162">NOTES</span></span>

## <span data-ttu-id="6ab93-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ab93-163">RELATED LINKS</span></span>
