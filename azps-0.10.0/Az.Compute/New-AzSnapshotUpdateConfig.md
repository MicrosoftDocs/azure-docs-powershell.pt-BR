---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azsnapshotupdateconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzSnapshotUpdateConfig.md
ms.openlocfilehash: c2c17fe3329170d65d61e5439e614717a8119f26
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776963"
---
# <span data-ttu-id="c12c8-101">New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="c12c8-101">New-AzSnapshotUpdateConfig</span></span>

## <span data-ttu-id="c12c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c12c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c12c8-103">Cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="c12c8-103">Creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="c12c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c12c8-104">SYNTAX</span></span>

```
New-AzSnapshotUpdateConfig [[-SkuName] <StorageAccountTypes>] [[-OsType] <OperatingSystemTypes>]
 [[-DiskSizeGB] <Int32>] [[-Tag] <Hashtable>] [-EncryptionSettingsEnabled <Boolean>]
 [-DiskEncryptionKey <KeyVaultAndSecretReference>] [-KeyEncryptionKey <KeyVaultAndKeyReference>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c12c8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c12c8-105">DESCRIPTION</span></span>
<span data-ttu-id="c12c8-106">O cmdlet **New-AzSnapshotUpdateConfig** cria um objeto de atualização de instantâneo configurável.</span><span class="sxs-lookup"><span data-stu-id="c12c8-106">The **New-AzSnapshotUpdateConfig** cmdlet creates a configurable snapshot update object.</span></span>

## <span data-ttu-id="c12c8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c12c8-107">EXAMPLES</span></span>

### <span data-ttu-id="c12c8-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c12c8-108">Example 1</span></span>
```
PS C:\> $snapshotupdateconfig = New-AzSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

<span data-ttu-id="c12c8-109">O primeiro comando cria um objeto de atualização de instantâneo vazio local com o tamanho 10GB em Premium_LRS tipo de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c12c8-109">The first command creates a local empty snapshot update object with size 10GB in Premium_LRS storage account type.</span></span> <span data-ttu-id="c12c8-110">Ele também define o tipo de sistema operacional Windows e habilita as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c12c8-110">It also sets Windows OS type and enables encryption settings.</span></span> <span data-ttu-id="c12c8-111">O segundo e terceiro comandos definem as configurações de chave de criptografia de disco e chave de criptografia de chave para o objeto de atualização de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c12c8-111">The second and third commands set the disk encryption key and key encryption key settings for the snapshot update object.</span></span> <span data-ttu-id="c12c8-112">O último comando usa o objeto de atualização de instantâneo e atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c12c8-112">The last command takes the snapshot update object and updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c12c8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c12c8-113">Example 2</span></span>
```
PS C:\> New-AzSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

<span data-ttu-id="c12c8-114">Este comando atualiza um instantâneo existente com o nome "Snapshot01" no grupo de recursos "ResourceGroup01" para o tamanho de disco de 10 GB.</span><span class="sxs-lookup"><span data-stu-id="c12c8-114">This command updates an existing snapshot with name 'Snapshot01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="c12c8-115">OS</span><span class="sxs-lookup"><span data-stu-id="c12c8-115">PARAMETERS</span></span>

### <span data-ttu-id="c12c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c12c8-116">-DefaultProfile</span></span>
<span data-ttu-id="c12c8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c12c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c12c8-118">-DiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c12c8-118">-DiskEncryptionKey</span></span>
<span data-ttu-id="c12c8-119">Especifica o objeto da chave de criptografia do disco em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c12c8-119">Specifies the disk encryption key object on a snapshot.</span></span>

```yaml
Type: KeyVaultAndSecretReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c12c8-120">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c12c8-120">-DiskSizeGB</span></span>
<span data-ttu-id="c12c8-121">Especifica o tamanho do disco em GB.</span><span class="sxs-lookup"><span data-stu-id="c12c8-121">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c12c8-122">-EncryptionSettingsEnabled</span><span class="sxs-lookup"><span data-stu-id="c12c8-122">-EncryptionSettingsEnabled</span></span>
<span data-ttu-id="c12c8-123">Habilite as configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="c12c8-123">Enable encryption settings.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c12c8-124">-KeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="c12c8-124">-KeyEncryptionKey</span></span>
<span data-ttu-id="c12c8-125">Especifica a chave de criptografia da chave em um instantâneo.</span><span class="sxs-lookup"><span data-stu-id="c12c8-125">Specifies the Key encryption key on a snapshot.</span></span>

```yaml
Type: KeyVaultAndKeyReference
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c12c8-126">-OsType</span><span class="sxs-lookup"><span data-stu-id="c12c8-126">-OsType</span></span>
<span data-ttu-id="c12c8-127">Especifica o tipo de sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c12c8-127">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c12c8-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c12c8-128">-SkuName</span></span>
<span data-ttu-id="c12c8-129">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c12c8-129">Specifies the Sku name of the storage account.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: AccountType
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c12c8-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="c12c8-130">-Tag</span></span>
<span data-ttu-id="c12c8-131">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="c12c8-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c12c8-132">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c12c8-132">For example:</span></span>

<span data-ttu-id="c12c8-133">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="c12c8-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c12c8-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c12c8-134">-Confirm</span></span>
<span data-ttu-id="c12c8-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c12c8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c12c8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c12c8-136">-WhatIf</span></span>
<span data-ttu-id="c12c8-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c12c8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c12c8-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c12c8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c12c8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c12c8-139">CommonParameters</span></span>
<span data-ttu-id="c12c8-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c12c8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c12c8-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c12c8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c12c8-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c12c8-142">INPUTS</span></span>

### <span data-ttu-id="c12c8-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c12c8-143">None</span></span>
<span data-ttu-id="c12c8-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c12c8-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c12c8-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c12c8-145">OUTPUTS</span></span>

### <span data-ttu-id="c12c8-146">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSSnapshotUpdate</span><span class="sxs-lookup"><span data-stu-id="c12c8-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshotUpdate</span></span>

## <span data-ttu-id="c12c8-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c12c8-147">NOTES</span></span>

## <span data-ttu-id="c12c8-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c12c8-148">RELATED LINKS</span></span>

