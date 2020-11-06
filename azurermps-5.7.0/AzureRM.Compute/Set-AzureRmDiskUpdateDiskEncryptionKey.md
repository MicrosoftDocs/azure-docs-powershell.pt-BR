---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 4d44bc014a3d38a89e6c9a6a6d755aa9353c052e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431704"
---
# <span data-ttu-id="ec392-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ec392-101">Set-AzureRmDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="ec392-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ec392-102">SYNOPSIS</span></span>
<span data-ttu-id="ec392-103">Define as propriedades da chave de criptografia do disco em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="ec392-103">Sets the disk encryption key properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec392-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ec392-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateDiskEncryptionKey [-DiskUpdate] <DiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec392-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ec392-105">DESCRIPTION</span></span>
<span data-ttu-id="ec392-106">O cmdlet **set-AzureRmDiskUpdateDiskEncryptionKey** define as propriedades da chave de criptografia de disco em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="ec392-106">The **Set-AzureRmDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="ec392-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ec392-107">EXAMPLES</span></span>

### <span data-ttu-id="ec392-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ec392-108">Example 1</span></span>
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

<span data-ttu-id="ec392-109">O primeiro comando cria um objeto de atualização de disco vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ec392-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ec392-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="ec392-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="ec392-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="ec392-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="ec392-112">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ec392-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ec392-113">OS</span><span class="sxs-lookup"><span data-stu-id="ec392-113">PARAMETERS</span></span>

### <span data-ttu-id="ec392-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ec392-114">-DiskUpdate</span></span>
<span data-ttu-id="ec392-115">Especifica um objeto de atualização de disco local.</span><span class="sxs-lookup"><span data-stu-id="ec392-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec392-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="ec392-116">-SecretUrl</span></span>
<span data-ttu-id="ec392-117">Especifica a URL secreta.</span><span class="sxs-lookup"><span data-stu-id="ec392-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="ec392-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="ec392-118">-SourceVaultId</span></span>
<span data-ttu-id="ec392-119">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="ec392-119">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="ec392-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ec392-120">-Confirm</span></span>
<span data-ttu-id="ec392-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec392-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec392-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec392-122">-WhatIf</span></span>
<span data-ttu-id="ec392-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ec392-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec392-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ec392-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec392-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec392-125">CommonParameters</span></span>
<span data-ttu-id="ec392-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec392-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec392-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec392-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec392-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ec392-128">INPUTS</span></span>

### <span data-ttu-id="ec392-129">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ec392-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="ec392-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ec392-130">System.String</span></span>

## <span data-ttu-id="ec392-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ec392-131">OUTPUTS</span></span>

### <span data-ttu-id="ec392-132">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="ec392-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="ec392-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ec392-133">NOTES</span></span>

## <span data-ttu-id="ec392-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ec392-134">RELATED LINKS</span></span>

