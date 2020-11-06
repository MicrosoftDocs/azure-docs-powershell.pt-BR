---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: ff70d3879685b0cdc9fcc42732a68e6b85bbd580
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426762"
---
# <span data-ttu-id="1bd07-101">Update-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1bd07-101">Update-AzureRmSnapshot</span></span>

## <span data-ttu-id="1bd07-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bd07-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd07-103">Atualiza um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="1bd07-103">Updates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bd07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bd07-104">SYNTAX</span></span>

### <span data-ttu-id="1bd07-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="1bd07-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <SnapshotUpdate> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bd07-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="1bd07-106">FriendMethod</span></span>
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bd07-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bd07-107">DESCRIPTION</span></span>
<span data-ttu-id="1bd07-108">O cmdlet **Update-AzureRmSnapshot** atualiza um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="1bd07-108">The **Update-AzureRmSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="1bd07-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bd07-109">EXAMPLES</span></span>

### <span data-ttu-id="1bd07-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1bd07-110">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="1bd07-111">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1bd07-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="1bd07-112">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="1bd07-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="1bd07-113">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="1bd07-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="1bd07-114">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1bd07-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="1bd07-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1bd07-115">Example 2</span></span>
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="1bd07-116">Este comando atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="1bd07-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="1bd07-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1bd07-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="1bd07-118">Esses comandos também atualizam um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="1bd07-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="1bd07-119">OS</span><span class="sxs-lookup"><span data-stu-id="1bd07-119">PARAMETERS</span></span>

### <span data-ttu-id="1bd07-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd07-120">-ResourceGroupName</span></span>
<span data-ttu-id="1bd07-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1bd07-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1bd07-122">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="1bd07-122">-Snapshot</span></span>
<span data-ttu-id="1bd07-123">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="1bd07-123">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd07-124">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="1bd07-124">-SnapshotName</span></span>
<span data-ttu-id="1bd07-125">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="1bd07-125">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1bd07-126">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="1bd07-126">-SnapshotUpdate</span></span>
<span data-ttu-id="1bd07-127">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="1bd07-127">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd07-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1bd07-128">-Confirm</span></span>
<span data-ttu-id="1bd07-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bd07-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bd07-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bd07-130">-WhatIf</span></span>
<span data-ttu-id="1bd07-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1bd07-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bd07-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1bd07-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bd07-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd07-133">CommonParameters</span></span>
<span data-ttu-id="1bd07-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bd07-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd07-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd07-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd07-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bd07-136">INPUTS</span></span>

### <span data-ttu-id="1bd07-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1bd07-137">System.String</span></span>
<span data-ttu-id="1bd07-138">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="1bd07-138">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="1bd07-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bd07-139">OUTPUTS</span></span>

### <span data-ttu-id="1bd07-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="1bd07-140">System.Object</span></span>

## <span data-ttu-id="1bd07-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bd07-141">NOTES</span></span>

## <span data-ttu-id="1bd07-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bd07-142">RELATED LINKS</span></span>
