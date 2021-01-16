---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 6c8f07cbdb70b84d235afa7ce953da0bac477f55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271285"
---
# <span data-ttu-id="1ca29-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1ca29-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="1ca29-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1ca29-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca29-103">Modifique um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1ca29-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="1ca29-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1ca29-104">SYNTAX</span></span>

### <span data-ttu-id="1ca29-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1ca29-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca29-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ca29-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca29-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="1ca29-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ca29-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ca29-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca29-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="1ca29-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ca29-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="1ca29-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ca29-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1ca29-111">DESCRIPTION</span></span>
<span data-ttu-id="1ca29-112">O cmdlet **Update-AzStorageEncryptionScope** modifica um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1ca29-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="1ca29-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ca29-113">EXAMPLES</span></span>

### <span data-ttu-id="1ca29-114">Exemplo 1: desabilitar um escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="1ca29-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="1ca29-115">Esse comando desabilita um escopo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="1ca29-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="1ca29-116">Exemplo 2: habilitar um escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="1ca29-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                                                          
----      -----    ------            --------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="1ca29-117">Esse comando habilita um escopo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="1ca29-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="1ca29-118">Exemplo 3: atualizar um escopo de criptografia para usar a criptografia de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ca29-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="1ca29-119">Esse comando atualiza um escopo de criptografia para usar a criptografia de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1ca29-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="1ca29-120">Exemplo 4: atualizar um escopo de criptografia para usar a criptografia do keyvault</span><span class="sxs-lookup"><span data-stu-id="1ca29-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="1ca29-121">Esse comando updtaes um escopo de criptografia para usar a criptografia do keyvault.</span><span class="sxs-lookup"><span data-stu-id="1ca29-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="1ca29-122">A identidade da conta de armazenamento precisa ter permissões Get, wrapkey, unwrapkey para a chave keyvault.</span><span class="sxs-lookup"><span data-stu-id="1ca29-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="1ca29-123">OS</span><span class="sxs-lookup"><span data-stu-id="1ca29-123">PARAMETERS</span></span>

### <span data-ttu-id="1ca29-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca29-124">-DefaultProfile</span></span>
<span data-ttu-id="1ca29-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ca29-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ca29-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="1ca29-126">-EncryptionScopeName</span></span>
<span data-ttu-id="1ca29-127">Nome do EncryptionScope de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="1ca29-127">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault, AccountObject, AccountObjectKeyVault
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ca29-128">-InputObject</span></span>
<span data-ttu-id="1ca29-129">Objeto EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1ca29-129">EncryptionScope object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope
Parameter Sets: EncryptionScopeObject, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="1ca29-130">-KeyUri</span></span>
<span data-ttu-id="1ca29-131">O URI da chave</span><span class="sxs-lookup"><span data-stu-id="1ca29-131">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="1ca29-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="1ca29-133">Criar escopo de criptografia com o código-fonte como Microsoft. keyvault</span><span class="sxs-lookup"><span data-stu-id="1ca29-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault, EncryptionScopeObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ca29-134">-ResourceGroupName</span></span>
<span data-ttu-id="1ca29-135">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ca29-135">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-136">-Estado</span><span class="sxs-lookup"><span data-stu-id="1ca29-136">-State</span></span>
<span data-ttu-id="1ca29-137">Atualizar estado do escopo de criptografia, os valores possíveis incluem: ' Enabled ', ' disabled '.</span><span class="sxs-lookup"><span data-stu-id="1ca29-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ca29-138">-StorageAccount</span></span>
<span data-ttu-id="1ca29-139">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1ca29-139">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1ca29-140">-StorageAccountName</span></span>
<span data-ttu-id="1ca29-141">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1ca29-141">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountNameKeyVault
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="1ca29-142">-StorageEncryption</span></span>
<span data-ttu-id="1ca29-143">Criar escopo de criptografia com keySource como Microsoft. Storage.</span><span class="sxs-lookup"><span data-stu-id="1ca29-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject, EncryptionScopeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ca29-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1ca29-144">-Confirm</span></span>
<span data-ttu-id="1ca29-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ca29-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ca29-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca29-146">-WhatIf</span></span>
<span data-ttu-id="1ca29-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ca29-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ca29-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ca29-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ca29-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca29-149">CommonParameters</span></span>
<span data-ttu-id="1ca29-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ca29-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca29-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca29-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca29-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1ca29-152">INPUTS</span></span>

### <span data-ttu-id="1ca29-153">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1ca29-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="1ca29-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1ca29-154">OUTPUTS</span></span>

### <span data-ttu-id="1ca29-155">Microsoft. Azure. Commands. Management. Storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="1ca29-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="1ca29-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1ca29-156">NOTES</span></span>

## <span data-ttu-id="1ca29-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ca29-157">RELATED LINKS</span></span>
