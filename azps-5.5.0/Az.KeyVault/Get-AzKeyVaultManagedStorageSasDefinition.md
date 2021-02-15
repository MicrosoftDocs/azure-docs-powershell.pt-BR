---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: c09218b960fb6c11b685106a3cb90bfdfd2f546a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113760"
---
# <span data-ttu-id="57ce4-101">Get-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="57ce4-101">Get-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="57ce4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="57ce4-103">Obtém definições do SAS de armazenamento gerenciado pelo Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="57ce4-103">Gets Key Vault managed Storage SAS Definitions.</span></span>

## <span data-ttu-id="57ce4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57ce4-104">SYNTAX</span></span>

### <span data-ttu-id="57ce4-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="57ce4-105">ByDefinitionName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [[-Name] <String>]
 [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57ce4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="57ce4-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-Name] <String>] [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57ce4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="57ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="57ce4-108">Obtém uma Definição SAS de Armazenamento gerenciada do Cofre de Teclas se o nome da definição for especificado.</span><span class="sxs-lookup"><span data-stu-id="57ce4-108">Gets a Key Vault managed Storage SAS Definition if the name of the definition is specified.</span></span> <span data-ttu-id="57ce4-109">Se o nome da definição não for especificado, todas as definições SAS associadas à Conta de Armazenamento Gerenciada do Cofre de Chave especificada no cofre serão listadas.</span><span class="sxs-lookup"><span data-stu-id="57ce4-109">If the definition name is not specified, then all the SAS definitions associated with the specified Key Vault managed Storage Account in the vault are listed.</span></span>

## <span data-ttu-id="57ce4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57ce4-110">EXAMPLES</span></span>

### <span data-ttu-id="57ce4-111">Exemplo 1: Listar todas as Definições do SAS de Armazenamento Gerenciado do Cofre de Chave</span><span class="sxs-lookup"><span data-stu-id="57ce4-111">Example 1: List all Key Vault managed Storage SAS Definitions</span></span>
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

<span data-ttu-id="57ce4-112">Lista todas as definições do SAS associadas à conta de armazenamento gerenciada do Cofre de Chaves "minhastorageaccount" gerenciada pelo cofre 'myvault'</span><span class="sxs-lookup"><span data-stu-id="57ce4-112">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'</span></span>

### <span data-ttu-id="57ce4-113">Exemplo 2: Obter uma Conta de Armazenamento Gerenciada do Cofre de Chave</span><span class="sxs-lookup"><span data-stu-id="57ce4-113">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="57ce4-114">Obtém os detalhes das 'contasas' de definição do SAS associadas à conta de armazenamento gerenciada do Cofre de Teclas 'mystorageaccount' gerenciada pelo cofre 'myvault'.</span><span class="sxs-lookup"><span data-stu-id="57ce4-114">Gets the details of SAS Definition 'accountsas' associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault'.</span></span>

### <span data-ttu-id="57ce4-115">Exemplo 3: Listar todas as Definições de Armazenamento Gerenciado do Cofre de Chave usando filtragem</span><span class="sxs-lookup"><span data-stu-id="57ce4-115">Example 3: List all Key Vault managed Storage SAS Definitions using filtering</span></span>
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

<span data-ttu-id="57ce4-116">Lista todas as definições do SAS associadas à conta de armazenamento gerenciada do Cofre de Chaves "minhastorageaccount" gerenciada pelo cofre "myvault" que começam com "conta".</span><span class="sxs-lookup"><span data-stu-id="57ce4-116">Lists all the SAS definitions associated with Key Vault managed Storage Account 'mystorageaccount' managed by vault 'myvault' that start with "account".</span></span>

## <span data-ttu-id="57ce4-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57ce4-117">PARAMETERS</span></span>

### <span data-ttu-id="57ce4-118">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="57ce4-118">-AccountName</span></span>
<span data-ttu-id="57ce4-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="57ce4-119">Vault name.</span></span>
<span data-ttu-id="57ce4-120">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="57ce4-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="57ce4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ce4-121">-DefaultProfile</span></span>
<span data-ttu-id="57ce4-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="57ce4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57ce4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57ce4-123">-InputObject</span></span>
<span data-ttu-id="57ce4-124">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="57ce4-124">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="57ce4-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="57ce4-125">-InRemovedState</span></span>
<span data-ttu-id="57ce4-126">Especifica se você deve mostrar as definições de sas de armazenamento excluídas anteriormente na saída.</span><span class="sxs-lookup"><span data-stu-id="57ce4-126">Specifies whether to show the previously deleted storage sas definitions in the output.</span></span>

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

### <span data-ttu-id="57ce4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="57ce4-127">-Name</span></span>
<span data-ttu-id="57ce4-128">Nome de definição de sas de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57ce4-128">Storage sas definition name.</span></span>
<span data-ttu-id="57ce4-129">O Cmdlet constrói o FQDN de uma definição de sas de armazenamento do nome do cofre, ambiente selecionado no momento, nome da conta de armazenamento e nome de definição SAS.</span><span class="sxs-lookup"><span data-stu-id="57ce4-129">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="57ce4-130">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="57ce4-130">-VaultName</span></span>
<span data-ttu-id="57ce4-131">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="57ce4-131">Vault name.</span></span>
<span data-ttu-id="57ce4-132">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="57ce4-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="57ce4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ce4-133">CommonParameters</span></span>
<span data-ttu-id="57ce4-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57ce4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ce4-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57ce4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ce4-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="57ce4-136">INPUTS</span></span>

### <span data-ttu-id="57ce4-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57ce4-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="57ce4-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="57ce4-138">OUTPUTS</span></span>

### <span data-ttu-id="57ce4-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57ce4-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

### <span data-ttu-id="57ce4-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="57ce4-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="57ce4-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="57ce4-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinition</span></span>

### <span data-ttu-id="57ce4-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57ce4-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageSasDefinitionIdentityItem</span></span>

## <span data-ttu-id="57ce4-143">Notas</span><span class="sxs-lookup"><span data-stu-id="57ce4-143">NOTES</span></span>

## <span data-ttu-id="57ce4-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57ce4-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

