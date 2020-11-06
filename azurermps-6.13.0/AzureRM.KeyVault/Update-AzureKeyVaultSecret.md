---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
ms.openlocfilehash: d895485354c33daa4eac57b699358ee0335905be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610590"
---
# <span data-ttu-id="e4012-101">Update-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e4012-101">Update-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="e4012-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4012-102">SYNOPSIS</span></span>
<span data-ttu-id="e4012-103">Atualiza os atributos de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e4012-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4012-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4012-104">SYNTAX</span></span>

### <span data-ttu-id="e4012-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="e4012-105">Default (Default)</span></span>
```
Update-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4012-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e4012-106">InputObject</span></span>
```
Update-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4012-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4012-107">DESCRIPTION</span></span>
<span data-ttu-id="e4012-108">O cmdlet **Update-AzureKeyVaultSecret** atualiza atributos editáveis de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e4012-108">The **Update-AzureKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="e4012-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4012-109">EXAMPLES</span></span>

### <span data-ttu-id="e4012-110">Exemplo 1: modificar os atributos de um segredo</span><span class="sxs-lookup"><span data-stu-id="e4012-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="e4012-111">Os primeiros quatro comandos definem atributos para a data de vencimento, a data de vencimento, as marcas e o tipo de contexto e armazenam os atributos em variáveis.</span><span class="sxs-lookup"><span data-stu-id="e4012-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="e4012-112">O comando final modifica os atributos do segredo chamado HR no cofre de chaves chamado ContosoVault, usando as variáveis armazenadas.</span><span class="sxs-lookup"><span data-stu-id="e4012-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="e4012-113">Exemplo 2: excluir as marcas e o tipo de conteúdo de um segredo</span><span class="sxs-lookup"><span data-stu-id="e4012-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="e4012-114">Esse comando exclui as marcas e o tipo de conteúdo da versão especificada do segredo chamado HR no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="e4012-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="e4012-115">Exemplo 3: desabilitar a versão atual dos segredos cujo nome começa com ele</span><span class="sxs-lookup"><span data-stu-id="e4012-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzureKeyVaultSecret -Enable $False
```

<span data-ttu-id="e4012-116">O primeiro comando armazena o valor da cadeia de caracteres contoso na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="e4012-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="e4012-117">O segundo comando armazena o valor da cadeia de caracteres na variável $Prefix.</span><span class="sxs-lookup"><span data-stu-id="e4012-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="e4012-118">O terceiro comando usa o cmdlet Get-AzureKeyVaultSecret para obter os segredos no cofre de chaves especificado e, em seguida, passa esses segredos para o cmdlet **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="e4012-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="e4012-119">O cmdlet **Where-Object** filtra os segredos dos nomes que começam com os caracteres.</span><span class="sxs-lookup"><span data-stu-id="e4012-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="e4012-120">O comando canaliza os segredos que correspondem ao filtro para o cmdlet Update-AzureKeyVaultSecret, que os desabilita.</span><span class="sxs-lookup"><span data-stu-id="e4012-120">The command pipes the secrets that match the filter to the Update-AzureKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="e4012-121">Exemplo 4: definir o ContentType para todas as versões de um segredo</span><span class="sxs-lookup"><span data-stu-id="e4012-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzureKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="e4012-122">Os primeiros três comandos definem variáveis de cadeia de caracteres para usar para os parâmetros *vaultname* , *Name* e *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="e4012-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="e4012-123">O quarto comando usa o cmdlet Get-AzureKeyVaultKey para obter as chaves especificadas e canaliza as chaves para o cmdlet Update-AzureKeyVaultSecret para definir o tipo de conteúdo como XML.</span><span class="sxs-lookup"><span data-stu-id="e4012-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzureKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="e4012-124">OS</span><span class="sxs-lookup"><span data-stu-id="e4012-124">PARAMETERS</span></span>

### <span data-ttu-id="e4012-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="e4012-125">-ContentType</span></span>
<span data-ttu-id="e4012-126">Tipo de conteúdo do segredo.</span><span class="sxs-lookup"><span data-stu-id="e4012-126">Secret's content type.</span></span>
<span data-ttu-id="e4012-127">Se não for especificado, o valor existente do tipo de conteúdo do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="e4012-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="e4012-128">Remova o valor de tipo de conteúdo existente especificando uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="e4012-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="e4012-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4012-129">-DefaultProfile</span></span>
<span data-ttu-id="e4012-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4012-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4012-131">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="e4012-131">-Enable</span></span>
<span data-ttu-id="e4012-132">Se houver, habilite um segredo se value for true.</span><span class="sxs-lookup"><span data-stu-id="e4012-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="e4012-133">Desabilite um segredo se o valor for falso.</span><span class="sxs-lookup"><span data-stu-id="e4012-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="e4012-134">Se não for especificado, o valor existente do estado Enabled/Disabled do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="e4012-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4012-135">-Expira em</span><span class="sxs-lookup"><span data-stu-id="e4012-135">-Expires</span></span>
<span data-ttu-id="e4012-136">O tempo de expiração de um segredo na hora UTC.</span><span class="sxs-lookup"><span data-stu-id="e4012-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="e4012-137">Se não for especificado, o valor existente do tempo de expiração do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="e4012-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="e4012-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4012-138">-InputObject</span></span>
<span data-ttu-id="e4012-139">Objeto secreto</span><span class="sxs-lookup"><span data-stu-id="e4012-139">Secret object</span></span>

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

### <span data-ttu-id="e4012-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4012-140">-Name</span></span>
<span data-ttu-id="e4012-141">Nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="e4012-141">Secret name.</span></span>
<span data-ttu-id="e4012-142">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="e4012-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="e4012-143">-Não antes</span><span class="sxs-lookup"><span data-stu-id="e4012-143">-NotBefore</span></span>
<span data-ttu-id="e4012-144">A hora UTC antes da qual o segredo não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="e4012-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="e4012-145">Se não for especificado, o valor existente do atributo não before do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="e4012-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="e4012-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4012-146">-PassThru</span></span>
<span data-ttu-id="e4012-147">O cmdlet não retorna objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="e4012-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="e4012-148">Se essa opção for especificada, retorne o objeto secreto.</span><span class="sxs-lookup"><span data-stu-id="e4012-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="e4012-149">-Marca</span><span class="sxs-lookup"><span data-stu-id="e4012-149">-Tag</span></span>
<span data-ttu-id="e4012-150">Uma Hashtable representando as marcas secretas.</span><span class="sxs-lookup"><span data-stu-id="e4012-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="e4012-151">Se não for especificado, as marcas existentes do segredo permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="e4012-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="e4012-152">Remova uma marca especificando uma Hashtable vazia.</span><span class="sxs-lookup"><span data-stu-id="e4012-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="e4012-153">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="e4012-153">-VaultName</span></span>
<span data-ttu-id="e4012-154">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="e4012-154">Vault name.</span></span>
<span data-ttu-id="e4012-155">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e4012-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e4012-156">-Versão</span><span class="sxs-lookup"><span data-stu-id="e4012-156">-Version</span></span>
<span data-ttu-id="e4012-157">Versão secreta.</span><span class="sxs-lookup"><span data-stu-id="e4012-157">Secret version.</span></span>
<span data-ttu-id="e4012-158">O cmdlet constrói o FQDN de um segredo do nome do cofre, ambiente selecionado atualmente, nome do segredo e versão secreta.</span><span class="sxs-lookup"><span data-stu-id="e4012-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4012-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4012-159">-Confirm</span></span>
<span data-ttu-id="e4012-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4012-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4012-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4012-161">-WhatIf</span></span>
<span data-ttu-id="e4012-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4012-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4012-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4012-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4012-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4012-164">CommonParameters</span></span>
<span data-ttu-id="e4012-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4012-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4012-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4012-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4012-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4012-167">INPUTS</span></span>

### <span data-ttu-id="e4012-168">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e4012-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="e4012-169">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e4012-169">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e4012-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4012-170">OUTPUTS</span></span>

### <span data-ttu-id="e4012-171">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e4012-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="e4012-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4012-172">NOTES</span></span>

## <span data-ttu-id="e4012-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4012-173">RELATED LINKS</span></span>
