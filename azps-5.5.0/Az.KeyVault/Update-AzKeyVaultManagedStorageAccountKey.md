---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113060"
---
# <span data-ttu-id="be2a8-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="be2a8-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="be2a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="be2a8-103">Regenera a chave especificada da Conta de Armazenamento gerenciada pelo Azure Vault.</span><span class="sxs-lookup"><span data-stu-id="be2a8-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="be2a8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be2a8-104">SYNTAX</span></span>

### <span data-ttu-id="be2a8-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="be2a8-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be2a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="be2a8-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be2a8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="be2a8-107">DESCRIPTION</span></span>
<span data-ttu-id="be2a8-108">Regenera a chave especificada da Conta de Armazenamento gerenciada pelo Azure Vault e define a chave como a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="be2a8-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="be2a8-109">O Cofre de Teclas proxifica a chamada para o Gerenciador de Recursos do Azure para regenerar a chave.</span><span class="sxs-lookup"><span data-stu-id="be2a8-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="be2a8-110">O chamador deve ter permissões para regenerar chaves em determinada Conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="be2a8-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="be2a8-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be2a8-111">EXAMPLES</span></span>

### <span data-ttu-id="be2a8-112">Exemplo 1: Regenerar uma chave</span><span class="sxs-lookup"><span data-stu-id="be2a8-112">Example 1: Regenerate a key</span></span>
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

<span data-ttu-id="be2a8-113">Regenera a "chave1" da conta "mystorageaccount" e define "chave1" como a ativa da Conta de Armazenamento gerenciada do Azure Do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="be2a8-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="be2a8-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be2a8-114">PARAMETERS</span></span>

### <span data-ttu-id="be2a8-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="be2a8-115">-AccountName</span></span>
<span data-ttu-id="be2a8-116">Nome da conta de armazenamento gerenciada do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="be2a8-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="be2a8-117">O Cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="be2a8-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="be2a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2a8-118">-DefaultProfile</span></span>
<span data-ttu-id="be2a8-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="be2a8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be2a8-120">-Forçar</span><span class="sxs-lookup"><span data-stu-id="be2a8-120">-Force</span></span>
<span data-ttu-id="be2a8-121">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="be2a8-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="be2a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be2a8-122">-InputObject</span></span>
<span data-ttu-id="be2a8-123">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="be2a8-123">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="be2a8-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="be2a8-124">-KeyName</span></span>
<span data-ttu-id="be2a8-125">Nome da chave da conta de armazenamento para regenerar e tornar ativos.</span><span class="sxs-lookup"><span data-stu-id="be2a8-125">Name of storage account key to regenerate and make active.</span></span>

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

### <span data-ttu-id="be2a8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be2a8-126">-PassThru</span></span>
<span data-ttu-id="be2a8-127">O Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="be2a8-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="be2a8-128">Se essa opção for especificada, o cmdlet retornará a conta de armazenamento gerenciado que foi excluída.</span><span class="sxs-lookup"><span data-stu-id="be2a8-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="be2a8-129">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="be2a8-129">-VaultName</span></span>
<span data-ttu-id="be2a8-130">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="be2a8-130">Vault name.</span></span>
<span data-ttu-id="be2a8-131">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="be2a8-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="be2a8-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="be2a8-132">-Confirm</span></span>
<span data-ttu-id="be2a8-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be2a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be2a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be2a8-134">-WhatIf</span></span>
<span data-ttu-id="be2a8-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="be2a8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be2a8-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be2a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be2a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2a8-137">CommonParameters</span></span>
<span data-ttu-id="be2a8-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be2a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2a8-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be2a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2a8-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="be2a8-140">INPUTS</span></span>

### <span data-ttu-id="be2a8-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="be2a8-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="be2a8-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="be2a8-142">OUTPUTS</span></span>

### <span data-ttu-id="be2a8-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="be2a8-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="be2a8-144">Notas</span><span class="sxs-lookup"><span data-stu-id="be2a8-144">NOTES</span></span>

## <span data-ttu-id="be2a8-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be2a8-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

