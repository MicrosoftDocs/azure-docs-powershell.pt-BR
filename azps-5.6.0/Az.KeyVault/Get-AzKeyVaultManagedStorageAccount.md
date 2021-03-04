---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 552a696a31b8c5fb26a1c6a17434ef53380d0491
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891837"
---
# <span data-ttu-id="2aa01-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2aa01-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2aa01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aa01-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa01-103">Obtém Contas de Armazenamento gerenciadas do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="2aa01-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="2aa01-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2aa01-104">SYNTAX</span></span>

### <span data-ttu-id="2aa01-105">ByAccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2aa01-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aa01-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2aa01-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aa01-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa01-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aa01-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2aa01-108">DESCRIPTION</span></span>
<span data-ttu-id="2aa01-109">Obtém uma Conta de Armazenamento gerenciada do Azure Key Vault se o nome da conta for especificado e as chaves da conta são gerenciadas pelo cofre especificado.</span><span class="sxs-lookup"><span data-stu-id="2aa01-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="2aa01-110">Se o nome da conta não for especificado, todas as contas cujas chaves são gerenciadas pelo cofre especificado serão listadas.</span><span class="sxs-lookup"><span data-stu-id="2aa01-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="2aa01-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aa01-111">EXAMPLES</span></span>

### <span data-ttu-id="2aa01-112">Exemplo 1: Listar todas as contas de armazenamento gerenciadas do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="2aa01-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="2aa01-113">Lista todas as contas cujas chaves são gerenciadas pelo cofre 'myvault'</span><span class="sxs-lookup"><span data-stu-id="2aa01-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="2aa01-114">Exemplo 2: Obter uma conta de armazenamento gerenciada do Cofre de Chaves</span><span class="sxs-lookup"><span data-stu-id="2aa01-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/maddie1/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : False
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="2aa01-115">Obtém os detalhes da Conta de Armazenamento gerenciada do Cofre de Chaves de 'mystorageaccount' se suas chaves são gerenciadas pelo cofre 'myvault'</span><span class="sxs-lookup"><span data-stu-id="2aa01-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="2aa01-116">Exemplo 3: Listar todas as Contas de Armazenamento gerenciadas do Cofre de Chaves usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="2aa01-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -Name "test*"

Id                  : https://myvault.vault.azure.net:443/storage/test1
Vault Name          : myvault
AccountName         : test1
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test1
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :

Id                  : https://myvault.vault.azure.net:443/storage/test2
Vault Name          : myvault
AccountName         : test2
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/test2
Enabled             : True
Created             : 4/25/2018 1:50:32 AM
Updated             : 4/25/2018 1:50:32 AM
Tags                :
```

<span data-ttu-id="2aa01-117">Lista todas as contas cujas chaves são gerenciadas pelo cofre 'myvault' que começam com "test"</span><span class="sxs-lookup"><span data-stu-id="2aa01-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="2aa01-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2aa01-118">PARAMETERS</span></span>

### <span data-ttu-id="2aa01-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2aa01-119">-AccountName</span></span>
<span data-ttu-id="2aa01-120">Nome da conta de armazenamento gerenciado do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="2aa01-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="2aa01-121">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento envelhecido.</span><span class="sxs-lookup"><span data-stu-id="2aa01-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="2aa01-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa01-122">-DefaultProfile</span></span>
<span data-ttu-id="2aa01-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2aa01-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2aa01-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa01-124">-InputObject</span></span>
<span data-ttu-id="2aa01-125">Objeto Vault.</span><span class="sxs-lookup"><span data-stu-id="2aa01-125">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa01-126">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2aa01-126">-InRemovedState</span></span>
<span data-ttu-id="2aa01-127">Especifica se as contas de armazenamento excluídas anteriormente serão especificadas na saída.</span><span class="sxs-lookup"><span data-stu-id="2aa01-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="2aa01-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa01-128">-ResourceId</span></span>
<span data-ttu-id="2aa01-129">ID do recurso Vault.</span><span class="sxs-lookup"><span data-stu-id="2aa01-129">Vault resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aa01-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2aa01-130">-VaultName</span></span>
<span data-ttu-id="2aa01-131">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="2aa01-131">Vault name.</span></span>
<span data-ttu-id="2aa01-132">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="2aa01-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aa01-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa01-133">CommonParameters</span></span>
<span data-ttu-id="2aa01-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa01-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa01-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aa01-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa01-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2aa01-136">INPUTS</span></span>

### <span data-ttu-id="2aa01-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="2aa01-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="2aa01-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2aa01-138">System.String</span></span>

## <span data-ttu-id="2aa01-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2aa01-139">OUTPUTS</span></span>

### <span data-ttu-id="2aa01-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2aa01-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="2aa01-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2aa01-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="2aa01-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2aa01-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="2aa01-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2aa01-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="2aa01-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="2aa01-144">NOTES</span></span>

## <span data-ttu-id="2aa01-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aa01-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

