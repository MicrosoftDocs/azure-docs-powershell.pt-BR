---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 52f6a58f74312b96d09f8dacd8b6ced23db5c26e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602032"
---
# <span data-ttu-id="57100-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="57100-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="57100-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57100-102">SYNOPSIS</span></span>
<span data-ttu-id="57100-103">Define as propriedades da chave de criptografia do disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="57100-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57100-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57100-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <SnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57100-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57100-105">DESCRIPTION</span></span>
<span data-ttu-id="57100-106">O cmdlet **set-AzureRmSnapshotUpdateDiskEncryptionKey** define as propriedades da chave de criptografia de disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="57100-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="57100-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57100-107">EXAMPLES</span></span>

### <span data-ttu-id="57100-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="57100-108">Example 1</span></span>
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

<span data-ttu-id="57100-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57100-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="57100-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="57100-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="57100-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="57100-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="57100-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="57100-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="57100-113">OS</span><span class="sxs-lookup"><span data-stu-id="57100-113">PARAMETERS</span></span>

### <span data-ttu-id="57100-114">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="57100-114">-SecretUrl</span></span>
<span data-ttu-id="57100-115">Especifica a URL secreta.</span><span class="sxs-lookup"><span data-stu-id="57100-115">Specifes the secret Url.</span></span>

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

### <span data-ttu-id="57100-116">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="57100-116">-SnapshotUpdate</span></span>
<span data-ttu-id="57100-117">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="57100-117">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="57100-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="57100-118">-SourceVaultId</span></span>
<span data-ttu-id="57100-119">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="57100-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="57100-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57100-120">-Confirm</span></span>
<span data-ttu-id="57100-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57100-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57100-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57100-122">-WhatIf</span></span>
<span data-ttu-id="57100-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57100-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57100-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57100-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57100-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57100-125">CommonParameters</span></span>
<span data-ttu-id="57100-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57100-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57100-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57100-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57100-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57100-128">INPUTS</span></span>

### <span data-ttu-id="57100-129">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="57100-129">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="57100-130">System. String</span><span class="sxs-lookup"><span data-stu-id="57100-130">System.String</span></span>

## <span data-ttu-id="57100-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57100-131">OUTPUTS</span></span>

### <span data-ttu-id="57100-132">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="57100-132">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="57100-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57100-133">NOTES</span></span>

## <span data-ttu-id="57100-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57100-134">RELATED LINKS</span></span>

