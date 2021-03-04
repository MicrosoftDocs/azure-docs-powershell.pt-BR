---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: ab126ee6bfc6a19f4a3a9997a75a01277437e42d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885450"
---
# <span data-ttu-id="f5fae-101">Remove-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5fae-101">Remove-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f5fae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5fae-102">SYNOPSIS</span></span>
<span data-ttu-id="f5fae-103">Remove uma Conta de Armazenamento gerenciada pelo Azure Key Vault e todas as definições SAS associadas.</span><span class="sxs-lookup"><span data-stu-id="f5fae-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

## <span data-ttu-id="f5fae-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f5fae-104">SYNTAX</span></span>

### <span data-ttu-id="f5fae-105">ByDefinitionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f5fae-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5fae-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5fae-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-InRemovedState] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5fae-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f5fae-107">DESCRIPTION</span></span>
<span data-ttu-id="f5fae-108">Desassocia uma conta de armazenamento do Azure do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f5fae-108">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="f5fae-109">Isso não remove uma conta de armazenamento do Azure, mas remove as chaves da conta de serem gerenciadas pelo Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f5fae-109">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="f5fae-110">Todas as definições de SAS gerenciadas do Cofre de Chaves associadas também são removidas.</span><span class="sxs-lookup"><span data-stu-id="f5fae-110">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="f5fae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5fae-111">EXAMPLES</span></span>

### <span data-ttu-id="f5fae-112">Exemplo 1: Remover uma Conta de Armazenamento gerenciada pelo Azure E todas as definições SAS associadas.</span><span class="sxs-lookup"><span data-stu-id="f5fae-112">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru

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

<span data-ttu-id="f5fae-113">Desassocia a conta de armazenamento do Azure 'mystorageaccount' do Key Vault 'myvault' e impede o Key Vault de gerenciar suas chaves.</span><span class="sxs-lookup"><span data-stu-id="f5fae-113">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="f5fae-114">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="f5fae-114">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="f5fae-115">Todas as definições de SAS de Armazenamento gerenciadas do Cofre de Chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="f5fae-115">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="f5fae-116">Exemplo 2: Remover uma Conta de Armazenamento gerenciada pelo Azure E todas as definições SAS associadas sem confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f5fae-116">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -PassThru -Force

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

