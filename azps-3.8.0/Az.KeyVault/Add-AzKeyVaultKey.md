---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: d0f26dda6e5fd79f20713dff61ed299a995d6fd3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778248"
---
# <span data-ttu-id="b2651-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2651-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="b2651-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2651-102">SYNOPSIS</span></span>
<span data-ttu-id="b2651-103">Cria uma chave em um cofre de chaves ou importa uma chave para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b2651-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="b2651-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2651-104">SYNTAX</span></span>

### <span data-ttu-id="b2651-105">InteractiveCreate (padrão)</span><span class="sxs-lookup"><span data-stu-id="b2651-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2651-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="b2651-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2651-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="b2651-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2651-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="b2651-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2651-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="b2651-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2651-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="b2651-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2651-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2651-111">DESCRIPTION</span></span>
<span data-ttu-id="b2651-112">O cmdlet **Add-AzKeyVaultKey** cria uma chave em um cofre de chaves do Azure Key Vault ou importa uma chave para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b2651-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="b2651-113">Use esse cmdlet para adicionar chaves usando qualquer um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="b2651-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="b2651-114">Crie uma chave em um HSM (módulo de segurança de hardware) no serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b2651-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="b2651-115">Crie uma chave no software no serviço de compartimentação de chave.</span><span class="sxs-lookup"><span data-stu-id="b2651-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="b2651-116">Importe uma chave do seu próprio HSM (módulo de segurança de hardware) para HSMs no serviço de compartimento de chave.</span><span class="sxs-lookup"><span data-stu-id="b2651-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="b2651-117">Importar uma chave de um arquivo. pfx em seu computador.</span><span class="sxs-lookup"><span data-stu-id="b2651-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="b2651-118">Importar uma chave de um arquivo. pfx no computador para módulos de segurança de hardware (HSMs) no serviço de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b2651-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="b2651-119">Para qualquer uma dessas operações, você pode fornecer atributos de chave ou aceitar as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="b2651-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="b2651-120">Se você criar ou importar uma chave com o mesmo nome de uma chave existente em seu cofre de chaves, a chave original será atualizada com os valores que você especificar para a nova chave.</span><span class="sxs-lookup"><span data-stu-id="b2651-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="b2651-121">Você pode acessar os valores anteriores usando o URI específico da versão para essa versão da chave.</span><span class="sxs-lookup"><span data-stu-id="b2651-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="b2651-122">Para saber mais sobre as principais versões e a estrutura de URI, consulte [sobre chaves e segredos](http://go.microsoft.com/fwlink/?linkid=518560) na documentação da API REST do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b2651-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="b2651-123">Observação: para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="b2651-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="b2651-124">Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="b2651-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="b2651-125">Como prática recomendada, faça backup da chave após criá-la ou atualizá-la usando o cmdlet Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="b2651-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="b2651-126">Não há nenhuma funcionalidade de cantais exclusões, portanto, se você excluir acidentalmente a chave ou excluí-la e, em seguida, mudar de ideia, a chave não será recuperável, a menos que você tenha um backup dela que possa restaurar.</span><span class="sxs-lookup"><span data-stu-id="b2651-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="b2651-127">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2651-127">EXAMPLES</span></span>

