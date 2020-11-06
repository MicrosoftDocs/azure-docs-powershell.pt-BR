---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: c7968d915ab28dca6bf595e5339d2681962ecdea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610648"
---
# <span data-ttu-id="ae432-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae432-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="ae432-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae432-102">SYNOPSIS</span></span>
<span data-ttu-id="ae432-103">Cria ou atualiza um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="ae432-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae432-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae432-104">SYNTAX</span></span>

### <span data-ttu-id="ae432-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae432-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae432-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae432-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae432-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae432-107">DESCRIPTION</span></span>
<span data-ttu-id="ae432-108">O cmdlet **set-AzureKeyVaultSecret** cria ou atualiza um segredo em um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae432-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="ae432-109">Se o segredo não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="ae432-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="ae432-110">Se o segredo já existir, esse cmdlet criará uma nova versão desse segredo.</span><span class="sxs-lookup"><span data-stu-id="ae432-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="ae432-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae432-111">EXAMPLES</span></span>

### <span data-ttu-id="ae432-112">Exemplo 1: modificar o valor de um segredo usando atributos padrão</span><span class="sxs-lookup"><span data-stu-id="ae432-112">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="ae432-113">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Secret.</span><span class="sxs-lookup"><span data-stu-id="ae432-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="ae432-114">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ae432-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="ae432-115">O segundo comando modifica o valor do segredo chamado ITSecret no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="ae432-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="ae432-116">O valor secreto se torna o valor armazenado em $Secret.</span><span class="sxs-lookup"><span data-stu-id="ae432-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="ae432-117">Exemplo 2: modificar o valor de um segredo usando atributos personalizados</span><span class="sxs-lookup"><span data-stu-id="ae432-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="ae432-118">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Secret.</span><span class="sxs-lookup"><span data-stu-id="ae432-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="ae432-119">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ae432-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="ae432-120">Os comandos a seguir definem atributos personalizados para a data de vencimento, as marcas e o tipo de contexto e armazenam os atributos em variáveis.</span><span class="sxs-lookup"><span data-stu-id="ae432-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="ae432-121">O comando final modifica os valores do segredo nomeado ITSecret no cofre de chaves chamado contoso, usando os valores especificados anteriormente como variáveis.</span><span class="sxs-lookup"><span data-stu-id="ae432-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="ae432-122">OS</span><span class="sxs-lookup"><span data-stu-id="ae432-122">PARAMETERS</span></span>

### <span data-ttu-id="ae432-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ae432-123">-ContentType</span></span>
<span data-ttu-id="ae432-124">Especifica o tipo de conteúdo de um segredo.</span><span class="sxs-lookup"><span data-stu-id="ae432-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="ae432-125">Para excluir o tipo de conteúdo existente, especifique uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="ae432-125">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae432-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae432-126">-DefaultProfile</span></span>
<span data-ttu-id="ae432-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ae432-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae432-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="ae432-128">-Disable</span></span>
<span data-ttu-id="ae432-129">Indica que esse cmdlet desabilita um segredo.</span><span class="sxs-lookup"><span data-stu-id="ae432-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="ae432-130">-Expira em</span><span class="sxs-lookup"><span data-stu-id="ae432-130">-Expires</span></span>
<span data-ttu-id="ae432-131">Especifica o tempo de expiração, como um objeto **DateTime** , para o segredo que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="ae432-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="ae432-132">Esse parâmetro usa o tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="ae432-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="ae432-133">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="ae432-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ae432-134">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ae432-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="ae432-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae432-135">-InputObject</span></span>
<span data-ttu-id="ae432-136">Objeto secreto</span><span class="sxs-lookup"><span data-stu-id="ae432-136">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae432-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae432-137">-Name</span></span>
<span data-ttu-id="ae432-138">Especifica o nome de um segredo a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ae432-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="ae432-139">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="ae432-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae432-140">-Não antes</span><span class="sxs-lookup"><span data-stu-id="ae432-140">-NotBefore</span></span>
<span data-ttu-id="ae432-141">Especifica o tempo, como um objeto **DateTime** , antes do qual o segredo não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="ae432-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="ae432-142">Esse parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="ae432-142">This parameter uses UTC.</span></span> <span data-ttu-id="ae432-143">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="ae432-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="ae432-144">-Secretvalue</span><span class="sxs-lookup"><span data-stu-id="ae432-144">-SecretValue</span></span>
<span data-ttu-id="ae432-145">Especifica o valor do segredo como um objeto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="ae432-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="ae432-146">Para obter um objeto **SecureString** , use o cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="ae432-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="ae432-147">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ae432-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae432-148">-Marca</span><span class="sxs-lookup"><span data-stu-id="ae432-148">-Tag</span></span>
<span data-ttu-id="ae432-149">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ae432-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae432-150">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ae432-150">For example:</span></span>

<span data-ttu-id="ae432-151">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ae432-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ae432-152">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="ae432-152">-VaultName</span></span>
<span data-ttu-id="ae432-153">Especifica o nome do cofre de chaves ao qual esse segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="ae432-153">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="ae432-154">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="ae432-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae432-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae432-155">-Confirm</span></span>
<span data-ttu-id="ae432-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae432-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae432-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae432-157">-WhatIf</span></span>
<span data-ttu-id="ae432-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae432-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae432-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae432-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae432-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae432-160">CommonParameters</span></span>
<span data-ttu-id="ae432-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae432-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae432-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae432-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae432-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae432-163">INPUTS</span></span>

### <span data-ttu-id="ae432-164">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ae432-164">None</span></span>
<span data-ttu-id="ae432-165">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ae432-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae432-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae432-166">OUTPUTS</span></span>

### <span data-ttu-id="ae432-167">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae432-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ae432-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae432-168">NOTES</span></span>

## <span data-ttu-id="ae432-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae432-169">RELATED LINKS</span></span>

[<span data-ttu-id="ae432-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae432-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="ae432-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ae432-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
