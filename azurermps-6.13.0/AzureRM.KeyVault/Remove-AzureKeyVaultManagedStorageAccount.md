---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c5f96c2e4840d35ac79e78c6778cb66ddc034180
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430232"
---
# <span data-ttu-id="edd85-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edd85-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="edd85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="edd85-102">SYNOPSIS</span></span>
<span data-ttu-id="edd85-103">Remove uma conta de armazenamento gerenciada do Key Vault e todas as definições de SAS associadas.</span><span class="sxs-lookup"><span data-stu-id="edd85-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edd85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="edd85-104">SYNTAX</span></span>

### <span data-ttu-id="edd85-105">ByDefinitionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="edd85-105">ByDefinitionName (Default)</span></span>
```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edd85-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="edd85-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edd85-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="edd85-107">DESCRIPTION</span></span>
<span data-ttu-id="edd85-108">Desassocia uma conta de armazenamento do Azure do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="edd85-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="edd85-109">Isso não remove uma conta de armazenamento do Azure, mas remove as chaves da conta de serem gerenciadas pelo cofre de chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="edd85-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="edd85-110">Todas as definições de SAS de armazenamento gerenciado de Key Vault também são removidas.</span><span class="sxs-lookup"><span data-stu-id="edd85-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="edd85-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="edd85-111">EXAMPLES</span></span>

### <span data-ttu-id="edd85-112">Exemplo 1: remover uma conta de armazenamento gerenciada do repositório de chaves e todas as definições de SAS associadas.</span><span class="sxs-lookup"><span data-stu-id="edd85-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="edd85-113">Desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves.</span><span class="sxs-lookup"><span data-stu-id="edd85-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="edd85-114">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="edd85-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="edd85-115">Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="edd85-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="edd85-116">Exemplo 2: remover uma conta de armazenamento gerenciada do repositório de chaves e todas as definições de SAS associadas sem confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="edd85-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="edd85-117">Desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves.</span><span class="sxs-lookup"><span data-stu-id="edd85-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="edd85-118">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="edd85-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="edd85-119">Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="edd85-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="edd85-120">Exemplo 3: excluir permanentemente (limpar) uma conta de armazenamento gerenciada do Azure e todas as definições de SAS associadas de um cofre habilitado para exclusão soft.</span><span class="sxs-lookup"><span data-stu-id="edd85-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="edd85-121">O exemplo pressupõe que a exclusão suave está habilitada para este cofre.</span><span class="sxs-lookup"><span data-stu-id="edd85-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="edd85-122">Verifique se esse é o caso examinando as propriedades do cofre ou o atributo RecoveryLevel de uma entidade no cofre.</span><span class="sxs-lookup"><span data-stu-id="edd85-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="edd85-123">O primeiro cmdlet desassocia a conta de armazenamento do Azure ' mystorageaccount ' do cofre de chaves ' myvault ' e impede que o cofre de chaves gerenciem suas chaves.</span><span class="sxs-lookup"><span data-stu-id="edd85-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="edd85-124">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="edd85-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="edd85-125">Todas as definições de SAS de armazenamento gerenciado de cofre de chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="edd85-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="edd85-126">O segundo cmdlet verifica se a conta de armazenamento está em um estado excluído, mas recuperável.</span><span class="sxs-lookup"><span data-stu-id="edd85-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="edd85-127">Alcançar esse Estado pode exigir algum tempo, aguarde ~ 30s antes de tentar.</span><span class="sxs-lookup"><span data-stu-id="edd85-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="edd85-128">O terceiro cmdlet remove permanentemente a conta de armazenamento – a recuperação não será mais possível.</span><span class="sxs-lookup"><span data-stu-id="edd85-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="edd85-129">OS</span><span class="sxs-lookup"><span data-stu-id="edd85-129">PARAMETERS</span></span>

### <span data-ttu-id="edd85-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="edd85-130">-AccountName</span></span>
<span data-ttu-id="edd85-131">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="edd85-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="edd85-132">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="edd85-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd85-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edd85-133">-DefaultProfile</span></span>
<span data-ttu-id="edd85-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="edd85-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edd85-135">-Force</span><span class="sxs-lookup"><span data-stu-id="edd85-135">-Force</span></span>
<span data-ttu-id="edd85-136">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="edd85-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="edd85-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edd85-137">-InputObject</span></span>
<span data-ttu-id="edd85-138">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="edd85-138">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edd85-139">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="edd85-139">-InRemovedState</span></span>
<span data-ttu-id="edd85-140">Remova permanentemente a conta de armazenamento gerenciado anteriormente excluída.</span><span class="sxs-lookup"><span data-stu-id="edd85-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="edd85-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edd85-141">-PassThru</span></span>
<span data-ttu-id="edd85-142">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="edd85-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="edd85-143">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="edd85-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="edd85-144">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="edd85-144">-VaultName</span></span>
<span data-ttu-id="edd85-145">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="edd85-145">Vault name.</span></span>
<span data-ttu-id="edd85-146">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="edd85-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edd85-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="edd85-147">-Confirm</span></span>
<span data-ttu-id="edd85-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edd85-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edd85-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edd85-149">-WhatIf</span></span>
<span data-ttu-id="edd85-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="edd85-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edd85-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="edd85-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edd85-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edd85-152">CommonParameters</span></span>
<span data-ttu-id="edd85-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edd85-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edd85-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edd85-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edd85-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="edd85-155">INPUTS</span></span>

### <span data-ttu-id="edd85-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="edd85-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="edd85-157">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="edd85-157">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="edd85-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="edd85-158">OUTPUTS</span></span>

### <span data-ttu-id="edd85-159">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="edd85-159">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="edd85-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="edd85-160">NOTES</span></span>

## <span data-ttu-id="edd85-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="edd85-161">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

