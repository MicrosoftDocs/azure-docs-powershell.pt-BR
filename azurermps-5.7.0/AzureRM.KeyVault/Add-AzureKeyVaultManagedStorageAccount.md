---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 526472514be086118f8c5ed74cefb6983ad67065
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428914"
---
# <span data-ttu-id="14454-101">Add-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14454-101">Add-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="14454-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14454-102">SYNOPSIS</span></span>
<span data-ttu-id="14454-103">Adiciona uma conta de armazenamento do Azure existente ao cofre de chaves especificado para que as chaves sejam gerenciadas pelo serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="14454-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14454-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14454-104">SYNTAX</span></span>

```
Add-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-AccountResourceId] <String> [-ActiveKeyName] <String> [-DisableAutoRegenerateKey]
 [-RegenerationPeriod <TimeSpan>] [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14454-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14454-105">DESCRIPTION</span></span>
<span data-ttu-id="14454-106">Configura uma conta de armazenamento existente do Azure com o Key Vault para que as chaves de conta de armazenamento sejam gerenciadas pelo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="14454-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="14454-107">A conta de armazenamento já deve existir.</span><span class="sxs-lookup"><span data-stu-id="14454-107">The Storage Account must already exist.</span></span> <span data-ttu-id="14454-108">As teclas de armazenamento nunca são expostas ao chamador.</span><span class="sxs-lookup"><span data-stu-id="14454-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="14454-109">O Key Vault automaticamente regenera e alterna a chave ativa com base no período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="14454-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span>

## <span data-ttu-id="14454-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14454-110">EXAMPLES</span></span>

### <span data-ttu-id="14454-111">Exemplo 1: definir uma conta de armazenamento do Azure com o cofre de chaves para gerenciar as chaves</span><span class="sxs-lookup"><span data-stu-id="14454-111">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="14454-112">Define uma conta de armazenamento com o Key Vault para que as chaves sejam gerenciadas pelo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="14454-112">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="14454-113">O conjunto de teclas ativas é ' key1 '.</span><span class="sxs-lookup"><span data-stu-id="14454-113">The active key set is 'key1'.</span></span> <span data-ttu-id="14454-114">Essa chave será usada para gerar tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="14454-114">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="14454-115">O cofre de chaves regenerará a chave "Key2" após o período de regeneração no momento do comando e a definirá como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="14454-115">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="14454-116">Esse processo de regeneração automática continuará entre ' key1 ' e ' Key2 ' com um intervalo de 90 dias.</span><span class="sxs-lookup"><span data-stu-id="14454-116">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="14454-117">Exemplo 2: definir uma conta de armazenamento clássica do Azure com o cofre de chaves para gerenciar as chaves</span><span class="sxs-lookup"><span data-stu-id="14454-117">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -ResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod
```

<span data-ttu-id="14454-118">Define uma conta de armazenamento clássica com o Key Vault para que as chaves sejam gerenciadas pelo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="14454-118">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="14454-119">O conjunto de teclas ativas é ' Primary '.</span><span class="sxs-lookup"><span data-stu-id="14454-119">The active key set is 'Primary'.</span></span> <span data-ttu-id="14454-120">Essa chave será usada para gerar tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="14454-120">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="14454-121">O cofre de chaves reproduzirá a tecla ' secundária ' após o período de regeneração da hora do comando e a definirá como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="14454-121">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="14454-122">Esse processo de regeneração automática continuará entre ' principal ' e ' secundário ', com um intervalo de 90 a dias.</span><span class="sxs-lookup"><span data-stu-id="14454-122">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="14454-123">OS</span><span class="sxs-lookup"><span data-stu-id="14454-123">PARAMETERS</span></span>

### <span data-ttu-id="14454-124">-AccountName</span><span class="sxs-lookup"><span data-stu-id="14454-124">-AccountName</span></span>
<span data-ttu-id="14454-125">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="14454-125">Key Vault managed storage account name.</span></span> <span data-ttu-id="14454-126">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="14454-126">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14454-127">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="14454-127">-AccountResourceId</span></span>
<span data-ttu-id="14454-128">ID do recurso do Azure da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="14454-128">Azure resource id of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14454-129">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="14454-129">-ActiveKeyName</span></span>
<span data-ttu-id="14454-130">Nome da chave da conta de armazenamento que deve ser usada para gerar tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="14454-130">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14454-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14454-131">-DefaultProfile</span></span>
<span data-ttu-id="14454-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="14454-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14454-133">-Disable</span><span class="sxs-lookup"><span data-stu-id="14454-133">-Disable</span></span>
<span data-ttu-id="14454-134">Desabilita o uso da chave da conta de armazenamento gerenciado para a geração de tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="14454-134">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14454-135">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="14454-135">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="14454-136">Regenerar chave automaticamente.</span><span class="sxs-lookup"><span data-stu-id="14454-136">Auto regenerate key.</span></span> <span data-ttu-id="14454-137">Se verdadeiro, a chave inativa da conta de armazenamento gerenciada será automaticamente regenerada e se tornará a nova chave ativa após o período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="14454-137">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="14454-138">Se falso, as chaves da conta de armazenamento gerenciado não serão regeneradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="14454-138">If false, then the keys of managed storage account are not auto regenerated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14454-139">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="14454-139">-RegenerationPeriod</span></span>
<span data-ttu-id="14454-140">Período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="14454-140">Regeneration period.</span></span> <span data-ttu-id="14454-141">Se a chave de regeração automática estiver habilitada, esse valor especificará o TimeSpan após o qual a chave inativa da conta de armazenamento gerenciado será regenerada automaticamente e se tornará a nova chave ativa.</span><span class="sxs-lookup"><span data-stu-id="14454-141">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14454-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="14454-142">-Tag</span></span>
<span data-ttu-id="14454-143">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="14454-143">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="14454-144">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="14454-144">For example:</span></span>

<span data-ttu-id="14454-145">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="14454-145">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14454-146">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="14454-146">-VaultName</span></span>
<span data-ttu-id="14454-147">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="14454-147">Vault name.</span></span>
<span data-ttu-id="14454-148">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="14454-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14454-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14454-149">-Confirm</span></span>
<span data-ttu-id="14454-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14454-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14454-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14454-151">-WhatIf</span></span>
<span data-ttu-id="14454-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14454-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14454-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14454-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14454-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14454-154">CommonParameters</span></span>
<span data-ttu-id="14454-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14454-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14454-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14454-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14454-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14454-157">INPUTS</span></span>

### <span data-ttu-id="14454-158">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="14454-158">None</span></span>
<span data-ttu-id="14454-159">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="14454-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="14454-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14454-160">OUTPUTS</span></span>

### <span data-ttu-id="14454-161">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="14454-161">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="14454-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14454-162">NOTES</span></span>

## <span data-ttu-id="14454-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14454-163">RELATED LINKS</span></span>

[<span data-ttu-id="14454-164">AzureRM. keyvault</span><span class="sxs-lookup"><span data-stu-id="14454-164">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
