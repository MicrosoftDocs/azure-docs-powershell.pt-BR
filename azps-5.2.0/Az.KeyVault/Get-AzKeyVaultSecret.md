---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 18b87f6a83f335958e9c10e392d859ae307e9e87
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262867"
---
# <span data-ttu-id="958b3-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="958b3-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="958b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="958b3-102">SYNOPSIS</span></span>
<span data-ttu-id="958b3-103">Obtém os segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="958b3-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="958b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="958b3-104">SYNTAX</span></span>

### <span data-ttu-id="958b3-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="958b3-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="958b3-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="958b3-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="958b3-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="958b3-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="958b3-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="958b3-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="958b3-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="958b3-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="958b3-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="958b3-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="958b3-114">DESCRIPTION</span></span>
<span data-ttu-id="958b3-115">O cmdlet **Get-AzKeyVaultSecret** Obtém segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="958b3-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="958b3-116">Esse cmdlet obtém um segredo específico ou todos os segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="958b3-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="958b3-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="958b3-117">EXAMPLES</span></span>

### <span data-ttu-id="958b3-118">Exemplo 1: obter todas as versões atuais de todos os segredos em um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="958b3-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="958b3-119">Esse comando obtém as versões atuais de todos os segredos no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="958b3-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="958b3-120">Exemplo 2: obter todas as versões de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="958b3-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="958b3-121">Este comando obtém todas as versões do segredo chamado secret1 no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="958b3-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="958b3-122">Exemplo 3: obter a versão atual de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="958b3-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="958b3-123">Esse comando obtém a versão atual do segredo chamado secret1 no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="958b3-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="958b3-124">Exemplo 4: obter uma versão específica de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="958b3-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="958b3-125">Esse comando obtém uma versão específica do segredo chamado secret1 no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="958b3-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="958b3-126">Exemplo 5: obter o valor de texto sem formatação da versão atual de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="958b3-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'

# Method 1: requires PowerShell >= 7.0
PS C:\> $secretInPlainText = $secret.SecretValue | ConvertFrom-SecureString -AsPlainText

# Method 2: works on older PowerShell versions
PS C:\> $secretValueText = '';
PS C:\> $ssPtr = [System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue)
PS C:\> try {
    $secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR($ssPtr)
} finally {
    [System.Runtime.InteropServices.Marshal]::ZeroFreeBSTR($ssPtr)
}

