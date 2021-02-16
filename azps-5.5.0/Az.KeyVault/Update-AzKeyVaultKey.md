---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113067"
---
# <span data-ttu-id="ac292-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ac292-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="ac292-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac292-102">SYNOPSIS</span></span>
<span data-ttu-id="ac292-103">Atualiza os atributos de uma chave em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="ac292-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac292-104">SYNTAX</span></span>

### <span data-ttu-id="ac292-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ac292-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac292-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="ac292-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac292-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac292-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac292-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac292-108">DESCRIPTION</span></span>
<span data-ttu-id="ac292-109">O cmdlet **Update-AzKeyVaultKey** atualiza os atributos editáveis de uma chave em um cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="ac292-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ac292-110">EXAMPLES</span></span>

### <span data-ttu-id="ac292-111">Exemplo 1: Modificar uma chave para habilita-la e definir a data de vencimento e as marcas</span><span class="sxs-lookup"><span data-stu-id="ac292-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="ac292-112">O primeiro comando cria um **objeto DateTime** usando o cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="ac292-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="ac292-113">Esse objeto especifica um período de dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="ac292-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="ac292-114">O comando armazena essa data na variável $Expires dados.</span><span class="sxs-lookup"><span data-stu-id="ac292-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="ac292-115">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="ac292-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="ac292-116">O segundo comando cria uma variável para armazenar valores de marca de alta gravidade e Contábil.</span><span class="sxs-lookup"><span data-stu-id="ac292-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="ac292-117">O comando final modifica uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="ac292-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="ac292-118">O comando habilita a chave, define o tempo de expiração para o tempo armazenado no $Expires e define as marcas armazenadas no $Tags.</span><span class="sxs-lookup"><span data-stu-id="ac292-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="ac292-119">Exemplo 2: modificar uma chave para excluir todas as marcas</span><span class="sxs-lookup"><span data-stu-id="ac292-119">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="ac292-120">Esses comandos exclui todas as marcas de uma versão específica de uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="ac292-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="ac292-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac292-121">PARAMETERS</span></span>

### <span data-ttu-id="ac292-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac292-122">-DefaultProfile</span></span>
<span data-ttu-id="ac292-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac292-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac292-124">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="ac292-124">-Enable</span></span>
<span data-ttu-id="ac292-125">O valor verdadeiro habilita a chave e um valor de falso desabilita a chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="ac292-126">Se não especificado, o estado habilitado/desabilitado existente permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="ac292-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="ac292-127">-Expira</span><span class="sxs-lookup"><span data-stu-id="ac292-127">-Expires</span></span>
<span data-ttu-id="ac292-128">O tempo de expiração de uma chave no horário UTC.</span><span class="sxs-lookup"><span data-stu-id="ac292-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="ac292-129">Se não especificado, o tempo de expiração existente da chave permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="ac292-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="ac292-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="ac292-130">-HsmName</span></span>
<span data-ttu-id="ac292-131">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="ac292-131">HSM name.</span></span> <span data-ttu-id="ac292-132">O Cmdlet construirá o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ac292-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac292-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac292-133">-InputObject</span></span>
<span data-ttu-id="ac292-134">Objeto-chave</span><span class="sxs-lookup"><span data-stu-id="ac292-134">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac292-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="ac292-135">-KeyOps</span></span>
<span data-ttu-id="ac292-136">As operações que podem ser executadas com a chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="ac292-137">Se não especificado, as operações de chave existentes da chave permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="ac292-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="ac292-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac292-138">-Name</span></span>
<span data-ttu-id="ac292-139">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-139">Key name.</span></span>
<span data-ttu-id="ac292-140">O Cmdlet construirá o FQDN de uma chave do nome do cofre, ambiente selecionado no momento e nome da chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac292-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ac292-141">-NotBefore</span></span>
<span data-ttu-id="ac292-142">O horário UTC antes do qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="ac292-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="ac292-143">Se não especificado, o atributo NotBefore existente da chave permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="ac292-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="ac292-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac292-144">-PassThru</span></span>
<span data-ttu-id="ac292-145">O Cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="ac292-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ac292-146">Se essa opção for especificada, retornará o objeto do pacote de chaves atualizado.</span><span class="sxs-lookup"><span data-stu-id="ac292-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="ac292-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="ac292-147">-Tag</span></span>
<span data-ttu-id="ac292-148">Uma tabela hash representa marcas-chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="ac292-149">Se não especificado, as marcas existentes da chave permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="ac292-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="ac292-150">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="ac292-150">-VaultName</span></span>
<span data-ttu-id="ac292-151">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="ac292-151">Vault name.</span></span>
<span data-ttu-id="ac292-152">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ac292-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ac292-153">-Versão</span><span class="sxs-lookup"><span data-stu-id="ac292-153">-Version</span></span>
<span data-ttu-id="ac292-154">Versão principal.</span><span class="sxs-lookup"><span data-stu-id="ac292-154">Key version.</span></span>
<span data-ttu-id="ac292-155">O Cmdlet construirá o FQDN de uma chave do nome do cofre, ambiente selecionado no momento, nome da chave e versão de chave.</span><span class="sxs-lookup"><span data-stu-id="ac292-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac292-156">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ac292-156">-Confirm</span></span>
<span data-ttu-id="ac292-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac292-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac292-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac292-158">-WhatIf</span></span>
<span data-ttu-id="ac292-159">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ac292-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac292-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ac292-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac292-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac292-161">CommonParameters</span></span>
<span data-ttu-id="ac292-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac292-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac292-163">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac292-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac292-164">Entradas</span><span class="sxs-lookup"><span data-stu-id="ac292-164">INPUTS</span></span>

### <span data-ttu-id="ac292-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ac292-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="ac292-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="ac292-166">OUTPUTS</span></span>

### <span data-ttu-id="ac292-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ac292-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="ac292-168">Notas</span><span class="sxs-lookup"><span data-stu-id="ac292-168">NOTES</span></span>

## <span data-ttu-id="ac292-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac292-169">RELATED LINKS</span></span>
