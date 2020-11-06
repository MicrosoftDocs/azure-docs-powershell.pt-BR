---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 84c6df195b0d24e5096748a4a5e3fd8360665831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427905"
---
# <span data-ttu-id="ab55d-101">Update-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab55d-101">Update-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ab55d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab55d-102">SYNOPSIS</span></span>
<span data-ttu-id="ab55d-103">Atualizar atributos editáveis de uma conta de armazenamento do Azure gerenciada do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ab55d-103">Update editable attributes of a Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab55d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab55d-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String>
 [-ActiveKeyName <String>] [-AutoRegenerateKey <Boolean>] [-RegenerationPeriod <TimeSpan>] [-Enable <Boolean>]
 [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab55d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab55d-105">DESCRIPTION</span></span>
<span data-ttu-id="ab55d-106">Atualize os atributos editáveis de um cofre de chaves da conta de armazenamento do Azure gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ab55d-106">Update the editable attributes of a Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ab55d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab55d-107">EXAMPLES</span></span>

### <span data-ttu-id="ab55d-108">Exemplo 1: atualizar a chave ativa para "Key2" em uma conta de armazenamento do Azure gerenciada do Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ab55d-108">Example 1:Update the active key to 'key2' on a Key Vault managed Azure Storage Account.</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -ActiveKeyName 'key2'
```

<span data-ttu-id="ab55d-109">Atualiza a chave ativa da conta de armazenamento do repositório de chaves do Azure para "Key2".</span><span class="sxs-lookup"><span data-stu-id="ab55d-109">Updates the Key Vault managed Azure Storage Account active key to 'key2'.</span></span> <span data-ttu-id="ab55d-110">"Key2" será usado para gerar tokens SAS após esta atualização.</span><span class="sxs-lookup"><span data-stu-id="ab55d-110">'key2' will be used to generate SAS tokens after this update.</span></span>

## <span data-ttu-id="ab55d-111">OS</span><span class="sxs-lookup"><span data-stu-id="ab55d-111">PARAMETERS</span></span>

### <span data-ttu-id="ab55d-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ab55d-112">-AccountName</span></span>
<span data-ttu-id="ab55d-113">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ab55d-113">Key Vault managed storage account name.</span></span> <span data-ttu-id="ab55d-114">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="ab55d-114">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab55d-115">-ActiveKeyName</span><span class="sxs-lookup"><span data-stu-id="ab55d-115">-ActiveKeyName</span></span>
<span data-ttu-id="ab55d-116">Nome da chave ativa.</span><span class="sxs-lookup"><span data-stu-id="ab55d-116">Active key name.</span></span>
<span data-ttu-id="ab55d-117">Se não for especificado, o valor existente do nome de chave ativa da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="ab55d-117">If not specified, the existing value of managed storage account's active key name remains unchanged</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab55d-118">-AutoRegenerateKey</span><span class="sxs-lookup"><span data-stu-id="ab55d-118">-AutoRegenerateKey</span></span>
<span data-ttu-id="ab55d-119">Regenerar chave automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ab55d-119">Auto regenerate key.</span></span>
<span data-ttu-id="ab55d-120">Se não for especificado, o valor existente da chave de regeração automática da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="ab55d-120">If not specified, the existing value of auto regenerate key of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab55d-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ab55d-121">-Confirm</span></span>
<span data-ttu-id="ab55d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab55d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab55d-123">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="ab55d-123">-Enable</span></span>
<span data-ttu-id="ab55d-124">Se presente, permite o uso de uma chave de conta de armazenamento gerenciada para geração de token SAS se value for true.</span><span class="sxs-lookup"><span data-stu-id="ab55d-124">If present, enables a use of a managed storage account key for sas token generation if value is true.</span></span> <span data-ttu-id="ab55d-125">Desabilita o uso de uma chave de conta de armazenamento gerenciado para a geração de token SAS se value for false.</span><span class="sxs-lookup"><span data-stu-id="ab55d-125">Disables use of a managed storage account key for sas token generation if value is false.</span></span> <span data-ttu-id="ab55d-126">Se não for especificado, o valor existente do estado habilitado/desabilitado da conta de armazenamento permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="ab55d-126">If not specified, the existing value of the storage account's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="ab55d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab55d-127">-PassThru</span></span>
<span data-ttu-id="ab55d-128">O cmdlet não retorna objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="ab55d-128">Cmdlet does not return object by default.</span></span> <span data-ttu-id="ab55d-129">Se essa opção for especificada, retorne o objeto de conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ab55d-129">If this switch is specified, return managed storage account object.</span></span>

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

### <span data-ttu-id="ab55d-130">-RegenerationPeriod</span><span class="sxs-lookup"><span data-stu-id="ab55d-130">-RegenerationPeriod</span></span>
<span data-ttu-id="ab55d-131">Período de regeneração.</span><span class="sxs-lookup"><span data-stu-id="ab55d-131">Regeneration period.</span></span> <span data-ttu-id="ab55d-132">Se a chave de regeração automática estiver habilitada, esse valor especificará o TimeSpan após o qual a chave inativa da conta de armazenamento gerenciado será gerada automaticamente e se tornará a chave ativa.</span><span class="sxs-lookup"><span data-stu-id="ab55d-132">If auto regenerate key is enabled, this value specifies the timespan after which managed storage account's inactive keygets auto regenerated and becomes the active key.</span></span> <span data-ttu-id="ab55d-133">Se não for especificado, o valor existente do período de regeneração das chaves da conta de armazenamento gerenciado permanecerá inalterado</span><span class="sxs-lookup"><span data-stu-id="ab55d-133">If not specified, the existing value of regeneration period of keys of managed storage account remains unchanged</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab55d-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="ab55d-134">-Tag</span></span>
<span data-ttu-id="ab55d-135">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ab55d-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ab55d-136">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ab55d-136">For example:</span></span>

<span data-ttu-id="ab55d-137">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ab55d-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab55d-138">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="ab55d-138">-VaultName</span></span>
<span data-ttu-id="ab55d-139">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="ab55d-139">Vault name.</span></span>
<span data-ttu-id="ab55d-140">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ab55d-140">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab55d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab55d-141">-WhatIf</span></span>
<span data-ttu-id="ab55d-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ab55d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab55d-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab55d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab55d-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab55d-144">-DefaultProfile</span></span>
<span data-ttu-id="ab55d-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab55d-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab55d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab55d-146">CommonParameters</span></span>
<span data-ttu-id="ab55d-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab55d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab55d-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab55d-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab55d-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab55d-149">INPUTS</span></span>

## <span data-ttu-id="ab55d-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab55d-150">OUTPUTS</span></span>

### <span data-ttu-id="ab55d-151">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab55d-151">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="ab55d-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab55d-152">NOTES</span></span>

## <span data-ttu-id="ab55d-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab55d-153">RELATED LINKS</span></span>

[<span data-ttu-id="ab55d-154">AzureRM. keyvault</span><span class="sxs-lookup"><span data-stu-id="ab55d-154">AzureRM.KeyVault</span></span>](/powershell/module/azurerm.keyvault)
