---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: f3a1e4d1e938b84a434c07451f3d2294e203f440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433248"
---
# <span data-ttu-id="95be0-101">Get-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95be0-101">Get-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="95be0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95be0-102">SYNOPSIS</span></span>
<span data-ttu-id="95be0-103">Obtém contas de armazenamento do Azure gerenciadas do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="95be0-103">Gets Key Vault managed Azure Storage Accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95be0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95be0-104">SYNTAX</span></span>

### <span data-ttu-id="95be0-105">ByAccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="95be0-105">ByAccountName (Default)</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [[-AccountName] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95be0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="95be0-106">ByInputObject</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95be0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="95be0-107">ByResourceId</span></span>
```
Get-AzureKeyVaultManagedStorageAccount [-ResourceId] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95be0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95be0-108">DESCRIPTION</span></span>
<span data-ttu-id="95be0-109">Obtém uma conta de armazenamento gerenciada do Key Vault, se o nome da conta for especificado e as chaves da conta forem gerenciadas pelo cofre especificado.</span><span class="sxs-lookup"><span data-stu-id="95be0-109">Gets a Key Vault managed Azure Storage Account if the name of the account is specified and the account keys are managed by the specified vault.</span></span> <span data-ttu-id="95be0-110">Se o nome da conta não for especificado, todas as contas cujas chaves são gerenciadas pelo cofre especificado são listadas.</span><span class="sxs-lookup"><span data-stu-id="95be0-110">If the account name is not specified, then all the accounts whose keys are managed by specified vault are listed.</span></span>

## <span data-ttu-id="95be0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95be0-111">EXAMPLES</span></span>

### <span data-ttu-id="95be0-112">Exemplo 1: lista todas as contas de armazenamento gerenciado do cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="95be0-112">Example 1: List all Key Vault managed Storage Accounts</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault'

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

<span data-ttu-id="95be0-113">Lista todas as contas cujas chaves são gerenciadas pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="95be0-113">Lists all the accounts whose keys are managed by vault 'myvault'</span></span>

### <span data-ttu-id="95be0-114">Exemplo 2: obter uma conta de armazenamento gerenciado do Key Vault</span><span class="sxs-lookup"><span data-stu-id="95be0-114">Example 2: Get a Key Vault managed Storage Account</span></span>
```powershell
PS C:\> Get-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -Name 'mystorageaccount'

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

<span data-ttu-id="95be0-115">Obtém os detalhes da conta de armazenamento gerenciado do Key Vault de ' mystorageaccount ' se suas chaves forem gerenciadas pelo cofre ' myvault '</span><span class="sxs-lookup"><span data-stu-id="95be0-115">Gets the details of Key Vault managed Storage Account of 'mystorageaccount' if its keys are managed by vault 'myvault'</span></span>

## <span data-ttu-id="95be0-116">OS</span><span class="sxs-lookup"><span data-stu-id="95be0-116">PARAMETERS</span></span>

### <span data-ttu-id="95be0-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="95be0-117">-AccountName</span></span>
<span data-ttu-id="95be0-118">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="95be0-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="95be0-119">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="95be0-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAccountName
Aliases: StorageAccountName, Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95be0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95be0-120">-DefaultProfile</span></span>
<span data-ttu-id="95be0-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="95be0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95be0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95be0-122">-InputObject</span></span>
<span data-ttu-id="95be0-123">Objeto do cofre.</span><span class="sxs-lookup"><span data-stu-id="95be0-123">Vault object.</span></span>

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

### <span data-ttu-id="95be0-124">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="95be0-124">-InRemovedState</span></span>
<span data-ttu-id="95be0-125">Especifica se as contas de armazenamento excluídas anteriormente devem ser mostradas na saída.</span><span class="sxs-lookup"><span data-stu-id="95be0-125">Specifies whether to show the previously deleted storage accounts in the output.</span></span>

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

### <span data-ttu-id="95be0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95be0-126">-ResourceId</span></span>
<span data-ttu-id="95be0-127">ID do recurso do cofre.</span><span class="sxs-lookup"><span data-stu-id="95be0-127">Vault resource id.</span></span>

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

### <span data-ttu-id="95be0-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="95be0-128">-VaultName</span></span>
<span data-ttu-id="95be0-129">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="95be0-129">Vault name.</span></span>
<span data-ttu-id="95be0-130">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="95be0-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="95be0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95be0-131">CommonParameters</span></span>
<span data-ttu-id="95be0-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95be0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95be0-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95be0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95be0-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95be0-134">INPUTS</span></span>

### <span data-ttu-id="95be0-135">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="95be0-135">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="95be0-136">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="95be0-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="95be0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="95be0-137">System.String</span></span>

## <span data-ttu-id="95be0-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95be0-138">OUTPUTS</span></span>

### <span data-ttu-id="95be0-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="95be0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="95be0-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95be0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

### <span data-ttu-id="95be0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="95be0-141">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccountIdentityItem</span></span>

### <span data-ttu-id="95be0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95be0-142">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="95be0-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95be0-143">NOTES</span></span>

## <span data-ttu-id="95be0-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95be0-144">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

