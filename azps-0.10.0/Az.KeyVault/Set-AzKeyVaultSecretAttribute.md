---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775768"
---
# <span data-ttu-id="d5dfa-101">Set-AzKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="d5dfa-101">Set-AzKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="d5dfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="d5dfa-103">Atualiza os atributos de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="d5dfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5dfa-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5dfa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="d5dfa-106">O cmdlet **set-AzKeyVaultSecretAttribute** atualiza atributos editáveis de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-106">The **Set-AzKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="d5dfa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5dfa-107">EXAMPLES</span></span>

### <span data-ttu-id="d5dfa-108">Exemplo 1: modificar os atributos de um segredo</span><span class="sxs-lookup"><span data-stu-id="d5dfa-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="d5dfa-109">Os primeiros quatro comandos definem atributos para a data de vencimento, a data de vencimento, as marcas e o tipo de contexto e armazenam os atributos em variáveis.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="d5dfa-110">O comando final modifica os atributos do segredo chamado HR no cofre de chaves chamado ContosoVault, usando as variáveis armazenadas.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="d5dfa-111">Exemplo 2: excluir as marcas e o tipo de conteúdo de um segredo</span><span class="sxs-lookup"><span data-stu-id="d5dfa-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="d5dfa-112">Esse comando exclui as marcas e o tipo de conteúdo da versão especificada do segredo chamado HR no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="d5dfa-113">Exemplo 3: desabilitar a versão atual dos segredos cujo nome começa com ele</span><span class="sxs-lookup"><span data-stu-id="d5dfa-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="d5dfa-114">O primeiro comando armazena o valor da cadeia de caracteres contoso na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="d5dfa-115">O segundo comando armazena o valor da cadeia de caracteres na variável $Prefix.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="d5dfa-116">O terceiro comando usa o cmdlet Get-AzKeyVaultSecret para obter os segredos no cofre de chaves especificado e, em seguida, passa esses segredos para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="d5dfa-116">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="d5dfa-117">O cmdlet **Where-Object** filtra os segredos dos nomes que começam com os caracteres.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="d5dfa-118">O comando canaliza os segredos que correspondem ao filtro para o cmdlet Set-AzKeyVaultSecretAttribute, que os desabilita.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-118">The command pipes the secrets that match the filter to the Set-AzKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="d5dfa-119">Exemplo 4: definir o ContentType para todas as versões de um segredo</span><span class="sxs-lookup"><span data-stu-id="d5dfa-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="d5dfa-120">Os primeiros três comandos definem variáveis de cadeia de caracteres para usar para os parâmetros *vaultname* , *Name* e *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="d5dfa-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="d5dfa-121">O quarto comando usa o cmdlet Get-AzKeyVaultKey para obter as chaves especificadas e canaliza as chaves para o cmdlet Set-AzKeyVaultSecretAttribute para definir o tipo de conteúdo como XML.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-121">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="d5dfa-122">OS</span><span class="sxs-lookup"><span data-stu-id="d5dfa-122">PARAMETERS</span></span>

### <span data-ttu-id="d5dfa-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="d5dfa-123">-ContentType</span></span>
<span data-ttu-id="d5dfa-124">Especifica o tipo de conteúdo de um segredo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="d5dfa-125">Se você não especificar esse parâmetro, não haverá nenhuma alteração no tipo de conteúdo do segredo atual.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="d5dfa-126">Para remover o tipo de conteúdo existente, especifique uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="d5dfa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5dfa-127">-DefaultProfile</span></span>
<span data-ttu-id="d5dfa-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d5dfa-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5dfa-129">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="d5dfa-129">-Enable</span></span>
<span data-ttu-id="d5dfa-130">Indica se um segredo deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="d5dfa-131">Especifique $False para desabilitar um segredo ou $True para habilitar um segredo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="d5dfa-132">Se você não especificar esse parâmetro, não haverá nenhuma alteração no estado habilitado ou desabilitado do segredo atual.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5dfa-133">-Expira em</span><span class="sxs-lookup"><span data-stu-id="d5dfa-133">-Expires</span></span>
<span data-ttu-id="d5dfa-134">Especifica a data e a hora em que um segredo expira.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="d5dfa-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5dfa-135">-Name</span></span>
<span data-ttu-id="d5dfa-136">Especifica o nome de um segredo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-136">Specifies the name of a secret.</span></span> <span data-ttu-id="d5dfa-137">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="d5dfa-138">-Não antes</span><span class="sxs-lookup"><span data-stu-id="d5dfa-138">-NotBefore</span></span>
<span data-ttu-id="d5dfa-139">Especifica o tempo universal coordenado (UTC) antes do qual o segredo não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="d5dfa-140">Se você não especificar esse parâmetro, não haverá nenhuma alteração no atributo não antes do segredo atual.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="d5dfa-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5dfa-141">-PassThru</span></span>
<span data-ttu-id="d5dfa-142">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d5dfa-143">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d5dfa-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="d5dfa-144">-Tag</span></span>
<span data-ttu-id="d5dfa-145">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d5dfa-146">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d5dfa-146">For example:</span></span>

<span data-ttu-id="d5dfa-147">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d5dfa-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d5dfa-148">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="d5dfa-148">-VaultName</span></span>
<span data-ttu-id="d5dfa-149">Especifica o nome do cofre de chaves a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="d5dfa-150">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado por esse parâmetro e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="d5dfa-151">-Versão</span><span class="sxs-lookup"><span data-stu-id="d5dfa-151">-Version</span></span>
<span data-ttu-id="d5dfa-152">Especifica a versão de um segredo.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="d5dfa-153">Esse cmdlet constrói o FQDN de um segredo com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do segredo e na versão secreta.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5dfa-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5dfa-154">-Confirm</span></span>
<span data-ttu-id="d5dfa-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5dfa-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5dfa-156">-WhatIf</span></span>
<span data-ttu-id="d5dfa-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5dfa-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5dfa-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5dfa-159">CommonParameters</span></span>
<span data-ttu-id="d5dfa-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5dfa-161">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5dfa-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5dfa-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5dfa-162">INPUTS</span></span>

### <span data-ttu-id="d5dfa-163">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d5dfa-163">None</span></span>
<span data-ttu-id="d5dfa-164">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5dfa-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5dfa-165">OUTPUTS</span></span>

### <span data-ttu-id="d5dfa-166">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="d5dfa-166">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="d5dfa-167">Retorna o objeto Microsoft. Azure. Commands. keyvault. Models. Secret se PassThru for especificado.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-167">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="d5dfa-168">Caso contrário, não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="d5dfa-168">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="d5dfa-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5dfa-169">NOTES</span></span>

## <span data-ttu-id="d5dfa-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5dfa-170">RELATED LINKS</span></span>

[<span data-ttu-id="d5dfa-171">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d5dfa-171">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="d5dfa-172">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d5dfa-172">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="d5dfa-173">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d5dfa-173">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
