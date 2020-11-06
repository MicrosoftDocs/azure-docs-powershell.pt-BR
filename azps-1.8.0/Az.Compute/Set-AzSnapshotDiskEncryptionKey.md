---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotDiskEncryptionKey.md
ms.openlocfilehash: f0c0fa6c8315aef711613dc599027d0653db803e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601248"
---
# <span data-ttu-id="da218-101">Set-AzSnapshotDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="da218-101">Set-AzSnapshotDiskEncryptionKey</span></span>

## <span data-ttu-id="da218-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da218-102">SYNOPSIS</span></span>
<span data-ttu-id="da218-103">Define as propriedades da chave de criptografia do disco em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="da218-103">Sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="da218-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da218-104">SYNTAX</span></span>

```
Set-AzSnapshotDiskEncryptionKey [-Snapshot] <PSSnapshot> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da218-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da218-105">DESCRIPTION</span></span>
<span data-ttu-id="da218-106">O cmdlet **set-AzSnapshotDiskEncryptionKey** define as propriedades da chave de criptografia de disco em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="da218-106">The **Set-AzSnapshotDiskEncryptionKey** cmdlet sets the disk encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="da218-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da218-107">EXAMPLES</span></span>

### <span data-ttu-id="da218-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="da218-108">Example 1</span></span>
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

<span data-ttu-id="da218-109">O primeiro comando cria um objeto de instantâneo vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="da218-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="da218-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="da218-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="da218-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="da218-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="da218-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="da218-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="da218-113">OS</span><span class="sxs-lookup"><span data-stu-id="da218-113">PARAMETERS</span></span>

### <span data-ttu-id="da218-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da218-114">-DefaultProfile</span></span>
<span data-ttu-id="da218-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da218-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da218-116">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="da218-116">-SecretUrl</span></span>
<span data-ttu-id="da218-117">Especifica a URL secreta.</span><span class="sxs-lookup"><span data-stu-id="da218-117">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="da218-118">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="da218-118">-Snapshot</span></span>
<span data-ttu-id="da218-119">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="da218-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da218-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="da218-120">-SourceVaultId</span></span>
<span data-ttu-id="da218-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="da218-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="da218-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da218-122">-Confirm</span></span>
<span data-ttu-id="da218-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da218-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da218-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da218-124">-WhatIf</span></span>
<span data-ttu-id="da218-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da218-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da218-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da218-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da218-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da218-127">CommonParameters</span></span>
<span data-ttu-id="da218-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da218-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da218-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da218-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da218-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da218-130">INPUTS</span></span>

### <span data-ttu-id="da218-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="da218-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="da218-132">System. String</span><span class="sxs-lookup"><span data-stu-id="da218-132">System.String</span></span>

## <span data-ttu-id="da218-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da218-133">OUTPUTS</span></span>

### <span data-ttu-id="da218-134">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="da218-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="da218-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da218-135">NOTES</span></span>

## <span data-ttu-id="da218-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da218-136">RELATED LINKS</span></span>
