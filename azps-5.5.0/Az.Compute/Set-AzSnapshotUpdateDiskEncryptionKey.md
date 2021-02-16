---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotUpdateDiskEncryptionKey.md
ms.openlocfilehash: b43593650e3eaed25e59526a067c4c569d19d28a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117825"
---
# <span data-ttu-id="60039-101">Set-AzSnapshotUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="60039-101">Set-AzSnapshotUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="60039-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60039-102">SYNOPSIS</span></span>
<span data-ttu-id="60039-103">Define as propriedades da chave de criptografia de disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="60039-103">Sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="60039-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60039-104">SYNTAX</span></span>

```
Set-AzSnapshotUpdateDiskEncryptionKey [-SnapshotUpdate] <PSSnapshotUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60039-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="60039-105">DESCRIPTION</span></span>
<span data-ttu-id="60039-106">O cmdlet **Set-AzSnapshotUpdateDiskEncryptionKey** define as propriedades da chave de criptografia de disco em um objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="60039-106">The **Set-AzSnapshotUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot update object.</span></span>

## <span data-ttu-id="60039-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="60039-107">EXAMPLES</span></span>

### <span data-ttu-id="60039-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60039-108">Example 1</span></span>
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

<span data-ttu-id="60039-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com tamanho de 10 GB Premium_LRS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="60039-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="60039-110">Ele também define o tipo do sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="60039-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="60039-111">O segundo e o terceiro comandos configuram a chave de criptografia de disco e as configurações da chave de criptografia para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="60039-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="60039-112">O último comando leva o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="60039-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="60039-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60039-113">PARAMETERS</span></span>

### <span data-ttu-id="60039-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60039-114">-DefaultProfile</span></span>
<span data-ttu-id="60039-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="60039-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60039-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="60039-116">-SecretUrl</span></span>
<span data-ttu-id="60039-117">Especifica a URL secreta.</span><span class="sxs-lookup"><span data-stu-id="60039-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="60039-118">-InstantâneoUpdate</span><span class="sxs-lookup"><span data-stu-id="60039-118">-SnapshotUpdate</span></span>
<span data-ttu-id="60039-119">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="60039-119">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="60039-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="60039-120">-SourceVaultId</span></span>
<span data-ttu-id="60039-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="60039-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="60039-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="60039-122">-Confirm</span></span>
<span data-ttu-id="60039-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60039-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60039-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60039-124">-WhatIf</span></span>
<span data-ttu-id="60039-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="60039-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60039-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60039-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60039-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60039-127">CommonParameters</span></span>
<span data-ttu-id="60039-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60039-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60039-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60039-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60039-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="60039-130">INPUTS</span></span>

### <span data-ttu-id="60039-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="60039-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="60039-132">System.String</span><span class="sxs-lookup"><span data-stu-id="60039-132">System.String</span></span>

## <span data-ttu-id="60039-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="60039-133">OUTPUTS</span></span>

### <span data-ttu-id="60039-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="60039-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="60039-135">Notas</span><span class="sxs-lookup"><span data-stu-id="60039-135">NOTES</span></span>

## <span data-ttu-id="60039-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60039-136">RELATED LINKS</span></span>
