---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermdiskconfig
schema: 2.0.0
ms.openlocfilehash: 8249bbb354d660f335316da503b0f19b6576fea6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785790"
---
# <span data-ttu-id="88e94-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="88e94-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="88e94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="88e94-102">SYNOPSIS</span></span>
<span data-ttu-id="88e94-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="88e94-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88e94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88e94-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88e94-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="88e94-105">DESCRIPTION</span></span>
<span data-ttu-id="88e94-106">O cmdlet **New-AzureRmDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="88e94-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="88e94-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="88e94-107">EXAMPLES</span></span>

### <span data-ttu-id="88e94-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="88e94-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="88e94-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="88e94-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="88e94-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="88e94-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="88e94-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="88e94-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="88e94-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="88e94-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="88e94-113">OS</span><span class="sxs-lookup"><span data-stu-id="88e94-113">PARAMETERS</span></span>

### <span data-ttu-id="88e94-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="88e94-114">-CreateOption</span></span>
<span data-ttu-id="88e94-115">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="88e94-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="88e94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e94-116">-DefaultProfile</span></span>
<span data-ttu-id="88e94-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="88e94-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88e94-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="88e94-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="88e94-119">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="88e94-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="88e94-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="88e94-120">-DiskSizeGB</span></span>
<span data-ttu-id="88e94-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="88e94-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="88e94-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="88e94-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="88e94-123">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="88e94-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="88e94-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="88e94-124">-ImageReference</span></span>
<span data-ttu-id="88e94-125">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="88e94-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="88e94-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="88e94-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="88e94-127">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="88e94-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="88e94-128">-Local</span><span class="sxs-lookup"><span data-stu-id="88e94-128">-Location</span></span>
<span data-ttu-id="88e94-129">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="88e94-129">Specifies a location.</span></span>

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

### <span data-ttu-id="88e94-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="88e94-130">-OsType</span></span>
<span data-ttu-id="88e94-131">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="88e94-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="88e94-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="88e94-132">-SkuName</span></span>
<span data-ttu-id="88e94-133">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="88e94-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="88e94-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="88e94-134">-SourceResourceId</span></span>
<span data-ttu-id="88e94-135">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="88e94-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="88e94-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="88e94-136">-SourceUri</span></span>
<span data-ttu-id="88e94-137">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="88e94-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="88e94-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="88e94-138">-StorageAccountId</span></span>
<span data-ttu-id="88e94-139">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="88e94-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="88e94-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="88e94-140">-Tag</span></span>
<span data-ttu-id="88e94-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="88e94-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88e94-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="88e94-142">For example:</span></span>

<span data-ttu-id="88e94-143">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="88e94-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="88e94-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="88e94-144">-Zone</span></span>
<span data-ttu-id="88e94-145">Especifica a lista de zonas lógicas do disco.</span><span class="sxs-lookup"><span data-stu-id="88e94-145">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88e94-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="88e94-146">-Confirm</span></span>
<span data-ttu-id="88e94-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88e94-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88e94-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88e94-148">-WhatIf</span></span>
<span data-ttu-id="88e94-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="88e94-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="88e94-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="88e94-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88e94-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e94-151">CommonParameters</span></span>
<span data-ttu-id="88e94-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88e94-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e94-153">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88e94-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e94-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="88e94-154">INPUTS</span></span>

### <span data-ttu-id="88e94-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="88e94-155">None</span></span>
<span data-ttu-id="88e94-156">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="88e94-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="88e94-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="88e94-157">OUTPUTS</span></span>

### <span data-ttu-id="88e94-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="88e94-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="88e94-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="88e94-159">NOTES</span></span>

## <span data-ttu-id="88e94-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="88e94-160">RELATED LINKS</span></span>