### <span data-ttu-id="b2651-128">Exemplo 1: criar uma chave</span><span class="sxs-lookup"><span data-stu-id="b2651-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="b2651-129">Esse comando cria uma chave protegida por software chamada ITSoftware no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="b2651-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="b2651-130">Exemplo 2: criar uma chave protegida pelo HSM</span><span class="sxs-lookup"><span data-stu-id="b2651-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="b2651-131">Esse comando cria uma chave protegida pelo HSM no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="b2651-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="b2651-132">Exemplo 3: criar uma chave com valores não padrão</span><span class="sxs-lookup"><span data-stu-id="b2651-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="b2651-133">O primeiro comando armazena os valores decodificar e verificar na variável $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="b2651-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="b2651-134">O segundo comando cria um objeto **DateTime** , definido em UTC, usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="b2651-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="b2651-135">Esse objeto especifica um tempo dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="b2651-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="b2651-136">O comando armazena essa data na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="b2651-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="b2651-137">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b2651-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b2651-138">O terceiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="b2651-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b2651-139">Esse objeto especifica a hora UTC atual.</span><span class="sxs-lookup"><span data-stu-id="b2651-139">That object specifies current UTC time.</span></span> <span data-ttu-id="b2651-140">O comando armazena essa data na variável $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="b2651-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="b2651-141">O comando final cria uma chave chamada ITHsmNonDefault que é uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="b2651-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="b2651-142">O comando especifica valores para operações de chave permitidas armazenadas $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="b2651-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="b2651-143">O comando especifica os horários dos parâmetros *expire* e não *antes* de serem criados nos comandos anteriores e marca para alta severidade e.</span><span class="sxs-lookup"><span data-stu-id="b2651-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="b2651-144">A nova chave está desativada.</span><span class="sxs-lookup"><span data-stu-id="b2651-144">The new key is disabled.</span></span> <span data-ttu-id="b2651-145">Você pode habilitá-lo usando o cmdlet **set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="b2651-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="b2651-146">Exemplo 4: importar uma chave protegida pelo HSM</span><span class="sxs-lookup"><span data-stu-id="b2651-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="b2651-147">Esse comando importa a chave chamada ITByok do local que o parâmetro *keyFilePath* especifica.</span><span class="sxs-lookup"><span data-stu-id="b2651-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="b2651-148">A chave importada é uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="b2651-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="b2651-149">Para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="b2651-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="b2651-150">Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="b2651-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="b2651-151">Exemplo 5: importar uma chave protegida por software</span><span class="sxs-lookup"><span data-stu-id="b2651-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="b2651-152">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="b2651-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="b2651-153">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="b2651-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="b2651-154">O segundo comando cria uma senha de software no cofre de chaves da contoso.</span><span class="sxs-lookup"><span data-stu-id="b2651-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="b2651-155">O comando especifica o local para a chave e a senha armazenadas em $Password.</span><span class="sxs-lookup"><span data-stu-id="b2651-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="b2651-156">Exemplo 6: importar uma chave e atribuir atributos</span><span class="sxs-lookup"><span data-stu-id="b2651-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="b2651-157">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="b2651-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="b2651-158">O segundo comando cria um objeto **DateTime** usando o cmdlet **Get-Date** e armazena esse objeto na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="b2651-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="b2651-159">O terceiro comando cria a variável $tags para definir marcas para alta severidade e para isso.</span><span class="sxs-lookup"><span data-stu-id="b2651-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="b2651-160">O comando final importa uma chave como uma chave HSM do local especificado.</span><span class="sxs-lookup"><span data-stu-id="b2651-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="b2651-161">O comando especifica o tempo de expiração armazenado no $Expires e a senha armazenados $Password e aplica as marcas armazenadas em $tags.</span><span class="sxs-lookup"><span data-stu-id="b2651-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="b2651-162">OS</span><span class="sxs-lookup"><span data-stu-id="b2651-162">PARAMETERS</span></span>

