---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: 8745202e860cb71d20e17d68203a9bc79b3167ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426783"
---
# <span data-ttu-id="e998a-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e998a-101">Set-AzureRmSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="e998a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e998a-102">SYNOPSIS</span></span>
<span data-ttu-id="e998a-103">Define as propriedades da chave de criptografia de chave em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="e998a-103">Sets the key encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e998a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e998a-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <SnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e998a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e998a-105">DESCRIPTION</span></span>
<span data-ttu-id="e998a-106">O cmdlet **set-AzureRmSnapshotUpdateKeyEncryptionKey** define as propriedades da chave de criptografia de chave em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="e998a-106">The **Set-AzureRmSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="e998a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e998a-107">EXAMPLES</span></span>

### <span data-ttu-id="e998a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e998a-108">Example 1</span></span>
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

<span data-ttu-id="e998a-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e998a-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e998a-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="e998a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e998a-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="e998a-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="e998a-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e998a-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e998a-113">OS</span><span class="sxs-lookup"><span data-stu-id="e998a-113">PARAMETERS</span></span>

### <span data-ttu-id="e998a-114">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="e998a-114">-KeyUrl</span></span>
<span data-ttu-id="e998a-115">Especifica a URL da chave.</span><span class="sxs-lookup"><span data-stu-id="e998a-115">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e998a-116">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e998a-116">-SnapshotUpdate</span></span>
<span data-ttu-id="e998a-117">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="e998a-117">Specifies a local snapshot update object.</span></span>

```yaml
Type: SnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e998a-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e998a-118">-SourceVaultId</span></span>
<span data-ttu-id="e998a-119">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="e998a-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e998a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e998a-120">-Confirm</span></span>
<span data-ttu-id="e998a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e998a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e998a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e998a-122">-WhatIf</span></span>
<span data-ttu-id="e998a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e998a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e998a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e998a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e998a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e998a-125">CommonParameters</span></span>
<span data-ttu-id="e998a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e998a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e998a-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e998a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e998a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e998a-128">INPUTS</span></span>

### <span data-ttu-id="e998a-129">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e998a-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="e998a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e998a-130">System.String</span></span>

## <span data-ttu-id="e998a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e998a-131">OUTPUTS</span></span>

### <span data-ttu-id="e998a-132">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="e998a-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="e998a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e998a-133">NOTES</span></span>

## <span data-ttu-id="e998a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e998a-134">RELATED LINKS</span></span>

