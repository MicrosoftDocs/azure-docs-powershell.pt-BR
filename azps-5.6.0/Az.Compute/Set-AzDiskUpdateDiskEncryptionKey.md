---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 06f0cf43e60bdf5e4172227937f786fed491f696
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893236"
---
# <span data-ttu-id="5bf68-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="5bf68-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="5bf68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bf68-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf68-103">Define as propriedades da chave de criptografia de disco em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="5bf68-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="5bf68-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5bf68-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bf68-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5bf68-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf68-106">O cmdlet **Set-AzDiskUpdateDiskEncryptionKey** define as propriedades da chave de criptografia de disco em um objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="5bf68-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="5bf68-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5bf68-107">EXAMPLES</span></span>

### <span data-ttu-id="5bf68-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5bf68-108">Example 1</span></span>
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

<span data-ttu-id="5bf68-109">O primeiro comando cria um objeto de atualização de disco vazio local com tamanho de 10 GB Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5bf68-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="5bf68-110">Ele também define o tipo de sistema operacional do Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5bf68-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="5bf68-111">O segundo e o terceiro comandos definirão as configurações de chave de criptografia de disco e chave de criptografia para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="5bf68-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="5bf68-112">O último comando pega o objeto de atualização de disco e atualiza um disco existente com o nome 'Disk01' no grupo de recursos 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="5bf68-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5bf68-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5bf68-113">PARAMETERS</span></span>

### <span data-ttu-id="5bf68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf68-114">-DefaultProfile</span></span>
<span data-ttu-id="5bf68-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5bf68-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bf68-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="5bf68-116">-DiskUpdate</span></span>
<span data-ttu-id="5bf68-117">Especifica um objeto de atualização de disco local.</span><span class="sxs-lookup"><span data-stu-id="5bf68-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="5bf68-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="5bf68-118">-SecretUrl</span></span>
<span data-ttu-id="5bf68-119">Especifica a Url secreta.</span><span class="sxs-lookup"><span data-stu-id="5bf68-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="5bf68-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5bf68-120">-SourceVaultId</span></span>
<span data-ttu-id="5bf68-121">Especifica a ID do cofre de origem.</span><span class="sxs-lookup"><span data-stu-id="5bf68-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="5bf68-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5bf68-122">-Confirm</span></span>
<span data-ttu-id="5bf68-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf68-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf68-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf68-124">-WhatIf</span></span>
<span data-ttu-id="5bf68-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5bf68-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5bf68-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5bf68-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf68-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf68-127">CommonParameters</span></span>
<span data-ttu-id="5bf68-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf68-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf68-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bf68-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf68-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5bf68-130">INPUTS</span></span>

### <span data-ttu-id="5bf68-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="5bf68-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="5bf68-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5bf68-132">System.String</span></span>

## <span data-ttu-id="5bf68-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5bf68-133">OUTPUTS</span></span>

### <span data-ttu-id="5bf68-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="5bf68-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="5bf68-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="5bf68-135">NOTES</span></span>

## <span data-ttu-id="5bf68-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5bf68-136">RELATED LINKS</span></span>
