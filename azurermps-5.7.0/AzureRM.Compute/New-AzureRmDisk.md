---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 04106c91e99372b985c0a10ac12a7944fdcb4e41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610413"
---
# <span data-ttu-id="18212-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="18212-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="18212-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18212-102">SYNOPSIS</span></span>
<span data-ttu-id="18212-103">Cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="18212-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18212-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18212-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="18212-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18212-105">DESCRIPTION</span></span>
<span data-ttu-id="18212-106">O cmdlet **New-AzureRmDisk** cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="18212-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="18212-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18212-107">EXAMPLES</span></span>

### <span data-ttu-id="18212-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="18212-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="18212-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="18212-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="18212-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="18212-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="18212-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="18212-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="18212-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="18212-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="18212-113">OS</span><span class="sxs-lookup"><span data-stu-id="18212-113">PARAMETERS</span></span>

### <span data-ttu-id="18212-114">-Disco</span><span class="sxs-lookup"><span data-stu-id="18212-114">-Disk</span></span>
<span data-ttu-id="18212-115">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="18212-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18212-116">-Diskname</span><span class="sxs-lookup"><span data-stu-id="18212-116">-DiskName</span></span>
<span data-ttu-id="18212-117">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="18212-117">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18212-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18212-118">-ResourceGroupName</span></span>
<span data-ttu-id="18212-119">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="18212-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18212-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18212-120">-Confirm</span></span>
<span data-ttu-id="18212-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18212-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18212-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18212-122">-WhatIf</span></span>
<span data-ttu-id="18212-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18212-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18212-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18212-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18212-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18212-125">CommonParameters</span></span>
<span data-ttu-id="18212-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18212-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18212-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18212-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18212-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18212-128">INPUTS</span></span>

### <span data-ttu-id="18212-129">System. String</span><span class="sxs-lookup"><span data-stu-id="18212-129">System.String</span></span>
<span data-ttu-id="18212-130">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="18212-130">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="18212-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18212-131">OUTPUTS</span></span>

### <span data-ttu-id="18212-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="18212-132">System.Object</span></span>

## <span data-ttu-id="18212-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18212-133">NOTES</span></span>

## <span data-ttu-id="18212-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18212-134">RELATED LINKS</span></span>

