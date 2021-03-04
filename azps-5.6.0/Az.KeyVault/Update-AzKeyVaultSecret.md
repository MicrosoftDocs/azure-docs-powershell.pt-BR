---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 975395c471a08eac745bd8a9ab07cec826d5c038
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888493"
---
# <span data-ttu-id="b7903-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7903-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="b7903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7903-102">SYNOPSIS</span></span>
<span data-ttu-id="b7903-103">Atualiza atributos de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b7903-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="b7903-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b7903-104">SYNTAX</span></span>

### <span data-ttu-id="b7903-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b7903-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7903-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7903-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7903-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b7903-107">DESCRIPTION</span></span>
<span data-ttu-id="b7903-108">O cmdlet **Update-AzKeyVaultSecret** atualiza atributos editáveis de um segredo em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="b7903-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="b7903-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7903-109">EXAMPLES</span></span>

### <span data-ttu-id="b7903-110">Exemplo 1: Modificar os atributos de um segredo</span><span class="sxs-lookup"><span data-stu-id="b7903-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="b7903-111">Os quatro primeiros comandos definem atributos para a data de expiração, a data notBefore, as marcas e o tipo de contexto e armazenam os atributos em variáveis.</span><span class="sxs-lookup"><span data-stu-id="b7903-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="b7903-112">O comando final modifica os atributos do segredo chamado HR no cofre de chaves chamado ContosoVault, usando as variáveis armazenadas.</span><span class="sxs-lookup"><span data-stu-id="b7903-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="b7903-113">Exemplo 2: excluir as marcas e o tipo de conteúdo de um segredo</span><span class="sxs-lookup"><span data-stu-id="b7903-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="b7903-114">Este comando exclui as marcas e o tipo de conteúdo da versão especificada do segredo chamado HR no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="b7903-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="b7903-115">Exemplo 3: Desabilitar a versão atual dos segredos cujo nome começa com a IT</span><span class="sxs-lookup"><span data-stu-id="b7903-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="b7903-116">O primeiro comando armazena o valor da cadeia de caracteres Contoso na $Vault variável.</span><span class="sxs-lookup"><span data-stu-id="b7903-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="b7903-117">O segundo comando armazena o valor da cadeia de caracteres IT na $Prefix variável.</span><span class="sxs-lookup"><span data-stu-id="b7903-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="b7903-118">O terceiro comando usa o cmdlet Get-AzKeyVaultSecret para obter os segredos no cofre de chaves especificado e, em seguida, passa esses segredos para o cmdlet **Where-Object.**</span><span class="sxs-lookup"><span data-stu-id="b7903-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="b7903-119">O cmdlet **Where-Object** filtra os segredos de nomes que começam com os caracteres IT.</span><span class="sxs-lookup"><span data-stu-id="b7903-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="b7903-120">O comando canalizará os segredos que corresponderem o filtro ao Update-AzKeyVaultSecret cmdlet, o que os desabilita.</span><span class="sxs-lookup"><span data-stu-id="b7903-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="b7903-121">Exemplo 4: definir o ContentType para todas as versões de um segredo</span><span class="sxs-lookup"><span data-stu-id="b7903-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="b7903-122">Os três primeiros comandos definem variáveis de cadeia de caracteres a ser usadas para os *parâmetros VaultName,* *Name* e *ContentType.*</span><span class="sxs-lookup"><span data-stu-id="b7903-122">The first three commands define string variables to use for the *VaultName*, *Name*, and *ContentType* parameters.</span></span> <span data-ttu-id="b7903-123">O quarto comando usa o cmdlet Get-AzKeyVaultKey para obter as chaves especificadas e canalizou as chaves para o cmdlet Update-AzKeyVaultSecret para definir seu tipo de conteúdo como XML.</span><span class="sxs-lookup"><span data-stu-id="b7903-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="b7903-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b7903-124">PARAMETERS</span></span>

