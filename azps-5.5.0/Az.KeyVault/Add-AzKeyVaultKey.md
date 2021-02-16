---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: da6460bf0a1126a11345336e4d55c300728bbd66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117601"
---
# <span data-ttu-id="951f9-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="951f9-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="951f9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="951f9-102">SYNOPSIS</span></span>
<span data-ttu-id="951f9-103">Cria uma chave em um cofre de chave ou importa uma chave para um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="951f9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="951f9-104">SYNTAX</span></span>

### <span data-ttu-id="951f9-105">InteractiveCreate (Padrão)</span><span class="sxs-lookup"><span data-stu-id="951f9-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="951f9-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="951f9-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="951f9-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="951f9-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="951f9-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="951f9-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="951f9-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="951f9-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="951f9-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="951f9-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="951f9-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951f9-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="951f9-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="951f9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="951f9-117">DESCRIPTION</span></span>
<span data-ttu-id="951f9-118">O cmdlet **Add-AzKeyVaultKey** cria uma chave em um cofre de chave no Cofre de Teclas do Azure ou importa uma chave para um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="951f9-119">Use este cmdlet para adicionar teclas usando qualquer um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="951f9-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="951f9-120">Crie uma chave em um módulo de segurança de hardware (HSM) no serviço Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="951f9-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="951f9-121">Crie uma chave no software no serviço Cofre de Chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="951f9-122">Importe uma chave do seu próprio módulo de segurança de hardware (HSM) para HSMs no serviço Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="951f9-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="951f9-123">Importe uma chave de um arquivo .pfx no computador.</span><span class="sxs-lookup"><span data-stu-id="951f9-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="951f9-124">Importe uma chave de um arquivo .pfx em seu computador para módulos de segurança de hardware (HSMs) no serviço Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="951f9-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="951f9-125">Para qualquer uma dessas operações, você pode fornecer atributos principais ou aceitar configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="951f9-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="951f9-126">Se você criar ou importar uma chave com o mesmo nome de uma chave existente no seu cofre de chaves, a chave original será atualizada com os valores especificados para a nova chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="951f9-127">Você pode acessar os valores anteriores usando o URI específico de versão para essa versão da chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="951f9-128">Para saber mais sobre as principais versões e a estrutura do URI, consulte [Sobre](http://go.microsoft.com/fwlink/?linkid=518560) Chaves e Segredos na documentação da API REST do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="951f9-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="951f9-129">Observação: para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo .byok) usando o conjunto de ferramentas BYOK do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="951f9-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="951f9-130">Para obter mais informações, consulte Como gerar e transferir HSM-Protected chaves do Cofre de Teclas [do Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="951f9-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="951f9-131">Como prática ideal, fazer o back up da chave depois que ela for criada ou atualizada usando o cmdlet Backup-AzKeyVaultKey usuário.</span><span class="sxs-lookup"><span data-stu-id="951f9-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="951f9-132">Não há nenhuma funcionalidade de preenchimento indefinível, portanto, se você excluir acidentalmente sua chave ou excluí-la e mudar de ideia, a chave não será recuperável, a menos que você tenha um backup dela que possa restaurar.</span><span class="sxs-lookup"><span data-stu-id="951f9-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="951f9-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="951f9-133">EXAMPLES</span></span>

### <span data-ttu-id="951f9-134">Exemplo 1: Criar uma chave</span><span class="sxs-lookup"><span data-stu-id="951f9-134">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="951f9-135">Esse comando cria uma chave protegida por software chamada ITSoftware no cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="951f9-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="951f9-136">Exemplo 2: Criar uma chave protegida por HSM</span><span class="sxs-lookup"><span data-stu-id="951f9-136">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="951f9-137">Esse comando cria uma chave protegida por HSM no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="951f9-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="951f9-138">Exemplo 3: Criar uma chave com valores não padrão</span><span class="sxs-lookup"><span data-stu-id="951f9-138">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="951f9-139">O primeiro comando armazena os valores descriptografar e verificar na variável $KeyOperations dados.</span><span class="sxs-lookup"><span data-stu-id="951f9-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="951f9-140">O segundo comando cria um **objeto DateTime,** definido em UTC, usando o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="951f9-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="951f9-141">Esse objeto especifica um período de dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="951f9-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="951f9-142">O comando armazena essa data na variável $Expires dados.</span><span class="sxs-lookup"><span data-stu-id="951f9-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="951f9-143">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="951f9-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="951f9-144">O terceiro comando cria um **objeto DateTime** usando o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="951f9-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="951f9-145">Esse objeto especifica a hora UTC atual.</span><span class="sxs-lookup"><span data-stu-id="951f9-145">That object specifies current UTC time.</span></span> <span data-ttu-id="951f9-146">O comando armazena essa data na variável $NotBefore dados.</span><span class="sxs-lookup"><span data-stu-id="951f9-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="951f9-147">O comando final cria uma chave chamada ITHsmNonDefault que é uma chave protegida por HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="951f9-148">O comando especifica valores para operações de teclas permitidas armazenadas $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="951f9-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="951f9-149">O comando especifica horas para os *parâmetros Expires* e *NotBefore* criados nos comandos anteriores e marcas para alta gravidade e IT.</span><span class="sxs-lookup"><span data-stu-id="951f9-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="951f9-150">A nova chave está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="951f9-150">The new key is disabled.</span></span> <span data-ttu-id="951f9-151">Você pode habilita-lo usando **o cmdlet Set-AzKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="951f9-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="951f9-152">Exemplo 4: Importar uma chave protegida por HSM</span><span class="sxs-lookup"><span data-stu-id="951f9-152">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="951f9-153">Esse comando importa a chave chamada ITByok do local especificado pelo parâmetro *KeyFilePath.*</span><span class="sxs-lookup"><span data-stu-id="951f9-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="951f9-154">A chave importada é uma chave protegida por HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="951f9-155">Para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo .byok) usando o conjunto de ferramentas BYOK do Cofre de Chave do Azure.</span><span class="sxs-lookup"><span data-stu-id="951f9-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="951f9-156">Para obter mais informações, consulte Como gerar e transferir HSM-Protected chaves do Cofre de Teclas [do Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="951f9-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="951f9-157">Exemplo 5: importar uma chave protegida por software</span><span class="sxs-lookup"><span data-stu-id="951f9-157">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="951f9-158">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e, em seguida, armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="951f9-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="951f9-159">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="951f9-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="951f9-160">O segundo comando cria uma senha de software no cofre de teclas contoso.</span><span class="sxs-lookup"><span data-stu-id="951f9-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="951f9-161">O comando especifica o local da chave e a senha armazenadas no $Password.</span><span class="sxs-lookup"><span data-stu-id="951f9-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="951f9-162">Exemplo 6: importar uma chave e atribuir atributos</span><span class="sxs-lookup"><span data-stu-id="951f9-162">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="951f9-163">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e, em seguida, armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="951f9-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="951f9-164">O segundo comando cria um **objeto DateTime** usando o cmdlet **Get-Date** e armazena esse objeto na variável $Expires dados.</span><span class="sxs-lookup"><span data-stu-id="951f9-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="951f9-165">O terceiro comando cria a $tags variável para definir marcas para alta gravidade e IT.</span><span class="sxs-lookup"><span data-stu-id="951f9-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="951f9-166">O comando final importa uma chave como uma tecla HSM do local especificado.</span><span class="sxs-lookup"><span data-stu-id="951f9-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="951f9-167">O comando especifica o tempo de expiração armazenado no $Expires e a senha armazenadas no $Password e aplica as marcas armazenadas no $tags.</span><span class="sxs-lookup"><span data-stu-id="951f9-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="951f9-168">Exemplo 7: Gerar uma chave do exchange (KEK) para o recurso "traga sua própria chave" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="951f9-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="951f9-169">Gera uma chave (chamada de chave do exchange (KEK)).</span><span class="sxs-lookup"><span data-stu-id="951f9-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="951f9-170">O KEK deve ser uma chave RSA-HSM que tenha apenas a operação de chave de importação.</span><span class="sxs-lookup"><span data-stu-id="951f9-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="951f9-171">Somente a SKU Premium do Cofre de Teclas é compatível com as teclas RSA-HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="951f9-172">Para obter mais detalhes, consulte https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="951f9-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="951f9-173">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="951f9-173">PARAMETERS</span></span>

### <span data-ttu-id="951f9-174">-CurveName</span><span class="sxs-lookup"><span data-stu-id="951f9-174">-CurveName</span></span>
<span data-ttu-id="951f9-175">Especifica o nome da curva da criptografia de curva elíptica, esse valor é válido quando KeyType é EC.</span><span class="sxs-lookup"><span data-stu-id="951f9-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951f9-176">-DefaultProfile</span></span>
<span data-ttu-id="951f9-177">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="951f9-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="951f9-178">-Destino</span><span class="sxs-lookup"><span data-stu-id="951f9-178">-Destination</span></span>
<span data-ttu-id="951f9-179">Especifica se você deve adicionar a chave como uma chave protegida por software ou uma chave protegida por HSM no serviço do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="951f9-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="951f9-180">Os valores válidos são: HSM e Software.</span><span class="sxs-lookup"><span data-stu-id="951f9-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="951f9-181">Observação: para usar o HSM como seu destino, você deve ter um cofre de chave compatível com HSMs.</span><span class="sxs-lookup"><span data-stu-id="951f9-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="951f9-182">Para obter mais informações sobre os níveis de serviço e os recursos do Cofre de Teclas do Azure, consulte o site de preços do Cofre de Chave do [Azure.](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="951f9-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="951f9-183">Esse parâmetro é necessário quando você cria uma nova chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="951f9-184">Se você importar uma chave usando o parâmetro *KeyFilePath,* este parâmetro será opcional:</span><span class="sxs-lookup"><span data-stu-id="951f9-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="951f9-185">Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tenha a extensão de nome de arquivo .byok, ela será importada como uma chave protegida por HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="951f9-186">O cmdlet não pode importar essa chave como chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="951f9-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="951f9-187">Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tenha uma extensão de nome de arquivo .pfx, ele importa a chave como uma chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="951f9-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-188">-Desabilitar</span><span class="sxs-lookup"><span data-stu-id="951f9-188">-Disable</span></span>
<span data-ttu-id="951f9-189">Indica que a chave que você está adicionando está definida como um estado inicial de desabilitação.</span><span class="sxs-lookup"><span data-stu-id="951f9-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="951f9-190">Qualquer tentativa de uso da chave falhará.</span><span class="sxs-lookup"><span data-stu-id="951f9-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="951f9-191">Use este parâmetro se você estiver pré-carregar as teclas que pretende habilitar mais tarde.</span><span class="sxs-lookup"><span data-stu-id="951f9-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="951f9-192">-Expira</span><span class="sxs-lookup"><span data-stu-id="951f9-192">-Expires</span></span>
<span data-ttu-id="951f9-193">Especifica o tempo de expiração, como um objeto **DateTime,** para a chave que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="951f9-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="951f9-194">Este parâmetro usa o Tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="951f9-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="951f9-195">Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="951f9-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="951f9-196">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="951f9-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="951f9-197">Se você não especificar esse parâmetro, a chave não expirará.</span><span class="sxs-lookup"><span data-stu-id="951f9-197">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="951f9-198">-HsmName</span></span>
<span data-ttu-id="951f9-199">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-199">HSM name.</span></span> <span data-ttu-id="951f9-200">O Cmdlet construirá o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="951f9-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="951f9-201">-HsmObject</span></span>
<span data-ttu-id="951f9-202">Objeto HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="951f9-203">-HsmResourceId</span></span>
<span data-ttu-id="951f9-204">ID do recurso do HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="951f9-205">-InputObject</span></span>
<span data-ttu-id="951f9-206">Objeto do cofre.</span><span class="sxs-lookup"><span data-stu-id="951f9-206">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="951f9-207">-KeyFilePassword</span></span>
<span data-ttu-id="951f9-208">Especifica uma senha para o arquivo importado como um objeto **SecureString.**</span><span class="sxs-lookup"><span data-stu-id="951f9-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="951f9-209">Para obter um **objeto SecureString,** use o cmdlet **ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="951f9-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="951f9-210">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="951f9-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="951f9-211">Você deve especificar essa senha para importar um arquivo com uma extensão de nome de arquivo .pfx.</span><span class="sxs-lookup"><span data-stu-id="951f9-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-212">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="951f9-212">-KeyFilePath</span></span>
<span data-ttu-id="951f9-213">Especifica o caminho de um arquivo local que contém material-chave que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="951f9-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="951f9-214">As extensões de nome de arquivo válidas são .byok e .pfx.</span><span class="sxs-lookup"><span data-stu-id="951f9-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="951f9-215">Se o arquivo for um arquivo .byok, a chave será protegida automaticamente por HSMs após a importação e você não poderá substituir esse padrão.</span><span class="sxs-lookup"><span data-stu-id="951f9-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="951f9-216">Se o arquivo for um arquivo .pfx, a chave será protegida automaticamente pelo software após a importação.</span><span class="sxs-lookup"><span data-stu-id="951f9-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="951f9-217">Para substituir esse padrão, de definir *o* parâmetro Destino como HSM para que a chave seja protegida por HSM.</span><span class="sxs-lookup"><span data-stu-id="951f9-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="951f9-218">Quando você especifica esse parâmetro, o *parâmetro* Destino é opcional.</span><span class="sxs-lookup"><span data-stu-id="951f9-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="951f9-219">-KeyOps</span></span>
<span data-ttu-id="951f9-220">Especifica uma matriz de operações que pode ser executada usando a chave que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="951f9-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="951f9-221">Se você não especificar esse parâmetro, todas as operações poderão ser executadas.</span><span class="sxs-lookup"><span data-stu-id="951f9-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="951f9-222">Os valores aceitáveis para este parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela especificação [JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="951f9-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="951f9-223">Criptografar</span><span class="sxs-lookup"><span data-stu-id="951f9-223">encrypt</span></span>
- <span data-ttu-id="951f9-224">Descriptografar</span><span class="sxs-lookup"><span data-stu-id="951f9-224">decrypt</span></span>
- <span data-ttu-id="951f9-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="951f9-225">wrapKey</span></span>
- <span data-ttu-id="951f9-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="951f9-226">unwrapKey</span></span>
- <span data-ttu-id="951f9-227">Sinal</span><span class="sxs-lookup"><span data-stu-id="951f9-227">sign</span></span>
- <span data-ttu-id="951f9-228">Verificar</span><span class="sxs-lookup"><span data-stu-id="951f9-228">verify</span></span>
- <span data-ttu-id="951f9-229">importar (somente para KEK, consulte o exemplo 7)</span><span class="sxs-lookup"><span data-stu-id="951f9-229">import (for KEK only, see example 7)</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="951f9-230">-KeyType</span></span>
<span data-ttu-id="951f9-231">Especifica o tipo de chave dessa chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-231">Specifies the key type of this key.</span></span> <span data-ttu-id="951f9-232">Ao importar teclas BYOK, ela é padrão para 'RSA'.</span><span class="sxs-lookup"><span data-stu-id="951f9-232">When importing BYOK keys, it defaults to 'RSA'.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-233">-Nome</span><span class="sxs-lookup"><span data-stu-id="951f9-233">-Name</span></span>
<span data-ttu-id="951f9-234">Especifica o nome da chave a ser adicionar ao cofre de teclas.</span><span class="sxs-lookup"><span data-stu-id="951f9-234">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="951f9-235">Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome especificado por esse parâmetro, o nome do cofre de chave e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="951f9-235">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="951f9-236">O nome deve ser uma cadeia de caracteres de 1 a 63 caracteres com apenas 0 a 9, a-z, A-Z e - (o símbolo de traço).</span><span class="sxs-lookup"><span data-stu-id="951f9-236">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-237">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="951f9-237">-NotBefore</span></span>
<span data-ttu-id="951f9-238">Especifica a hora, como um objeto **DateTime,** antes do qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="951f9-238">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="951f9-239">Este parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="951f9-239">This parameter uses UTC.</span></span> <span data-ttu-id="951f9-240">Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="951f9-240">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="951f9-241">Se você não especificar esse parâmetro, a chave poderá ser usada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="951f9-241">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-242">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="951f9-242">-ResourceId</span></span>
<span data-ttu-id="951f9-243">ID do Recurso do Cofre.</span><span class="sxs-lookup"><span data-stu-id="951f9-243">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-244">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="951f9-244">-Size</span></span>
<span data-ttu-id="951f9-245">Tamanho da tecla RSA, em bits.</span><span class="sxs-lookup"><span data-stu-id="951f9-245">RSA key size, in bits.</span></span> <span data-ttu-id="951f9-246">Se não especificado, o serviço fornecerá um padrão seguro.</span><span class="sxs-lookup"><span data-stu-id="951f9-246">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-247">-Tag</span><span class="sxs-lookup"><span data-stu-id="951f9-247">-Tag</span></span>
<span data-ttu-id="951f9-248">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="951f9-248">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="951f9-249">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="951f9-249">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="951f9-250">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="951f9-250">-VaultName</span></span>
<span data-ttu-id="951f9-251">Especifica o nome do cofre de chave ao qual este cmdlet adiciona a chave.</span><span class="sxs-lookup"><span data-stu-id="951f9-251">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="951f9-252">Esse cmdlet construirá o FQDN de um cofre de teclas com base no nome especificado por esse parâmetro e no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="951f9-252">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="951f9-253">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="951f9-253">-Confirm</span></span>
<span data-ttu-id="951f9-254">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="951f9-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="951f9-255">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="951f9-255">-WhatIf</span></span>
<span data-ttu-id="951f9-256">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="951f9-256">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="951f9-257">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="951f9-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="951f9-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951f9-258">CommonParameters</span></span>
<span data-ttu-id="951f9-259">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="951f9-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951f9-260">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="951f9-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951f9-261">Entradas</span><span class="sxs-lookup"><span data-stu-id="951f9-261">INPUTS</span></span>

### <span data-ttu-id="951f9-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="951f9-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="951f9-263">System.String</span><span class="sxs-lookup"><span data-stu-id="951f9-263">System.String</span></span>

## <span data-ttu-id="951f9-264">Saídas</span><span class="sxs-lookup"><span data-stu-id="951f9-264">OUTPUTS</span></span>

### <span data-ttu-id="951f9-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="951f9-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="951f9-266">Notas</span><span class="sxs-lookup"><span data-stu-id="951f9-266">NOTES</span></span>

## <span data-ttu-id="951f9-267">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="951f9-267">RELATED LINKS</span></span>

[<span data-ttu-id="951f9-268">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="951f9-268">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="951f9-269">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="951f9-269">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="951f9-270">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="951f9-270">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="951f9-271">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="951f9-271">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
