---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: 73c765d35238d960a95b86c90ad2ff7f2cd5db11
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259163"
---
# <span data-ttu-id="91e23-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="91e23-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="91e23-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91e23-102">SYNOPSIS</span></span>
<span data-ttu-id="91e23-103">Define as propriedades da chave de criptografia de chave em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="91e23-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="91e23-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91e23-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91e23-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91e23-105">DESCRIPTION</span></span>
<span data-ttu-id="91e23-106">O cmdlet **set-AzDiskUpdateKeyEncryptionKey** define as propriedades da chave de criptografia de chave em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="91e23-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="91e23-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91e23-107">EXAMPLES</span></span>

### <span data-ttu-id="91e23-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91e23-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="91e23-109">O primeiro comando cria um objeto de atualização de disco vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="91e23-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="91e23-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="91e23-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="91e23-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="91e23-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="91e23-112">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="91e23-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="91e23-113">OS</span><span class="sxs-lookup"><span data-stu-id="91e23-113">PARAMETERS</span></span>

### <span data-ttu-id="91e23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e23-114">-DefaultProfile</span></span>
<span data-ttu-id="91e23-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91e23-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91e23-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="91e23-116">-DiskUpdate</span></span>
<span data-ttu-id="91e23-117">Especifica um objeto de atualização de disco local.</span><span class="sxs-lookup"><span data-stu-id="91e23-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91e23-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="91e23-118">-KeyUrl</span></span>
<span data-ttu-id="91e23-119">Especifica a URL da chave.</span><span class="sxs-lookup"><span data-stu-id="91e23-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="91e23-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="91e23-120">-SourceVaultId</span></span>
<span data-ttu-id="91e23-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="91e23-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="91e23-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91e23-122">-Confirm</span></span>
<span data-ttu-id="91e23-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91e23-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91e23-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91e23-124">-WhatIf</span></span>
<span data-ttu-id="91e23-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91e23-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91e23-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91e23-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91e23-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e23-127">CommonParameters</span></span>
<span data-ttu-id="91e23-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91e23-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e23-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91e23-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e23-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91e23-130">INPUTS</span></span>

### <span data-ttu-id="91e23-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="91e23-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="91e23-132">System. String</span><span class="sxs-lookup"><span data-stu-id="91e23-132">System.String</span></span>

## <span data-ttu-id="91e23-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91e23-133">OUTPUTS</span></span>

### <span data-ttu-id="91e23-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="91e23-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="91e23-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91e23-135">NOTES</span></span>

## <span data-ttu-id="91e23-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91e23-136">RELATED LINKS</span></span>
