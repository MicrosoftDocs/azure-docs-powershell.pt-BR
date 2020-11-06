---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: 31f0312e2afe82adc1f7e3906b7efa312192585a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439963"
---
# <span data-ttu-id="114a7-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="114a7-101">Set-AzureRmSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="114a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="114a7-102">SYNOPSIS</span></span>
<span data-ttu-id="114a7-103">Define as propriedades da chave de criptografia do disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="114a7-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="114a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="114a7-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="114a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="114a7-105">DESCRIPTION</span></span>
<span data-ttu-id="114a7-106">O cmdlet **set-AzureRmSnapshotUpdateDiskEncryptionKey** define as propriedades da chave de criptografia de disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="114a7-106">The **Set-AzureRmSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="114a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="114a7-107">EXAMPLES</span></span>

### <span data-ttu-id="114a7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="114a7-108">Example 1</span></span>
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

<span data-ttu-id="114a7-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="114a7-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="114a7-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="114a7-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="114a7-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="114a7-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="114a7-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="114a7-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="114a7-113">OS</span><span class="sxs-lookup"><span data-stu-id="114a7-113">PARAMETERS</span></span>

### <span data-ttu-id="114a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114a7-114">-DefaultProfile</span></span>
<span data-ttu-id="114a7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="114a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="114a7-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="114a7-116">-SecretUrl</span></span>
<span data-ttu-id="114a7-117">Especifica a URL secreta.</span><span class="sxs-lookup"><span data-stu-id="114a7-117">Specifes the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114a7-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="114a7-118">-SnapshotUpdate</span></span>
<span data-ttu-id="114a7-119">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="114a7-119">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="114a7-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="114a7-120">-SourceVaultId</span></span>
<span data-ttu-id="114a7-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="114a7-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="114a7-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="114a7-122">-Confirm</span></span>
<span data-ttu-id="114a7-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="114a7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="114a7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="114a7-124">-WhatIf</span></span>
<span data-ttu-id="114a7-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="114a7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="114a7-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="114a7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="114a7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114a7-127">CommonParameters</span></span>
<span data-ttu-id="114a7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="114a7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114a7-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114a7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114a7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="114a7-130">INPUTS</span></span>

### <span data-ttu-id="114a7-131">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="114a7-131">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>
<span data-ttu-id="114a7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="114a7-132">System.String</span></span>

## <span data-ttu-id="114a7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="114a7-133">OUTPUTS</span></span>

### <span data-ttu-id="114a7-134">Microsoft. Azure. Management. COMPUTE. Models. SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="114a7-134">Microsoft.Azure.Management.Compute.Models.SnapshotUpdate</span></span>

## <span data-ttu-id="114a7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="114a7-135">NOTES</span></span>

## <span data-ttu-id="114a7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="114a7-136">RELATED LINKS</span></span>

