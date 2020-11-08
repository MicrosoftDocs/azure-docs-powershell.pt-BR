---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 18f013643ad65bd4f7c70f3181e5950e10aa08ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116767"
---
# <span data-ttu-id="b8445-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="b8445-101">Update-AzDisk</span></span>

## <span data-ttu-id="b8445-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8445-102">SYNOPSIS</span></span>
<span data-ttu-id="b8445-103">Atualiza um disco.</span><span class="sxs-lookup"><span data-stu-id="b8445-103">Updates a disk.</span></span>

## <span data-ttu-id="b8445-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8445-104">SYNTAX</span></span>

### <span data-ttu-id="b8445-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="b8445-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8445-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b8445-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8445-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b8445-107">DESCRIPTION</span></span>
<span data-ttu-id="b8445-108">O cmdlet **Update-AzDisk** atualiza um disco.</span><span class="sxs-lookup"><span data-stu-id="b8445-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="b8445-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8445-109">EXAMPLES</span></span>

### <span data-ttu-id="b8445-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b8445-110">Example 1</span></span>
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

<span data-ttu-id="b8445-111">O primeiro comando cria um objeto de atualização de disco vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b8445-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="b8445-112">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="b8445-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="b8445-113">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de disco.</span><span class="sxs-lookup"><span data-stu-id="b8445-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="b8445-114">O último comando usa o objeto de atualização de disco e atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b8445-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="b8445-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b8445-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="b8445-116">Este comando atualiza um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="b8445-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="b8445-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b8445-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="b8445-118">Esses comandos também atualizam um disco existente com o nome "Disk01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="b8445-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="b8445-119">OS</span><span class="sxs-lookup"><span data-stu-id="b8445-119">PARAMETERS</span></span>

### <span data-ttu-id="b8445-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8445-120">-AsJob</span></span>
<span data-ttu-id="b8445-121">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="b8445-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8445-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8445-122">-DefaultProfile</span></span>
<span data-ttu-id="b8445-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8445-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8445-124">-Disco</span><span class="sxs-lookup"><span data-stu-id="b8445-124">-Disk</span></span>
<span data-ttu-id="b8445-125">Especifica um objeto de disco local.</span><span class="sxs-lookup"><span data-stu-id="b8445-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8445-126">-Diskname</span><span class="sxs-lookup"><span data-stu-id="b8445-126">-DiskName</span></span>
<span data-ttu-id="b8445-127">Especifica o nome de um disco.</span><span class="sxs-lookup"><span data-stu-id="b8445-127">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8445-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="b8445-128">-DiskUpdate</span></span>
<span data-ttu-id="b8445-129">Especifica um objeto de atualização de disco local.</span><span class="sxs-lookup"><span data-stu-id="b8445-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8445-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8445-130">-ResourceGroupName</span></span>
<span data-ttu-id="b8445-131">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b8445-131">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8445-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b8445-132">-Confirm</span></span>
<span data-ttu-id="b8445-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8445-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8445-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8445-134">-WhatIf</span></span>
<span data-ttu-id="b8445-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8445-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8445-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8445-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8445-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8445-137">CommonParameters</span></span>
<span data-ttu-id="b8445-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8445-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8445-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8445-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8445-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b8445-140">INPUTS</span></span>

### <span data-ttu-id="b8445-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b8445-141">System.String</span></span>

### <span data-ttu-id="b8445-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="b8445-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="b8445-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="b8445-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="b8445-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b8445-144">OUTPUTS</span></span>

### <span data-ttu-id="b8445-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="b8445-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="b8445-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b8445-146">NOTES</span></span>

## <span data-ttu-id="b8445-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8445-147">RELATED LINKS</span></span>
