---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: aa73d486f1dda2c006453b5482a3a27096050beb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597236"
---
# <span data-ttu-id="5fb17-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5fb17-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="5fb17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fb17-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb17-103">Define as propriedades da chave de criptografia de chave em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5fb17-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="5fb17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fb17-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fb17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fb17-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb17-106">O cmdlet **set-AzSnapshotUpdateKeyEncryptionKey** define as propriedades da chave de criptografia de chave em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5fb17-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="5fb17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fb17-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb17-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5fb17-108">Example 1</span></span>
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

<span data-ttu-id="5fb17-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5fb17-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="5fb17-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5fb17-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5fb17-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="5fb17-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="5fb17-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="5fb17-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5fb17-113">OS</span><span class="sxs-lookup"><span data-stu-id="5fb17-113">PARAMETERS</span></span>

### <span data-ttu-id="5fb17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb17-114">-DefaultProfile</span></span>
<span data-ttu-id="5fb17-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb17-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fb17-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="5fb17-116">-KeyUrl</span></span>
<span data-ttu-id="5fb17-117">Especifica a URL da chave.</span><span class="sxs-lookup"><span data-stu-id="5fb17-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="5fb17-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5fb17-118">-SnapshotUpdate</span></span>
<span data-ttu-id="5fb17-119">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="5fb17-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="5fb17-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5fb17-120">-SourceVaultId</span></span>
<span data-ttu-id="5fb17-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="5fb17-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="5fb17-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fb17-122">-Confirm</span></span>
<span data-ttu-id="5fb17-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fb17-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fb17-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fb17-124">-WhatIf</span></span>
<span data-ttu-id="5fb17-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fb17-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5fb17-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fb17-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fb17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb17-127">CommonParameters</span></span>
<span data-ttu-id="5fb17-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb17-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fb17-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb17-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fb17-130">INPUTS</span></span>

### <span data-ttu-id="5fb17-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5fb17-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="5fb17-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5fb17-132">System.String</span></span>

## <span data-ttu-id="5fb17-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fb17-133">OUTPUTS</span></span>

### <span data-ttu-id="5fb17-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="5fb17-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="5fb17-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fb17-135">NOTES</span></span>

## <span data-ttu-id="5fb17-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fb17-136">RELATED LINKS</span></span>
