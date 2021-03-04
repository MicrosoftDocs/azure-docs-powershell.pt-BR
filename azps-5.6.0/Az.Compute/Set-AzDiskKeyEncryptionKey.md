---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: 4a130755b4cfd84b0394d51c7dcf65b0437925e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885484"
---
# <span data-ttu-id="dfceb-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="dfceb-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="dfceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfceb-102">SYNOPSIS</span></span>
<span data-ttu-id="dfceb-103">Define as propriedades principais da chave de criptografia em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="dfceb-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="dfceb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dfceb-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfceb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfceb-105">DESCRIPTION</span></span>
<span data-ttu-id="dfceb-106">O cmdlet **Set-AzDiskKeyEncryptionKey** define as principais propriedades da chave de criptografia em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="dfceb-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="dfceb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfceb-107">EXAMPLES</span></span>

### <span data-ttu-id="dfceb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dfceb-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskconfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1';
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="dfceb-109">O primeiro comando cria um objeto de disco vazio local com tamanho de 5 GB Standard_LRS de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dfceb-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="dfceb-110">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="dfceb-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="dfceb-111">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="dfceb-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="dfceb-112">O último comando pega o objeto de disco e cria um disco com o nome 'Disk01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="dfceb-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="dfceb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dfceb-113">PARAMETERS</span></span>

### <span data-ttu-id="dfceb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfceb-114">-DefaultProfile</span></span>
<span data-ttu-id="dfceb-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="dfceb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfceb-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="dfceb-116">-Disk</span></span>
<span data-ttu-id="dfceb-117">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="dfceb-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfceb-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="dfceb-118">-KeyUrl</span></span>
<span data-ttu-id="dfceb-119">Especifica a Url da chave.</span><span class="sxs-lookup"><span data-stu-id="dfceb-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="dfceb-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="dfceb-120">-SourceVaultId</span></span>
<span data-ttu-id="dfceb-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="dfceb-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="dfceb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfceb-122">-Confirm</span></span>
<span data-ttu-id="dfceb-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfceb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfceb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfceb-124">-WhatIf</span></span>
<span data-ttu-id="dfceb-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dfceb-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfceb-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dfceb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfceb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfceb-127">CommonParameters</span></span>
<span data-ttu-id="dfceb-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfceb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfceb-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfceb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfceb-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfceb-130">INPUTS</span></span>

### <span data-ttu-id="dfceb-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="dfceb-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="dfceb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dfceb-132">System.String</span></span>

## <span data-ttu-id="dfceb-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dfceb-133">OUTPUTS</span></span>

### <span data-ttu-id="dfceb-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="dfceb-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="dfceb-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="dfceb-135">NOTES</span></span>

## <span data-ttu-id="dfceb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfceb-136">RELATED LINKS</span></span>
