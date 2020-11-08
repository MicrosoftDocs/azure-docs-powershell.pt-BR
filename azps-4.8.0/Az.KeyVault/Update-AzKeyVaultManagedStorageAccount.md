---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 72d23725f537df4f3e2244e799437394496bf434
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111702"
---
# <span data-ttu-id="f2503-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2503-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f2503-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2503-102">SYNOPSIS</span></span>
<span data-ttu-id="f2503-103">Atualizar atributos editáveis de uma conta de armazenamento do Azure gerenciada do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f2503-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="f2503-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2503-104">SYNTAX</span></span>

### <span data-ttu-id="f2503-105">ByDefinitionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2503-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2503-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2503-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2503-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2503-107">DESCRIPTION</span></span>
<span data-ttu-id="f2503-108">Atualize os atributos editáveis de um cofre de chaves da conta de armazenamento do Azure gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2503-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="f2503-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2503-109">EXAMPLES</span></span>

### <span data-ttu-id="f2503-110">Exemplo 1: atualizar a chave ativa para "Key2" em uma conta de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f2503-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key2
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="f2503-111">Atualiza a chave ativa da conta de armazenamento do repositório de chaves do Azure para "Key2".</span><span class="sxs-lookup"><span data-stu-id="f2503-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="f2503-112">"Key2" será usado para gerar tokens SAS após esta atualização.</span><span class="sxs-lookup"><span data-stu-id="f2503-112">'key2' will be used to generate SAS tokens after this update.</span></span>

### <span data-ttu-id="f2503-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f2503-113">Example 2</span></span>

<span data-ttu-id="f2503-114">Atualizar atributos editáveis de uma conta de armazenamento do Azure gerenciada do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f2503-114">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="f2503-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="f2503-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultManagedStorageAccount -AccountName 'mystorageaccount' -AutoRegenerateKey $false -RegenerationPeriod $regenerationPeriod -VaultName 'myvault'
```

## <span data-ttu-id="f2503-116">OS</span><span class="sxs-lookup"><span data-stu-id="f2503-116">PARAMETERS</span></span>

### <span data-ttu-id="f2503-117">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f2503-117">-AccountName</span></span>
<span data-ttu-id="f2503-118">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f2503-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="f2503-119">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f2503-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="f2503-120">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="f2503-120">-ActiveKeyName</span></span>
<span data-ttu-id="f2503-121">Nome da chave ativa.</span><span class="sxs-lookup"><span data-stu-id="f2503-121">Active key name.</span></span>
<span data-ttu-id="f2503-122">Se não for especificado, o valor existente do nome de chave ativa da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="f2503-122">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2503-123">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="f2503-123">-AutoRegenerateKey</span></span>
<span data-ttu-id="f2503-124">Regenerar chave automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f2503-124">Auto regenerate key.</span></span>
<span data-ttu-id="f2503-125">Se não for especificado, o valor existente da chave de regeração automática da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="f2503-125">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2503-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2503-126">-DefaultProfile</span></span>
<span data-ttu-id="f2503-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f2503-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2503-128">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="f2503-128">-Enable</span></span>
<span data-ttu-id="f2503-129">Se presente, permite o uso de uma chave de conta de armazenamento gerenciada para geração de token SAS se value for true.</span><span class="sxs-lookup"><span data-stu-id="f2503-129">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="f2503-130">Desabilita o uso de uma chave de conta de armazenamento gerenciado para a geração de token SAS se value for false.</span><span class="sxs-lookup"><span data-stu-id="f2503-130">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="f2503-131">Se não for especificado, o valor existente do estado habilitado/desabilitado da conta de armazenamento permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="f2503-131">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2503-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2503-132">-InputObject</span></span>
<span data-ttu-id="f2503-133">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="f2503-133">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="f2503-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2503-134">-PassThru</span></span>
<span data-ttu-id="f2503-135">O cmdlet não retorna objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="f2503-135">Cmdlet does not return object by default.</span></span> <span data-ttu-id="f2503-136">Se essa opção for especificada, retorne o objeto de conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2503-136">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="f2503-137">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="f2503-137">-RegenerationPeriod</span></span>
<span data-ttu-id="f2503-138">Período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="f2503-138">Regeneration period.</span></span> <span data-ttu-id="f2503-139">Se a chave de regeração automática estiver habilitada, esse valor especificará o TimeSpan após o qual a chave inativa da conta de armazenamento gerenciado será gerada automaticamente e se tornará a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="f2503-139">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="f2503-140">Se não for especificado, o valor existente do período de regeneração das chaves da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="f2503-140">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2503-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="f2503-141">-Tag</span></span>
<span data-ttu-id="f2503-142">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f2503-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f2503-143">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f2503-143">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2503-144">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="f2503-144">-VaultName</span></span>
<span data-ttu-id="f2503-145">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="f2503-145">Vault name.</span></span>
<span data-ttu-id="f2503-146">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="f2503-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f2503-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f2503-147">-Confirm</span></span>
<span data-ttu-id="f2503-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2503-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2503-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2503-149">-WhatIf</span></span>
<span data-ttu-id="f2503-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f2503-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2503-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f2503-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2503-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2503-152">CommonParameters</span></span>
<span data-ttu-id="f2503-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2503-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2503-154">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2503-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2503-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2503-155">INPUTS</span></span>

### <span data-ttu-id="f2503-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f2503-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="f2503-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2503-157">OUTPUTS</span></span>

### <span data-ttu-id="f2503-158">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2503-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="f2503-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2503-159">NOTES</span></span>

## <span data-ttu-id="f2503-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2503-160">RELATED LINKS</span></span>

[<span data-ttu-id="f2503-161">AZ. keyvault</span><span class="sxs-lookup"><span data-stu-id="f2503-161">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
