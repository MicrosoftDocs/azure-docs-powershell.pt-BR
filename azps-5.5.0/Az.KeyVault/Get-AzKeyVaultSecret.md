---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultSecret.md
ms.openlocfilehash: 6824777d5df0f06705f4c10c4af248f1f8e8714a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118968"
---
# <span data-ttu-id="5b093-101">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5b093-101">Get-AzKeyVaultSecret</span></span>

## <span data-ttu-id="5b093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b093-102">SYNOPSIS</span></span>
<span data-ttu-id="5b093-103">Obtém os segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b093-103">Gets the secrets in a key vault.</span></span>

## <span data-ttu-id="5b093-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b093-104">SYNTAX</span></span>

### <span data-ttu-id="5b093-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b093-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-106">BySecsecname</span><span class="sxs-lookup"><span data-stu-id="5b093-106">BySecretName</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-107">BySecversãos</span><span class="sxs-lookup"><span data-stu-id="5b093-107">BySecretVersions</span></span>
```
Get-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="5b093-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-109">ByInputObjectSecsecsecname</span><span class="sxs-lookup"><span data-stu-id="5b093-109">ByInputObjectSecretName</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-110">ByInputObjectSecversãos</span><span class="sxs-lookup"><span data-stu-id="5b093-110">ByInputObjectSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="5b093-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-112">ByResourceIdSecsecname</span><span class="sxs-lookup"><span data-stu-id="5b093-112">ByResourceIdSecretName</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String> [-AsPlainText]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b093-113">ByResourceIdSecversãos</span><span class="sxs-lookup"><span data-stu-id="5b093-113">ByResourceIdSecretVersions</span></span>
```
Get-AzKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b093-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b093-114">DESCRIPTION</span></span>
<span data-ttu-id="5b093-115">O cmdlet **Get-AzKeyVaultSec ltda obtém** segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b093-115">The **Get-AzKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="5b093-116">Este cmdlet obtém um segredo específico ou todos os segredos em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b093-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="5b093-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b093-117">EXAMPLES</span></span>

### <span data-ttu-id="5b093-118">Exemplo 1: Obter todas as versões atuais de todos os segredos em um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="5b093-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
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

<span data-ttu-id="5b093-119">Esse comando obtém as versões atuais de todos os segredos no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5b093-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="5b093-120">Exemplo 2: Obter todas as versões de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="5b093-120">Example 2: Get all versions of a specific secret</span></span>
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

<span data-ttu-id="5b093-121">Esse comando obtém todas as versões do segredo denominado secret1 no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5b093-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="5b093-122">Exemplo 3: Obter a versão atual de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="5b093-122">Example 3: Get the current version of a specific secret</span></span>
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

<span data-ttu-id="5b093-123">Esse comando obtém a versão atual do segredo chamado secret1 no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5b093-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="5b093-124">Exemplo 4: Obter uma versão específica de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="5b093-124">Example 4: Get a specific version of a specific secret</span></span>
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