### <span data-ttu-id="b2651-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2651-163">-DefaultProfile</span></span>
<span data-ttu-id="b2651-164">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b2651-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2651-165">-Destino</span><span class="sxs-lookup"><span data-stu-id="b2651-165">-Destination</span></span>
<span data-ttu-id="b2651-166">Especifica se a chave deve ser adicionada como uma chave protegida por software ou uma chave protegida pelo HSM no serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b2651-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="b2651-167">Os valores válidos são: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="b2651-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="b2651-168">Observação: para usar o HSM como destino, você deve ter um cofre de chaves com suporte para HSMs.</span><span class="sxs-lookup"><span data-stu-id="b2651-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="b2651-169">Para obter mais informações sobre os níveis de serviço e os recursos do cofre de chaves do Azure, consulte o [site de preços do Azure Key Vault](http://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="b2651-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="b2651-170">Esse parâmetro é necessário quando você cria uma nova chave.</span><span class="sxs-lookup"><span data-stu-id="b2651-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="b2651-171">Se você importar uma chave usando o parâmetro *keyFilePath* , esse parâmetro será opcional:</span><span class="sxs-lookup"><span data-stu-id="b2651-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="b2651-172">Se você não especificar esse parâmetro, e esse cmdlet importar uma chave que tenha extensão de nome de arquivo. byok, ele importa essa chave como uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="b2651-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="b2651-173">O cmdlet não pode importar essa chave como chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="b2651-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="b2651-174">Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tem uma extensão de nome de arquivo. pfx, ele importa a chave como uma chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="b2651-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="b2651-175">-Disable</span><span class="sxs-lookup"><span data-stu-id="b2651-175">-Disable</span></span>
<span data-ttu-id="b2651-176">Indica que a chave que você está adicionando está definida como um estado inicial de desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b2651-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="b2651-177">Qualquer tentativa de usar a chave irá falhar.</span><span class="sxs-lookup"><span data-stu-id="b2651-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="b2651-178">Use esse parâmetro se você estiver precarregando chaves que pretende habilitar mais tarde.</span><span class="sxs-lookup"><span data-stu-id="b2651-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="b2651-179">-Expira em</span><span class="sxs-lookup"><span data-stu-id="b2651-179">-Expires</span></span>
<span data-ttu-id="b2651-180">Especifica o tempo de expiração, como um objeto **DateTime** , para a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="b2651-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="b2651-181">Esse parâmetro usa o tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="b2651-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="b2651-182">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="b2651-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b2651-183">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b2651-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="b2651-184">Se você não especificar esse parâmetro, a chave não expira.</span><span class="sxs-lookup"><span data-stu-id="b2651-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="b2651-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2651-185">-InputObject</span></span>
<span data-ttu-id="b2651-186">Objeto do cofre.</span><span class="sxs-lookup"><span data-stu-id="b2651-186">Vault object.</span></span>

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

### <span data-ttu-id="b2651-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="b2651-187">-KeyFilePassword</span></span>
<span data-ttu-id="b2651-188">Especifica uma senha para o arquivo importado como um objeto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="b2651-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="b2651-189">Para obter um objeto **SecureString** , use o cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="b2651-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="b2651-190">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="b2651-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="b2651-191">Você deve especificar essa senha para importar um arquivo com uma extensão de nome de arquivo. pfx.</span><span class="sxs-lookup"><span data-stu-id="b2651-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2651-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="b2651-192">-KeyFilePath</span></span>
<span data-ttu-id="b2651-193">Especifica o caminho de um arquivo local que contém o material da chave que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="b2651-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="b2651-194">As extensões de nome de arquivo válidas são. byok e. pfx.</span><span class="sxs-lookup"><span data-stu-id="b2651-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="b2651-195">Se o arquivo for um arquivo. byok, a chave será automaticamente protegida por HSMs após a importação, e você não poderá substituir esse padrão.</span><span class="sxs-lookup"><span data-stu-id="b2651-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="b2651-196">Se o arquivo for um arquivo. pfx, a chave será automaticamente protegida pelo software após a importação.</span><span class="sxs-lookup"><span data-stu-id="b2651-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="b2651-197">Para substituir esse padrão, defina o parâmetro *Destination* como HSM para que a chave seja protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="b2651-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="b2651-198">Quando você especifica esse parâmetro, o parâmetro *Destination* é opcional.</span><span class="sxs-lookup"><span data-stu-id="b2651-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2651-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="b2651-199">-KeyOps</span></span>
<span data-ttu-id="b2651-200">Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="b2651-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="b2651-201">Se você não especificar esse parâmetro, todas as operações poderão ser executadas.</span><span class="sxs-lookup"><span data-stu-id="b2651-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="b2651-202">Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela [especificação JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="b2651-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="b2651-203">Com</span><span class="sxs-lookup"><span data-stu-id="b2651-203">Encrypt</span></span>
- <span data-ttu-id="b2651-204">Criptografá</span><span class="sxs-lookup"><span data-stu-id="b2651-204">Decrypt</span></span>
- <span data-ttu-id="b2651-205">Quebrada</span><span class="sxs-lookup"><span data-stu-id="b2651-205">Wrap</span></span>
- <span data-ttu-id="b2651-206">Desenvolva</span><span class="sxs-lookup"><span data-stu-id="b2651-206">Unwrap</span></span>
- <span data-ttu-id="b2651-207">Designa</span><span class="sxs-lookup"><span data-stu-id="b2651-207">Sign</span></span>
- <span data-ttu-id="b2651-208">Verificar</span><span class="sxs-lookup"><span data-stu-id="b2651-208">Verify</span></span>

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

### <span data-ttu-id="b2651-209">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2651-209">-Name</span></span>
<span data-ttu-id="b2651-210">Especifica o nome da chave a ser adicionada ao cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b2651-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="b2651-211">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="b2651-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="b2651-212">O nome deve ser uma cadeia de caracteres de 1 a 63 caracteres com tamanho que contenha apenas 0-9, a-z, A-Z e-(o símbolo de traço).</span><span class="sxs-lookup"><span data-stu-id="b2651-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="b2651-213">-Não antes</span><span class="sxs-lookup"><span data-stu-id="b2651-213">-NotBefore</span></span>
<span data-ttu-id="b2651-214">Especifica o tempo, como um objeto **DateTime** , antes do qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="b2651-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="b2651-215">Esse parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="b2651-215">This parameter uses UTC.</span></span> <span data-ttu-id="b2651-216">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="b2651-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b2651-217">Se você não especificar esse parâmetro, a chave pode ser usada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b2651-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="b2651-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2651-218">-ResourceId</span></span>
<span data-ttu-id="b2651-219">ID do recurso do cofre.</span><span class="sxs-lookup"><span data-stu-id="b2651-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="b2651-220">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="b2651-220">-Size</span></span>
<span data-ttu-id="b2651-221">Tamanho da chave RSA, em bits.</span><span class="sxs-lookup"><span data-stu-id="b2651-221">RSA key size, in bits.</span></span> <span data-ttu-id="b2651-222">Se não for especificado, o serviço fornecerá um padrão seguro.</span><span class="sxs-lookup"><span data-stu-id="b2651-222">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2651-223">-Marca</span><span class="sxs-lookup"><span data-stu-id="b2651-223">-Tag</span></span>
<span data-ttu-id="b2651-224">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b2651-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b2651-225">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b2651-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b2651-226">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="b2651-226">-VaultName</span></span>
<span data-ttu-id="b2651-227">Especifica o nome do cofre de chaves para o qual esse cmdlet adiciona a chave.</span><span class="sxs-lookup"><span data-stu-id="b2651-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="b2651-228">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="b2651-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="b2651-229">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b2651-229">-Confirm</span></span>
<span data-ttu-id="b2651-230">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2651-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2651-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2651-231">-WhatIf</span></span>
<span data-ttu-id="b2651-232">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b2651-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2651-233">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2651-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2651-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2651-234">CommonParameters</span></span>
<span data-ttu-id="b2651-235">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2651-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2651-236">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2651-236">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2651-237">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2651-237">INPUTS</span></span>

### <span data-ttu-id="b2651-238">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b2651-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b2651-239">System. String</span><span class="sxs-lookup"><span data-stu-id="b2651-239">System.String</span></span>

## <span data-ttu-id="b2651-240">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2651-240">OUTPUTS</span></span>

### <span data-ttu-id="b2651-241">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2651-241">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b2651-242">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2651-242">NOTES</span></span>

## <span data-ttu-id="b2651-243">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2651-243">RELATED LINKS</span></span>

[<span data-ttu-id="b2651-244">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2651-244">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="b2651-245">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2651-245">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="b2651-246">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b2651-246">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="b2651-247">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="b2651-247">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
