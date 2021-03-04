---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 53b27c8144e0016962584baf40543dddf70b7bf3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887811"
---
# <span data-ttu-id="c55fa-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="c55fa-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="c55fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c55fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c55fa-103">Atualiza um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c55fa-103">Updates a snapshot.</span></span>

## <span data-ttu-id="c55fa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c55fa-104">SYNTAX</span></span>

### <span data-ttu-id="c55fa-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c55fa-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c55fa-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="c55fa-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c55fa-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c55fa-107">DESCRIPTION</span></span>
<span data-ttu-id="c55fa-108">O cmdlet **Update-AzSnapshot** atualiza um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c55fa-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="c55fa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c55fa-109">EXAMPLES</span></span>

### <span data-ttu-id="c55fa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c55fa-110">Example 1</span></span>
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

<span data-ttu-id="c55fa-111">O primeiro comando cria um objeto de atualização de instantâneo vazio local com tamanho de 10 GB Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c55fa-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="c55fa-112">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c55fa-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="c55fa-113">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c55fa-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="c55fa-114">O último comando pega o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="c55fa-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c55fa-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c55fa-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="c55fa-116">Este comando atualiza um instantâneo existente com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01' para o tamanho do disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="c55fa-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="c55fa-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c55fa-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="c55fa-118">Esses comandos também atualizam um instantâneo existente com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01' para o tamanho do disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="c55fa-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="c55fa-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c55fa-119">PARAMETERS</span></span>

### <span data-ttu-id="c55fa-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c55fa-120">-AsJob</span></span>
<span data-ttu-id="c55fa-121">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c55fa-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c55fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c55fa-122">-DefaultProfile</span></span>
<span data-ttu-id="c55fa-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c55fa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c55fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c55fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="c55fa-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c55fa-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55fa-126">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="c55fa-126">-Snapshot</span></span>
<span data-ttu-id="c55fa-127">Especifica um objeto instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="c55fa-127">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c55fa-128">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="c55fa-128">-SnapshotName</span></span>
<span data-ttu-id="c55fa-129">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c55fa-129">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c55fa-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c55fa-130">-SnapshotUpdate</span></span>
<span data-ttu-id="c55fa-131">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="c55fa-131">Specifies a local snapshot update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c55fa-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c55fa-132">-Confirm</span></span>
<span data-ttu-id="c55fa-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c55fa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c55fa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c55fa-134">-WhatIf</span></span>
<span data-ttu-id="c55fa-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c55fa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c55fa-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c55fa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c55fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c55fa-137">CommonParameters</span></span>
<span data-ttu-id="c55fa-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c55fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c55fa-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c55fa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c55fa-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c55fa-140">INPUTS</span></span>

### <span data-ttu-id="c55fa-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c55fa-141">System.String</span></span>

### <span data-ttu-id="c55fa-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c55fa-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="c55fa-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="c55fa-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="c55fa-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c55fa-144">OUTPUTS</span></span>

### <span data-ttu-id="c55fa-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="c55fa-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="c55fa-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="c55fa-146">NOTES</span></span>

## <span data-ttu-id="c55fa-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c55fa-147">RELATED LINKS</span></span>
