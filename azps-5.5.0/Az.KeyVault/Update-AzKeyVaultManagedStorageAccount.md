---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 72d23725f537df4f3e2244e799437394496bf434
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113061"
---
# <span data-ttu-id="7cfbd-101">Update-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cfbd-101">Update-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7cfbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7cfbd-102">SYNOPSIS</span></span>
<span data-ttu-id="7cfbd-103">Atualizar atributos editáveis de uma Conta de Armazenamento gerenciada do Azure do Cofre de Chave.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="7cfbd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cfbd-104">SYNTAX</span></span>

### <span data-ttu-id="7cfbd-105">ByDefinitionName (Default)</span><span class="sxs-lookup"><span data-stu-id="7cfbd-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-ActiveKeyName <String>]
 [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cfbd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7cfbd-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cfbd-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cfbd-107">DESCRIPTION</span></span>
<span data-ttu-id="7cfbd-108">Atualize os atributos editáveis de uma Conta de Armazenamento gerenciada pelo Azure Do Cofre de Chave.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="7cfbd-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7cfbd-109">EXAMPLES</span></span>

### <span data-ttu-id="7cfbd-110">Exemplo 1: Atualizar a chave ativa para 'chave2' em uma Conta de Armazenamento gerenciada do Azure Do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
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

<span data-ttu-id="7cfbd-111">Atualiza a chave ativa da conta ativa gerenciada do Azure Storage Vault para 'chave2'.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="7cfbd-112">A 'chave2' será usada para gerar tokens SAS após esta atualização.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-112">'key2' will be used to generate SAS tokens after this update.</span></span>

### <span data-ttu-id="7cfbd-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7cfbd-113">Example 2</span></span>

<span data-ttu-id="7cfbd-114">Atualizar atributos editáveis de uma Conta de Armazenamento gerenciada do Azure do Cofre de Chave.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-114">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="7cfbd-115">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="7cfbd-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultManagedStorageAccount -AccountName 'mystorageaccount' -AutoRegenerateKey $false -RegenerationPeriod $regenerationPeriod -VaultName 'myvault'
```

## <span data-ttu-id="7cfbd-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cfbd-116">PARAMETERS</span></span>

### <span data-ttu-id="7cfbd-117">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="7cfbd-117">-AccountName</span></span>
<span data-ttu-id="7cfbd-118">Nome da conta de armazenamento gerenciada do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-118">Key Vault managed storage account name.</span></span> <span data-ttu-id="7cfbd-119">O Cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, do ambiente selecionado no momento e do nome da conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-119">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="7cfbd-120">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="7cfbd-120">-ActiveKeyName</span></span>
<span data-ttu-id="7cfbd-121">Nome da chave ativa.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-121">Active key name.</span></span>
<span data-ttu-id="7cfbd-122">Se não especificado, o valor existente do nome da chave ativa da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="7cfbd-122">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="7cfbd-123">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="7cfbd-123">-AutoRegenerateKey</span></span>
<span data-ttu-id="7cfbd-124">Tecla de regeneração automática.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-124">Auto regenerate key.</span></span>
<span data-ttu-id="7cfbd-125">Se não especificado, o valor existente da chave de regeneração automática da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="7cfbd-125">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="7cfbd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cfbd-126">-DefaultProfile</span></span>
<span data-ttu-id="7cfbd-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7cfbd-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cfbd-128">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="7cfbd-128">-Enable</span></span>
<span data-ttu-id="7cfbd-129">Se presente, habilita o uso de uma chave de conta de armazenamento gerenciada para a geração de token sas se o valor for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-129">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="7cfbd-130">Desabilita o uso de uma chave de conta de armazenamento gerenciada para a geração de token sas se o valor for falso.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-130">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="7cfbd-131">Se não especificado, o valor existente do estado habilitado/desabilitado da conta de armazenamento permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-131">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="7cfbd-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cfbd-132">-InputObject</span></span>
<span data-ttu-id="7cfbd-133">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-133">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="7cfbd-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7cfbd-134">-PassThru</span></span>
<span data-ttu-id="7cfbd-135">O Cmdlet não retorna objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-135">Cmdlet does not return object by default.</span></span> <span data-ttu-id="7cfbd-136">Se essa opção for especificada, retorne o objeto de conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-136">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="7cfbd-137">-DesalmadaPeriod</span><span class="sxs-lookup"><span data-stu-id="7cfbd-137">-RegenerationPeriod</span></span>
<span data-ttu-id="7cfbd-138">Período de recuperação.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-138">Regeneration period.</span></span> <span data-ttu-id="7cfbd-139">Se a chave de regeneração automática estiver habilitada, esse valor especificará o período após o qual a chave inativa da conta de armazenamento gerenciada será automaticamente regenerada e se tornará a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-139">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="7cfbd-140">Se não especificado, o valor existente do período de recuperação das chaves da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="7cfbd-140">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="7cfbd-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="7cfbd-141">-Tag</span></span>
<span data-ttu-id="7cfbd-142">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7cfbd-143">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="7cfbd-143">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7cfbd-144">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="7cfbd-144">-VaultName</span></span>
<span data-ttu-id="7cfbd-145">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-145">Vault name.</span></span>
<span data-ttu-id="7cfbd-146">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7cfbd-147">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7cfbd-147">-Confirm</span></span>
<span data-ttu-id="7cfbd-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cfbd-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cfbd-149">-WhatIf</span></span>
<span data-ttu-id="7cfbd-150">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cfbd-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cfbd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cfbd-152">CommonParameters</span></span>
<span data-ttu-id="7cfbd-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cfbd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cfbd-154">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cfbd-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cfbd-155">Entradas</span><span class="sxs-lookup"><span data-stu-id="7cfbd-155">INPUTS</span></span>

### <span data-ttu-id="7cfbd-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7cfbd-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="7cfbd-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="7cfbd-157">OUTPUTS</span></span>

### <span data-ttu-id="7cfbd-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cfbd-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="7cfbd-159">Notas</span><span class="sxs-lookup"><span data-stu-id="7cfbd-159">NOTES</span></span>

## <span data-ttu-id="7cfbd-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7cfbd-160">RELATED LINKS</span></span>

[<span data-ttu-id="7cfbd-161">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cfbd-161">Az.KeyVault</span></span>](/powershell/module/az.keyvault)
