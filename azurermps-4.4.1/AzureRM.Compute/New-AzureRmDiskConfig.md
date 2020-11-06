---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDiskConfig.md
ms.openlocfilehash: 70ee169903ca70b539e8eda2043ffcd0fd2928c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441391"
---
# <span data-ttu-id="8e777-101">New-AzureRmDiskConfig</span><span class="sxs-lookup"><span data-stu-id="8e777-101">New-AzureRmDiskConfig</span></span>

## <span data-ttu-id="8e777-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8e777-102">SYNOPSIS</span></span>
<span data-ttu-id="8e777-103">Cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="8e777-103">Creates a configurable disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e777-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e777-104">SYNTAX</span></span>

```
New-AzureRmDiskConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Location] <String>] [-Zone <String[]>] [-Tag <Hashtable>]
 [-CreateOption <DiskCreateOption>] [-StorageAccountId <String>] [-ImageReference <ImageDiskReference>]
 [-SourceUri <String>] [-SourceResourceId <String>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e777-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8e777-105">DESCRIPTION</span></span>
<span data-ttu-id="8e777-106">O cmdlet **New-AzureRmDiskConfig** cria um objeto de disco configurável.</span><span class="sxs-lookup"><span data-stu-id="8e777-106">The **New-AzureRmDiskConfig** cmdlet creates a configurable disk object.</span></span>

## <span data-ttu-id="8e777-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e777-107">EXAMPLES</span></span>

### <span data-ttu-id="8e777-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e777-108">Example 1</span></span>
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

<span data-ttu-id="8e777-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e777-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="8e777-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="8e777-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="8e777-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="8e777-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="8e777-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8e777-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8e777-113">OS</span><span class="sxs-lookup"><span data-stu-id="8e777-113">PARAMETERS</span></span>

### <span data-ttu-id="8e777-114">-Createoption</span><span class="sxs-lookup"><span data-stu-id="8e777-114">-CreateOption</span></span>
<span data-ttu-id="8e777-115">Especifica se esse cmdlet cria um disco na máquina virtual a partir de uma plataforma ou de uma imagem de usuário, cria um disco vazio ou anexa um disco existente.</span><span class="sxs-lookup"><span data-stu-id="8e777-115">Specifies whether this cmdlet creates a disk in the virtual machine from a platform or user image, creates an empty disk, or attaches an existing disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.DiskCreateOption]
Parameter Sets: (All)
Aliases: 
Accepted values: Empty, Attach, FromImage, Import, Copy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e777-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e777-116">-DefaultProfile</span></span>
<span data-ttu-id="8e777-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e777-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e777-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8e777-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="8e777-119">Especifica o objeto da chave de criptografia do disco em um disco.</span><span class="sxs-lookup"><span data-stu-id="8e777-119">Specifies the disk encryption key object on a disk.</span></span>

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

### <span data-ttu-id="8e777-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="8e777-120">-DiskSizeGB</span></span>
<span data-ttu-id="8e777-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="8e777-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e777-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="8e777-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="8e777-123">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="8e777-123">Enable encryption settings.</span></span>

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

### <span data-ttu-id="8e777-124">-ImageReference</span><span class="sxs-lookup"><span data-stu-id="8e777-124">-ImageReference</span></span>
<span data-ttu-id="8e777-125">Especifica a referência de imagem em um disco.</span><span class="sxs-lookup"><span data-stu-id="8e777-125">Specifies the image reference on a disk.</span></span>

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

### <span data-ttu-id="8e777-126">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8e777-126">-KeyEncryptionKey</span></span>
<span data-ttu-id="8e777-127">Especifica a chave de criptografia da chave em um disco.</span><span class="sxs-lookup"><span data-stu-id="8e777-127">Specifies the Key encryption key on a disk.</span></span>

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

### <span data-ttu-id="8e777-128">-Local</span><span class="sxs-lookup"><span data-stu-id="8e777-128">-Location</span></span>
<span data-ttu-id="8e777-129">Especifica um local.</span><span class="sxs-lookup"><span data-stu-id="8e777-129">Specifies a location.</span></span>

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

### <span data-ttu-id="8e777-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="8e777-130">-OsType</span></span>
<span data-ttu-id="8e777-131">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8e777-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="8e777-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8e777-132">-SkuName</span></span>
<span data-ttu-id="8e777-133">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e777-133">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e777-134">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8e777-134">-SourceResourceId</span></span>
<span data-ttu-id="8e777-135">Especifica a ID do recurso de origem.</span><span class="sxs-lookup"><span data-stu-id="8e777-135">Specifies the  source resource ID.</span></span>

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

### <span data-ttu-id="8e777-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="8e777-136">-SourceUri</span></span>
<span data-ttu-id="8e777-137">Especifica o URI de origem.</span><span class="sxs-lookup"><span data-stu-id="8e777-137">Specifies the source Uri.</span></span>

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

### <span data-ttu-id="8e777-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e777-138">-StorageAccountId</span></span>
<span data-ttu-id="8e777-139">Especifica a ID da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8e777-139">Specifies the storage account ID.</span></span>

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

### <span data-ttu-id="8e777-140">-Marca</span><span class="sxs-lookup"><span data-stu-id="8e777-140">-Tag</span></span>
<span data-ttu-id="8e777-141">Especifica que recursos e grupos de recursos podem ser marcados com um conjunto de pares de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="8e777-141">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

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

### <span data-ttu-id="8e777-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="8e777-142">-Zone</span></span>
<span data-ttu-id="8e777-143">Especifica a lista de zonas lógicas do disco.</span><span class="sxs-lookup"><span data-stu-id="8e777-143">Specifies the logical zone list for Disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e777-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8e777-144">-Confirm</span></span>
<span data-ttu-id="8e777-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e777-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e777-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e777-146">-WhatIf</span></span>
<span data-ttu-id="8e777-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e777-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e777-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e777-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e777-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e777-149">CommonParameters</span></span>
<span data-ttu-id="8e777-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e777-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e777-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e777-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e777-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8e777-152">INPUTS</span></span>

### <span data-ttu-id="8e777-153">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. Models. StorageAccountTypes, Microsoft. Azure. Management. Compute, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8e777-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>
<span data-ttu-id="8e777-154">System. Anulável `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. String System. Collections. Hashtable System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable` 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] Microsoft. COMPUTE. Management. COMPUTE. Models. KeyVaultAndSecretReference Microsoft. Azure. Management. Compute</span><span class="sxs-lookup"><span data-stu-id="8e777-154">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.String System.Collections.Hashtable System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOption, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
Microsoft.Azure.Management.Compute.Models.ImageDiskReference
System.Nullable`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference</span></span>

## <span data-ttu-id="8e777-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8e777-155">OUTPUTS</span></span>

### <span data-ttu-id="8e777-156">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="8e777-156">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="8e777-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8e777-157">NOTES</span></span>

## <span data-ttu-id="8e777-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e777-158">RELATED LINKS</span></span>
