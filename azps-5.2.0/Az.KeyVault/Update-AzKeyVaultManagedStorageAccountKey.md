---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258532"
---
# <span data-ttu-id="fe3f0-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="fe3f0-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="fe3f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe3f0-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3f0-103">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="fe3f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe3f0-104">SYNTAX</span></span>

### <span data-ttu-id="fe3f0-105">ByDefinitionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe3f0-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3f0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fe3f0-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe3f0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe3f0-107">DESCRIPTION</span></span>
<span data-ttu-id="fe3f0-108">Regenera a chave especificada da conta de armazenamento do Azure gerenciada do Key Vault e define a chave como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="fe3f0-109">Os proxies do cofre de chaves chamam a chamada para o Azure Resource Manager para regenerar a chave.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="fe3f0-110">O chamador deve possuem permissões para gerar novamente as chaves em uma determinada conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="fe3f0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe3f0-111">EXAMPLES</span></span>

### <span data-ttu-id="fe3f0-112">Exemplo 1: regenerar uma chave</span><span class="sxs-lookup"><span data-stu-id="fe3f0-112">Example 1: Regenerate a key</span></span>
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

<span data-ttu-id="fe3f0-113">Gera novamente ' key1 ' da conta ' mystorageaccount ' e define ' key1 ' como o ativo da conta de armazenamento do Azure gerenciada do compartimento de chaves.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="fe3f0-114">OS</span><span class="sxs-lookup"><span data-stu-id="fe3f0-114">PARAMETERS</span></span>

### <span data-ttu-id="fe3f0-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fe3f0-115">-AccountName</span></span>
<span data-ttu-id="fe3f0-116">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="fe3f0-117">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="fe3f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3f0-118">-DefaultProfile</span></span>
<span data-ttu-id="fe3f0-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fe3f0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe3f0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fe3f0-120">-Force</span></span>
<span data-ttu-id="fe3f0-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fe3f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe3f0-122">-InputObject</span></span>
<span data-ttu-id="fe3f0-123">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="fe3f0-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fe3f0-124">-KeyName</span></span>
<span data-ttu-id="fe3f0-125">Nome da chave da conta de armazenamento para gerar novamente e ativar.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="fe3f0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe3f0-126">-PassThru</span></span>
<span data-ttu-id="fe3f0-127">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fe3f0-128">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciada que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="fe3f0-129">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="fe3f0-129">-VaultName</span></span>
<span data-ttu-id="fe3f0-130">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-130">Vault name.</span></span>
<span data-ttu-id="fe3f0-131">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fe3f0-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe3f0-132">-Confirm</span></span>
<span data-ttu-id="fe3f0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3f0-134">-WhatIf</span></span>
<span data-ttu-id="fe3f0-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3f0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3f0-137">CommonParameters</span></span>
<span data-ttu-id="fe3f0-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3f0-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe3f0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3f0-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe3f0-140">INPUTS</span></span>

### <span data-ttu-id="fe3f0-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fe3f0-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="fe3f0-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe3f0-142">OUTPUTS</span></span>

### <span data-ttu-id="fe3f0-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fe3f0-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fe3f0-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe3f0-144">NOTES</span></span>

## <span data-ttu-id="fe3f0-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe3f0-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