# Method 3: works in ConstrainedLanguage mode
$secretInPlainText = [pscredential]::new("DoesntMatter", $secret.SecretValue).GetNetworkCredential().Password
```

<span data-ttu-id="958b3-127">Esses comandos obtêm a versão atual de um segredo chamado ITSecret e exibem o valor de texto sem formatação desse segredo.</span><span class="sxs-lookup"><span data-stu-id="958b3-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

<span data-ttu-id="958b3-128">(Observação: Use o método 3 se você estiver trabalhando no [modo de ConstrainedLanguage](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language)do PowerShell, por exemplo, em estações de trabalho do Access seguras/privilegiadas.)</span><span class="sxs-lookup"><span data-stu-id="958b3-128">(Note: use method 3 if you are working in PowerShell [ConstrainedLanguage mode](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_language_modes?view=powershell-7.1#constrained-language-constrained-language), for example, on secure/privileged access workstations.)</span></span>

### <span data-ttu-id="958b3-129">Exemplo 6: obter todos os segredos que foram excluídos, mas não foram removidos para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="958b3-129">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="958b3-130">Esse comando obtém todos os segredos que foram excluídos anteriormente, mas não foram removidos, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="958b3-130">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="958b3-131">Exemplo 7: Obtém a ITSecret secreta que foi excluída, mas não é eliminada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="958b3-131">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="958b3-132">Esse comando obtém o segredo ' secret1 ' que foi excluído anteriormente, mas não foi removido, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="958b3-132">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="958b3-133">Esse comando retornará metadados como a data de exclusão e a data de descarte programada desse segredo excluído.</span><span class="sxs-lookup"><span data-stu-id="958b3-133">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="958b3-134">Exemplo 8: obter todas as versões atuais de todos os segredos em um cofre de chaves usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="958b3-134">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultSecret -VaultName 'Contoso' -Name "secret*"

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="958b3-135">Esse comando obtém as versões atuais de todos os segredos no cofre de chaves chamado contoso que começam com "Secret".</span><span class="sxs-lookup"><span data-stu-id="958b3-135">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="958b3-136">OS</span><span class="sxs-lookup"><span data-stu-id="958b3-136">PARAMETERS</span></span>

### <span data-ttu-id="958b3-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="958b3-137">-DefaultProfile</span></span>
<span data-ttu-id="958b3-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="958b3-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="958b3-139">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="958b3-139">-IncludeVersions</span></span>
<span data-ttu-id="958b3-140">Indica que esse cmdlet obtém todas as versões de um segredo.</span><span class="sxs-lookup"><span data-stu-id="958b3-140">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="958b3-141">A versão atual de um segredo é a primeira na lista.</span><span class="sxs-lookup"><span data-stu-id="958b3-141">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="958b3-142">Se você especificar esse parâmetro, também deverá especificar o *nome* e os parâmetros de *cofrename* .</span><span class="sxs-lookup"><span data-stu-id="958b3-142">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="958b3-143">Se você não especificar o parâmetro *IncludeVersions* , esse cmdlet obtém a versão atual do segredo com o *nome* especificado.</span><span class="sxs-lookup"><span data-stu-id="958b3-143">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958b3-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="958b3-144">-InputObject</span></span>
<span data-ttu-id="958b3-145">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="958b3-145">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="958b3-146">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="958b3-146">-InRemovedState</span></span>
<span data-ttu-id="958b3-147">Especifica se os segredos excluídos anteriormente na saída devem ser mostrados</span><span class="sxs-lookup"><span data-stu-id="958b3-147">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958b3-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="958b3-148">-Name</span></span>
<span data-ttu-id="958b3-149">Especifica o nome do segredo a obter.</span><span class="sxs-lookup"><span data-stu-id="958b3-149">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="958b3-150">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="958b3-150">-ResourceId</span></span>
<span data-ttu-id="958b3-151">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="958b3-151">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="958b3-152">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="958b3-152">-VaultName</span></span>
<span data-ttu-id="958b3-153">Especifica o nome do cofre de chaves ao qual o segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="958b3-153">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="958b3-154">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome que esse parâmetro especifica e seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="958b3-154">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958b3-155">-Versão</span><span class="sxs-lookup"><span data-stu-id="958b3-155">-Version</span></span>
<span data-ttu-id="958b3-156">Especifica a versão secreta.</span><span class="sxs-lookup"><span data-stu-id="958b3-156">Specifies the secret version.</span></span>
<span data-ttu-id="958b3-157">Esse cmdlet constrói o FQDN de um segredo com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do segredo e na versão secreta.</span><span class="sxs-lookup"><span data-stu-id="958b3-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="958b3-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="958b3-158">CommonParameters</span></span>
<span data-ttu-id="958b3-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="958b3-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="958b3-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="958b3-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="958b3-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="958b3-161">INPUTS</span></span>

### <span data-ttu-id="958b3-162">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="958b3-162">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="958b3-163">System. String</span><span class="sxs-lookup"><span data-stu-id="958b3-163">System.String</span></span>

## <span data-ttu-id="958b3-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="958b3-164">OUTPUTS</span></span>

### <span data-ttu-id="958b3-165">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="958b3-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="958b3-166">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="958b3-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="958b3-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="958b3-167">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="958b3-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="958b3-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="958b3-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="958b3-169">NOTES</span></span>

## <span data-ttu-id="958b3-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="958b3-170">RELATED LINKS</span></span>

[<span data-ttu-id="958b3-171">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="958b3-171">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="958b3-172">Desfazer-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="958b3-172">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="958b3-173">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="958b3-173">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

