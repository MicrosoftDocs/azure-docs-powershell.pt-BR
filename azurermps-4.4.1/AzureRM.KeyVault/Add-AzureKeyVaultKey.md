---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://go.microsoft.com/fwlink/?LinkId=690295
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 0046a1ed2b2580d1cafbdaa31d9fad53a09ea644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441553"
---
# <span data-ttu-id="613a2-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="613a2-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="613a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="613a2-102">SYNOPSIS</span></span>
<span data-ttu-id="613a2-103">Cria uma chave em um cofre de chaves ou importa uma chave para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="613a2-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="613a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="613a2-104">SYNTAX</span></span>

### <span data-ttu-id="613a2-105">Criar (padrão)</span><span class="sxs-lookup"><span data-stu-id="613a2-105">Create (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="613a2-106">Importações</span><span class="sxs-lookup"><span data-stu-id="613a2-106">Import</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="613a2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="613a2-107">DESCRIPTION</span></span>
<span data-ttu-id="613a2-108">O cmdlet **Add-AzureKeyVaultKey** cria uma chave em um cofre de chaves do Azure Key Vault ou importa uma chave para um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="613a2-108">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="613a2-109">Use esse cmdlet para adicionar chaves usando qualquer um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="613a2-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="613a2-110">Crie uma chave em um HSM (módulo de segurança de hardware) no serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="613a2-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="613a2-111">Crie uma chave no software no serviço de compartimentação de chave.</span><span class="sxs-lookup"><span data-stu-id="613a2-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="613a2-112">Importe uma chave do seu próprio HSM (módulo de segurança de hardware) para HSMs no serviço de compartimento de chave.</span><span class="sxs-lookup"><span data-stu-id="613a2-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="613a2-113">Importar uma chave de um arquivo. pfx em seu computador.</span><span class="sxs-lookup"><span data-stu-id="613a2-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="613a2-114">Importar uma chave de um arquivo. pfx no computador para módulos de segurança de hardware (HSMs) no serviço de cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="613a2-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="613a2-115">Para qualquer uma dessas operações, você pode fornecer atributos de chave ou aceitar as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="613a2-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="613a2-116">Se você criar ou importar uma chave com o mesmo nome de uma chave existente em seu cofre de chaves, a chave original será atualizada com os valores que você especificar para a nova chave.</span><span class="sxs-lookup"><span data-stu-id="613a2-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="613a2-117">Você pode acessar os valores anteriores usando o URI específico da versão para essa versão da chave.</span><span class="sxs-lookup"><span data-stu-id="613a2-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="613a2-118">Para saber mais sobre as principais versões e a estrutura de URI, consulte [sobre as chaves andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) na documentação da API REST do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="613a2-118">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="613a2-119">Observação: para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="613a2-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="613a2-120">Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="613a2-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="613a2-121">Como prática recomendada, faça backup da chave após criá-la ou atualizá-la usando o cmdlet Backup-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="613a2-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="613a2-122">Não há nenhuma funcionalidade de cantais exclusões, portanto, se você excluir acidentalmente a chave ou excluí-la e, em seguida, mudar de ideia, a chave não será recuperável, a menos que você tenha um backup dela que possa restaurar.</span><span class="sxs-lookup"><span data-stu-id="613a2-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="613a2-123">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="613a2-123">EXAMPLES</span></span>

