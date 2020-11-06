---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1a21db1918d9baef48d3efd15dc72c2cb542a925
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430212"
---
# <span data-ttu-id="fcb47-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcb47-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fcb47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fcb47-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb47-103">Atualizar atributos editáveis de uma conta de armazenamento do Azure gerenciada do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fcb47-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcb47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcb47-104">SYNTAX</span></span>

### <span data-ttu-id="fcb47-105">ByDefinitionName (padrão)</span><span class="sxs-lookup"><span data-stu-id="fcb47-105">ByDefinitionName (Default)</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcb47-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fcb47-106">ByInputObject</span></span>
```
Update-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcb47-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fcb47-107">DESCRIPTION</span></span>
<span data-ttu-id="fcb47-108">Atualize os atributos editáveis de um cofre de chaves da conta de armazenamento do Azure gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fcb47-108">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="fcb47-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fcb47-109">EXAMPLES</span></span>

### <span data-ttu-id="fcb47-110">Exemplo 1: atualizar a chave ativa para "Key2" em uma conta de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="fcb47-110">Example 1: Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```powershell
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'

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

<span data-ttu-id="fcb47-111">Atualiza a chave ativa da conta de armazenamento do repositório de chaves do Azure para "Key2".</span><span class="sxs-lookup"><span data-stu-id="fcb47-111">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="fcb47-112">"Key2" será usado para gerar tokens SAS após esta atualização.</span><span class="sxs-lookup"><span data-stu-id="fcb47-112">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="fcb47-113">OS</span><span class="sxs-lookup"><span data-stu-id="fcb47-113">PARAMETERS</span></span>

### <span data-ttu-id="fcb47-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fcb47-114">-AccountName</span></span>
<span data-ttu-id="fcb47-115">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="fcb47-115">Key Vault managed storage account name.</span></span> <span data-ttu-id="fcb47-116">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="fcb47-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="fcb47-117">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="fcb47-117">-ActiveKeyName</span></span>
<span data-ttu-id="fcb47-118">Nome da chave ativa.</span><span class="sxs-lookup"><span data-stu-id="fcb47-118">Active key name.</span></span>
<span data-ttu-id="fcb47-119">Se não for especificado, o valor existente do nome de chave ativa da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="fcb47-119">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

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

### <span data-ttu-id="fcb47-120">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="fcb47-120">-AutoRegenerateKey</span></span>
<span data-ttu-id="fcb47-121">Regenerar chave automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fcb47-121">Auto regenerate key.</span></span>
<span data-ttu-id="fcb47-122">Se não for especificado, o valor existente da chave de regeração automática da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="fcb47-122">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="fcb47-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb47-123">-DefaultProfile</span></span>
<span data-ttu-id="fcb47-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="fcb47-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fcb47-125">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="fcb47-125">-Enable</span></span>
<span data-ttu-id="fcb47-126">Se presente, permite o uso de uma chave de conta de armazenamento gerenciada para geração de token SAS se value for true.</span><span class="sxs-lookup"><span data-stu-id="fcb47-126">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="fcb47-127">Desabilita o uso de uma chave de conta de armazenamento gerenciado para a geração de token SAS se value for false.</span><span class="sxs-lookup"><span data-stu-id="fcb47-127">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="fcb47-128">Se não for especificado, o valor existente do estado habilitado/desabilitado da conta de armazenamento permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="fcb47-128">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="fcb47-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcb47-129">-InputObject</span></span>
<span data-ttu-id="fcb47-130">Objeto ManagedStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="fcb47-130">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="fcb47-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcb47-131">-PassThru</span></span>
<span data-ttu-id="fcb47-132">O cmdlet não retorna objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="fcb47-132">Cmdlet does not return object by default.</span></span> <span data-ttu-id="fcb47-133">Se essa opção for especificada, retorne o objeto de conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fcb47-133">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="fcb47-134">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="fcb47-134">-RegenerationPeriod</span></span>
<span data-ttu-id="fcb47-135">Período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="fcb47-135">Regeneration period.</span></span> <span data-ttu-id="fcb47-136">Se a chave de regeração automática estiver habilitada, esse valor especificará o TimeSpan após o qual a chave inativa da conta de armazenamento gerenciado será gerada automaticamente e se tornará a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="fcb47-136">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="fcb47-137">Se não for especificado, o valor existente do período de regeneração das chaves da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="fcb47-137">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

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

### <span data-ttu-id="fcb47-138">-Marca</span><span class="sxs-lookup"><span data-stu-id="fcb47-138">-Tag</span></span>
<span data-ttu-id="fcb47-139">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fcb47-139">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fcb47-140">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fcb47-140">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fcb47-141">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="fcb47-141">-VaultName</span></span>
<span data-ttu-id="fcb47-142">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="fcb47-142">Vault name.</span></span>
<span data-ttu-id="fcb47-143">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="fcb47-143">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fcb47-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fcb47-144">-Confirm</span></span>
<span data-ttu-id="fcb47-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcb47-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb47-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb47-146">-WhatIf</span></span>
<span data-ttu-id="fcb47-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fcb47-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcb47-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fcb47-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb47-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb47-149">CommonParameters</span></span>
<span data-ttu-id="fcb47-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb47-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb47-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb47-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb47-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fcb47-152">INPUTS</span></span>

### <span data-ttu-id="fcb47-153">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fcb47-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>
<span data-ttu-id="fcb47-154">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fcb47-154">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fcb47-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fcb47-155">OUTPUTS</span></span>

### <span data-ttu-id="fcb47-156">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcb47-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fcb47-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fcb47-157">NOTES</span></span>

## <span data-ttu-id="fcb47-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fcb47-158">RELATED LINKS</span></span>

[<span data-ttu-id="fcb47-159">AzureRM. keyvault</span><span class="sxs-lookup"><span data-stu-id="fcb47-159">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
