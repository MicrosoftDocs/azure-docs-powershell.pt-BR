---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940973"
---
# <span data-ttu-id="2cfd2-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2cfd2-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="2cfd2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cfd2-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfd2-103">Define as propriedades da chave de criptografia do disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="2cfd2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cfd2-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cfd2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cfd2-105">DESCRIPTION</span></span>
<span data-ttu-id="2cfd2-106">O cmdlet **set-AzSnapshotUpdateDiskEncryptionKey** define as propriedades da chave de criptografia de disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="2cfd2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cfd2-107">EXAMPLES</span></span>

### <span data-ttu-id="2cfd2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2cfd2-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="2cfd2-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2cfd2-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2cfd2-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="2cfd2-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2cfd2-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2cfd2-113">OS</span><span class="sxs-lookup"><span data-stu-id="2cfd2-113">PARAMETERS</span></span>

### <span data-ttu-id="2cfd2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfd2-114">-DefaultProfile</span></span>
<span data-ttu-id="2cfd2-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cfd2-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="2cfd2-116">-SecretUrl</span></span>
<span data-ttu-id="2cfd2-117">Especifica a URL secreta.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="2cfd2-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="2cfd2-118">-SnapshotUpdate</span></span>
<span data-ttu-id="2cfd2-119">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="2cfd2-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="2cfd2-120">-SourceVaultId</span></span>
<span data-ttu-id="2cfd2-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="2cfd2-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2cfd2-122">-Confirm</span></span>
<span data-ttu-id="2cfd2-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cfd2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cfd2-124">-WhatIf</span></span>
<span data-ttu-id="2cfd2-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cfd2-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cfd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfd2-127">CommonParameters</span></span>
<span data-ttu-id="2cfd2-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfd2-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cfd2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfd2-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cfd2-130">INPUTS</span></span>

### <span data-ttu-id="2cfd2-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="2cfd2-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="2cfd2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfd2-132">System.String</span></span>

## <span data-ttu-id="2cfd2-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cfd2-133">OUTPUTS</span></span>

### <span data-ttu-id="2cfd2-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="2cfd2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="2cfd2-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cfd2-135">NOTES</span></span>

## <span data-ttu-id="2cfd2-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cfd2-136">RELATED LINKS</span></span>
