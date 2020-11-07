---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermsnapshotkeyencryptionkey
schema: 2.0.0
ms.openlocfilehash: f1ca99aacc8e2c737ed8ddbbe9fa899afe78c12a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785356"
---
# <span data-ttu-id="00ce7-101">Set-AzureRmSnapshotKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="00ce7-101">Set-AzureRmSnapshotKeyEncryptionKey</span></span>

## <span data-ttu-id="00ce7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="00ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="00ce7-103">Define as propriedades da chave de criptografia de chave em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="00ce7-103">Sets the key encryption key properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00ce7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="00ce7-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotKeyEncryptionKey [-Snapshot] <PSSnapshot> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00ce7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="00ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="00ce7-106">O cmdlet **set-AzureRmSnapshotKeyEncryptionKey** define as propriedades da chave de criptografia de chave em um objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="00ce7-106">The **Set-AzureRmSnapshotKeyEncryptionKey** cmdlet sets the key encryption key properties on a snapshot object.</span></span>

## <span data-ttu-id="00ce7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="00ce7-107">EXAMPLES</span></span>

### <span data-ttu-id="00ce7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="00ce7-108">Example 1</span></span>
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

<span data-ttu-id="00ce7-109">O primeiro comando cria um objeto de instantâneo vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="00ce7-109">The first command creates a local empty snapshot object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="00ce7-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="00ce7-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="00ce7-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="00ce7-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot object.</span></span>
<span data-ttu-id="00ce7-112">O último comando pega o objeto de instantâneo e cria um instantâneo com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="00ce7-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="00ce7-113">OS</span><span class="sxs-lookup"><span data-stu-id="00ce7-113">PARAMETERS</span></span>

### <span data-ttu-id="00ce7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ce7-114">-DefaultProfile</span></span>
<span data-ttu-id="00ce7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="00ce7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ce7-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="00ce7-116">-KeyUrl</span></span>
<span data-ttu-id="00ce7-117">Especifica a URL da chave.</span><span class="sxs-lookup"><span data-stu-id="00ce7-117">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ce7-118">-Instantâneo</span><span class="sxs-lookup"><span data-stu-id="00ce7-118">-Snapshot</span></span>
<span data-ttu-id="00ce7-119">Especifica um objeto de instantâneo local.</span><span class="sxs-lookup"><span data-stu-id="00ce7-119">Specifies a local snapshot object.</span></span>

```yaml
Type: PSSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00ce7-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="00ce7-120">-SourceVaultId</span></span>
<span data-ttu-id="00ce7-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="00ce7-121">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00ce7-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="00ce7-122">-Confirm</span></span>
<span data-ttu-id="00ce7-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00ce7-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ce7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ce7-124">-WhatIf</span></span>
<span data-ttu-id="00ce7-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="00ce7-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00ce7-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="00ce7-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ce7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ce7-127">CommonParameters</span></span>
<span data-ttu-id="00ce7-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ce7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ce7-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00ce7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ce7-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="00ce7-130">INPUTS</span></span>

### <span data-ttu-id="00ce7-131">Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="00ce7-131">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="00ce7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="00ce7-132">System.String</span></span>

## <span data-ttu-id="00ce7-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="00ce7-133">OUTPUTS</span></span>

### <span data-ttu-id="00ce7-134">Microsoft. Azure. Management. COMPUTE. Models. snapshot</span><span class="sxs-lookup"><span data-stu-id="00ce7-134">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="00ce7-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="00ce7-135">NOTES</span></span>

## <span data-ttu-id="00ce7-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="00ce7-136">RELATED LINKS</span></span>

