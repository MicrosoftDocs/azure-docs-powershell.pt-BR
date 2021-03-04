---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 81276c0896d6cb6685d3ce3ee71bb72cb39b690a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885864"
---
# <span data-ttu-id="bb2a5-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a5-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="bb2a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb2a5-103">Obtém chaves do Cofre de Chaves.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="bb2a5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb2a5-104">SYNTAX</span></span>

### <span data-ttu-id="bb2a5-105">ByVaultName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb2a5-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bb2a5-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bb2a5-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bb2a5-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bb2a5-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bb2a5-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -ResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb2a5-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="bb2a5-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb2a5-123">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb2a5-123">DESCRIPTION</span></span>
<span data-ttu-id="bb2a5-124">O cmdlet **Get-AzKeyVaultKey** obtém as chaves do Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="bb2a5-125">Este cmdlet obtém um **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** ou uma lista de todos os objetos **KeyBundle** em um cofre de chaves ou por versão.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="bb2a5-126">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb2a5-126">EXAMPLES</span></span>

### <span data-ttu-id="bb2a5-127">Exemplo 1: Obter todas as chaves em um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="bb2a5-127">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="bb2a5-128">Este comando obtém todas as chaves do cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="bb2a5-129">Exemplo 2: Obter a versão atual de uma chave</span><span class="sxs-lookup"><span data-stu-id="bb2a5-129">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="bb2a5-130">Este comando obtém a versão atual da chave chamada test1 no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="bb2a5-131">Exemplo 3: Obter todas as versões de uma chave</span><span class="sxs-lookup"><span data-stu-id="bb2a5-131">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="bb2a5-132">Este comando obtém todas as versões da chave chamada ITPfx no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="bb2a5-133">Exemplo 4: Obter uma versão específica de uma chave</span><span class="sxs-lookup"><span data-stu-id="bb2a5-133">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="bb2a5-134">Este comando obtém uma versão específica da chave chamada test1 no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="bb2a5-135">Depois de executar esse comando, você pode inspecionar várias propriedades da chave navegando o objeto $Key.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="bb2a5-136">Exemplo 5: Obter todas as chaves que foram excluídas, mas não limpas para este cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="bb2a5-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
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

<span data-ttu-id="bb2a5-137">Este comando obtém todas as chaves que foram excluídas anteriormente, mas não limpas, no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="bb2a5-138">Exemplo 6: obtém a chave ITPfx que foi excluída, mas não limpa para esse cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="bb2a5-139">Este comando obtém o teste de chave3 que foi excluído anteriormente, mas não limpo, no cofre de chaves chamado Contoso.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="bb2a5-140">Este comando retornará metadados, como a data de exclusão e a data de exclusão agendada dessa chave excluída.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="bb2a5-141">Exemplo 7: Obter todas as chaves em um cofre de chaves usando filtragem</span><span class="sxs-lookup"><span data-stu-id="bb2a5-141">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="bb2a5-142">Este comando obtém todas as chaves no cofre de chaves chamada Contoso que começam com "test".</span><span class="sxs-lookup"><span data-stu-id="bb2a5-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="bb2a5-143">Exemplo 8: Baixar uma chave pública como um arquivo .pem</span><span class="sxs-lookup"><span data-stu-id="bb2a5-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="bb2a5-144">Você pode baixar a chave pública de uma chave RSA especificando o `-OutFile` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="bb2a5-145">Esta é uma etapa da importação de chaves protegidas por HSM para o Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="bb2a5-146">Consulte https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="bb2a5-146">See https://docs.microsoft.com/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="bb2a5-147">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb2a5-147">PARAMETERS</span></span>

### <span data-ttu-id="bb2a5-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb2a5-148">-DefaultProfile</span></span>
<span data-ttu-id="bb2a5-149">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="bb2a5-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb2a5-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-150">-HsmName</span></span>
<span data-ttu-id="bb2a5-151">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-151">HSM name.</span></span> <span data-ttu-id="bb2a5-152">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a5-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="bb2a5-153">-HsmObject</span></span>
<span data-ttu-id="bb2a5-154">Objeto HSM.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a5-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="bb2a5-155">-HsmResourceId</span></span>
<span data-ttu-id="bb2a5-156">ID de Recurso HSM.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a5-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="bb2a5-157">-IncludeVersions</span></span>
<span data-ttu-id="bb2a5-158">Indica que esse cmdlet obtém todas as versões de uma chave.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="bb2a5-159">A versão atual de uma chave é a primeira da lista.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="bb2a5-160">Se você especificar esse parâmetro, também deverá especificar os parâmetros *Name* e *VaultName.*</span><span class="sxs-lookup"><span data-stu-id="bb2a5-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="bb2a5-161">Se você não especificar o *parâmetro IncludeVersions,* este cmdlet obtém a versão atual da chave com o *Nome especificado*.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a5-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb2a5-162">-InputObject</span></span>
<span data-ttu-id="bb2a5-163">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-163">KeyVault object.</span></span>

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

### <span data-ttu-id="bb2a5-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="bb2a5-164">-InRemovedState</span></span>
<span data-ttu-id="bb2a5-165">Especifica se as teclas excluídas anteriormente serão mostradas na saída</span><span class="sxs-lookup"><span data-stu-id="bb2a5-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a5-166">-Name</span><span class="sxs-lookup"><span data-stu-id="bb2a5-166">-Name</span></span>
<span data-ttu-id="bb2a5-167">Especifica o nome do pacote de chaves a ser obter.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="bb2a5-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="bb2a5-168">-OutFile</span></span>
<span data-ttu-id="bb2a5-169">Especifica o arquivo de saída para o qual esse cmdlet salva a chave.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="bb2a5-170">A chave pública é salva no formato PEM por padrão.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-170">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="bb2a5-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb2a5-171">-ResourceId</span></span>
<span data-ttu-id="bb2a5-172">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-172">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a5-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="bb2a5-173">-VaultName</span></span>
<span data-ttu-id="bb2a5-174">Especifica o nome do cofre de chaves do qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="bb2a5-175">Este cmdlet constrói o FQDN (nome de domínio totalmente qualificado) de um cofre de chaves com base no nome especificado por esse parâmetro e no ambiente selecionado.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="bb2a5-176">-Version</span><span class="sxs-lookup"><span data-stu-id="bb2a5-176">-Version</span></span>
<span data-ttu-id="bb2a5-177">Especifica a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-177">Specifies the key version.</span></span>
<span data-ttu-id="bb2a5-178">Este cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado no momento, no nome da chave e na versão da chave.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb2a5-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb2a5-179">CommonParameters</span></span>
<span data-ttu-id="bb2a5-180">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb2a5-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb2a5-181">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb2a5-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb2a5-182">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb2a5-182">INPUTS</span></span>

### <span data-ttu-id="bb2a5-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="bb2a5-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="bb2a5-184">System.String</span><span class="sxs-lookup"><span data-stu-id="bb2a5-184">System.String</span></span>

## <span data-ttu-id="bb2a5-185">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb2a5-185">OUTPUTS</span></span>

### <span data-ttu-id="bb2a5-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bb2a5-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bb2a5-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a5-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="bb2a5-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="bb2a5-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="bb2a5-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a5-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="bb2a5-190">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb2a5-190">NOTES</span></span>

## <span data-ttu-id="bb2a5-191">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb2a5-191">RELATED LINKS</span></span>

[<span data-ttu-id="bb2a5-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a5-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="bb2a5-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bb2a5-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="bb2a5-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="bb2a5-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="bb2a5-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="bb2a5-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

