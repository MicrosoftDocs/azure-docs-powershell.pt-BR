---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 153cd3099b750732e281992e98cdafb173a71276
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432121"
---
# <span data-ttu-id="470a5-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="470a5-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="470a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="470a5-102">SYNOPSIS</span></span>
<span data-ttu-id="470a5-103">Cria uma chave em um cofre de chaves ou importa uma chave para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="470a5-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="470a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="470a5-104">SYNTAX</span></span>

### <span data-ttu-id="470a5-105">InteractiveCreate (padrão)</span><span class="sxs-lookup"><span data-stu-id="470a5-105">InteractiveCreate (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="470a5-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="470a5-106">InteractiveImport</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="470a5-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="470a5-107">InputObjectCreate</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="470a5-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="470a5-108">InputObjectImport</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="470a5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="470a5-109">DESCRIPTION</span></span>
<span data-ttu-id="470a5-110">O cmdlet **Add-AzureKeyVaultKey** cria uma chave em um cofre de chaves do Azure Key Vault ou importa uma chave para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="470a5-110">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="470a5-111">Use esse cmdlet para adicionar chaves usando qualquer um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="470a5-111">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="470a5-112">Crie uma chave em um HSM (módulo de segurança de hardware) no serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="470a5-112">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="470a5-113">Crie uma chave no software no serviço de compartimentação de chave.</span><span class="sxs-lookup"><span data-stu-id="470a5-113">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="470a5-114">Importe uma chave do seu próprio HSM (módulo de segurança de hardware) para HSMs no serviço de compartimento de chave.</span><span class="sxs-lookup"><span data-stu-id="470a5-114">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="470a5-115">Importar uma chave de um arquivo. pfx em seu computador.</span><span class="sxs-lookup"><span data-stu-id="470a5-115">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="470a5-116">Importar uma chave de um arquivo. pfx no computador para módulos de segurança de hardware (HSMs) no serviço de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="470a5-116">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="470a5-117">Para qualquer uma dessas operações, você pode fornecer atributos de chave ou aceitar as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="470a5-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="470a5-118">Se você criar ou importar uma chave com o mesmo nome de uma chave existente em seu cofre de chaves, a chave original será atualizada com os valores que você especificar para a nova chave.</span><span class="sxs-lookup"><span data-stu-id="470a5-118">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="470a5-119">Você pode acessar os valores anteriores usando o URI específico da versão para essa versão da chave.</span><span class="sxs-lookup"><span data-stu-id="470a5-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="470a5-120">Para saber mais sobre as principais versões e a estrutura de URI, consulte [sobre as chaves andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) na documentação da API REST do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="470a5-120">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="470a5-121">Observação: para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="470a5-121">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="470a5-122">Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="470a5-122">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="470a5-123">Como prática recomendada, faça backup da chave após criá-la ou atualizá-la usando o cmdlet Backup-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="470a5-123">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="470a5-124">Não há nenhuma funcionalidade de cantais exclusões, portanto, se você excluir acidentalmente a chave ou excluí-la e, em seguida, mudar de ideia, a chave não será recuperável, a menos que você tenha um backup dela que possa restaurar.</span><span class="sxs-lookup"><span data-stu-id="470a5-124">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="470a5-125">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="470a5-125">EXAMPLES</span></span>

