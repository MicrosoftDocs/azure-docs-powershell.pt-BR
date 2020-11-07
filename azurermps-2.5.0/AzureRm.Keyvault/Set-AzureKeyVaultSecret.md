---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 0c482d3fd4e2e02221799ea72e61eacc80ff9e2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786097"
---
# <span data-ttu-id="dadb5-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dadb5-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="dadb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dadb5-102">SYNOPSIS</span></span>
<span data-ttu-id="dadb5-103">Cria ou atualiza um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="dadb5-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dadb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dadb5-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dadb5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dadb5-105">DESCRIPTION</span></span>
<span data-ttu-id="dadb5-106">O cmdlet **set-AzureKeyVaultSecret** cria ou atualiza um segredo em um cofre de chaves no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="dadb5-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="dadb5-107">Se o segredo não existir, esse cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="dadb5-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="dadb5-108">Se o segredo já existir, esse cmdlet criará uma nova versão desse segredo.</span><span class="sxs-lookup"><span data-stu-id="dadb5-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="dadb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dadb5-109">EXAMPLES</span></span>

### <span data-ttu-id="dadb5-110">Exemplo 1: modificar o valor de um segredo usando atributos padrão</span><span class="sxs-lookup"><span data-stu-id="dadb5-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="dadb5-111">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Secret.</span><span class="sxs-lookup"><span data-stu-id="dadb5-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="dadb5-112">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="dadb5-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="dadb5-113">O segundo comando modifica o valor do segredo chamado ITSecret no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="dadb5-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="dadb5-114">O valor secreto se torna o valor armazenado em $Secret.</span><span class="sxs-lookup"><span data-stu-id="dadb5-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="dadb5-115">Exemplo 2: modificar o valor de um segredo usando atributos personalizados</span><span class="sxs-lookup"><span data-stu-id="dadb5-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="dadb5-116">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e armazena essa cadeia de caracteres na variável $Secret.</span><span class="sxs-lookup"><span data-stu-id="dadb5-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="dadb5-117">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="dadb5-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="dadb5-118">Os comandos a seguir definem atributos personalizados para a data de vencimento, as marcas e o tipo de contexto e armazenam os atributos em variáveis.</span><span class="sxs-lookup"><span data-stu-id="dadb5-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="dadb5-119">O comando final modifica os valores do segredo nomeado ITSecret no cofre de chaves chamado contoso, usando os valores especificados anteriormente como variáveis.</span><span class="sxs-lookup"><span data-stu-id="dadb5-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="dadb5-120">OS</span><span class="sxs-lookup"><span data-stu-id="dadb5-120">PARAMETERS</span></span>

### <span data-ttu-id="dadb5-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="dadb5-121">-ContentType</span></span>
<span data-ttu-id="dadb5-122">Especifica o tipo de conteúdo de um segredo.</span><span class="sxs-lookup"><span data-stu-id="dadb5-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="dadb5-123">Para excluir o tipo de conteúdo existente, especifique uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="dadb5-123">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="dadb5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dadb5-124">-DefaultProfile</span></span>
<span data-ttu-id="dadb5-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="dadb5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dadb5-126">-Disable</span><span class="sxs-lookup"><span data-stu-id="dadb5-126">-Disable</span></span>
<span data-ttu-id="dadb5-127">Indica que esse cmdlet desabilita um segredo.</span><span class="sxs-lookup"><span data-stu-id="dadb5-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="dadb5-128">-Expira em</span><span class="sxs-lookup"><span data-stu-id="dadb5-128">-Expires</span></span>
<span data-ttu-id="dadb5-129">Especifica o tempo de expiração, como um objeto **DateTime** , para o segredo que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="dadb5-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="dadb5-130">Esse parâmetro usa o tempo universal coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="dadb5-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="dadb5-131">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="dadb5-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="dadb5-132">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="dadb5-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="dadb5-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="dadb5-133">-Name</span></span>
<span data-ttu-id="dadb5-134">Especifica o nome de um segredo a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="dadb5-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="dadb5-135">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="dadb5-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dadb5-136">-Não antes</span><span class="sxs-lookup"><span data-stu-id="dadb5-136">-NotBefore</span></span>
<span data-ttu-id="dadb5-137">Especifica o tempo, como um objeto **DateTime** , antes do qual o segredo não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="dadb5-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="dadb5-138">Esse parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="dadb5-138">This parameter uses UTC.</span></span> <span data-ttu-id="dadb5-139">Para obter um objeto **DateTime** , use o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="dadb5-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="dadb5-140">-Secretvalue</span><span class="sxs-lookup"><span data-stu-id="dadb5-140">-SecretValue</span></span>
<span data-ttu-id="dadb5-141">Especifica o valor do segredo como um objeto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="dadb5-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="dadb5-142">Para obter um objeto **SecureString** , use o cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="dadb5-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="dadb5-143">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="dadb5-143">For more information, type `Get-Help
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

### <span data-ttu-id="dadb5-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="dadb5-144">-Tag</span></span>
<span data-ttu-id="dadb5-145">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="dadb5-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dadb5-146">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="dadb5-146">For example:</span></span>

<span data-ttu-id="dadb5-147">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="dadb5-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dadb5-148">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="dadb5-148">-VaultName</span></span>
<span data-ttu-id="dadb5-149">Especifica o nome do cofre de chaves ao qual esse segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="dadb5-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="dadb5-150">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="dadb5-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dadb5-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dadb5-151">-Confirm</span></span>
<span data-ttu-id="dadb5-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dadb5-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dadb5-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dadb5-153">-WhatIf</span></span>
<span data-ttu-id="dadb5-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dadb5-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dadb5-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dadb5-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dadb5-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dadb5-156">CommonParameters</span></span>
<span data-ttu-id="dadb5-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dadb5-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dadb5-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dadb5-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dadb5-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dadb5-159">INPUTS</span></span>

## <span data-ttu-id="dadb5-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dadb5-160">OUTPUTS</span></span>

### <span data-ttu-id="dadb5-161">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="dadb5-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="dadb5-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dadb5-162">NOTES</span></span>

## <span data-ttu-id="dadb5-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dadb5-163">RELATED LINKS</span></span>

[<span data-ttu-id="dadb5-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dadb5-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="dadb5-165">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="dadb5-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