### <span data-ttu-id="613a2-124">Exemplo 1: criar uma chave</span><span class="sxs-lookup"><span data-stu-id="613a2-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="613a2-125">Esse comando cria uma chave protegida por software chamada ITSoftware no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="613a2-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="613a2-126">Exemplo 2: criar uma chave protegida pelo HSM</span><span class="sxs-lookup"><span data-stu-id="613a2-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="613a2-127">Esse comando cria uma chave protegida pelo HSM no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="613a2-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="613a2-128">Exemplo 3: criar uma chave com valores não padrão</span><span class="sxs-lookup"><span data-stu-id="613a2-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="613a2-129">O primeiro comando armazena os valores decodificar e verificar na variável $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="613a2-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="613a2-130">O segundo comando cria um objeto **DateTime** , definido em UTC, usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="613a2-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="613a2-131">Esse objeto especifica um tempo dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="613a2-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="613a2-132">O comando armazena essa data na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="613a2-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="613a2-133">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="613a2-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="613a2-134">O terceiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="613a2-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="613a2-135">Esse objeto especifica a hora UTC atual.</span><span class="sxs-lookup"><span data-stu-id="613a2-135">That object specifies current UTC time.</span></span> <span data-ttu-id="613a2-136">O comando armazena essa data na variável $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="613a2-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="613a2-137">O comando final cria uma chave chamada ITHsmNonDefault que é uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="613a2-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="613a2-138">O comando especifica valores para operações de chave permitidas armazenadas $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="613a2-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="613a2-139">O comando especifica os horários dos parâmetros *expire* e não *antes* de serem criados nos comandos anteriores e marca para alta severidade e.</span><span class="sxs-lookup"><span data-stu-id="613a2-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="613a2-140">A nova chave está desativada.</span><span class="sxs-lookup"><span data-stu-id="613a2-140">The new key is disabled.</span></span> <span data-ttu-id="613a2-141">Você pode habilitá-lo usando o cmdlet **set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="613a2-141">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="613a2-142">Exemplo 4: importar uma chave protegida pelo HSM</span><span class="sxs-lookup"><span data-stu-id="613a2-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="613a2-143">Esse comando importa a chave chamada ITByok do local que o parâmetro *keyFilePath* especifica.</span><span class="sxs-lookup"><span data-stu-id="613a2-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="613a2-144">A chave importada é uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="613a2-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="613a2-145">Para importar uma chave do seu próprio módulo de segurança de hardware, primeiro você deve gerar um pacote BYOK (um arquivo com uma extensão de nome de arquivo. BYOK) usando o conjunto de ferramentas do Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="613a2-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="613a2-146">Para obter mais informações, consulte [como gerar e transferir chaves do HSM-Protected para o cofre de chaves do Azure](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="613a2-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="613a2-147">Exemplo 5: importar uma chave protegida por software</span><span class="sxs-lookup"><span data-stu-id="613a2-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="613a2-148">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="613a2-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="613a2-149">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="613a2-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="613a2-150">O segundo comando cria uma senha de software no cofre de chaves da contoso.</span><span class="sxs-lookup"><span data-stu-id="613a2-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="613a2-151">O comando especifica o local para a chave e a senha armazenadas em $Password.</span><span class="sxs-lookup"><span data-stu-id="613a2-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="613a2-152">Exemplo 6: importar uma chave e atribuir atributos</span><span class="sxs-lookup"><span data-stu-id="613a2-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="613a2-153">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Password.</span><span class="sxs-lookup"><span data-stu-id="613a2-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="613a2-154">O segundo comando cria um objeto **DateTime** usando o cmdlet **Get-Date** e armazena esse objeto na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="613a2-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="613a2-155">O terceiro comando cria a variável $tags para definir marcas para alta severidade e para isso.</span><span class="sxs-lookup"><span data-stu-id="613a2-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="613a2-156">O comando final importa uma chave como uma chave HSM do local especificado.</span><span class="sxs-lookup"><span data-stu-id="613a2-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="613a2-157">O comando especifica o tempo de expiração armazenado no $Expires e a senha armazenados $Password e aplica as marcas armazenadas em $tags.</span><span class="sxs-lookup"><span data-stu-id="613a2-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="613a2-158">OS</span><span class="sxs-lookup"><span data-stu-id="613a2-158">PARAMETERS</span></span>