### <span data-ttu-id="470a5-126">Exemplo 1: criar uma chave</span><span class="sxs-lookup"><span data-stu-id="470a5-126">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="470a5-127">Esse comando cria uma chave protegida por software chamada ITSoftware no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="470a5-127">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="470a5-128">Exemplo 2: criar uma chave protegida pelo HSM</span><span class="sxs-lookup"><span data-stu-id="470a5-128">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="470a5-129">Esse comando cria uma chave protegida pelo HSM no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="470a5-129">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="470a5-130">Exemplo 3: criar uma chave com valores não padrão</span><span class="sxs-lookup"><span data-stu-id="470a5-130">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="470a5-131">O primeiro comando armazena os valores decodificar e verificar na variável $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="470a5-131">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="470a5-132">O segundo comando cria um objeto **DateTime** , definido em UTC, usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="470a5-132">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="470a5-133">Esse objeto especifica um tempo dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="470a5-133">That object specifies a time two years in the future.</span></span> <span data-ttu-id="470a5-134">O comando armazena essa data na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="470a5-134">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="470a5-135">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="470a5-135">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="470a5-136">O terceiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="470a5-136">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="470a5-137">Esse objeto especifica a hora UTC atual.</span><span class="sxs-lookup"><span data-stu-id="470a5-137">That object specifies current UTC time.</span></span> <span data-ttu-id="470a5-138">O comando armazena essa data na variável $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="470a5-138">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="470a5-139">O comando final cria uma chave chamada ITHsmNonDefault que é uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="470a5-139">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="470a5-140">O comando especifica valores para operações de chave permitidas armazenadas $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="470a5-140">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="470a5-141">O comando especifica os horários dos parâmetros *expire* e não *antes* de serem criados nos comandos anteriores e marca para alta severidade e.</span><span class="sxs-lookup"><span data-stu-id="470a5-141">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="470a5-142">A nova chave está desativada.</span><span class="sxs-lookup"><span data-stu-id="470a5-142">The new key is disabled.</span></span> <span data-ttu-id="470a5-143">Você pode habilitá-lo usando o cmdlet **set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="470a5-143">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="470a5-144">Exemplo 4: importar uma chave protegida pelo HSM</span><span class="sxs-lookup"><span data-stu-id="470a5-144">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="470a5-145">Esse comando importa a chave chamada ITByok do local que o parâmetro *keyFilePath* especifica.</span><span class="sxs-lookup"><span data-stu-id="470a5-145">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="470a5-146">A chave importada é uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="470a5-146">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="470a5-147">Para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="470a5-147">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="470a5-148">Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="470a5-148">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="470a5-149">Exemplo 5: importar uma chave protegida por software</span><span class="sxs-lookup"><span data-stu-id="470a5-149">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="470a5-150">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="470a5-150">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="470a5-151">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="470a5-151">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="470a5-152">O segundo comando cria uma senha de software no cofre de chaves da contoso.</span><span class="sxs-lookup"><span data-stu-id="470a5-152">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="470a5-153">O comando especifica o local para a chave e a senha armazenadas em $Password.</span><span class="sxs-lookup"><span data-stu-id="470a5-153">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="470a5-154">Exemplo 6: importar uma chave e atribuir atributos</span><span class="sxs-lookup"><span data-stu-id="470a5-154">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="470a5-155">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="470a5-155">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="470a5-156">O segundo comando cria um objeto **DateTime** usando o cmdlet **Get-Date** e armazena esse objeto na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="470a5-156">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="470a5-157">O terceiro comando cria a variável $tags para definir marcas para alta severidade e para isso.</span><span class="sxs-lookup"><span data-stu-id="470a5-157">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="470a5-158">O comando final importa uma chave como uma chave HSM do local especificado.</span><span class="sxs-lookup"><span data-stu-id="470a5-158">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="470a5-159">O comando especifica o tempo de expiração armazenado no $Expires e a senha armazenados $Password e aplica as marcas armazenadas em $tags.</span><span class="sxs-lookup"><span data-stu-id="470a5-159">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="470a5-160">OS</span><span class="sxs-lookup"><span data-stu-id="470a5-160">PARAMETERS</span></span>

