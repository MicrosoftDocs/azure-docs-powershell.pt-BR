---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 81cf8a6d011575702f8eead878e8987a5a0fd456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610833"
---
# <span data-ttu-id="40b87-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="40b87-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="40b87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40b87-102">SYNOPSIS</span></span>
<span data-ttu-id="40b87-103">Atualiza um disco.</span><span class="sxs-lookup"><span data-stu-id="40b87-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40b87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40b87-104">SYNTAX</span></span>

### <span data-ttu-id="40b87-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="40b87-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40b87-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="40b87-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b87-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40b87-107">DESCRIPTION</span></span>
<span data-ttu-id="40b87-108">O cmdlet **Update-AzureRmDisk** atualiza um disco.</span><span class="sxs-lookup"><span data-stu-id="40b87-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="40b87-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40b87-109">EXAMPLES</span></span>

### <span data-ttu-id="40b87-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="40b87-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="40b87-111">O primeiro comando cria um objeto de atualização de disco vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="40b87-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="40b87-112">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="40b87-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="40b87-113">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="40b87-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="40b87-114">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="40b87-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="40b87-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="40b87-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="40b87-116">Este comando atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="40b87-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="40b87-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="40b87-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="40b87-118">Esses comandos também atualizam um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="40b87-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="40b87-119">OS</span><span class="sxs-lookup"><span data-stu-id="40b87-119">PARAMETERS</span></span>

### <span data-ttu-id="40b87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b87-120">-DefaultProfile</span></span>
<span data-ttu-id="40b87-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40b87-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b87-122">-Disco</span><span class="sxs-lookup"><span data-stu-id="40b87-122">-Disk</span></span>
<span data-ttu-id="40b87-123">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="40b87-123">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40b87-124">-Diskname</span><span class="sxs-lookup"><span data-stu-id="40b87-124">-DiskName</span></span>
<span data-ttu-id="40b87-125">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="40b87-125">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="40b87-126">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="40b87-126">-DiskUpdate</span></span>
<span data-ttu-id="40b87-127">Especifica um objeto de atualização de disco local.</span><span class="sxs-lookup"><span data-stu-id="40b87-127">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40b87-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b87-128">-ResourceGroupName</span></span>
<span data-ttu-id="40b87-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="40b87-129">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="40b87-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40b87-130">-Confirm</span></span>
<span data-ttu-id="40b87-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40b87-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b87-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b87-132">-WhatIf</span></span>
<span data-ttu-id="40b87-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40b87-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b87-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40b87-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b87-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b87-135">CommonParameters</span></span>
<span data-ttu-id="40b87-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b87-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b87-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b87-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b87-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40b87-138">INPUTS</span></span>

### <span data-ttu-id="40b87-139">System. String</span><span class="sxs-lookup"><span data-stu-id="40b87-139">System.String</span></span>
<span data-ttu-id="40b87-140">Microsoft. Azure. Management. COMPUTE. Models. DiskUpdate Microsoft. Azure. Management. COMPUTE. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="40b87-140">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="40b87-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40b87-141">OUTPUTS</span></span>

### <span data-ttu-id="40b87-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="40b87-142">System.Object</span></span>

## <span data-ttu-id="40b87-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40b87-143">NOTES</span></span>

## <span data-ttu-id="40b87-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40b87-144">RELATED LINKS</span></span>

