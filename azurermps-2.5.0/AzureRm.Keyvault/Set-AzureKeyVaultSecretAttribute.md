---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
ms.openlocfilehash: f8463533f8a153b74df1863ba251950f16f9e19a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785194"
---
# <span data-ttu-id="4eb7d-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="4eb7d-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="4eb7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4eb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb7d-103">Atualiza os atributos de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eb7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4eb7d-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb7d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4eb7d-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb7d-106">O cmdlet **set-AzureKeyVaultSecretAttribute** atualiza atributos editáveis de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="4eb7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4eb7d-107">EXAMPLES</span></span>

### <span data-ttu-id="4eb7d-108">Exemplo 1: modificar os atributos de um segredo</span><span class="sxs-lookup"><span data-stu-id="4eb7d-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="4eb7d-109">Os primeiros quatro comandos definem atributos para a data de vencimento, a data de vencimento, as marcas e o tipo de contexto e armazenam os atributos em variáveis.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="4eb7d-110">O comando final modifica os atributos do segredo chamado HR no cofre de chaves chamado ContosoVault, usando as variáveis armazenadas.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="4eb7d-111">Exemplo 2: excluir as marcas e o tipo de conteúdo de um segredo</span><span class="sxs-lookup"><span data-stu-id="4eb7d-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="4eb7d-112">Esse comando exclui as marcas e o tipo de conteúdo da versão especificada do segredo chamado HR no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="4eb7d-113">Exemplo 3: desabilitar a versão atual dos segredos cujo nome começa com ele</span><span class="sxs-lookup"><span data-stu-id="4eb7d-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="4eb7d-114">O primeiro comando armazena o valor da cadeia de caracteres contoso na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="4eb7d-115">O segundo comando armazena o valor da cadeia de caracteres na variável $Prefix.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="4eb7d-116">O terceiro comando usa o cmdlet Get-AzureKeyVaultSecret para obter os segredos no cofre de chaves especificado e, em seguida, passa esses segredos para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="4eb7d-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="4eb7d-117">O cmdlet **Where-Object** filtra os segredos dos nomes que começam com os caracteres.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="4eb7d-118">O comando canaliza os segredos que correspondem ao filtro para o cmdlet Set-AzureKeyVaultSecretAttribute, que os desabilita.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="4eb7d-119">Exemplo 4: definir o ContentType para todas as versões de um segredo</span><span class="sxs-lookup"><span data-stu-id="4eb7d-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="4eb7d-120">Os primeiros três comandos definem variáveis de cadeia de caracteres para usar para os parâmetros *vaultname* , *Name* e *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="4eb7d-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="4eb7d-121">O quarto comando usa o cmdlet Get-AzureKeyVaultKey para obter as chaves especificadas e canaliza as chaves para o cmdlet Set-AzureKeyVaultSecretAttribute para definir o tipo de conteúdo como XML.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="4eb7d-122">OS</span><span class="sxs-lookup"><span data-stu-id="4eb7d-122">PARAMETERS</span></span>

### <span data-ttu-id="4eb7d-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="4eb7d-123">-ContentType</span></span>
<span data-ttu-id="4eb7d-124">Especifica o tipo de conteúdo de um segredo.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="4eb7d-125">Se você não especificar esse parâmetro, não haverá nenhuma alteração no tipo de conteúdo do segredo atual.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="4eb7d-126">Para remover o tipo de conteúdo existente, especifique uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="4eb7d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb7d-127">-DefaultProfile</span></span>
<span data-ttu-id="4eb7d-128">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4eb7d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4eb7d-129">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="4eb7d-129">-Enable</span></span>
<span data-ttu-id="4eb7d-130">Indica se um segredo deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="4eb7d-131">Especifique $False para desabilitar um segredo ou $True para habilitar um segredo.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="4eb7d-132">Se você não especificar esse parâmetro, não haverá nenhuma alteração no estado habilitado ou desabilitado do segredo atual.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="4eb7d-133">-Expira em</span><span class="sxs-lookup"><span data-stu-id="4eb7d-133">-Expires</span></span>
<span data-ttu-id="4eb7d-134">Especifica a data e a hora em que um segredo expira.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="4eb7d-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="4eb7d-135">-Name</span></span>
<span data-ttu-id="4eb7d-136">Especifica o nome de um segredo.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-136">Specifies the name of a secret.</span></span> <span data-ttu-id="4eb7d-137">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um segredo com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="4eb7d-138">-Não antes</span><span class="sxs-lookup"><span data-stu-id="4eb7d-138">-NotBefore</span></span>
<span data-ttu-id="4eb7d-139">Especifica o tempo universal coordenado (UTC) antes do qual o segredo não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="4eb7d-140">Se você não especificar esse parâmetro, não haverá nenhuma alteração no atributo não antes do segredo atual.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="4eb7d-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4eb7d-141">-PassThru</span></span>
<span data-ttu-id="4eb7d-142">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4eb7d-143">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4eb7d-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="4eb7d-144">-Tag</span></span>
<span data-ttu-id="4eb7d-145">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4eb7d-146">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4eb7d-146">For example:</span></span>

<span data-ttu-id="4eb7d-147">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4eb7d-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4eb7d-148">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="4eb7d-148">-VaultName</span></span>
<span data-ttu-id="4eb7d-149">Especifica o nome do cofre de chaves a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="4eb7d-150">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado por esse parâmetro e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="4eb7d-151">-Versão</span><span class="sxs-lookup"><span data-stu-id="4eb7d-151">-Version</span></span>
<span data-ttu-id="4eb7d-152">Especifica a versão de um segredo.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="4eb7d-153">Esse cmdlet constrói o FQDN de um segredo com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do segredo e na versão secreta.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="4eb7d-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4eb7d-154">-Confirm</span></span>
<span data-ttu-id="4eb7d-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4eb7d-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb7d-156">-WhatIf</span></span>
<span data-ttu-id="4eb7d-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb7d-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4eb7d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb7d-159">CommonParameters</span></span>
<span data-ttu-id="4eb7d-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb7d-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb7d-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb7d-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4eb7d-162">INPUTS</span></span>

## <span data-ttu-id="4eb7d-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4eb7d-163">OUTPUTS</span></span>

### <span data-ttu-id="4eb7d-164">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="4eb7d-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="4eb7d-165">Retorna o objeto Microsoft. Azure. Commands. keyvault. Models. Secret se PassThru for especificado.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="4eb7d-166">Caso contrário, não retorna nada.</span><span class="sxs-lookup"><span data-stu-id="4eb7d-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="4eb7d-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4eb7d-167">NOTES</span></span>

## <span data-ttu-id="4eb7d-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4eb7d-168">RELATED LINKS</span></span>

[<span data-ttu-id="4eb7d-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="4eb7d-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="4eb7d-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4eb7d-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="4eb7d-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4eb7d-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
