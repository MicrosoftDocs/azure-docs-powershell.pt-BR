---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 844802c01b9b3bff7f59b795d5ba7712b9a7f4c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901476"
---
# <span data-ttu-id="24e20-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="24e20-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="24e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24e20-102">SYNOPSIS</span></span>
<span data-ttu-id="24e20-103">Remove as definições SAS gerenciadas pelo Azure Storage do Azure.</span><span class="sxs-lookup"><span data-stu-id="24e20-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="24e20-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="24e20-104">SYNTAX</span></span>

### <span data-ttu-id="24e20-105">ByDefinitionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="24e20-105">ByDefinitionName (Default)</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e20-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="24e20-106">ByInputObject</span></span>
```
Remove-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageSasDefinitionIdentityItem>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e20-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="24e20-107">DESCRIPTION</span></span>
<span data-ttu-id="24e20-108">Remove as definições SAS gerenciadas pelo Azure Storage do Azure.</span><span class="sxs-lookup"><span data-stu-id="24e20-108">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="24e20-109">Isso também remove o segredo usado para obter o token SAS de acordo com essa definição do SAS.</span><span class="sxs-lookup"><span data-stu-id="24e20-109">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="24e20-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24e20-110">EXAMPLES</span></span>

### <span data-ttu-id="24e20-111">Exemplo 1: Remover uma definição SAS gerenciada do Azure Storage do Azure Vault.</span><span class="sxs-lookup"><span data-stu-id="24e20-111">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="24e20-112">Remove uma definição de armazenamento gerenciado do Cofre de Chaves 'mysasdef' associada à conta 'mystorageaccount' no cofre 'myvault'.</span><span class="sxs-lookup"><span data-stu-id="24e20-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="24e20-113">Exemplo 2: Remover uma definição SAS gerenciada do Azure Storage do Azure sem confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="24e20-113">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -PassThru -Force

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/mysasdef
Vault Name  : myvault
AccountName : mystorageaccount
Name        : mysasdef
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="24e20-114">Remove uma definição de armazenamento gerenciado do Cofre de Chaves 'mysasdef' associada à conta 'mystorageaccount' no cofre 'myvault'.</span><span class="sxs-lookup"><span data-stu-id="24e20-114">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="24e20-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="24e20-115">PARAMETERS</span></span>

### <span data-ttu-id="24e20-116">-AccountName</span><span class="sxs-lookup"><span data-stu-id="24e20-116">-AccountName</span></span>
<span data-ttu-id="24e20-117">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="24e20-117">Storage account name.</span></span>
<span data-ttu-id="24e20-118">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="24e20-118">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e20-119">-DefaultProfile</span></span>
<span data-ttu-id="24e20-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="24e20-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24e20-121">-Force</span><span class="sxs-lookup"><span data-stu-id="24e20-121">-Force</span></span>
<span data-ttu-id="24e20-122">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="24e20-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="24e20-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24e20-123">-InputObject</span></span>
<span data-ttu-id="24e20-124">Objeto ManagedStorageSasDefinition.</span><span class="sxs-lookup"><span data-stu-id="24e20-124">ManagedStorageSasDefinition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24e20-125">-Name</span><span class="sxs-lookup"><span data-stu-id="24e20-125">-Name</span></span>
<span data-ttu-id="24e20-126">Nome da definição de sas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="24e20-126">Storage sas definition name.</span></span>
<span data-ttu-id="24e20-127">O cmdlet constrói o FQDN de uma definição de sas de armazenamento a partir do nome do cofre, do ambiente selecionado no momento, do nome da conta de armazenamento e do nome da definição de sas.</span><span class="sxs-lookup"><span data-stu-id="24e20-127">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e20-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24e20-128">-PassThru</span></span>
<span data-ttu-id="24e20-129">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="24e20-129">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="24e20-130">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada excluída.</span><span class="sxs-lookup"><span data-stu-id="24e20-130">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="24e20-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="24e20-131">-VaultName</span></span>
<span data-ttu-id="24e20-132">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="24e20-132">Vault name.</span></span>
<span data-ttu-id="24e20-133">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="24e20-133">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="24e20-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24e20-134">-Confirm</span></span>
<span data-ttu-id="24e20-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e20-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e20-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e20-136">-WhatIf</span></span>
<span data-ttu-id="24e20-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24e20-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e20-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24e20-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e20-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e20-139">CommonParameters</span></span>
<span data-ttu-id="24e20-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e20-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e20-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24e20-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e20-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24e20-142">INPUTS</span></span>

### <span data-ttu-id="24e20-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="24e20-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="24e20-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="24e20-144">OUTPUTS</span></span>

### <span data-ttu-id="24e20-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="24e20-145">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="24e20-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="24e20-146">NOTES</span></span>

## <span data-ttu-id="24e20-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24e20-147">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

