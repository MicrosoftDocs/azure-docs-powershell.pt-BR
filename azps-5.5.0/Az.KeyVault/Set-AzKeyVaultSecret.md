---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113086"
---
# <span data-ttu-id="55765-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="55765-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="55765-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55765-102">SYNOPSIS</span></span>
<span data-ttu-id="55765-103">Cria ou atualiza um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="55765-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="55765-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55765-104">SYNTAX</span></span>

### <span data-ttu-id="55765-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="55765-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55765-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="55765-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55765-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="55765-107">DESCRIPTION</span></span>
<span data-ttu-id="55765-108">O cmdlet **Set-AzKeyVaultSec ltd cria** ou atualiza um segredo em um cofre de chave no Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="55765-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="55765-109">Se o segredo não existir, este cmdlet o criará.</span><span class="sxs-lookup"><span data-stu-id="55765-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="55765-110">Se o segredo já existir, este cmdlet criará uma nova versão desse segredo.</span><span class="sxs-lookup"><span data-stu-id="55765-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="55765-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="55765-111">EXAMPLES</span></span>

### <span data-ttu-id="55765-112">Exemplo 1: modificar o valor de um segredo usando atributos padrão</span><span class="sxs-lookup"><span data-stu-id="55765-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="55765-113">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e, em seguida, armazena essa cadeia de caracteres na variável $Secret.</span><span class="sxs-lookup"><span data-stu-id="55765-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="55765-114">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="55765-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="55765-115">O segundo comando modifica o valor do segredo chamado ITSecsecsec no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="55765-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="55765-116">O valor secreto torna-se o valor armazenado $Secret.</span><span class="sxs-lookup"><span data-stu-id="55765-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="55765-117">Exemplo 2: modificar o valor de um segredo usando atributos personalizados</span><span class="sxs-lookup"><span data-stu-id="55765-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="55765-118">O primeiro comando converte uma cadeia de caracteres em uma cadeia de caracteres segura usando o cmdlet **ConvertTo-SecureString** e, em seguida, armazena essa cadeia de caracteres na variável $Secret.</span><span class="sxs-lookup"><span data-stu-id="55765-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="55765-119">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="55765-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="55765-120">Os próximos comandos definem atributos personalizados para a data de vencimento, marcas e tipo de contexto e armazenam os atributos em variáveis.</span><span class="sxs-lookup"><span data-stu-id="55765-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="55765-121">O comando final modifica os valores do segredo chamado ITSecsecsec no cofre de chaves chamado Contoso, usando os valores especificados anteriormente como variáveis.</span><span class="sxs-lookup"><span data-stu-id="55765-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="55765-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55765-122">PARAMETERS</span></span>

### <span data-ttu-id="55765-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="55765-123">-ContentType</span></span>
<span data-ttu-id="55765-124">Especifica o tipo de conteúdo de um segredo.</span><span class="sxs-lookup"><span data-stu-id="55765-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="55765-125">Para excluir o tipo de conteúdo existente, especifique uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="55765-125">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55765-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55765-126">-DefaultProfile</span></span>
<span data-ttu-id="55765-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="55765-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55765-128">-Desabilitar</span><span class="sxs-lookup"><span data-stu-id="55765-128">-Disable</span></span>
<span data-ttu-id="55765-129">Indica que esse cmdlet desabilita um segredo.</span><span class="sxs-lookup"><span data-stu-id="55765-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="55765-130">-Expira</span><span class="sxs-lookup"><span data-stu-id="55765-130">-Expires</span></span>
<span data-ttu-id="55765-131">Especifica o tempo de expiração, como um objeto **DateTime,** para o segredo que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="55765-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="55765-132">Este parâmetro usa o Tempo Universal Coordenado (UTC).</span><span class="sxs-lookup"><span data-stu-id="55765-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="55765-133">Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="55765-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="55765-134">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="55765-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="55765-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55765-135">-InputObject</span></span>
<span data-ttu-id="55765-136">Objeto secreto</span><span class="sxs-lookup"><span data-stu-id="55765-136">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55765-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="55765-137">-Name</span></span>
<span data-ttu-id="55765-138">Especifica o nome de um segredo a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="55765-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="55765-139">Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome especificado por este parâmetro, o nome do cofre de chave e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="55765-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55765-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="55765-140">-NotBefore</span></span>
<span data-ttu-id="55765-141">Especifica a hora, como um objeto **DateTime,** antes do qual o segredo não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="55765-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="55765-142">Este parâmetro usa UTC.</span><span class="sxs-lookup"><span data-stu-id="55765-142">This parameter uses UTC.</span></span> <span data-ttu-id="55765-143">Para obter um **objeto DateTime,** use o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="55765-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="55765-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="55765-144">-SecretValue</span></span>
<span data-ttu-id="55765-145">Especifica o valor do segredo como um objeto **SecureString.**</span><span class="sxs-lookup"><span data-stu-id="55765-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="55765-146">Para obter um **objeto SecureString,** use o cmdlet **ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="55765-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="55765-147">Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="55765-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55765-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="55765-148">-Tag</span></span>
<span data-ttu-id="55765-149">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="55765-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="55765-150">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="55765-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="55765-151">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="55765-151">-VaultName</span></span>
<span data-ttu-id="55765-152">Especifica o nome do cofre de chave ao qual este segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="55765-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="55765-153">Esse cmdlet construirá o FQDN de um cofre de teclas com base no nome especificado por esse parâmetro e no ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="55765-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55765-154">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="55765-154">-Confirm</span></span>
<span data-ttu-id="55765-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55765-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55765-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55765-156">-WhatIf</span></span>
<span data-ttu-id="55765-157">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="55765-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55765-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55765-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55765-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55765-159">CommonParameters</span></span>
<span data-ttu-id="55765-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55765-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55765-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55765-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55765-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="55765-162">INPUTS</span></span>

### <span data-ttu-id="55765-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecibleIdentityItem</span><span class="sxs-lookup"><span data-stu-id="55765-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="55765-164">Saídas</span><span class="sxs-lookup"><span data-stu-id="55765-164">OUTPUTS</span></span>

### <span data-ttu-id="55765-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="55765-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="55765-166">Notas</span><span class="sxs-lookup"><span data-stu-id="55765-166">NOTES</span></span>

## <span data-ttu-id="55765-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55765-167">RELATED LINKS</span></span>

[<span data-ttu-id="55765-168">Get-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="55765-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="55765-169">Remove-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="55765-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