<span data-ttu-id="f5fae-117">Desassocia a conta de armazenamento do Azure 'mystorageaccount' do Key Vault 'myvault' e impede o Key Vault de gerenciar suas chaves.</span><span class="sxs-lookup"><span data-stu-id="f5fae-117">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="f5fae-118">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="f5fae-118">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="f5fae-119">Todas as definições de SAS de Armazenamento gerenciadas do Cofre de Chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="f5fae-119">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="f5fae-120">Exemplo 3: excluir permanentemente (limpar) uma Conta de Armazenamento gerenciada do Azure Key Vault e todas as definições SAS associadas de um cofre habilitado para exclusão suave.</span><span class="sxs-lookup"><span data-stu-id="f5fae-120">Example 3: Permanently delete (purge) a Key Vault managed Azure Storage Account and all associated SAS definitions from a soft-delete-enabled vault.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' 
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -InRemovedState
```

<span data-ttu-id="f5fae-121">O exemplo supõe que a exclusão suave está habilitada para esse cofre.</span><span class="sxs-lookup"><span data-stu-id="f5fae-121">The example assumes that soft-delete is enabled for this vault.</span></span> <span data-ttu-id="f5fae-122">Verifique se esse é o caso examinando as propriedades do cofre ou o atributo RecoveryLevel de uma entidade no cofre.</span><span class="sxs-lookup"><span data-stu-id="f5fae-122">Verify whether that is the case by examining the vault properties, or the RecoveryLevel attribute of an entity in the vault.</span></span>
<span data-ttu-id="f5fae-123">O primeiro cmdlet desassocia a conta de armazenamento do Azure 'mystorageaccount' do Key Vault 'myvault' e impede o Key Vault de gerenciar suas chaves.</span><span class="sxs-lookup"><span data-stu-id="f5fae-123">The first cmdlet disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="f5fae-124">A conta "mystorageaccount" não será removida.</span><span class="sxs-lookup"><span data-stu-id="f5fae-124">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="f5fae-125">Todas as definições de SAS de Armazenamento gerenciadas do Cofre de Chaves associadas a essa conta serão removidas.</span><span class="sxs-lookup"><span data-stu-id="f5fae-125">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>
<span data-ttu-id="f5fae-126">O segundo cmdlet verifica se a conta de armazenamento está em um estado excluído, mas recuperável.</span><span class="sxs-lookup"><span data-stu-id="f5fae-126">The second cmdlet verifies that the storage account is in a deleted, but recoverable state.</span></span> <span data-ttu-id="f5fae-127">Chegar a esse estado pode exigir algum tempo, permita ~30s antes de tentar.</span><span class="sxs-lookup"><span data-stu-id="f5fae-127">Reaching this state may require some time, please allow ~30s before attempting.</span></span>
<span data-ttu-id="f5fae-128">O terceiro cmdlet remove permanentemente a conta de armazenamento - a recuperação não será mais possível.</span><span class="sxs-lookup"><span data-stu-id="f5fae-128">The third cmdlet permanently removes the storage account - recovery will no longer be possible.</span></span>

## <span data-ttu-id="f5fae-129">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f5fae-129">PARAMETERS</span></span>

### <span data-ttu-id="f5fae-130">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5fae-130">-AccountName</span></span>
<span data-ttu-id="f5fae-131">Nome da conta de armazenamento gerenciado do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="f5fae-131">Key Vault managed storage account name.</span></span> <span data-ttu-id="f5fae-132">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento envelhecido.</span><span class="sxs-lookup"><span data-stu-id="f5fae-132">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="f5fae-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5fae-133">-DefaultProfile</span></span>
<span data-ttu-id="f5fae-134">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f5fae-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5fae-135">-Force</span><span class="sxs-lookup"><span data-stu-id="f5fae-135">-Force</span></span>
<span data-ttu-id="f5fae-136">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="f5fae-136">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f5fae-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5fae-137">-InputObject</span></span>
<span data-ttu-id="f5fae-138">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f5fae-138">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="f5fae-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f5fae-139">-InRemovedState</span></span>
<span data-ttu-id="f5fae-140">Remova permanentemente a conta de armazenamento gerenciado excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f5fae-140">Permanently remove the previously deleted managed storage account.</span></span>

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

### <span data-ttu-id="f5fae-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5fae-141">-PassThru</span></span>
<span data-ttu-id="f5fae-142">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f5fae-142">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f5fae-143">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada excluída.</span><span class="sxs-lookup"><span data-stu-id="f5fae-143">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="f5fae-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f5fae-144">-VaultName</span></span>
<span data-ttu-id="f5fae-145">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="f5fae-145">Vault name.</span></span>
<span data-ttu-id="f5fae-146">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="f5fae-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f5fae-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5fae-147">-Confirm</span></span>
<span data-ttu-id="f5fae-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5fae-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5fae-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5fae-149">-WhatIf</span></span>
<span data-ttu-id="f5fae-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5fae-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5fae-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5fae-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5fae-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5fae-152">CommonParameters</span></span>
<span data-ttu-id="f5fae-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5fae-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5fae-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5fae-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5fae-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5fae-155">INPUTS</span></span>

### <span data-ttu-id="f5fae-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f5fae-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="f5fae-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f5fae-157">OUTPUTS</span></span>

### <span data-ttu-id="f5fae-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5fae-158">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f5fae-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="f5fae-159">NOTES</span></span>

## <span data-ttu-id="f5fae-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5fae-160">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

