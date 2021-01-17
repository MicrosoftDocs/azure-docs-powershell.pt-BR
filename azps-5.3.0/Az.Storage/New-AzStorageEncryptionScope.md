---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: 011bdd96d69ae73ca62145b85f6e636751f8eb9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427728"
---
# <span data-ttu-id="dc1d8-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="dc1d8-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="dc1d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1d8-103">Cria um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="dc1d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc1d8-104">SYNTAX</span></span>

### <span data-ttu-id="dc1d8-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dc1d8-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc1d8-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="dc1d8-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc1d8-107">Accountobject</span><span class="sxs-lookup"><span data-stu-id="dc1d8-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc1d8-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="dc1d8-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc1d8-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc1d8-109">DESCRIPTION</span></span>
<span data-ttu-id="dc1d8-110">O cmdlet **New-AzStorageEncryptionScope** cria um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="dc1d8-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc1d8-111">EXAMPLES</span></span>

### <span data-ttu-id="dc1d8-112">Exemplo 1: criar um escopo de criptografia com criptografia de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dc1d8-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri                                         
----      -----    ------            --------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="dc1d8-113">Esse comando cria um escopo de criptografia com criptografia de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="dc1d8-114">Exemplo 2: criar um escopo de criptografia com criptografia do keyvault</span><span class="sxs-lookup"><span data-stu-id="dc1d8-114">Example 2: Create an encryption scope with Keyvault Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57
```

<span data-ttu-id="dc1d8-115">Esse comando cria um escopo de criptografia com criptografia de compartimento de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-115">This command creates an encryption scope with Keyvault Encryption.</span></span>
<span data-ttu-id="dc1d8-116">A identidade da conta de armazenamento precisa ter permissões Get, wrapkey, unwrapkey para a chave keyvault.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="dc1d8-117">OS</span><span class="sxs-lookup"><span data-stu-id="dc1d8-117">PARAMETERS</span></span>

### <span data-ttu-id="dc1d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1d8-118">-DefaultProfile</span></span>
<span data-ttu-id="dc1d8-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc1d8-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="dc1d8-120">-EncryptionScopeName</span></span>
<span data-ttu-id="dc1d8-121">Nome do EncryptionScope de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="dc1d8-121">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1d8-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="dc1d8-122">-KeyUri</span></span>
<span data-ttu-id="dc1d8-123">O URI da chave</span><span class="sxs-lookup"><span data-stu-id="dc1d8-123">The key Uri</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1d8-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="dc1d8-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="dc1d8-125">Criar escopo de criptografia com o código-fonte como Microsoft. keyvault</span><span class="sxs-lookup"><span data-stu-id="dc1d8-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameKeyVault, AccountObjectKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="dc1d8-127">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc1d8-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc1d8-128">-StorageAccount</span></span>
<span data-ttu-id="dc1d8-129">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="dc1d8-129">Storage account object</span></span>

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

### <span data-ttu-id="dc1d8-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dc1d8-130">-StorageAccountName</span></span>
<span data-ttu-id="dc1d8-131">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="dc1d8-132">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="dc1d8-132">-StorageEncryption</span></span>
<span data-ttu-id="dc1d8-133">Criar escopo de criptografia com keySource como Microsoft. Storage.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-133">Create encryption scope with keySource as Microsoft.Storage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc1d8-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc1d8-134">-Confirm</span></span>
<span data-ttu-id="dc1d8-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc1d8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc1d8-136">-WhatIf</span></span>
<span data-ttu-id="dc1d8-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc1d8-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc1d8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1d8-139">CommonParameters</span></span>
<span data-ttu-id="dc1d8-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1d8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1d8-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1d8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1d8-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc1d8-142">INPUTS</span></span>

### <span data-ttu-id="dc1d8-143">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc1d8-143">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dc1d8-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc1d8-144">OUTPUTS</span></span>

### <span data-ttu-id="dc1d8-145">Microsoft. Azure. Commands. Management. Storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="dc1d8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="dc1d8-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc1d8-146">NOTES</span></span>

## <span data-ttu-id="dc1d8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc1d8-147">RELATED LINKS</span></span>