### <span data-ttu-id="470a5-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470a5-161">-DefaultProfile</span></span>
<span data-ttu-id="470a5-162">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="470a5-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-163">-Destino</span><span class="sxs-lookup"><span data-stu-id="470a5-163">-Destination</span></span>
<span data-ttu-id="470a5-164">Especifica se a chave deve ser adicionada como uma chave protegida por software ou uma chave protegida pelo HSM no serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="470a5-164">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="470a5-165">Os valores válidos são: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="470a5-165">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="470a5-166">Observação: para usar o HSM como destino, você deve ter um cofre de chaves com suporte para HSMs.</span><span class="sxs-lookup"><span data-stu-id="470a5-166">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="470a5-167">Para obter mais informações sobre os níveis de serviço e os recursos do cofre de chaves do Azure, consulte o [site de preços do Azure Key Vault](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="470a5-167">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="470a5-168">Esse parâmetro é necessário quando você cria uma nova chave.</span><span class="sxs-lookup"><span data-stu-id="470a5-168">This parameter is required when you create a new key.</span></span> <span data-ttu-id="470a5-169">Se você importar uma chave usando o parâmetro *keyFilePath* , esse parâmetro será opcional:</span><span class="sxs-lookup"><span data-stu-id="470a5-169">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="470a5-170">Se você não especificar esse parâmetro, e esse cmdlet importar uma chave que tenha extensão de nome de arquivo. byok, ele importa essa chave como uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="470a5-170">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="470a5-171">O cmdlet não pode importar essa chave como chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="470a5-171">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="470a5-172">Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tem uma extensão de nome de arquivo. pfx, ele importa a chave como uma chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="470a5-172">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InputObjectCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-173">-Disable</span><span class="sxs-lookup"><span data-stu-id="470a5-173">-Disable</span></span>
<span data-ttu-id="470a5-174">Indica que a chave que você está adicionando está definida como um estado inicial de desabilitado.</span><span class="sxs-lookup"><span data-stu-id="470a5-174">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="470a5-175">Qualquer tentativa de usar a chave irá falhar.</span><span class="sxs-lookup"><span data-stu-id="470a5-175">Any attempt to use the key will fail.</span></span> <span data-ttu-id="470a5-176">Use esse parâmetro se você estiver precarregando chaves que pretende habilitar mais tarde.</span><span class="sxs-lookup"><span data-stu-id="470a5-176">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-177">-Expira em</span><span class="sxs-lookup"><span data-stu-id="470a5-177">-Expires</span></span>
<span data-ttu-id="470a5-178">Especifica o tempo de expiração, como um objeto **DateTime** , para a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="470a5-178">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="470a5-179">Esse parâmetro usa o tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="470a5-179">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="470a5-180">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="470a5-180">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="470a5-181">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="470a5-181">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="470a5-182">Se você não especificar esse parâmetro, a chave não expira.</span><span class="sxs-lookup"><span data-stu-id="470a5-182">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-183">-InputObject</span><span class="sxs-lookup"><span data-stu-id="470a5-183">-InputObject</span></span>
<span data-ttu-id="470a5-184">Objeto do cofre.</span><span class="sxs-lookup"><span data-stu-id="470a5-184">Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-185">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="470a5-185">-KeyFilePassword</span></span>
<span data-ttu-id="470a5-186">Especifica uma senha para o arquivo importado como um objeto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="470a5-186">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="470a5-187">Para obter um objeto **SecureString** , use o cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="470a5-187">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="470a5-188">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="470a5-188">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="470a5-189">Você deve especificar essa senha para importar um arquivo com uma extensão de nome de arquivo. pfx.</span><span class="sxs-lookup"><span data-stu-id="470a5-189">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-190">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="470a5-190">-KeyFilePath</span></span>
<span data-ttu-id="470a5-191">Especifica o caminho de um arquivo local que contém o material da chave que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="470a5-191">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="470a5-192">As extensões de nome de arquivo válidas são. byok e. pfx.</span><span class="sxs-lookup"><span data-stu-id="470a5-192">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="470a5-193">Se o arquivo for um arquivo. byok, a chave será automaticamente protegida por HSMs após a importação, e você não poderá substituir esse padrão.</span><span class="sxs-lookup"><span data-stu-id="470a5-193">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="470a5-194">Se o arquivo for um arquivo. pfx, a chave será automaticamente protegida pelo software após a importação.</span><span class="sxs-lookup"><span data-stu-id="470a5-194">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="470a5-195">Para substituir esse padrão, defina o parâmetro *Destination* como HSM para que a chave seja protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="470a5-195">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="470a5-196">Quando você especifica esse parâmetro, o parâmetro *Destination* é opcional.</span><span class="sxs-lookup"><span data-stu-id="470a5-196">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveImport, InputObjectImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-197">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="470a5-197">-KeyOps</span></span>
<span data-ttu-id="470a5-198">Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="470a5-198">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="470a5-199">Se você não especificar esse parâmetro, todas as operações poderão ser executadas.</span><span class="sxs-lookup"><span data-stu-id="470a5-199">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="470a5-200">Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela [especificação JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="470a5-200">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="470a5-201">Com</span><span class="sxs-lookup"><span data-stu-id="470a5-201">Encrypt</span></span>
- <span data-ttu-id="470a5-202">Criptografá</span><span class="sxs-lookup"><span data-stu-id="470a5-202">Decrypt</span></span>
- <span data-ttu-id="470a5-203">Quebrada</span><span class="sxs-lookup"><span data-stu-id="470a5-203">Wrap</span></span>
- <span data-ttu-id="470a5-204">Desenvolva</span><span class="sxs-lookup"><span data-stu-id="470a5-204">Unwrap</span></span>
- <span data-ttu-id="470a5-205">Designa</span><span class="sxs-lookup"><span data-stu-id="470a5-205">Sign</span></span>
- <span data-ttu-id="470a5-206">Verificar</span><span class="sxs-lookup"><span data-stu-id="470a5-206">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-207">-Nome</span><span class="sxs-lookup"><span data-stu-id="470a5-207">-Name</span></span>
<span data-ttu-id="470a5-208">Especifica o nome da chave a ser adicionada ao cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="470a5-208">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="470a5-209">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="470a5-209">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="470a5-210">O nome deve ser uma cadeia de caracteres de 1 a 63 caracteres com tamanho que contenha apenas 0-9, a-z, A-Z e-(o símbolo de traço).</span><span class="sxs-lookup"><span data-stu-id="470a5-210">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-211">-Não antes</span><span class="sxs-lookup"><span data-stu-id="470a5-211">-NotBefore</span></span>
<span data-ttu-id="470a5-212">Especifica o tempo, como um objeto **DateTime** , antes do qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="470a5-212">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="470a5-213">Esse parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="470a5-213">This parameter uses UTC.</span></span> <span data-ttu-id="470a5-214">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="470a5-214">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="470a5-215">Se você não especificar esse parâmetro, a chave pode ser usada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="470a5-215">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-216">-Marca</span><span class="sxs-lookup"><span data-stu-id="470a5-216">-Tag</span></span>
<span data-ttu-id="470a5-217">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="470a5-217">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="470a5-218">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="470a5-218">For example:</span></span>

<span data-ttu-id="470a5-219">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="470a5-219">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-220">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="470a5-220">-VaultName</span></span>
<span data-ttu-id="470a5-221">Especifica o nome do cofre de chaves para o qual esse cmdlet adiciona a chave.</span><span class="sxs-lookup"><span data-stu-id="470a5-221">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="470a5-222">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="470a5-222">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-223">-Confirme</span><span class="sxs-lookup"><span data-stu-id="470a5-223">-Confirm</span></span>
<span data-ttu-id="470a5-224">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="470a5-224">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="470a5-225">-WhatIf</span></span>
<span data-ttu-id="470a5-226">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="470a5-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="470a5-227">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="470a5-227">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470a5-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470a5-228">CommonParameters</span></span>
<span data-ttu-id="470a5-229">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470a5-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470a5-230">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470a5-230">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470a5-231">SENSORES</span><span class="sxs-lookup"><span data-stu-id="470a5-231">INPUTS</span></span>

### <span data-ttu-id="470a5-232">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="470a5-232">None</span></span>
<span data-ttu-id="470a5-233">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="470a5-233">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="470a5-234">EXIBE</span><span class="sxs-lookup"><span data-stu-id="470a5-234">OUTPUTS</span></span>

### <span data-ttu-id="470a5-235">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="470a5-235">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="470a5-236">INFORMA</span><span class="sxs-lookup"><span data-stu-id="470a5-236">NOTES</span></span>

## <span data-ttu-id="470a5-237">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="470a5-237">RELATED LINKS</span></span>

[<span data-ttu-id="470a5-238">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="470a5-238">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="470a5-239">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="470a5-239">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="470a5-240">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="470a5-240">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="470a5-241">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="470a5-241">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
