---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskkeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskKeyEncryptionKey.md
ms.openlocfilehash: c207ccf33b42cf0e7cf1fdb319d0ba17d040d3d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597253"
---
# <span data-ttu-id="48f4a-101">Set-AzDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="48f4a-101">Set-AzDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="48f4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="48f4a-103">Define as propriedades da chave de criptografia de chave em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="48f4a-103">Sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="48f4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48f4a-104">SYNTAX</span></span>

```
Set-AzDiskKeyEncryptionKey [-Disk] <PSDisk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48f4a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="48f4a-106">O cmdlet **set-AzDiskKeyEncryptionKey** define as propriedades da chave de criptografia de chave em um objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="48f4a-106">The **Set-AzDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="48f4a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48f4a-107">EXAMPLES</span></span>

### <span data-ttu-id="48f4a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="48f4a-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="48f4a-109">O primeiro comando cria um objeto de disco vazio local com o tamanho de 5 GB em Standard_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="48f4a-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="48f4a-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="48f4a-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="48f4a-111">O segundo e o terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de disco.</span><span class="sxs-lookup"><span data-stu-id="48f4a-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="48f4a-112">O último comando pega o objeto de disco e cria um disco com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="48f4a-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="48f4a-113">OS</span><span class="sxs-lookup"><span data-stu-id="48f4a-113">PARAMETERS</span></span>

### <span data-ttu-id="48f4a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f4a-114">-DefaultProfile</span></span>
<span data-ttu-id="48f4a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48f4a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48f4a-116">-Disco</span><span class="sxs-lookup"><span data-stu-id="48f4a-116">-Disk</span></span>
<span data-ttu-id="48f4a-117">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="48f4a-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="48f4a-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="48f4a-118">-KeyUrl</span></span>
<span data-ttu-id="48f4a-119">Especifica a URL da chave.</span><span class="sxs-lookup"><span data-stu-id="48f4a-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="48f4a-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="48f4a-120">-SourceVaultId</span></span>
<span data-ttu-id="48f4a-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="48f4a-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="48f4a-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48f4a-122">-Confirm</span></span>
<span data-ttu-id="48f4a-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48f4a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48f4a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48f4a-124">-WhatIf</span></span>
<span data-ttu-id="48f4a-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48f4a-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48f4a-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48f4a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48f4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f4a-127">CommonParameters</span></span>
<span data-ttu-id="48f4a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48f4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f4a-129">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48f4a-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f4a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48f4a-130">INPUTS</span></span>

### <span data-ttu-id="48f4a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="48f4a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="48f4a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="48f4a-132">System.String</span></span>

## <span data-ttu-id="48f4a-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48f4a-133">OUTPUTS</span></span>

### <span data-ttu-id="48f4a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="48f4a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="48f4a-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48f4a-135">NOTES</span></span>

## <span data-ttu-id="48f4a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48f4a-136">RELATED LINKS</span></span>
