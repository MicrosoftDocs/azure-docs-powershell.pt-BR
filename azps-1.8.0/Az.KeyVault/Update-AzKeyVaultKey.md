---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: fb27aead0c45270a04c7a9f7f0c97eaa9d83cc08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770586"
---
# <span data-ttu-id="3f891-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3f891-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="3f891-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f891-102">SYNOPSIS</span></span>
<span data-ttu-id="3f891-103">Atualiza os atributos de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3f891-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="3f891-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f891-104">SYNTAX</span></span>

### <span data-ttu-id="3f891-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f891-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f891-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3f891-106">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f891-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f891-107">DESCRIPTION</span></span>
<span data-ttu-id="3f891-108">O cmdlet **Update-AzKeyVaultKey** atualiza os atributos editáveis de uma chave em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3f891-108">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="3f891-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f891-109">EXAMPLES</span></span>

### <span data-ttu-id="3f891-110">Exemplo 1: modificar uma chave para habilitá-la e definir a data de expiração e as marcas</span><span class="sxs-lookup"><span data-stu-id="3f891-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
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

<span data-ttu-id="3f891-111">O primeiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="3f891-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="3f891-112">Esse objeto especifica um tempo dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="3f891-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="3f891-113">O comando armazena essa data na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="3f891-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="3f891-114">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="3f891-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="3f891-115">O segundo comando cria uma variável para armazenar valores de marca de alta gravidade e contabilidade.</span><span class="sxs-lookup"><span data-stu-id="3f891-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="3f891-116">O comando final modifica uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="3f891-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="3f891-117">O comando habilita a chave, define seu tempo de expiração para a hora armazenada em $Expires e define as marcas armazenadas no $Tags.</span><span class="sxs-lookup"><span data-stu-id="3f891-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="3f891-118">Exemplo 2: modificar uma tecla para excluir todas as marcas</span><span class="sxs-lookup"><span data-stu-id="3f891-118">Example 2: Modify a key to delete all tags</span></span>
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

<span data-ttu-id="3f891-119">Esses comandos excluem todas as marcas para uma versão específica de uma chave chamada ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="3f891-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="3f891-120">OS</span><span class="sxs-lookup"><span data-stu-id="3f891-120">PARAMETERS</span></span>

### <span data-ttu-id="3f891-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f891-121">-DefaultProfile</span></span>
<span data-ttu-id="3f891-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f891-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f891-123">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="3f891-123">-Enable</span></span>
<span data-ttu-id="3f891-124">O valor de true permite que a chave e um valor false desativassem a chave.</span><span class="sxs-lookup"><span data-stu-id="3f891-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="3f891-125">Se não for especificado, o estado Enabled/Disabled existente permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="3f891-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="3f891-126">-Expira em</span><span class="sxs-lookup"><span data-stu-id="3f891-126">-Expires</span></span>
<span data-ttu-id="3f891-127">O tempo de expiração de uma chave no horário UTC.</span><span class="sxs-lookup"><span data-stu-id="3f891-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="3f891-128">Se não for especificado, o tempo de expiração existente da chave permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="3f891-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="3f891-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f891-129">-InputObject</span></span>
<span data-ttu-id="3f891-130">Objeto-chave</span><span class="sxs-lookup"><span data-stu-id="3f891-130">Key object</span></span>

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

### <span data-ttu-id="3f891-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="3f891-131">-KeyOps</span></span>
<span data-ttu-id="3f891-132">As operações que podem ser executadas com a chave.</span><span class="sxs-lookup"><span data-stu-id="3f891-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="3f891-133">Se não for especificado, as operações de chave existentes da chave permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="3f891-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="3f891-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f891-134">-Name</span></span>
<span data-ttu-id="3f891-135">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="3f891-135">Key name.</span></span>
<span data-ttu-id="3f891-136">O cmdlet constrói o FQDN de uma chave do nome do cofre, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="3f891-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f891-137">-Não antes</span><span class="sxs-lookup"><span data-stu-id="3f891-137">-NotBefore</span></span>
<span data-ttu-id="3f891-138">A hora UTC antes da qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="3f891-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="3f891-139">Se não for especificado, o atributo nobefore existente da chave permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="3f891-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="3f891-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f891-140">-PassThru</span></span>
<span data-ttu-id="3f891-141">O cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="3f891-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3f891-142">Se essa opção for especificada, retornará o objeto do pacote de chaves atualizado.</span><span class="sxs-lookup"><span data-stu-id="3f891-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="3f891-143">-Marca</span><span class="sxs-lookup"><span data-stu-id="3f891-143">-Tag</span></span>
<span data-ttu-id="3f891-144">Uma Hashtable representa as marcas de tecla.</span><span class="sxs-lookup"><span data-stu-id="3f891-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="3f891-145">Se não for especificado, as marcas existentes da tecla permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="3f891-145">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="3f891-146">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="3f891-146">-VaultName</span></span>
<span data-ttu-id="3f891-147">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="3f891-147">Vault name.</span></span>
<span data-ttu-id="3f891-148">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="3f891-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3f891-149">-Versão</span><span class="sxs-lookup"><span data-stu-id="3f891-149">-Version</span></span>
<span data-ttu-id="3f891-150">Versão principal.</span><span class="sxs-lookup"><span data-stu-id="3f891-150">Key version.</span></span>
<span data-ttu-id="3f891-151">O cmdlet constrói o FQDN de uma chave do nome do cofre, o ambiente selecionado no momento, o nome da chave e a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="3f891-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="3f891-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3f891-152">-Confirm</span></span>
<span data-ttu-id="3f891-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f891-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f891-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f891-154">-WhatIf</span></span>
<span data-ttu-id="3f891-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3f891-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f891-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3f891-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f891-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f891-157">CommonParameters</span></span>
<span data-ttu-id="3f891-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f891-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f891-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f891-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f891-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f891-160">INPUTS</span></span>

### <span data-ttu-id="3f891-161">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3f891-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="3f891-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f891-162">OUTPUTS</span></span>

### <span data-ttu-id="3f891-163">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3f891-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="3f891-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f891-164">NOTES</span></span>

## <span data-ttu-id="3f891-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f891-165">RELATED LINKS</span></span>
