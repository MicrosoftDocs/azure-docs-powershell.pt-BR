---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 80ff79e71498cc76479592b65207da09fabed6a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888503"
---
# <span data-ttu-id="dccc4-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="dccc4-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="dccc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dccc4-102">SYNOPSIS</span></span>
<span data-ttu-id="dccc4-103">Regenera a chave especificada da Conta de Armazenamento gerenciada do Azure Vault.</span><span class="sxs-lookup"><span data-stu-id="dccc4-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="dccc4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dccc4-104">SYNTAX</span></span>

### <span data-ttu-id="dccc4-105">ByDefinitionName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dccc4-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccc4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dccc4-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dccc4-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dccc4-107">DESCRIPTION</span></span>
<span data-ttu-id="dccc4-108">Regenera a chave especificada da Conta de Armazenamento gerenciada do Azure Vault e define a chave como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="dccc4-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="dccc4-109">O Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span><span class="sxs-lookup"><span data-stu-id="dccc4-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="dccc4-110">O chamador deve possuir permissões para regenerar chaves em determinada Conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="dccc4-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="dccc4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dccc4-111">EXAMPLES</span></span>

### <span data-ttu-id="dccc4-112">Exemplo 1: Regenerar uma chave</span><span class="sxs-lookup"><span data-stu-id="dccc4-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

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

<span data-ttu-id="dccc4-113">Regenera 'key1' da conta 'mystorageaccount' e define 'key1' como o ativo da Conta de Armazenamento gerenciada do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="dccc4-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="dccc4-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dccc4-114">PARAMETERS</span></span>

### <span data-ttu-id="dccc4-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dccc4-115">-AccountName</span></span>
<span data-ttu-id="dccc4-116">Nome da conta de armazenamento gerenciado do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="dccc4-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="dccc4-117">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento envelhecido.</span><span class="sxs-lookup"><span data-stu-id="dccc4-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="dccc4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dccc4-118">-DefaultProfile</span></span>
<span data-ttu-id="dccc4-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="dccc4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dccc4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dccc4-120">-Force</span></span>
<span data-ttu-id="dccc4-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="dccc4-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dccc4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dccc4-122">-InputObject</span></span>
<span data-ttu-id="dccc4-123">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="dccc4-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="dccc4-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dccc4-124">-KeyName</span></span>
<span data-ttu-id="dccc4-125">Nome da chave da conta de armazenamento para se regenerar e tornar ativo.</span><span class="sxs-lookup"><span data-stu-id="dccc4-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dccc4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dccc4-126">-PassThru</span></span>
<span data-ttu-id="dccc4-127">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="dccc4-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="dccc4-128">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada excluída.</span><span class="sxs-lookup"><span data-stu-id="dccc4-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="dccc4-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dccc4-129">-VaultName</span></span>
<span data-ttu-id="dccc4-130">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="dccc4-130">Vault name.</span></span>
<span data-ttu-id="dccc4-131">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="dccc4-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="dccc4-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dccc4-132">-Confirm</span></span>
<span data-ttu-id="dccc4-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dccc4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dccc4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dccc4-134">-WhatIf</span></span>
<span data-ttu-id="dccc4-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dccc4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dccc4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dccc4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dccc4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccc4-137">CommonParameters</span></span>
<span data-ttu-id="dccc4-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccc4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccc4-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dccc4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccc4-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dccc4-140">INPUTS</span></span>

### <span data-ttu-id="dccc4-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="dccc4-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="dccc4-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dccc4-142">OUTPUTS</span></span>

### <span data-ttu-id="dccc4-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dccc4-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="dccc4-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="dccc4-144">NOTES</span></span>

## <span data-ttu-id="dccc4-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dccc4-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

