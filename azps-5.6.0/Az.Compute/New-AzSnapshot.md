---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzSnapshot.md
ms.openlocfilehash: f73132550eceb092c8c869e7a555173c11d7d226
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888996"
---
# <span data-ttu-id="b8be6-101">New-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8be6-101">New-AzSnapshot</span></span>

## <span data-ttu-id="b8be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8be6-102">SYNOPSIS</span></span>
<span data-ttu-id="b8be6-103">Cria um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b8be6-103">Creates a snapshot.</span></span>

## <span data-ttu-id="b8be6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8be6-104">SYNTAX</span></span>

```
New-AzSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8be6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8be6-105">DESCRIPTION</span></span>
<span data-ttu-id="b8be6-106">O cmdlet **New-AzSnapshot** cria um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b8be6-106">The **New-AzSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="b8be6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8be6-107">EXAMPLES</span></span>

### <span data-ttu-id="b8be6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8be6-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="b8be6-109">O primeiro comando cria um objeto instantâneo vazio local com tamanho de 5 GB Standard_LRS de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b8be6-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="b8be6-110">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b8be6-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b8be6-111">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b8be6-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="b8be6-112">O último comando pega o objeto instantâneo e cria um instantâneo com o nome 'Instantâneo01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="b8be6-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b8be6-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8be6-113">PARAMETERS</span></span>

### <span data-ttu-id="b8be6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8be6-114">-AsJob</span></span>
<span data-ttu-id="b8be6-115">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="b8be6-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b8be6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8be6-116">-DefaultProfile</span></span>
<span data-ttu-id="b8be6-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="b8be6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8be6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8be6-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8be6-119">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8be6-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b8be6-120">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="b8be6-120">-Snapshot</span></span>
<span data-ttu-id="b8be6-121">Especifica um objeto instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="b8be6-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8be6-122">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="b8be6-122">-SnapshotName</span></span>
<span data-ttu-id="b8be6-123">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="b8be6-123">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="b8be6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8be6-124">-Confirm</span></span>
<span data-ttu-id="b8be6-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8be6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8be6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8be6-126">-WhatIf</span></span>
<span data-ttu-id="b8be6-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8be6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8be6-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8be6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8be6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8be6-129">CommonParameters</span></span>
<span data-ttu-id="b8be6-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8be6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8be6-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8be6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8be6-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8be6-132">INPUTS</span></span>

### <span data-ttu-id="b8be6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b8be6-133">System.String</span></span>

### <span data-ttu-id="b8be6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8be6-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b8be6-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8be6-135">OUTPUTS</span></span>

### <span data-ttu-id="b8be6-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="b8be6-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="b8be6-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8be6-137">NOTES</span></span>

## <span data-ttu-id="b8be6-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8be6-138">RELATED LINKS</span></span>