### <span data-ttu-id="b7903-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b7903-125">-ContentType</span></span>
<span data-ttu-id="b7903-126">Tipo de conteúdo de Secret.</span><span class="sxs-lookup"><span data-stu-id="b7903-126">Secret's content type.</span></span>
<span data-ttu-id="b7903-127">Se não for especificado, o valor existente do tipo de conteúdo do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="b7903-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="b7903-128">Remova o valor de tipo de conteúdo existente especificando uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="b7903-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="b7903-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7903-129">-DefaultProfile</span></span>
<span data-ttu-id="b7903-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7903-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7903-131">-Enable</span><span class="sxs-lookup"><span data-stu-id="b7903-131">-Enable</span></span>
<span data-ttu-id="b7903-132">Se presente, habilita um segredo se o valor for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="b7903-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="b7903-133">Desabilite um segredo se o valor for false.</span><span class="sxs-lookup"><span data-stu-id="b7903-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="b7903-134">Se não for especificado, o valor existente do estado habilitado/desabilitado do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="b7903-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="b7903-135">-Expires</span><span class="sxs-lookup"><span data-stu-id="b7903-135">-Expires</span></span>
<span data-ttu-id="b7903-136">O tempo de expiração de um segredo no horário UTC.</span><span class="sxs-lookup"><span data-stu-id="b7903-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="b7903-137">Se não for especificado, o valor existente do tempo de expiração do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="b7903-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

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

### <span data-ttu-id="b7903-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7903-138">-InputObject</span></span>
<span data-ttu-id="b7903-139">Objeto Secret</span><span class="sxs-lookup"><span data-stu-id="b7903-139">Secret object</span></span>

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

### <span data-ttu-id="b7903-140">-Name</span><span class="sxs-lookup"><span data-stu-id="b7903-140">-Name</span></span>
<span data-ttu-id="b7903-141">Nome secreto.</span><span class="sxs-lookup"><span data-stu-id="b7903-141">Secret name.</span></span>
<span data-ttu-id="b7903-142">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.</span><span class="sxs-lookup"><span data-stu-id="b7903-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="b7903-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b7903-143">-NotBefore</span></span>
<span data-ttu-id="b7903-144">O horário UTC antes do qual o segredo não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="b7903-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="b7903-145">Se não for especificado, o valor existente do atributo NotBefore do segredo permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="b7903-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

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

### <span data-ttu-id="b7903-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7903-146">-PassThru</span></span>
<span data-ttu-id="b7903-147">O cmdlet não retorna o objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="b7903-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="b7903-148">Se essa opção for especificada, retorne o objeto Secret.</span><span class="sxs-lookup"><span data-stu-id="b7903-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="b7903-149">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7903-149">-Tag</span></span>
<span data-ttu-id="b7903-150">Uma hashtable que representa marcas secretas.</span><span class="sxs-lookup"><span data-stu-id="b7903-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="b7903-151">Se não for especificado, as marcas existentes do segredo permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="b7903-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="b7903-152">Remova uma marca especificando uma Hashtable vazia.</span><span class="sxs-lookup"><span data-stu-id="b7903-152">Remove a tag by specifying an empty Hashtable.</span></span>

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

### <span data-ttu-id="b7903-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b7903-153">-VaultName</span></span>
<span data-ttu-id="b7903-154">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="b7903-154">Vault name.</span></span>
<span data-ttu-id="b7903-155">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="b7903-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b7903-156">-Version</span><span class="sxs-lookup"><span data-stu-id="b7903-156">-Version</span></span>
<span data-ttu-id="b7903-157">Versão secreta.</span><span class="sxs-lookup"><span data-stu-id="b7903-157">Secret version.</span></span>
<span data-ttu-id="b7903-158">O cmdlet constrói o FQDN de um segredo do nome do cofre, ambiente atualmente selecionado, nome secreto e versão secreta.</span><span class="sxs-lookup"><span data-stu-id="b7903-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

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

### <span data-ttu-id="b7903-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7903-159">-Confirm</span></span>
<span data-ttu-id="b7903-160">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7903-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7903-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7903-161">-WhatIf</span></span>
<span data-ttu-id="b7903-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7903-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7903-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7903-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7903-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7903-164">CommonParameters</span></span>
<span data-ttu-id="b7903-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7903-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7903-166">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7903-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7903-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7903-167">INPUTS</span></span>

### <span data-ttu-id="b7903-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b7903-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="b7903-169">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b7903-169">OUTPUTS</span></span>

### <span data-ttu-id="b7903-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b7903-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="b7903-171">NOTES</span><span class="sxs-lookup"><span data-stu-id="b7903-171">NOTES</span></span>

## <span data-ttu-id="b7903-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7903-172">RELATED LINKS</span></span>
