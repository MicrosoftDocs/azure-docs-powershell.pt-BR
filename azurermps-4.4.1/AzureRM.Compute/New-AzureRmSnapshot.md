---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmSnapshot.md
ms.openlocfilehash: c7d88f16ff9eb6bb32cdf286ef37a1aba17030cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441174"
---
# <span data-ttu-id="14097-101">New-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="14097-101">New-AzureRmSnapshot</span></span>

## <span data-ttu-id="14097-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14097-102">SYNOPSIS</span></span>
<span data-ttu-id="14097-103">Cria um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="14097-103">Creates a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14097-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14097-104">SYNTAX</span></span>

```
New-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <PSSnapshot>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14097-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14097-105">DESCRIPTION</span></span>
<span data-ttu-id="14097-106">O cmdlet **New-AzureRmSnapshot** cria um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="14097-106">The **New-AzureRmSnapshot** cmdlet creates a snapshot.</span></span>

## <span data-ttu-id="14097-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14097-107">EXAMPLES</span></span>

### <span data-ttu-id="14097-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14097-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotconfig = Set-AzureRmSnapshotDiskEncryptionKey -Snapshot $snapshotconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotconfig = Set-AzureRmSnapshotKeyEncryptionKey -Snapshot $snapshotconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="14097-109">O primeiro comando cria um objeto de instantâneo vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="14097-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="14097-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="14097-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="14097-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="14097-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="14097-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="14097-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="14097-113">OS</span><span class="sxs-lookup"><span data-stu-id="14097-113">PARAMETERS</span></span>

### <span data-ttu-id="14097-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14097-114">-DefaultProfile</span></span>
<span data-ttu-id="14097-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14097-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14097-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14097-116">-ResourceGroupName</span></span>
<span data-ttu-id="14097-117">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14097-117">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14097-118">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="14097-118">-Snapshot</span></span>
<span data-ttu-id="14097-119">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="14097-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14097-120">-Instantâneoname</span><span class="sxs-lookup"><span data-stu-id="14097-120">-SnapshotName</span></span>
<span data-ttu-id="14097-121">Especifica o nome de um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="14097-121">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14097-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14097-122">-Confirm</span></span>
<span data-ttu-id="14097-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14097-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14097-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14097-124">-WhatIf</span></span>
<span data-ttu-id="14097-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14097-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14097-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14097-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14097-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14097-127">CommonParameters</span></span>
<span data-ttu-id="14097-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14097-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14097-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14097-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14097-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14097-130">INPUTS</span></span>

### <span data-ttu-id="14097-131">System. String</span><span class="sxs-lookup"><span data-stu-id="14097-131">System.String</span></span>
<span data-ttu-id="14097-132">Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="14097-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="14097-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14097-133">OUTPUTS</span></span>

### <span data-ttu-id="14097-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="14097-134">System.Object</span></span>

## <span data-ttu-id="14097-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14097-135">NOTES</span></span>

## <span data-ttu-id="14097-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14097-136">RELATED LINKS</span></span>
