---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 90f6347346c0967e29917ffe56e7ba13f7e705de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117602"
---
# <span data-ttu-id="8f099-101">Add-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8f099-101">Add-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8f099-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f099-102">SYNOPSIS</span></span>
<span data-ttu-id="8f099-103">Adiciona uma Conta de Armazenamento do Azure existente ao cofre de chave especificado para que suas chaves sejam gerenciadas pelo serviço cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8f099-103">Adds an existing Azure Storage Account to the specified key vault for its keys to be managed by the Key Vault service.</span></span>

## <span data-ttu-id="8f099-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f099-104">SYNTAX</span></span>

```
Add-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-AccountResourceId] <String>
 [-ActiveKeyName] <String> [-DisableAutoRegenerateKey] [-RegenerationPeriod <TimeSpan>] [-Disable]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f099-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f099-105">DESCRIPTION</span></span>
<span data-ttu-id="8f099-106">Configura uma conta de armazenamento existente do Azure com o Cofre de Teclas para chaves de Conta de Armazenamento a serem gerenciadas pelo Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="8f099-106">Sets up an existing Azure Storage Account with Key Vault for Storage Account keys to be managed by Key Vault.</span></span> <span data-ttu-id="8f099-107">A Conta de Armazenamento já deve existir.</span><span class="sxs-lookup"><span data-stu-id="8f099-107">The Storage Account must already exist.</span></span> <span data-ttu-id="8f099-108">As Teclas de Armazenamento nunca são expostas ao chamador.</span><span class="sxs-lookup"><span data-stu-id="8f099-108">The Storage Keys are never exposed to caller.</span></span>
<span data-ttu-id="8f099-109">O Cofre de Teclas se regenera automaticamente e alterna a chave ativa com base no período de inspeções.</span><span class="sxs-lookup"><span data-stu-id="8f099-109">Key Vault auto regenerates and switches the active key based on the regeneration period.</span></span> <span data-ttu-id="8f099-110">Consulte a conta de armazenamento gerenciada do Cofre de Chaves [do Azure - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) para ter uma visão geral desse recurso.</span><span class="sxs-lookup"><span data-stu-id="8f099-110">See [Azure Key Vault managed storage account - PowerShell](https://docs.microsoft.com/azure/key-vault/key-vault-overview-storage-keys-powershell) for an overview of this feature.</span></span>

## <span data-ttu-id="8f099-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f099-111">EXAMPLES</span></span>

### <span data-ttu-id="8f099-112">Exemplo 1: Definir uma conta de armazenamento do Azure com o Cofre de Teclas para gerenciar suas chaves</span><span class="sxs-lookup"><span data-stu-id="8f099-112">Example 1: Set an Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="8f099-113">Define uma Conta de Armazenamento com o Cofre de Teclas para que suas chaves sejam gerenciadas pelo Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="8f099-113">Sets a Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="8f099-114">O conjunto de teclas ativas é "chave1".</span><span class="sxs-lookup"><span data-stu-id="8f099-114">The active key set is 'key1'.</span></span> <span data-ttu-id="8f099-115">Essa chave será usada para gerar tokens sas.</span><span class="sxs-lookup"><span data-stu-id="8f099-115">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="8f099-116">O Cofre de Teclas regenerará a tecla "chave2" após o período de insinuidade do tempo deste comando e a definirá como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="8f099-116">Key Vault will regenerate 'key2' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="8f099-117">Esse processo de recuperação automática continuará entre "chave1" e "tecla2" com um intervalo de 90 dias.</span><span class="sxs-lookup"><span data-stu-id="8f099-117">This auto regeneration process will continue between 'key1' and 'key2' with a gap of 90 days.</span></span>

### <span data-ttu-id="8f099-118">Exemplo 2: Definir uma conta de armazenamento clássica do Azure com o Cofre de Teclas para gerenciar suas chaves</span><span class="sxs-lookup"><span data-stu-id="8f099-118">Example 2: Set a Classic Azure Storage Account with Key Vault to manage its keys</span></span>
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

<span data-ttu-id="8f099-119">Define uma conta de armazenamento clássica com o Cofre de Teclas para que suas chaves sejam gerenciadas pelo Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="8f099-119">Sets a Classic Storage Account with Key Vault for its keys to be managed by Key Vault.</span></span> <span data-ttu-id="8f099-120">O conjunto de chaves ativas é "Principal".</span><span class="sxs-lookup"><span data-stu-id="8f099-120">The active key set is 'Primary'.</span></span> <span data-ttu-id="8f099-121">Essa chave será usada para gerar tokens sas.</span><span class="sxs-lookup"><span data-stu-id="8f099-121">This key will be used to generate sas tokens.</span></span> <span data-ttu-id="8f099-122">O Cofre de Teclas regenerará a tecla "Secundária" após o período de insinuidade do tempo deste comando e a definirá como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="8f099-122">Key Vault will regenerate 'Secondary' key after the regeneration period from the time of this command and set it as the active key.</span></span> <span data-ttu-id="8f099-123">Esse processo de auto-recuperação continuará entre "Principal" e "Secundário" com um intervalo de 90 dias.</span><span class="sxs-lookup"><span data-stu-id="8f099-123">This auto regeneration process will continue between 'Primary' and 'Secondary' with a gap of 90 days.</span></span>

## <span data-ttu-id="8f099-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f099-124">PARAMETERS</span></span>

### <span data-ttu-id="8f099-125">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="8f099-125">-AccountName</span></span>
<span data-ttu-id="8f099-126">Nome da conta de armazenamento gerenciada do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="8f099-126">Key Vault managed storage account name.</span></span> <span data-ttu-id="8f099-127">O Cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8f099-127">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="8f099-128">-AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="8f099-128">-AccountResourceId</span></span>
<span data-ttu-id="8f099-129">ID de recurso do Azure da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8f099-129">Azure resource id of the storage account.</span></span>

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

### <span data-ttu-id="8f099-130">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="8f099-130">-ActiveKeyName</span></span>
<span data-ttu-id="8f099-131">Nome da chave da conta de armazenamento que deve ser usada para gerar tokens sas.</span><span class="sxs-lookup"><span data-stu-id="8f099-131">Name of the storage account key that must be used for generating sas tokens.</span></span>

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

### <span data-ttu-id="8f099-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f099-132">-DefaultProfile</span></span>
<span data-ttu-id="8f099-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8f099-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f099-134">-Desabilitar</span><span class="sxs-lookup"><span data-stu-id="8f099-134">-Disable</span></span>
<span data-ttu-id="8f099-135">Desabilita o uso da chave da conta de armazenamento gerenciado para geração de tokens sas.</span><span class="sxs-lookup"><span data-stu-id="8f099-135">Disables the use of managed storage account's key for generation of sas tokens.</span></span>

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

### <span data-ttu-id="8f099-136">-DisableAutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="8f099-136">-DisableAutoRegenerateKey</span></span>
<span data-ttu-id="8f099-137">Tecla de regeneração automática.</span><span class="sxs-lookup"><span data-stu-id="8f099-137">Auto regenerate key.</span></span> <span data-ttu-id="8f099-138">Se for verdadeira, a chave inativa da conta de armazenamento gerenciada será automaticamente regenerada e se tornará a nova chave ativa após o período de inatividade.</span><span class="sxs-lookup"><span data-stu-id="8f099-138">If true, then the managed storage account's inactive key gets auto regenerated and becomes the new active key after the regeneration period.</span></span> <span data-ttu-id="8f099-139">Se for falso, as chaves da conta de armazenamento gerenciado não serão regeneradas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8f099-139">If false, then the keys of managed storage account are not auto regenerated.</span></span>

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

### <span data-ttu-id="8f099-140">-DesalmadaPeriod</span><span class="sxs-lookup"><span data-stu-id="8f099-140">-RegenerationPeriod</span></span>
<span data-ttu-id="8f099-141">Período de recuperação.</span><span class="sxs-lookup"><span data-stu-id="8f099-141">Regeneration period.</span></span> <span data-ttu-id="8f099-142">Se a chave de regeneração automática estiver habilitada, esse valor especificará o período após o qual a chave inativa da conta de armazenamento gerenciada será automaticamente regenerada e se tornará a nova chave ativa.</span><span class="sxs-lookup"><span data-stu-id="8f099-142">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the new active key.</span></span>

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

### <span data-ttu-id="8f099-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="8f099-143">-Tag</span></span>
<span data-ttu-id="8f099-144">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8f099-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8f099-145">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="8f099-145">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8f099-146">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="8f099-146">-VaultName</span></span>
<span data-ttu-id="8f099-147">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="8f099-147">Vault name.</span></span>
<span data-ttu-id="8f099-148">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="8f099-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8f099-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f099-149">-Confirm</span></span>
<span data-ttu-id="8f099-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f099-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f099-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f099-151">-WhatIf</span></span>
<span data-ttu-id="8f099-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f099-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f099-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f099-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f099-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f099-154">CommonParameters</span></span>
<span data-ttu-id="8f099-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f099-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f099-156">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f099-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f099-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f099-157">INPUTS</span></span>

### <span data-ttu-id="8f099-158">System.String</span><span class="sxs-lookup"><span data-stu-id="8f099-158">System.String</span></span>

### <span data-ttu-id="8f099-159">System.Nullable'1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8f099-159">System.Nullable\`1[[System.TimeSpan, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8f099-160">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8f099-160">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8f099-161">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f099-161">OUTPUTS</span></span>

### <span data-ttu-id="8f099-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8f099-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="8f099-163">Notas</span><span class="sxs-lookup"><span data-stu-id="8f099-163">NOTES</span></span>

## <span data-ttu-id="8f099-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f099-164">RELATED LINKS</span></span>

[<span data-ttu-id="8f099-165">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8f099-165">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
