---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzSnapshot.md
ms.openlocfilehash: 6cfe2fd958d74740195b0bb29d3defa34f1310a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259326"
---
# <span data-ttu-id="2cfdd-101">Update-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="2cfdd-101">Update-AzSnapshot</span></span>

## <span data-ttu-id="2cfdd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2cfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfdd-103">Atualiza um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-103">Updates a snapshot.</span></span>

## <span data-ttu-id="2cfdd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cfdd-104">SYNTAX</span></span>

### <span data-ttu-id="2cfdd-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="2cfdd-105">DefaultParameter (Default)</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-SnapshotUpdate] <PSSnapshotUpdate>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cfdd-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2cfdd-106">FriendMethod</span></span>
```
Update-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cfdd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2cfdd-107">DESCRIPTION</span></span>
<span data-ttu-id="2cfdd-108">O cmdlet **Update-AzSnapshot** atualiza um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-108">The **Update-AzSnapshot** cmdlet updates a snapshot.</span></span>

## <span data-ttu-id="2cfdd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2cfdd-109">EXAMPLES</span></span>

### <span data-ttu-id="2cfdd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2cfdd-110">Example 1</span></span>
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

<span data-ttu-id="2cfdd-111">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-111">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2cfdd-112">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2cfdd-113">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-113">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span>
<span data-ttu-id="2cfdd-114">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2cfdd-114">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2cfdd-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2cfdd-115">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="2cfdd-116">Este comando atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-116">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="2cfdd-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2cfdd-117">Example 3</span></span>
```
PS C:\> $snapshot = Get-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

<span data-ttu-id="2cfdd-118">Esses comandos também atualizam um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-118">These commands also update an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="2cfdd-119">OS</span><span class="sxs-lookup"><span data-stu-id="2cfdd-119">PARAMETERS</span></span>

### <span data-ttu-id="2cfdd-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cfdd-120">-AsJob</span></span>
<span data-ttu-id="2cfdd-121">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2cfdd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfdd-122">-DefaultProfile</span></span>
<span data-ttu-id="2cfdd-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cfdd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfdd-124">-ResourceGroupName</span></span>
<span data-ttu-id="2cfdd-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2cfdd-126">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="2cfdd-126">-Snapshot</span></span>
<span data-ttu-id="2cfdd-127">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-127">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="2cfdd-128">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="2cfdd-128">-SnapshotName</span></span>
<span data-ttu-id="2cfdd-129">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-129">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="2cfdd-130">-SnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="2cfdd-130">-SnapshotUpdate</span></span>
<span data-ttu-id="2cfdd-131">Especifica um objeto de atualização de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-131">Specifies a local snapshot update object.</span></span>

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

### <span data-ttu-id="2cfdd-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2cfdd-132">-Confirm</span></span>
<span data-ttu-id="2cfdd-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cfdd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cfdd-134">-WhatIf</span></span>
<span data-ttu-id="2cfdd-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cfdd-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cfdd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfdd-137">CommonParameters</span></span>
<span data-ttu-id="2cfdd-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfdd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfdd-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cfdd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfdd-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2cfdd-140">INPUTS</span></span>

### <span data-ttu-id="2cfdd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2cfdd-141">System.String</span></span>

### <span data-ttu-id="2cfdd-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="2cfdd-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

### <span data-ttu-id="2cfdd-143">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="2cfdd-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="2cfdd-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2cfdd-144">OUTPUTS</span></span>

### <span data-ttu-id="2cfdd-145">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="2cfdd-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="2cfdd-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2cfdd-146">NOTES</span></span>

## <span data-ttu-id="2cfdd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2cfdd-147">RELATED LINKS</span></span>
