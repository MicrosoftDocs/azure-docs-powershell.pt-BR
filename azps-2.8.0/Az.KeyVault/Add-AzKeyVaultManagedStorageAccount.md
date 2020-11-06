---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 56883ecc1ca562ed4a259be9d1940683e652a280
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596222"
---
# <span data-ttu-id="57c68-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57c68-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="57c68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57c68-102">SYNOPSIS</span></span>
<span data-ttu-id="57c68-103">Adiciona uma conta de armazenamento do Azure existente ao cofre de chaves especificado para que as chaves sejam gerenciadas pelo serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c68-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="57c68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="57c68-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57c68-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="57c68-105">DESCRIPTION</span></span>
<span data-ttu-id="57c68-106">Configura uma conta de armazenamento existente do Azure com o Key Vault para que as chaves de conta de armazenamento sejam gerenciadas pelo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c68-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="57c68-107">A conta de armazenamento já deve existir.</span><span class="sxs-lookup"><span data-stu-id="57c68-107">The Storage Account must already exist.</span></span> <span data-ttu-id="57c68-108">As teclas de armazenamento nunca são expostas ao chamador.</span><span class="sxs-lookup"><span data-stu-id="57c68-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="57c68-109">O Key Vault automaticamente regenera e alterna a chave ativa com base no período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="57c68-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="57c68-110">Consulte [conta de armazenamento gerenciado do repositório de chave do Azure-PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) para obter uma visão geral deste recurso.</span><span class="sxs-lookup"><span data-stu-id="57c68-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="57c68-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57c68-111">EXAMPLES</span></span>

