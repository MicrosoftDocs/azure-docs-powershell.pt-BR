---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageEncryptionScope.md
ms.openlocfilehash: ab2750bff8ccc3f53761671455bc50fe3ec154d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891959"
---
# <span data-ttu-id="b060c-101">New-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b060c-101">New-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="b060c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b060c-102">SYNOPSIS</span></span>
<span data-ttu-id="b060c-103">Cria um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b060c-103">Creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="b060c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b060c-104">SYNTAX</span></span>

### <span data-ttu-id="b060c-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b060c-105">AccountName (Default)</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-StorageEncryption] [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b060c-106">AccountNameKeyVault</span><span class="sxs-lookup"><span data-stu-id="b060c-106">AccountNameKeyVault</span></span>
```
New-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -EncryptionScopeName <String> [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b060c-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b060c-107">AccountObject</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-StorageEncryption] [-RequireInfrastructureEncryption] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b060c-108">AccountObjectKeyVault</span><span class="sxs-lookup"><span data-stu-id="b060c-108">AccountObjectKeyVault</span></span>
```
New-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> -EncryptionScopeName <String>
 [-KeyvaultEncryption] -KeyUri <String> [-RequireInfrastructureEncryption]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b060c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b060c-109">DESCRIPTION</span></span>
<span data-ttu-id="b060c-110">O cmdlet **New-AzStorageEncryptionScope** cria um escopo de criptografia para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b060c-110">The **New-AzStorageEncryptionScope** cmdlet creates an encryption scope for a Storage account.</span></span>

## <span data-ttu-id="b060c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b060c-111">EXAMPLES</span></span>

### <span data-ttu-id="b060c-112">Exemplo 1: Criar um escopo de criptografia com Criptografia de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="b060c-112">Example 1: Create an encryption scope with Storage Encryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"  -EncryptionScopeName testscope -StorageEncryption

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source            KeyVaultKeyUri RequireInfrastructureEncryption                                         
----      -----    ------            -------------- -------------------------------                                         
testscope Enabled  Microsoft.Storage
```

<span data-ttu-id="b060c-113">Este comando cria um escopo de criptografia com Criptografia de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b060c-113">This command creates an encryption scope with Storage Encryption.</span></span>

### <span data-ttu-id="b060c-114">Exemplo 2: Criar um escopo de criptografia com Criptografia Keyvault e RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="b060c-114">Example 2: Create an encryption scope with Keyvault Encryption, and RequireInfrastructureEncryption</span></span>
```
PS C:\> New-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" `
    -EncryptionScopeName testscope -KeyvaultEncryption -KeyUri "https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57" `
    -RequireInfrastructureEncryption 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name         State   Source           KeyVaultKeyUri                                                                          RequireInfrastructureEncryption                                       
----         -----   ------             --------------                                                                        -------------------------------                                     
testscope Enabled  Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname/34a0ba563b4243d9a0ef2b1d3c0c7d57  True 
```

<span data-ttu-id="b060c-115">Este comando cria um escopo de criptografia com Criptografia Keyvault e RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="b060c-115">This command creates an encryption scope with Keyvault Encryption and RequireInfrastructureEncryption.</span></span>
<span data-ttu-id="b060c-116">A Identidade da conta de armazenamento precisa ter permissões get,wrapkey,unwrapkey para a chave keyvault.</span><span class="sxs-lookup"><span data-stu-id="b060c-116">The Storage account Identity need have get,wrapkey,unwrapkey permissions to the keyvault key.</span></span>

## <span data-ttu-id="b060c-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b060c-117">PARAMETERS</span></span>

### <span data-ttu-id="b060c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b060c-118">-DefaultProfile</span></span>
<span data-ttu-id="b060c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b060c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b060c-120">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="b060c-120">-EncryptionScopeName</span></span>
<span data-ttu-id="b060c-121">Nome do Azure Storage EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b060c-121">Azure Storage EncryptionScope name</span></span>

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

### <span data-ttu-id="b060c-122">-KeyUri</span><span class="sxs-lookup"><span data-stu-id="b060c-122">-KeyUri</span></span>
<span data-ttu-id="b060c-123">A chave Uri</span><span class="sxs-lookup"><span data-stu-id="b060c-123">The key Uri</span></span>

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

### <span data-ttu-id="b060c-124">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="b060c-124">-KeyvaultEncryption</span></span>
<span data-ttu-id="b060c-125">Criar escopo de criptografia com keySource como Microsoft.Keyvault</span><span class="sxs-lookup"><span data-stu-id="b060c-125">Create encryption scope with keySource as Microsoft.Keyvault</span></span>

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

### <span data-ttu-id="b060c-126">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="b060c-126">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="b060c-127">O escopo de criptografia aplicará uma camada secundária de criptografia com chaves gerenciadas da plataforma para dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="b060c-127">The encryption scope will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="b060c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b060c-128">-ResourceGroupName</span></span>
<span data-ttu-id="b060c-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="b060c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b060c-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b060c-130">-StorageAccount</span></span>
<span data-ttu-id="b060c-131">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b060c-131">Storage account object</span></span>

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

### <span data-ttu-id="b060c-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b060c-132">-StorageAccountName</span></span>
<span data-ttu-id="b060c-133">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b060c-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="b060c-134">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="b060c-134">-StorageEncryption</span></span>
<span data-ttu-id="b060c-135">Criar escopo de criptografia com keySource como Microsoft.Storage.</span><span class="sxs-lookup"><span data-stu-id="b060c-135">Create encryption scope with keySource as Microsoft.Storage.</span></span>

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

### <span data-ttu-id="b060c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b060c-136">-Confirm</span></span>
<span data-ttu-id="b060c-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b060c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b060c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b060c-138">-WhatIf</span></span>
<span data-ttu-id="b060c-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b060c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b060c-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b060c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b060c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b060c-141">CommonParameters</span></span>
<span data-ttu-id="b060c-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b060c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b060c-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b060c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b060c-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b060c-144">INPUTS</span></span>

### <span data-ttu-id="b060c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b060c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="b060c-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b060c-146">OUTPUTS</span></span>

### <span data-ttu-id="b060c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="b060c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="b060c-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="b060c-148">NOTES</span></span>

## <span data-ttu-id="b060c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b060c-149">RELATED LINKS</span></span>
