---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 30a6ac1a3d74423302cc8b39e8b494e2f1ee2e22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602028"
---
# <span data-ttu-id="6dba3-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="6dba3-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="6dba3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6dba3-102">SYNOPSIS</span></span>
<span data-ttu-id="6dba3-103">Atualiza um disco.</span><span class="sxs-lookup"><span data-stu-id="6dba3-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dba3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6dba3-104">SYNTAX</span></span>

### <span data-ttu-id="6dba3-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="6dba3-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <DiskUpdate> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dba3-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="6dba3-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dba3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6dba3-107">DESCRIPTION</span></span>
<span data-ttu-id="6dba3-108">O cmdlet **Update-AzureRmDisk** atualiza um disco.</span><span class="sxs-lookup"><span data-stu-id="6dba3-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="6dba3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6dba3-109">EXAMPLES</span></span>

### <span data-ttu-id="6dba3-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6dba3-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="6dba3-111">O primeiro comando cria um objeto de atualização de disco vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6dba3-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="6dba3-112">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6dba3-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="6dba3-113">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="6dba3-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="6dba3-114">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6dba3-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="6dba3-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6dba3-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="6dba3-116">Este comando atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="6dba3-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="6dba3-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6dba3-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="6dba3-118">Esses comandos também atualizam um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="6dba3-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="6dba3-119">OS</span><span class="sxs-lookup"><span data-stu-id="6dba3-119">PARAMETERS</span></span>

### <span data-ttu-id="6dba3-120">-Disco</span><span class="sxs-lookup"><span data-stu-id="6dba3-120">-Disk</span></span>
<span data-ttu-id="6dba3-121">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="6dba3-121">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dba3-122">-Diskname</span><span class="sxs-lookup"><span data-stu-id="6dba3-122">-DiskName</span></span>
<span data-ttu-id="6dba3-123">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="6dba3-123">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dba3-124">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="6dba3-124">-DiskUpdate</span></span>
<span data-ttu-id="6dba3-125">Especifica um objeto de atualização de disco local.</span><span class="sxs-lookup"><span data-stu-id="6dba3-125">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dba3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dba3-126">-ResourceGroupName</span></span>
<span data-ttu-id="6dba3-127">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6dba3-127">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dba3-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6dba3-128">-Confirm</span></span>
<span data-ttu-id="6dba3-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dba3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dba3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dba3-130">-WhatIf</span></span>
<span data-ttu-id="6dba3-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6dba3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dba3-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6dba3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dba3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dba3-133">CommonParameters</span></span>
<span data-ttu-id="6dba3-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dba3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dba3-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dba3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dba3-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6dba3-136">INPUTS</span></span>

### <span data-ttu-id="6dba3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6dba3-137">System.String</span></span>
<span data-ttu-id="6dba3-138">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="6dba3-138">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="6dba3-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6dba3-139">OUTPUTS</span></span>

### <span data-ttu-id="6dba3-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="6dba3-140">System.Object</span></span>

## <span data-ttu-id="6dba3-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6dba3-141">NOTES</span></span>

## <span data-ttu-id="6dba3-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dba3-142">RELATED LINKS</span></span>

