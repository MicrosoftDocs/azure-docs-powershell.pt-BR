---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageEncryptionScope.md
ms.openlocfilehash: 153165406fd02561dbece79e18558065ff34c8f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888044"
---
# <span data-ttu-id="479bf-101">Update-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="479bf-101">Update-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="479bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="479bf-102">SYNOPSIS</span></span>
<span data-ttu-id="479bf-103">Modificar um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="479bf-103">Modify an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="479bf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="479bf-104">SYNTAX</span></span>

### <span data-ttu-id="479bf-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="479bf-105">AccountName (Default)</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="479bf-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="479bf-106">AccountNameKeyVault</span></span>
```
Update-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="479bf-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="479bf-107">AccountObject</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="479bf-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="479bf-108">AccountObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="479bf-109">EncryptionScopeObject</span><span class="sxs-lookup"><span data-stu-id="479bf-109">EncryptionScopeObject</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-StorageEncryption] [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="479bf-110">EncryptionScopeObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="479bf-110">EncryptionScopeObjectKeyVault</span></span>
```
Update-AzStorageEncryptionScope -InputObject <PSEncryptionScope> [-KeyvaultEncryption] -KeyUri <String>
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="479bf-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="479bf-111">DESCRIPTION</span></span>
<span data-ttu-id="479bf-112">O cmdlet **Update-AzStorageEncryptionScope** modifica um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="479bf-112">The **Update-AzStorageEncryptionScope** cmdlet modifies an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="479bf-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="479bf-113">EXAMPLES</span></span>

### <span data-ttu-id="479bf-114">Exemplo 1: Desabilitar um escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="479bf-114">Example 1: Disable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Disabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Disabled Microsoft.Storage
```

<span data-ttu-id="479bf-115">Este comando desabilita um escopo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="479bf-115">This command disables an encryption scope.</span></span>

### <span data-ttu-id="479bf-116">Exemplo 2: Habilitar um escopo de criptografia</span><span class="sxs-lookup"><span data-stu-id="479bf-116">Example 2: Enable an encryption scope</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -State Enabled 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                                                           
----      -----    ------            -------------- -------------------------------                                                                          
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="479bf-117">Esse comando habilita um escopo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="479bf-117">This command enables an encryption scope.</span></span>

### <span data-ttu-id="479bf-118">Exemplo 3: atualizar um escopo de criptografia para usar a Criptografia de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="479bf-118">Example 3: Update an encryption scope to use Storage Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                          
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="479bf-119">Este comando atualiza um escopo de criptografia para usar a Criptografia de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="479bf-119">This command updates an encryption scope to use Storage Encryption.</span></span>

### <span data-ttu-id="479bf-120">Exemplo 4: atualizar um escopo de criptografia para usar a Criptografia Keyvault</span><span class="sxs-lookup"><span data-stu-id="479bf-120">Example 4: Update an encryption scope to use Keyvault Encryption</span></span>
```
PS C:\> Update-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                                                          RequireInfrastructureEncryption 
----      -----    ------             --------------                                                                          -------------------------------
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57   
```

<span data-ttu-id="479bf-121">Esse comando updta um escopo de criptografia para usar a Criptografia Keyvault.</span><span class="sxs-lookup"><span data-stu-id="479bf-121">This command updtaes an encryption scope to use Keyvault Encryption.</span></span>
<span data-ttu-id="479bf-122">A Identidade da conta de armazenamento precisa ter permissões get,wrapkey,unwrapkey para a chave keyvault.</span><span class="sxs-lookup"><span data-stu-id="479bf-122">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="479bf-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="479bf-123">PARAMETERS</span></span>

### <span data-ttu-id="479bf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="479bf-124">-DefaultProfile</span></span>
<span data-ttu-id="479bf-125">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="479bf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="479bf-126">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="479bf-126">-EncryptionScopeName</span></span>
<span data-ttu-id="479bf-127">Nome do Azure Storage EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="479bf-127">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="479bf-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="479bf-128">-InputObject</span></span>
<span data-ttu-id="479bf-129">Objeto EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="479bf-129">EncryptionScope object</span></span>

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

### <span data-ttu-id="479bf-130">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="479bf-130">-KeyUri</span></span>
<span data-ttu-id="479bf-131">A chave Uri</span><span class="sxs-lookup"><span data-stu-id="479bf-131">The key Uri</span></span>

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

### <span data-ttu-id="479bf-132">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="479bf-132">-KeyvaultEncryption</span></span>
<span data-ttu-id="479bf-133">Criar escopo de criptografia com keySource como Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="479bf-133">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="479bf-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="479bf-134">-ResourceGroupName</span></span>
<span data-ttu-id="479bf-135">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="479bf-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="479bf-136">-State</span><span class="sxs-lookup"><span data-stu-id="479bf-136">-State</span></span>
<span data-ttu-id="479bf-137">Atualizar o estado do escopo de criptografia, os valores possíveis incluem: 'Habilitado', 'Desabilitado'.</span><span class="sxs-lookup"><span data-stu-id="479bf-137">Update encryption scope State, Possible values include: 'Enabled', 'Disabled'.</span></span>

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

### <span data-ttu-id="479bf-138">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="479bf-138">-StorageAccount</span></span>
<span data-ttu-id="479bf-139">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="479bf-139">Storage account object</span></span>

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

### <span data-ttu-id="479bf-140">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="479bf-140">-StorageAccountName</span></span>
<span data-ttu-id="479bf-141">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="479bf-141">Storage Account Name.</span></span>

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

### <span data-ttu-id="479bf-142">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="479bf-142">-StorageEncryption</span></span>
<span data-ttu-id="479bf-143">Criar escopo de criptografia com keySource como Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="479bf-143">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="479bf-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="479bf-144">-Confirm</span></span>
<span data-ttu-id="479bf-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="479bf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="479bf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="479bf-146">-WhatIf</span></span>
<span data-ttu-id="479bf-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="479bf-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="479bf-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="479bf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="479bf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479bf-149">CommonParameters</span></span>
<span data-ttu-id="479bf-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="479bf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479bf-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="479bf-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479bf-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="479bf-152">INPUTS</span></span>

### <span data-ttu-id="479bf-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="479bf-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="479bf-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="479bf-154">OUTPUTS</span></span>

### <span data-ttu-id="479bf-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="479bf-155">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="479bf-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="479bf-156">NOTES</span></span>

## <span data-ttu-id="479bf-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="479bf-157">RELATED LINKS</span></span>
