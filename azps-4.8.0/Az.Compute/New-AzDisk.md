---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDisk.md
ms.openlocfilehash: 9491c5292353678f3c8159b8c3cb1d960b7bb774
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955973"
---
# <span data-ttu-id="393e7-101">New-AzDisk</span><span class="sxs-lookup"><span data-stu-id="393e7-101">New-AzDisk</span></span>

## <span data-ttu-id="393e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="393e7-102">SYNOPSIS</span></span>
<span data-ttu-id="393e7-103">Cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="393e7-103">Creates a managed disk.</span></span>

## <span data-ttu-id="393e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="393e7-104">SYNTAX</span></span>

```
New-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="393e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="393e7-105">DESCRIPTION</span></span>
<span data-ttu-id="393e7-106">O cmdlet **New-AzDisk** cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="393e7-106">The **New-AzDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="393e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="393e7-107">EXAMPLES</span></span>

### <span data-ttu-id="393e7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="393e7-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="393e7-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="393e7-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="393e7-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="393e7-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="393e7-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="393e7-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="393e7-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="393e7-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="393e7-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="393e7-113">Example 2</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType Standard_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $diskConfig.EncryptionSettingsCollection = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsCollection

PS C:\> $encryptionSettingsElement1 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_1
PS C:\> $encryptionSettingsElement1.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_1

PS C:\> $encryptionSettingsElement2 = New-Object Microsoft.Azure.Management.Compute.Models.EncryptionSettingsElement
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndSecretReference
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SourceVault.Id = $disk_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.DiskEncryptionKey.SecretUrl = $disk_encryption_secret_url_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey = New-Object Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault = New-Object Microsoft.Azure.Management.Compute.Models.SourceVault
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.SourceVault.Id = $key_encryption_key_id_2
PS C:\> $encryptionSettingsElement2.KeyEncryptionKey.KeyUrl = $key_encryption_key_url_2

PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement1
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettings += $encryptionSettingsElement2
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="393e7-114">O comando acima cria um disco com duas configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="393e7-114">The above command creates a disk with two encryption settings.</span></span>

## <span data-ttu-id="393e7-115">OS</span><span class="sxs-lookup"><span data-stu-id="393e7-115">PARAMETERS</span></span>

### <span data-ttu-id="393e7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="393e7-116">-AsJob</span></span>
<span data-ttu-id="393e7-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="393e7-117">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="393e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="393e7-118">-DefaultProfile</span></span>
<span data-ttu-id="393e7-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="393e7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="393e7-120">-Disco</span><span class="sxs-lookup"><span data-stu-id="393e7-120">-Disk</span></span>
<span data-ttu-id="393e7-121">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="393e7-121">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="393e7-122">-Diskname</span><span class="sxs-lookup"><span data-stu-id="393e7-122">-DiskName</span></span>
<span data-ttu-id="393e7-123">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="393e7-123">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="393e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="393e7-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="393e7-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="393e7-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="393e7-126">-Confirm</span></span>
<span data-ttu-id="393e7-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="393e7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="393e7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="393e7-128">-WhatIf</span></span>
<span data-ttu-id="393e7-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="393e7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="393e7-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="393e7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="393e7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="393e7-131">CommonParameters</span></span>
<span data-ttu-id="393e7-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="393e7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="393e7-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="393e7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="393e7-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="393e7-134">INPUTS</span></span>

### <span data-ttu-id="393e7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="393e7-135">System.String</span></span>

### <span data-ttu-id="393e7-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="393e7-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="393e7-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="393e7-137">OUTPUTS</span></span>

### <span data-ttu-id="393e7-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="393e7-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="393e7-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="393e7-139">NOTES</span></span>

## <span data-ttu-id="393e7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="393e7-140">RELATED LINKS</span></span>