### <span data-ttu-id="57c68-112">Exemplo 1: definir uma conta de armazenamento do Azure com o cofre de chaves para gerenciar as chaves</span><span class="sxs-lookup"><span data-stu-id="57c68-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $storage = Get-AzStorageAccount -ResourceGroupName "mystorageResourceGroup" -StorageAccountName "mystorage"
PS C:\> $servicePrincipal = Get-AzADServicePrincipal -ServicePrincipalName cfa8b339-82a2-471a-a3c9-0fc0be7a4093
PS C:\> New-AzRoleAssignment -ObjectId $servicePrincipal.Id -RoleDefinitionName 'Storage Account Key Operator Service Role' -Scope $storage.Id
PS C:\> $userPrincipalId = $(Get-AzADUser -SearchString "developer@contoso.com").Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ObjectId $userPrincipalId -PermissionsToStorage get, set
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount' -ActiveKeyName 'key1' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="57c68-113">Define uma conta de armazenamento com o Key Vault para que as chaves sejam gerenciadas pelo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c68-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="57c68-114">O conjunto de teclas ativas é ' key1 '.</span><span class="sxs-lookup"><span data-stu-id="57c68-114">The active key set is 'key1'.</span></span> <span data-ttu-id="57c68-115">Essa chave será usada para gerar tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="57c68-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="57c68-116">O cofre de chaves regenerará a chave "Key2" após o período de regeneração no momento do comando e a definirá como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="57c68-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="57c68-117">Esse processo de regeneração automática continuará entre ' key1 ' e ' Key2 ' com um intervalo de 90 dias.</span><span class="sxs-lookup"><span data-stu-id="57c68-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="57c68-118">Exemplo 2: definir uma conta de armazenamento clássica do Azure com o cofre de chaves para gerenciar as chaves</span><span class="sxs-lookup"><span data-stu-id="57c68-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
```powershell
PS C:\> $regenerationPeriod = [System.Timespan]::FromDays(90)
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -AccountResourceId '/subscriptions/<subscription id>/resourceGroups/myresourcegroup/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount' -ActiveKeyName 'Primary' -RegenerationPeriod $regenerationPeriod

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myvault/providers/Microsoft.Cl
                      assicStorage/storageAccounts/mystorageaccount
Active Key Name     : Primary
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="57c68-119">Define uma conta de armazenamento clássica com o Key Vault para que as chaves sejam gerenciadas pelo cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c68-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="57c68-120">O conjunto de teclas ativas é ' Primary '.</span><span class="sxs-lookup"><span data-stu-id="57c68-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="57c68-121">Essa chave será usada para gerar tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="57c68-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="57c68-122">O cofre de chaves reproduzirá a tecla ' secundária ' após o período de regeneração da hora do comando e a definirá como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="57c68-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="57c68-123">Esse processo de regeneração automática continuará entre ' principal ' e ' secundário ', com um intervalo de 90 a dias.</span><span class="sxs-lookup"><span data-stu-id="57c68-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="57c68-124">OS</span><span class="sxs-lookup"><span data-stu-id="57c68-124">PARAMETERS</span></span>

### <span data-ttu-id="57c68-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57c68-125">-AccountName</span></span>
<span data-ttu-id="57c68-126">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="57c68-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="57c68-127">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="57c68-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c68-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="57c68-128">-AccountResourceId</span></span>
<span data-ttu-id="57c68-129">ID do recurso do Azure da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57c68-129">Azure resource id of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountResourceId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c68-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="57c68-130">-ActiveKeyName</span></span>
<span data-ttu-id="57c68-131">Nome da chave da conta de armazenamento que deve ser usada para gerar tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="57c68-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c68-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c68-132">-DefaultProfile</span></span>
<span data-ttu-id="57c68-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="57c68-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57c68-134">-Disable</span><span class="sxs-lookup"><span data-stu-id="57c68-134">-Disable</span></span>
<span data-ttu-id="57c68-135">Desabilita o uso da chave da conta de armazenamento gerenciado para a geração de tokens SAS.</span><span class="sxs-lookup"><span data-stu-id="57c68-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="57c68-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="57c68-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="57c68-137">Regenerar chave automaticamente.</span><span class="sxs-lookup"><span data-stu-id="57c68-137">Auto regenerate key.</span></span> <span data-ttu-id="57c68-138">Se verdadeiro, a chave inativa da conta de armazenamento gerenciada será automaticamente regenerada e se tornará a nova chave ativa após o período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="57c68-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="57c68-139">Se falso, as chaves da conta de armazenamento gerenciado não serão regeneradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="57c68-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="57c68-140">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="57c68-140">-RegenerationPeriod</span></span>
<span data-ttu-id="57c68-141">Período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="57c68-141">Regeneration period.</span></span> <span data-ttu-id="57c68-142">Se a chave de regeração automática estiver habilitada, esse valor especificará o TimeSpan após o qual a chave inativa da conta de armazenamento gerenciado será regenerada automaticamente e se tornará a nova chave ativa.</span><span class="sxs-lookup"><span data-stu-id="57c68-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c68-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="57c68-143">-Tag</span></span>
<span data-ttu-id="57c68-144">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="57c68-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="57c68-145">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="57c68-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c68-146">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="57c68-146">-VaultName</span></span>
<span data-ttu-id="57c68-147">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="57c68-147">Vault name.</span></span>
<span data-ttu-id="57c68-148">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="57c68-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="57c68-149">-Confirme</span><span class="sxs-lookup"><span data-stu-id="57c68-149">-Confirm</span></span>
<span data-ttu-id="57c68-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57c68-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c68-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c68-151">-WhatIf</span></span>
<span data-ttu-id="57c68-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57c68-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c68-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57c68-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c68-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c68-154">CommonParameters</span></span>
<span data-ttu-id="57c68-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c68-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c68-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c68-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c68-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="57c68-157">INPUTS</span></span>

### <span data-ttu-id="57c68-158">System. String</span><span class="sxs-lookup"><span data-stu-id="57c68-158">System.String</span></span>

### <span data-ttu-id="57c68-159">System. Nullable ' 1 [[System. TimeSpan, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57c68-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="57c68-160">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="57c68-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57c68-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="57c68-161">OUTPUTS</span></span>

### <span data-ttu-id="57c68-162">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57c68-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="57c68-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="57c68-163">NOTES</span></span>

## <span data-ttu-id="57c68-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57c68-164">RELATED LINKS</span></span>

[<span data-ttu-id="57c68-165">AZ. keyvault</span><span class="sxs-lookup"><span data-stu-id="57c68-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