### <span data-ttu-id="613a2-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="613a2-159">-Confirm</span></span>
<span data-ttu-id="613a2-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="613a2-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="613a2-161">-Destino</span><span class="sxs-lookup"><span data-stu-id="613a2-161">-Destination</span></span>
<span data-ttu-id="613a2-162">Especifica se a chave deve ser adicionada como uma chave protegida por software ou uma chave protegida pelo HSM no serviço do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="613a2-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="613a2-163">Os valores válidos são: HSM e software.</span><span class="sxs-lookup"><span data-stu-id="613a2-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="613a2-164">Observação: para usar o HSM como destino, você deve ter um cofre de chaves com suporte para HSMs.</span><span class="sxs-lookup"><span data-stu-id="613a2-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="613a2-165">Para obter mais informações sobre os níveis de serviço e os recursos do cofre de chaves do Azure, consulte o [site de preços do Azure Key Vault](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="613a2-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="613a2-166">Esse parâmetro é necessário quando você cria uma nova chave.</span><span class="sxs-lookup"><span data-stu-id="613a2-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="613a2-167">Se você importar uma chave usando o parâmetro *keyFilePath* , esse parâmetro será opcional:</span><span class="sxs-lookup"><span data-stu-id="613a2-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="613a2-168">Se você não especificar esse parâmetro, e esse cmdlet importar uma chave que tenha extensão de nome de arquivo. byok, ele importa essa chave como uma chave protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="613a2-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="613a2-169">O cmdlet não pode importar essa chave como chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="613a2-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="613a2-170">Se você não especificar esse parâmetro e esse cmdlet importar uma chave que tem uma extensão de nome de arquivo. pfx, ele importa a chave como uma chave protegida por software.</span><span class="sxs-lookup"><span data-stu-id="613a2-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software, HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software, HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a2-171">-Disable</span><span class="sxs-lookup"><span data-stu-id="613a2-171">-Disable</span></span>
<span data-ttu-id="613a2-172">Indica que a chave que você está adicionando está definida como um estado inicial de desabilitado.</span><span class="sxs-lookup"><span data-stu-id="613a2-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="613a2-173">Qualquer tentativa de usar a chave irá falhar.</span><span class="sxs-lookup"><span data-stu-id="613a2-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="613a2-174">Use esse parâmetro se você estiver precarregando chaves que pretende habilitar mais tarde.</span><span class="sxs-lookup"><span data-stu-id="613a2-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="613a2-175">-Expira em</span><span class="sxs-lookup"><span data-stu-id="613a2-175">-Expires</span></span>
<span data-ttu-id="613a2-176">Especifica o tempo de expiração, como um objeto **DateTime** , para a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="613a2-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="613a2-177">Esse parâmetro usa o tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="613a2-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="613a2-178">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="613a2-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="613a2-179">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="613a2-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="613a2-180">Se você não especificar esse parâmetro, a chave não expira.</span><span class="sxs-lookup"><span data-stu-id="613a2-180">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a2-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="613a2-181">-KeyFilePassword</span></span>
<span data-ttu-id="613a2-182">Especifica uma senha para o arquivo importado como um objeto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="613a2-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="613a2-183">Para obter um objeto **SecureString** , use o cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="613a2-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="613a2-184">Para obter mais informações, digite `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="613a2-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="613a2-185">Você deve especificar essa senha para importar um arquivo com uma extensão de nome de arquivo. pfx.</span><span class="sxs-lookup"><span data-stu-id="613a2-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a2-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="613a2-186">-KeyFilePath</span></span>
<span data-ttu-id="613a2-187">Especifica o caminho de um arquivo local que contém o material da chave que este cmdlet importa.</span><span class="sxs-lookup"><span data-stu-id="613a2-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="613a2-188">As extensões de nome de arquivo válidas são. byok e. pfx.</span><span class="sxs-lookup"><span data-stu-id="613a2-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="613a2-189">Se o arquivo for um arquivo. byok, a chave será automaticamente protegida por HSMs após a importação, e você não poderá substituir esse padrão.</span><span class="sxs-lookup"><span data-stu-id="613a2-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="613a2-190">Se o arquivo for um arquivo. pfx, a chave será automaticamente protegida pelo software após a importação.</span><span class="sxs-lookup"><span data-stu-id="613a2-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="613a2-191">Para substituir esse padrão, defina o parâmetro *Destination* como HSM para que a chave seja protegida pelo HSM.</span><span class="sxs-lookup"><span data-stu-id="613a2-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="613a2-192">Quando você especifica esse parâmetro, o parâmetro *Destination* é opcional.</span><span class="sxs-lookup"><span data-stu-id="613a2-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="613a2-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="613a2-193">-KeyOps</span></span>
<span data-ttu-id="613a2-194">Especifica uma matriz de operações que podem ser realizadas usando a chave que esse cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="613a2-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="613a2-195">Se você não especificar esse parâmetro, todas as operações poderão ser executadas.</span><span class="sxs-lookup"><span data-stu-id="613a2-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="613a2-196">Os valores aceitáveis para esse parâmetro são uma lista separada por vírgula das operações principais, conforme definido pela [especificação JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="613a2-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="613a2-197">Com</span><span class="sxs-lookup"><span data-stu-id="613a2-197">Encrypt</span></span>
- <span data-ttu-id="613a2-198">Criptografá</span><span class="sxs-lookup"><span data-stu-id="613a2-198">Decrypt</span></span>
- <span data-ttu-id="613a2-199">Quebrada</span><span class="sxs-lookup"><span data-stu-id="613a2-199">Wrap</span></span>
- <span data-ttu-id="613a2-200">Desenvolva</span><span class="sxs-lookup"><span data-stu-id="613a2-200">Unwrap</span></span>
- <span data-ttu-id="613a2-201">Designa</span><span class="sxs-lookup"><span data-stu-id="613a2-201">Sign</span></span>
- <span data-ttu-id="613a2-202">Verificar</span><span class="sxs-lookup"><span data-stu-id="613a2-202">Verify</span></span>
- <span data-ttu-id="613a2-203">Fazer</span><span class="sxs-lookup"><span data-stu-id="613a2-203">Backup</span></span>
- <span data-ttu-id="613a2-204">Restaurar</span><span class="sxs-lookup"><span data-stu-id="613a2-204">Restore</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a2-205">-Nome</span><span class="sxs-lookup"><span data-stu-id="613a2-205">-Name</span></span>
<span data-ttu-id="613a2-206">Especifica o nome da chave a ser adicionada ao cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="613a2-206">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="613a2-207">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de uma chave com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="613a2-207">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="613a2-208">O nome deve ser uma cadeia de caracteres de 1 a 63 caracteres com tamanho que contenha apenas 0-9, a-z, A-Z e-(o símbolo de traço).</span><span class="sxs-lookup"><span data-stu-id="613a2-208">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="613a2-209">-Não antes</span><span class="sxs-lookup"><span data-stu-id="613a2-209">-NotBefore</span></span>
<span data-ttu-id="613a2-210">Especifica o tempo, como um objeto **DateTime** , antes do qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="613a2-210">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="613a2-211">Esse parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="613a2-211">This parameter uses UTC.</span></span> <span data-ttu-id="613a2-212">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="613a2-212">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="613a2-213">Se você não especificar esse parâmetro, a chave pode ser usada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="613a2-213">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="613a2-214">-Marca</span><span class="sxs-lookup"><span data-stu-id="613a2-214">-Tag</span></span>
<span data-ttu-id="613a2-215">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="613a2-215">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="613a2-216">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="613a2-216">For example:</span></span>

<span data-ttu-id="613a2-217">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="613a2-217">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="613a2-218">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="613a2-218">-VaultName</span></span>
<span data-ttu-id="613a2-219">Especifica o nome do cofre de chaves para o qual esse cmdlet adiciona a chave.</span><span class="sxs-lookup"><span data-stu-id="613a2-219">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="613a2-220">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="613a2-220">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="613a2-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="613a2-221">-WhatIf</span></span>
<span data-ttu-id="613a2-222">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="613a2-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="613a2-223">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="613a2-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="613a2-224">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613a2-224">-DefaultProfile</span></span>
<span data-ttu-id="613a2-225">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="613a2-225">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="613a2-226">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613a2-226">CommonParameters</span></span>
<span data-ttu-id="613a2-227">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="613a2-227">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613a2-228">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="613a2-228">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613a2-229">SENSORES</span><span class="sxs-lookup"><span data-stu-id="613a2-229">INPUTS</span></span>

## <span data-ttu-id="613a2-230">EXIBE</span><span class="sxs-lookup"><span data-stu-id="613a2-230">OUTPUTS</span></span>

### <span data-ttu-id="613a2-231">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="613a2-231">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="613a2-232">INFORMA</span><span class="sxs-lookup"><span data-stu-id="613a2-232">NOTES</span></span>

## <span data-ttu-id="613a2-233">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="613a2-233">RELATED LINKS</span></span>

[<span data-ttu-id="613a2-234">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="613a2-234">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="613a2-235">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="613a2-235">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="613a2-236">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="613a2-236">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="613a2-237">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="613a2-237">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
