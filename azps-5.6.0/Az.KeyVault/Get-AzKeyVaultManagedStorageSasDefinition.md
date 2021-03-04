---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: acb0e2811f184f7c3162635b87849a35ce9156ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891836"
---
# <span data-ttu-id="4a8a0-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="4a8a0-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="4a8a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8a0-103">Obtém definições de SAS de armazenamento gerenciado do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="4a8a0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4a8a0-104">SYNTAX</span></span>

### <span data-ttu-id="4a8a0-105">ByDefinitionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4a8a0-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a8a0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4a8a0-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a8a0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4a8a0-107">DESCRIPTION</span></span>
<span data-ttu-id="4a8a0-108">Obtém uma Definição SAS de Armazenamento gerenciado do Cofre de Chaves se o nome da definição for especificado.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="4a8a0-109">Se o nome da definição não for especificado, todas as definições SAS associadas à Conta de Armazenamento gerenciada do Cofre de Chaves especificada no cofre serão listadas.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="4a8a0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a8a0-110">EXAMPLES</span></span>

### <span data-ttu-id="4a8a0-111">Exemplo 1: listar todas as definições de SAS de armazenamento gerenciado do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="4a8a0-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="4a8a0-112">Lista todas as definições do SAS associadas à conta de armazenamento gerenciada do Cofre de Chaves 'mystorageaccount' gerenciada pelo cofre 'myvault'</span><span class="sxs-lookup"><span data-stu-id="4a8a0-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="4a8a0-113">Exemplo 2: Obter uma conta de armazenamento gerenciada do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="4a8a0-113">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'accountsas'

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas
Secret Id   : https://myvault.vault.azure.net/secrets/mystorageaccount-accountsas
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas
Parameter   :
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="4a8a0-114">Obtém os detalhes de 'accountsas' de definição do SAS associados à conta de armazenamento gerenciada do Cofre de Chaves 'mystorageaccount' gerenciada pelo cofre 'myvault'.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="4a8a0-115">Exemplo 3: Listar todas as definições de SAS de armazenamento gerenciado do Cofre de Chaves usando filtragem</span><span class="sxs-lookup"><span data-stu-id="4a8a0-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageSasDefinition -VaultName 'myvault' -AccountName 'mystorageaccount' -Name "account*"

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas1
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas1
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :

Id          : https://myvault.vault.azure.net:443/storage/mystorageaccount/sas/accountsas2
Vault Name  : myvault
AccountName : mystorageaccount
Name        : accountsas2
Enabled     : True
Created     : 5/24/2018 9:11:08 PM
Updated     : 5/24/2018 9:11:08 PM
Tags        :
```

<span data-ttu-id="4a8a0-116">Lista todas as definições SAS associadas à conta de armazenamento gerenciada do Cofre de Chaves 'mystorageaccount' gerenciada pelo cofre 'myvault' que começam com "conta".</span><span class="sxs-lookup"><span data-stu-id="4a8a0-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="4a8a0-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4a8a0-117">PARAMETERS</span></span>

### <span data-ttu-id="4a8a0-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a8a0-118">-AccountName</span></span>
<span data-ttu-id="4a8a0-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-119">Vault name.</span></span>
<span data-ttu-id="4a8a0-120">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4a8a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8a0-121">-DefaultProfile</span></span>
<span data-ttu-id="4a8a0-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4a8a0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a8a0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a8a0-123">-InputObject</span></span>
<span data-ttu-id="4a8a0-124">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="4a8a0-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4a8a0-125">-InRemovedState</span></span>
<span data-ttu-id="4a8a0-126">Especifica se as definições de sas de armazenamento excluídas anteriormente serão especificadas na saída.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="4a8a0-127">-Name</span><span class="sxs-lookup"><span data-stu-id="4a8a0-127">-Name</span></span>
<span data-ttu-id="4a8a0-128">Nome da definição de sas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-128">Storage sas definition name.</span></span>
<span data-ttu-id="4a8a0-129">O cmdlet constrói o FQDN de uma definição de sas de armazenamento a partir do nome do cofre, do ambiente selecionado no momento, do nome da conta de armazenamento e do nome da definição de sas.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a8a0-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4a8a0-130">-VaultName</span></span>
<span data-ttu-id="4a8a0-131">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-131">Vault name.</span></span>
<span data-ttu-id="4a8a0-132">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4a8a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8a0-133">CommonParameters</span></span>
<span data-ttu-id="4a8a0-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a8a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8a0-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a8a0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8a0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a8a0-136">INPUTS</span></span>

### <span data-ttu-id="4a8a0-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4a8a0-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="4a8a0-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4a8a0-138">OUTPUTS</span></span>

### <span data-ttu-id="4a8a0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4a8a0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="4a8a0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="4a8a0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="4a8a0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="4a8a0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="4a8a0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4a8a0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="4a8a0-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="4a8a0-143">NOTES</span></span>

## <span data-ttu-id="4a8a0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a8a0-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

