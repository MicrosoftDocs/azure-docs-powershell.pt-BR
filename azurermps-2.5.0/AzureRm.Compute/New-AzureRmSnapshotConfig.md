---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermsnapshotconfig
schema: 2.0.0
ms.openlocfilehash: a18eb8513e419d174efac9179cb65fe175d12dd1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786333"
---
# <span data-ttu-id="74da6-101">New-AzureRmSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="74da6-101">New-AzureRmSnapshotConfig</span></span>

## <span data-ttu-id="74da6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74da6-102">SYNOPSIS</span></span>
<span data-ttu-id="74da6-103">Cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="74da6-103">Creates a configurable snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74da6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74da6-104">SYNTAX</span></span>

```
New-AzureRmSnapshotConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Tag <Hashtable>] [-CreateOption <DiskCreateOption>]
 [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>] [-SourceUri <String>]
 [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74da6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74da6-105">DESCRIPTION</span></span>
<span data-ttu-id="74da6-106">O cmdlet **New-AzureRmSnapshotConfig** cria um objeto de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="74da6-106">The **New-AzureRmSnapshotConfig** cmdlet creates a configurable snapshot object.</span></span>

## <span data-ttu-id="74da6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74da6-107">EXAMPLES</span></span>

### <span data-ttu-id="74da6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74da6-108">Example 1</span></span>
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

<span data-ttu-id="74da6-109">O primeiro comando cria um objeto de instantâneo vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74da6-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="74da6-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="74da6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="74da6-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="74da6-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="74da6-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="74da6-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="74da6-113">OS</span><span class="sxs-lookup"><span data-stu-id="74da6-113">PARAMETERS</span></span>

### <span data-ttu-id="74da6-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="74da6-114">-CreateOption</span></span>
<span data-ttu-id="74da6-115">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="74da6-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: DiskCreateOption
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74da6-116">-DefaultProfile</span></span>
<span data-ttu-id="74da6-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="74da6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="74da6-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="74da6-119">Especifica o objeto da chave de criptografia do disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="74da6-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="74da6-120">-DiskSizeGB</span></span>
<span data-ttu-id="74da6-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="74da6-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="74da6-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="74da6-123">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="74da6-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="74da6-124">-ImageReference</span></span>
<span data-ttu-id="74da6-125">Especifica a referência de imagem em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="74da6-125">Specifies the image reference on a snapshot.</span></span>

```yaml
Type: ImageDiskReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="74da6-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="74da6-127">Especifica a chave de criptografia da chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="74da6-127">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-128">-Local</span><span class="sxs-lookup"><span data-stu-id="74da6-128">-Location</span></span>
<span data-ttu-id="74da6-129">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="74da6-129">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="74da6-130">-OsType</span></span>
<span data-ttu-id="74da6-131">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="74da6-131">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="74da6-132">-SkuName</span></span>
<span data-ttu-id="74da6-133">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74da6-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="74da6-134">-SourceResourceId</span></span>
<span data-ttu-id="74da6-135">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="74da6-135">Specifies the source resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="74da6-136">-SourceUri</span></span>
<span data-ttu-id="74da6-137">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="74da6-137">Specifies the source Uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="74da6-138">-StorageAccountId</span></span>
<span data-ttu-id="74da6-139">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="74da6-139">Specifies the storage account ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="74da6-140">-Tag</span></span>
<span data-ttu-id="74da6-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="74da6-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="74da6-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="74da6-142">For example:</span></span>

<span data-ttu-id="74da6-143">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="74da6-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="74da6-144">-Confirm</span></span>
<span data-ttu-id="74da6-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74da6-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74da6-146">-WhatIf</span></span>
<span data-ttu-id="74da6-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74da6-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74da6-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74da6-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74da6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74da6-149">CommonParameters</span></span>
<span data-ttu-id="74da6-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74da6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74da6-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74da6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74da6-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74da6-152">INPUTS</span></span>

### <span data-ttu-id="74da6-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="74da6-153">None</span></span>
<span data-ttu-id="74da6-154">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="74da6-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="74da6-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74da6-155">OUTPUTS</span></span>

### <span data-ttu-id="74da6-156">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="74da6-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="74da6-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74da6-157">NOTES</span></span>

## <span data-ttu-id="74da6-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74da6-158">RELATED LINKS</span></span>

