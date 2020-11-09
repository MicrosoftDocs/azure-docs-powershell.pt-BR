---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280504"
---
# <span data-ttu-id="1e5ba-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="1e5ba-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="1e5ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5ba-103">Obtém definições de SAS de armazenamento gerenciado do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="1e5ba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e5ba-104">SYNTAX</span></span>

### <span data-ttu-id="1e5ba-105">ByDefinitionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1e5ba-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e5ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1e5ba-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e5ba-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1e5ba-107">DESCRIPTION</span></span>
<span data-ttu-id="1e5ba-108">Obtém uma definição de SAS de armazenamento gerenciado de um cofre de chaves se o nome da definição for especificado.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="1e5ba-109">Se o nome da definição não for especificado, todas as definições de SAS associadas à conta de armazenamento gerenciado do cofre de chaves especificado no cofre serão listadas.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="1e5ba-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1e5ba-110">EXAMPLES</span></span>

### <span data-ttu-id="1e5ba-111">Exemplo 1: listar todas as definições de SAS de armazenamento gerenciado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="1e5ba-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
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

<span data-ttu-id="1e5ba-112">Lista todas as definições de SAS associadas à conta de armazenamento gerenciado do Key Vault ' mystorageaccount ' gerenciada pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="1e5ba-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="1e5ba-113">Exemplo 2: obter uma conta de armazenamento gerenciado do Key Vault</span><span class="sxs-lookup"><span data-stu-id="1e5ba-113">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="1e5ba-114">Obtém os detalhes da definição SAS ' contasas ' associadas à conta de armazenamento gerenciado do Key Vault ' mystorageaccount ' gerenciada pelo cofre ' myvault '.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="1e5ba-115">Exemplo 3: listar todas as definições de armazenamento gerenciado do cofre de chaves usando filtragem</span><span class="sxs-lookup"><span data-stu-id="1e5ba-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
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

<span data-ttu-id="1e5ba-116">Lista todas as definições de SAS associadas à conta de armazenamento gerenciado do Key Vault ' mystorageaccount ' gerenciada pelo cofre ' myvault ' que começa com "conta".</span><span class="sxs-lookup"><span data-stu-id="1e5ba-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="1e5ba-117">OS</span><span class="sxs-lookup"><span data-stu-id="1e5ba-117">PARAMETERS</span></span>

### <span data-ttu-id="1e5ba-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1e5ba-118">-AccountName</span></span>
<span data-ttu-id="1e5ba-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-119">Vault name.</span></span>
<span data-ttu-id="1e5ba-120">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1e5ba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5ba-121">-DefaultProfile</span></span>
<span data-ttu-id="1e5ba-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1e5ba-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e5ba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e5ba-123">-InputObject</span></span>
<span data-ttu-id="1e5ba-124">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="1e5ba-125">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="1e5ba-125">-InRemovedState</span></span>
<span data-ttu-id="1e5ba-126">Especifica se as definições de SAS de armazenamento excluídas anteriormente devem ser exibidas na saída.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="1e5ba-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e5ba-127">-Name</span></span>
<span data-ttu-id="1e5ba-128">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-128">Storage sas definition name.</span></span>
<span data-ttu-id="1e5ba-129">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="1e5ba-130">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="1e5ba-130">-VaultName</span></span>
<span data-ttu-id="1e5ba-131">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-131">Vault name.</span></span>
<span data-ttu-id="1e5ba-132">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1e5ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5ba-133">CommonParameters</span></span>
<span data-ttu-id="1e5ba-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5ba-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e5ba-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5ba-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1e5ba-136">INPUTS</span></span>

### <span data-ttu-id="1e5ba-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1e5ba-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="1e5ba-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1e5ba-138">OUTPUTS</span></span>

### <span data-ttu-id="1e5ba-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1e5ba-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="1e5ba-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="1e5ba-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="1e5ba-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="1e5ba-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="1e5ba-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1e5ba-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="1e5ba-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1e5ba-143">NOTES</span></span>

## <span data-ttu-id="1e5ba-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e5ba-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

