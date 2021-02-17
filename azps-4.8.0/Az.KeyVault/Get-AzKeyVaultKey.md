---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: e0601285bf2adc7204cd5a946e07d032579e080b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404710"
---
# <span data-ttu-id="18722-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18722-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="18722-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18722-102">SYNOPSIS</span></span>
<span data-ttu-id="18722-103">Obtém as chaves do Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="18722-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="18722-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18722-104">SYNTAX</span></span>

### <span data-ttu-id="18722-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="18722-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="18722-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="18722-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="18722-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="18722-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="18722-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="18722-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="18722-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18722-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="18722-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18722-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="18722-114">DESCRIPTION</span></span>
<span data-ttu-id="18722-115">O **cmdlet Get-AzKeyVaultKey** obtém as teclas do Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="18722-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="18722-116">Este cmdlet obtém um **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** específico ou uma lista de todos os objetos **KeyBundle** em um cofre de teclas ou por versão.</span><span class="sxs-lookup"><span data-stu-id="18722-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="18722-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="18722-117">EXAMPLES</span></span>

### <span data-ttu-id="18722-118">Exemplo 1: Obter todas as chaves em um cofre de chave</span><span class="sxs-lookup"><span data-stu-id="18722-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="18722-119">Esse comando obtém todas as chaves no cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="18722-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="18722-120">Exemplo 2: Obter a versão atual de uma chave</span><span class="sxs-lookup"><span data-stu-id="18722-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="18722-121">Esse comando obtém a versão atual da chave chamada teste1 no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="18722-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="18722-122">Exemplo 3: Obter todas as versões de uma chave</span><span class="sxs-lookup"><span data-stu-id="18722-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="18722-123">Esse comando obtém todas as versões da chave itpfx chamada ITPfx no cofre de teclas chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="18722-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="18722-124">Exemplo 4: Obter uma versão específica de uma chave</span><span class="sxs-lookup"><span data-stu-id="18722-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="18722-125">Esse comando obtém uma versão específica da chave chamada teste1 no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="18722-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="18722-126">Depois de executar esse comando, você pode inspecionar várias propriedades da chave navegando pelo objeto $Key dados.</span><span class="sxs-lookup"><span data-stu-id="18722-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="18722-127">Exemplo 5: Obter todas as chaves que foram excluídas, mas não limpas para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="18722-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="18722-128">Esse comando obtém todas as teclas que foram excluídas anteriormente, mas não limpas, no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="18722-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="18722-129">Exemplo 6: obtém a chave ITPfx que foi excluída, mas não limpa para esse cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="18722-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="18722-130">Esse comando obtém o teste de chave3 que foi excluído anteriormente, mas não limpo, no cofre de chave chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="18722-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="18722-131">Esse comando retornará metadados como a data de exclusão e a data de purgação agendada dessa chave excluída.</span><span class="sxs-lookup"><span data-stu-id="18722-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="18722-132">Exemplo 7: Obter todas as chaves em um cofre de teclas usando filtragem</span><span class="sxs-lookup"><span data-stu-id="18722-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="18722-133">Esse comando obtém todas as chaves no cofre de teclas chamado Contoso que começam com "teste".</span><span class="sxs-lookup"><span data-stu-id="18722-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="18722-134">Exemplo 8: Baixar uma chave pública como um arquivo .pem</span><span class="sxs-lookup"><span data-stu-id="18722-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="18722-135">Você pode baixar a chave pública de uma tecla RSA especificando o `-OutFile` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="18722-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="18722-136">Esta é uma etapa da importação de chaves protegidas por HSM para o Cofre de Teclas do Azure.</span><span class="sxs-lookup"><span data-stu-id="18722-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="18722-137">Ver https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="18722-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="18722-138">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18722-138">PARAMETERS</span></span>

### <span data-ttu-id="18722-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18722-139">-DefaultProfile</span></span>
<span data-ttu-id="18722-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="18722-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18722-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="18722-141">-IncludeVersions</span></span>
<span data-ttu-id="18722-142">Indica que esse cmdlet obtém todas as versões de uma chave.</span><span class="sxs-lookup"><span data-stu-id="18722-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="18722-143">A versão atual de uma chave é a primeira da lista.</span><span class="sxs-lookup"><span data-stu-id="18722-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="18722-144">Se você especificar esse parâmetro, também deverá especificar os parâmetros *Nome* e *Nomedo* Cofre.</span><span class="sxs-lookup"><span data-stu-id="18722-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="18722-145">Se você não especificar o parâmetro *IncludeVersions,* este cmdlet obtém a versão atual da chave com o Nome *especificado.*</span><span class="sxs-lookup"><span data-stu-id="18722-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18722-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18722-146">-InputObject</span></span>
<span data-ttu-id="18722-147">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="18722-147">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18722-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="18722-148">-InRemovedState</span></span>
<span data-ttu-id="18722-149">Especifica se as teclas excluídas anteriormente na saída</span><span class="sxs-lookup"><span data-stu-id="18722-149">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="18722-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="18722-150">-Name</span></span>
<span data-ttu-id="18722-151">Especifica o nome do pacote de chaves a ser obter.</span><span class="sxs-lookup"><span data-stu-id="18722-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18722-152">-OutFile</span><span class="sxs-lookup"><span data-stu-id="18722-152">-OutFile</span></span>
<span data-ttu-id="18722-153">Especifica o arquivo de saída para o qual este cmdlet salva a chave.</span><span class="sxs-lookup"><span data-stu-id="18722-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="18722-154">A chave pública é salva no formato PEM por padrão.</span><span class="sxs-lookup"><span data-stu-id="18722-154">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="18722-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18722-155">-ResourceId</span></span>
<span data-ttu-id="18722-156">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="18722-156">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18722-157">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="18722-157">-VaultName</span></span>
<span data-ttu-id="18722-158">Especifica o nome do cofre de chave do qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="18722-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="18722-159">Este cmdlet construirá o nome de domínio totalmente qualificado (FQDN) de um cofre de teclas com base no nome especificado por esse parâmetro e no ambiente selecionado.</span><span class="sxs-lookup"><span data-stu-id="18722-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18722-160">-Versão</span><span class="sxs-lookup"><span data-stu-id="18722-160">-Version</span></span>
<span data-ttu-id="18722-161">Especifica a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="18722-161">Specifies the key version.</span></span>
<span data-ttu-id="18722-162">Este cmdlet construirá o FQDN de uma chave com base no nome do cofre de chave, no ambiente selecionado no momento, no nome da chave e na versão da chave.</span><span class="sxs-lookup"><span data-stu-id="18722-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18722-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18722-163">CommonParameters</span></span>
<span data-ttu-id="18722-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18722-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18722-165">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="18722-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18722-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="18722-166">INPUTS</span></span>

### <span data-ttu-id="18722-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="18722-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="18722-168">System.String</span><span class="sxs-lookup"><span data-stu-id="18722-168">System.String</span></span>

## <span data-ttu-id="18722-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="18722-169">OUTPUTS</span></span>

### <span data-ttu-id="18722-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="18722-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="18722-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18722-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="18722-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="18722-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="18722-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18722-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="18722-174">Notas</span><span class="sxs-lookup"><span data-stu-id="18722-174">NOTES</span></span>

## <span data-ttu-id="18722-175">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18722-175">RELATED LINKS</span></span>

[<span data-ttu-id="18722-176">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18722-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="18722-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="18722-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="18722-178">Desfazer-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="18722-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)