<span data-ttu-id="5b093-125">Esse comando obtém uma versão específica do segredo chamado secret1 no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5b093-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="5b093-126">Exemplo 5: Obter o valor de texto sem texto da versão atual de um segredo específico</span><span class="sxs-lookup"><span data-stu-id="5b093-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secretText = Get-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -AsPlainText
```

<span data-ttu-id="5b093-127">O cmdlet retorna o segredo como uma cadeia de caracteres quando `-AsPlainText` é aplicado.</span><span class="sxs-lookup"><span data-stu-id="5b093-127">The cmdlet returns the secret as a string when `-AsPlainText` is applied.</span></span>

### <span data-ttu-id="5b093-128">Exemplo 6: Obter todos os segredos que foram excluídos, mas não limpos para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b093-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="5b093-129">Esse comando obtém todos os segredos que foram excluídos anteriormente, mas não limpos, no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5b093-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="5b093-130">Exemplo 7: Obtém o ITSecsecsec secreto que foi excluído, mas não limpo para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5b093-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="5b093-131">Esse comando obtém o segredo "secret1" que foi excluído anteriormente, mas não limpo, no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="5b093-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="5b093-132">Esse comando retornará metadados como a data de exclusão e a data de purgação agendada desse segredo excluído.</span><span class="sxs-lookup"><span data-stu-id="5b093-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

### <span data-ttu-id="5b093-133">Exemplo 8: Obter todas as versões atuais de todos os segredos em um cofre de chaves usando filtragem</span><span class="sxs-lookup"><span data-stu-id="5b093-133">Example 8: Get all current versions of all secrets in a key vault using filtering</span></span>
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

<span data-ttu-id="5b093-134">Esse comando obtém as versões atuais de todos os segredos no cofre de chaves chamado Contoso que começam com "segredo".</span><span class="sxs-lookup"><span data-stu-id="5b093-134">This command gets the current versions of all secrets in the key vault named Contoso that start with "secret".</span></span>

## <span data-ttu-id="5b093-135">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b093-135">PARAMETERS</span></span>

### <span data-ttu-id="5b093-136">-AsPlainText</span><span class="sxs-lookup"><span data-stu-id="5b093-136">-AsPlainText</span></span>
<span data-ttu-id="5b093-137">Quando definido, o cmdlet converterá em segredo na cadeia de caracteres segura para a cadeia de texto sem formatação descriptografada como saída.</span><span class="sxs-lookup"><span data-stu-id="5b093-137">When set, the cmdlet will convert secret in secure string to the decrypted plaintext string as output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, BySecretName, ByInputObjectVaultName, ByInputObjectSecretName, ByResourceIdVaultName, ByResourceIdSecretName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b093-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b093-138">-DefaultProfile</span></span>
<span data-ttu-id="5b093-139">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5b093-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b093-140">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="5b093-140">-IncludeVersions</span></span>
<span data-ttu-id="5b093-141">Indica que esse cmdlet obtém todas as versões de um segredo.</span><span class="sxs-lookup"><span data-stu-id="5b093-141">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="5b093-142">A versão atual de um segredo é a primeira da lista.</span><span class="sxs-lookup"><span data-stu-id="5b093-142">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="5b093-143">Se você especificar esse parâmetro, também deverá especificar os parâmetros *Nome* e *Nomedo* Cofre.</span><span class="sxs-lookup"><span data-stu-id="5b093-143">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="5b093-144">Se você não especificar o parâmetro *IncludeVersions,* este cmdlet obtém a versão atual do segredo com o Nome *especificado.*</span><span class="sxs-lookup"><span data-stu-id="5b093-144">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

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

### <span data-ttu-id="5b093-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b093-145">-InputObject</span></span>
<span data-ttu-id="5b093-146">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5b093-146">KeyVault Object.</span></span>

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

### <span data-ttu-id="5b093-147">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="5b093-147">-InRemovedState</span></span>
<span data-ttu-id="5b093-148">Especifica se você deve mostrar os segredos excluídos anteriormente na saída</span><span class="sxs-lookup"><span data-stu-id="5b093-148">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="5b093-149">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b093-149">-Name</span></span>
<span data-ttu-id="5b093-150">Especifica o nome do segredo a ser obter.</span><span class="sxs-lookup"><span data-stu-id="5b093-150">Specifies the name of the secret to get.</span></span>

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

### <span data-ttu-id="5b093-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b093-151">-ResourceId</span></span>
<span data-ttu-id="5b093-152">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5b093-152">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="5b093-153">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="5b093-153">-VaultName</span></span>
<span data-ttu-id="5b093-154">Especifica o nome do cofre de chave ao qual o segredo pertence.</span><span class="sxs-lookup"><span data-stu-id="5b093-154">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="5b093-155">Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de um cofre de teclas com base no nome especificado por esse parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="5b093-155">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="5b093-156">-Versão</span><span class="sxs-lookup"><span data-stu-id="5b093-156">-Version</span></span>
<span data-ttu-id="5b093-157">Especifica a versão secreta.</span><span class="sxs-lookup"><span data-stu-id="5b093-157">Specifies the secret version.</span></span>
<span data-ttu-id="5b093-158">Este cmdlet construirá o FQDN de um segredo com base no nome do cofre de chave, no ambiente selecionado no momento, no nome secreto e na versão secreta.</span><span class="sxs-lookup"><span data-stu-id="5b093-158">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="5b093-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b093-159">CommonParameters</span></span>
<span data-ttu-id="5b093-160">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b093-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b093-161">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b093-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b093-162">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b093-162">INPUTS</span></span>

### <span data-ttu-id="5b093-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5b093-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5b093-164">System.String</span><span class="sxs-lookup"><span data-stu-id="5b093-164">System.String</span></span>

## <span data-ttu-id="5b093-165">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b093-165">OUTPUTS</span></span>

### <span data-ttu-id="5b093-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecibleIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5b093-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="5b093-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="5b093-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="5b093-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecitorIdentityItem</span><span class="sxs-lookup"><span data-stu-id="5b093-168">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="5b093-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecsec</span><span class="sxs-lookup"><span data-stu-id="5b093-169">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="5b093-170">Notas</span><span class="sxs-lookup"><span data-stu-id="5b093-170">NOTES</span></span>

## <span data-ttu-id="5b093-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b093-171">RELATED LINKS</span></span>

[<span data-ttu-id="5b093-172">Remove-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="5b093-172">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="5b093-173">Desfazer-AzKeyVaultSecanteRemoval</span><span class="sxs-lookup"><span data-stu-id="5b093-173">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

[<span data-ttu-id="5b093-174">Set-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="5b093-174">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

