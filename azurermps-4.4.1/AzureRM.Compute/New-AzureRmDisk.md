---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmDisk.md
ms.openlocfilehash: 4392c1ccf19474e1a8f73c5bccca2c09f53cbea8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611003"
---
# <span data-ttu-id="609d8-101">New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="609d8-101">New-AzureRmDisk</span></span>

## <span data-ttu-id="609d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="609d8-102">SYNOPSIS</span></span>
<span data-ttu-id="609d8-103">Cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="609d8-103">Creates a managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="609d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="609d8-104">SYNTAX</span></span>

```
New-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="609d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="609d8-105">DESCRIPTION</span></span>
<span data-ttu-id="609d8-106">O cmdlet **New-AzureRmDisk** cria um disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="609d8-106">The **New-AzureRmDisk** cmdlet creates a managed disk.</span></span>

## <span data-ttu-id="609d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="609d8-107">EXAMPLES</span></span>

### <span data-ttu-id="609d8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="609d8-108">Example 1</span></span>
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

<span data-ttu-id="609d8-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="609d8-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="609d8-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="609d8-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="609d8-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="609d8-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="609d8-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="609d8-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="609d8-113">OS</span><span class="sxs-lookup"><span data-stu-id="609d8-113">PARAMETERS</span></span>

### <span data-ttu-id="609d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609d8-114">-DefaultProfile</span></span>
<span data-ttu-id="609d8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="609d8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="609d8-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="609d8-116">-Disk</span></span>
<span data-ttu-id="609d8-117">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="609d8-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="609d8-118">-Diskname</span><span class="sxs-lookup"><span data-stu-id="609d8-118">-DiskName</span></span>
<span data-ttu-id="609d8-119">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="609d8-119">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="609d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="609d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="609d8-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="609d8-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="609d8-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="609d8-122">-Confirm</span></span>
<span data-ttu-id="609d8-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="609d8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="609d8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="609d8-124">-WhatIf</span></span>
<span data-ttu-id="609d8-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="609d8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="609d8-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="609d8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="609d8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609d8-127">CommonParameters</span></span>
<span data-ttu-id="609d8-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="609d8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609d8-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="609d8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609d8-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="609d8-130">INPUTS</span></span>

### <span data-ttu-id="609d8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="609d8-131">System.String</span></span>
<span data-ttu-id="609d8-132">Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="609d8-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="609d8-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="609d8-133">OUTPUTS</span></span>

### <span data-ttu-id="609d8-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="609d8-134">System.Object</span></span>

## <span data-ttu-id="609d8-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="609d8-135">NOTES</span></span>

## <span data-ttu-id="609d8-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="609d8-136">RELATED LINKS</span></span>

