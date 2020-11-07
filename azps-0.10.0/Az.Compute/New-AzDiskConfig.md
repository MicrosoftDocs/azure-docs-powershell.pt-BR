---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzDiskConfig.md
ms.openlocfilehash: 851687bdc00b25bd283433fbc00254380a8ef3a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776975"
---
# <span data-ttu-id="b2020-101">New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b2020-101">New-AzDiskConfig</span></span>

## <span data-ttu-id="b2020-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2020-102">SYNOPSIS</span></span>
<span data-ttu-id="b2020-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="b2020-103">Creates a configurable disk object.</span></span>

## <span data-ttu-id="b2020-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2020-104">SYNTAX</span></span>

```
New-AzDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2020-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2020-105">DESCRIPTION</span></span>
<span data-ttu-id="b2020-106">O cmdlet **New-AzDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="b2020-106">The **New-AzDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="b2020-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2020-107">EXAMPLES</span></span>

### <span data-ttu-id="b2020-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2020-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="b2020-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2020-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span> <span data-ttu-id="b2020-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b2020-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="b2020-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="b2020-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span> <span data-ttu-id="b2020-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b2020-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b2020-113">OS</span><span class="sxs-lookup"><span data-stu-id="b2020-113">PARAMETERS</span></span>

### <span data-ttu-id="b2020-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="b2020-114">-CreateOption</span></span>
<span data-ttu-id="b2020-115">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="b2020-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

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

### <span data-ttu-id="b2020-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2020-116">-DefaultProfile</span></span>
<span data-ttu-id="b2020-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2020-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2020-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b2020-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="b2020-119">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="b2020-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="b2020-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="b2020-120">-DiskSizeGB</span></span>
<span data-ttu-id="b2020-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="b2020-121">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="b2020-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="b2020-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="b2020-123">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b2020-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="b2020-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="b2020-124">-ImageReference</span></span>
<span data-ttu-id="b2020-125">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="b2020-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="b2020-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b2020-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="b2020-127">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="b2020-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="b2020-128">-Local</span><span class="sxs-lookup"><span data-stu-id="b2020-128">-Location</span></span>
<span data-ttu-id="b2020-129">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="b2020-129">Specifies a location.</span></span>

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

### <span data-ttu-id="b2020-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="b2020-130">-OsType</span></span>
<span data-ttu-id="b2020-131">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b2020-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="b2020-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b2020-132">-SkuName</span></span>
<span data-ttu-id="b2020-133">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2020-133">Specifies the Sku name of the storage account.</span></span>

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

### <span data-ttu-id="b2020-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="b2020-134">-SourceResourceId</span></span>
<span data-ttu-id="b2020-135">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="b2020-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="b2020-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="b2020-136">-SourceUri</span></span>
<span data-ttu-id="b2020-137">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="b2020-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="b2020-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b2020-138">-StorageAccountId</span></span>
<span data-ttu-id="b2020-139">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b2020-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="b2020-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="b2020-140">-Tag</span></span>
<span data-ttu-id="b2020-141">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b2020-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b2020-142">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="b2020-142">For example:</span></span>

<span data-ttu-id="b2020-143">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b2020-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b2020-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="b2020-144">-Zone</span></span>
<span data-ttu-id="b2020-145">Especifica a lista de zonas lógicas do disco.</span><span class="sxs-lookup"><span data-stu-id="b2020-145">Specifies the logical zone list for Disk.</span></span>

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

### <span data-ttu-id="b2020-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2020-146">-Confirm</span></span>
<span data-ttu-id="b2020-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2020-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2020-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2020-148">-WhatIf</span></span>
<span data-ttu-id="b2020-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2020-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2020-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2020-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2020-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2020-151">CommonParameters</span></span>
<span data-ttu-id="b2020-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2020-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2020-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2020-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2020-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2020-154">INPUTS</span></span>

### <span data-ttu-id="b2020-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b2020-155">None</span></span>
<span data-ttu-id="b2020-156">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b2020-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b2020-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2020-157">OUTPUTS</span></span>

### <span data-ttu-id="b2020-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="b2020-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="b2020-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2020-159">NOTES</span></span>

## <span data-ttu-id="b2020-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2020-160">RELATED LINKS</span></span>

