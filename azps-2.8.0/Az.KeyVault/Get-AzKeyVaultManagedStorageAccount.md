---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 165419eb13376becedf72b4e44ee17f0c3655ec4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596190"
---
# <span data-ttu-id="1481d-101">Get-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1481d-101">Get-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1481d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1481d-102">SYNOPSIS</span></span>
<span data-ttu-id="1481d-103">Obtém contas de armazenamento do Azure gerenciadas do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="1481d-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

## <span data-ttu-id="1481d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1481d-104">SYNTAX</span></span>

### <span data-ttu-id="1481d-105">ByAccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1481d-105">ByAccountName (Default)</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1481d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1481d-106">ByInputObject</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1481d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1481d-107">ByResourceId</span></span>
```
Get-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1481d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1481d-108">DESCRIPTION</span></span>
<span data-ttu-id="1481d-109">Obtém uma conta de armazenamento gerenciada do Key Vault, se o nome da conta for especificado e as chaves da conta forem gerenciadas pelo cofre especificado.</span><span class="sxs-lookup"><span data-stu-id="1481d-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="1481d-110">Se o nome da conta não for especificado, todas as contas cujas chaves são gerenciadas pelo cofre especificado são listadas.</span><span class="sxs-lookup"><span data-stu-id="1481d-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="1481d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1481d-111">EXAMPLES</span></span>

### <span data-ttu-id="1481d-112">Exemplo 1: lista todas as contas de armazenamento gerenciado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="1481d-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
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

<span data-ttu-id="1481d-113">Lista todas as contas cujas chaves são gerenciadas pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="1481d-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="1481d-114">Exemplo 2: obter uma conta de armazenamento gerenciado do Key Vault</span><span class="sxs-lookup"><span data-stu-id="1481d-114">Example 2: Get a Key Vault managed Storage Account</span></span>
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

<span data-ttu-id="1481d-115">Obtém os detalhes da conta de armazenamento gerenciado do Key Vault de ' mystorageaccount ' se suas chaves forem gerenciadas pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="1481d-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="1481d-116">Exemplo 3: listar todas as contas de armazenamento gerenciadas do cofre de chaves usando filtragem</span><span class="sxs-lookup"><span data-stu-id="1481d-116">Example 3: List all Key Vault managed Storage Accounts using filtering</span></span>
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

<span data-ttu-id="1481d-117">Lista todas as contas cujas chaves são gerenciadas pelo cofre ' myvault ' que começam com "Test"</span><span class="sxs-lookup"><span data-stu-id="1481d-117">Lists all the accounts whose keys are managed by vault 'myvault' that start with "test"</span></span>

## <span data-ttu-id="1481d-118">OS</span><span class="sxs-lookup"><span data-stu-id="1481d-118">PARAMETERS</span></span>

### <span data-ttu-id="1481d-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1481d-119">-AccountName</span></span>
<span data-ttu-id="1481d-120">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="1481d-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="1481d-121">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="1481d-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="1481d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1481d-122">-DefaultProfile</span></span>
<span data-ttu-id="1481d-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1481d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1481d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1481d-124">-InputObject</span></span>
<span data-ttu-id="1481d-125">Objeto do cofre.</span><span class="sxs-lookup"><span data-stu-id="1481d-125">Vault object.</span></span>

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

### <span data-ttu-id="1481d-126">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="1481d-126">-InRemovedState</span></span>
<span data-ttu-id="1481d-127">Especifica se as contas de armazenamento excluídas anteriormente devem ser mostradas na saída.</span><span class="sxs-lookup"><span data-stu-id="1481d-127">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="1481d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1481d-128">-ResourceId</span></span>
<span data-ttu-id="1481d-129">ID do recurso do cofre.</span><span class="sxs-lookup"><span data-stu-id="1481d-129">Vault resource id.</span></span>

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

### <span data-ttu-id="1481d-130">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="1481d-130">-VaultName</span></span>
<span data-ttu-id="1481d-131">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="1481d-131">Vault name.</span></span>
<span data-ttu-id="1481d-132">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="1481d-132">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1481d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1481d-133">CommonParameters</span></span>
<span data-ttu-id="1481d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1481d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1481d-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1481d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1481d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1481d-136">INPUTS</span></span>

### <span data-ttu-id="1481d-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1481d-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1481d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1481d-138">System.String</span></span>

## <span data-ttu-id="1481d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1481d-139">OUTPUTS</span></span>

### <span data-ttu-id="1481d-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1481d-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="1481d-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1481d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="1481d-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1481d-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="1481d-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1481d-143">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="1481d-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1481d-144">NOTES</span></span>

## <span data-ttu-id="1481d-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1481d-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

