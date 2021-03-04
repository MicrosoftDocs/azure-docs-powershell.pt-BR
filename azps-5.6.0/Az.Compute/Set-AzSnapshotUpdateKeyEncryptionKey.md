---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateKeyEncryptionKey.md
ms.openlocfilehash: b87dbef98f336d1171da4b33d4ced1cc86e04fdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886342"
---
# <span data-ttu-id="d405d-101">Set-AzSnapshotUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d405d-101">Set-AzSnapshotUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="d405d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d405d-102">SYNOPSIS</span></span>
<span data-ttu-id="d405d-103">Define as propriedades principais da chave de criptografia em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="d405d-103">Sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="d405d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d405d-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateKeyEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-KeyUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d405d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d405d-105">DESCRIPTION</span></span>
<span data-ttu-id="d405d-106">O cmdlet **Set-AzSnapshotUpdateKeyEncryptionKey** define as principais propriedades da chave de criptografia em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="d405d-106">The **Set-AzSnapshotUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="d405d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d405d-107">EXAMPLES</span></span>

### <span data-ttu-id="d405d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d405d-108">Example 1</span></span>
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

<span data-ttu-id="d405d-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com tamanho de 10 GB Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d405d-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d405d-110">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="d405d-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="d405d-111">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="d405d-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="d405d-112">O último comando pega o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="d405d-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d405d-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d405d-113">PARAMETERS</span></span>

### <span data-ttu-id="d405d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d405d-114">-DefaultProfile</span></span>
<span data-ttu-id="d405d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="d405d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d405d-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="d405d-116">-KeyUrl</span></span>
<span data-ttu-id="d405d-117">Especifica a Url da chave.</span><span class="sxs-lookup"><span data-stu-id="d405d-117">Specifies the key Url.</span></span>

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

### <span data-ttu-id="d405d-118">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d405d-118">-SnapshotUpdate</span></span>
<span data-ttu-id="d405d-119">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="d405d-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="d405d-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d405d-120">-SourceVaultId</span></span>
<span data-ttu-id="d405d-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="d405d-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="d405d-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d405d-122">-Confirm</span></span>
<span data-ttu-id="d405d-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d405d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d405d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d405d-124">-WhatIf</span></span>
<span data-ttu-id="d405d-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d405d-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d405d-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d405d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d405d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d405d-127">CommonParameters</span></span>
<span data-ttu-id="d405d-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d405d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d405d-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d405d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d405d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d405d-130">INPUTS</span></span>

### <span data-ttu-id="d405d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d405d-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="d405d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d405d-132">System.String</span></span>

## <span data-ttu-id="d405d-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d405d-133">OUTPUTS</span></span>

### <span data-ttu-id="d405d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="d405d-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="d405d-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="d405d-135">NOTES</span></span>

## <span data-ttu-id="d405d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d405d-136">RELATED LINKS</span></span>
