---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 21d2f6efa039dbd9b229562fcefd53c715f400fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596196"
---
# <span data-ttu-id="6f226-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f226-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="6f226-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f226-102">SYNOPSIS</span></span>
<span data-ttu-id="6f226-103">Obtém chaves do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6f226-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="6f226-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f226-104">SYNTAX</span></span>

### <span data-ttu-id="6f226-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f226-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="6f226-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="6f226-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="6f226-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="6f226-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="6f226-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="6f226-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="6f226-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f226-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="6f226-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f226-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f226-114">DESCRIPTION</span></span>
<span data-ttu-id="6f226-115">O cmdlet **Get-AzKeyVaultKey** Obtém as chaves do cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="6f226-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="6f226-116">Esse cmdlet obtém um determinado **Microsoft. Azure. Commands. subvault. Models. keybundle** ou uma lista de todos os objetos **keybundle** em um cofre de chaves ou por versão.</span><span class="sxs-lookup"><span data-stu-id="6f226-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="6f226-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f226-117">EXAMPLES</span></span>

### <span data-ttu-id="6f226-118">Exemplo 1: obter todas as chaves em um cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="6f226-118">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="6f226-119">Esse comando obtém todas as chaves no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="6f226-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="6f226-120">Exemplo 2: obter a versão atual de uma chave</span><span class="sxs-lookup"><span data-stu-id="6f226-120">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="6f226-121">Esse comando obtém a versão atual da chave chamada Test1 no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="6f226-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="6f226-122">Exemplo 3: obter todas as versões de uma chave</span><span class="sxs-lookup"><span data-stu-id="6f226-122">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="6f226-123">Este comando obtém todas as versões a chave chamada ITPfx na chave vaultnamed contoso.</span><span class="sxs-lookup"><span data-stu-id="6f226-123">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="6f226-124">Exemplo 4: obter uma versão específica de uma chave</span><span class="sxs-lookup"><span data-stu-id="6f226-124">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="6f226-125">Esse comando obtém uma versão específica da chave chamada Test1 no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="6f226-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="6f226-126">Depois de executar esse comando, você pode inspecionar várias propriedades da chave navegando no objeto $Key.</span><span class="sxs-lookup"><span data-stu-id="6f226-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="6f226-127">Exemplo 5: obter todas as chaves que foram excluídas, mas não eliminadas para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6f226-127">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="6f226-128">Esse comando obtém todas as chaves que foram excluídas anteriormente, mas não foram limpas, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="6f226-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="6f226-129">Exemplo 6: Obtém a chave ITPfx que foi excluída, mas não é eliminada para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6f226-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="6f226-130">Esse comando obtém a chave test3 que foi excluída anteriormente, mas não foi eliminada, no cofre de chaves chamado contoso.</span><span class="sxs-lookup"><span data-stu-id="6f226-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="6f226-131">Esse comando retornará metadados como a data de exclusão e a data de descarte programada dessa chave excluída.</span><span class="sxs-lookup"><span data-stu-id="6f226-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="6f226-132">Exemplo 7: obter todas as chaves em um cofre de chaves usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="6f226-132">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="6f226-133">Esse comando obtém todas as chaves no cofre de chaves chamada contoso que começam com "Test".</span><span class="sxs-lookup"><span data-stu-id="6f226-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

## <span data-ttu-id="6f226-134">OS</span><span class="sxs-lookup"><span data-stu-id="6f226-134">PARAMETERS</span></span>

### <span data-ttu-id="6f226-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f226-135">-DefaultProfile</span></span>
<span data-ttu-id="6f226-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6f226-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f226-137">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="6f226-137">-IncludeVersions</span></span>
<span data-ttu-id="6f226-138">Indica que esse cmdlet obtém todas as versões de uma chave.</span><span class="sxs-lookup"><span data-stu-id="6f226-138">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="6f226-139">A versão atual de uma chave é a primeira na lista.</span><span class="sxs-lookup"><span data-stu-id="6f226-139">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="6f226-140">Se você especificar esse parâmetro, também deverá especificar o *nome* e os parâmetros de *cofrename* .</span><span class="sxs-lookup"><span data-stu-id="6f226-140">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="6f226-141">Se você não especificar o parâmetro *IncludeVersions* , esse cmdlet obtém a versão atual da chave com o *nome* especificado.</span><span class="sxs-lookup"><span data-stu-id="6f226-141">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="6f226-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f226-142">-InputObject</span></span>
<span data-ttu-id="6f226-143">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="6f226-143">KeyVault object.</span></span>

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

### <span data-ttu-id="6f226-144">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="6f226-144">-InRemovedState</span></span>
<span data-ttu-id="6f226-145">Especifica se as chaves excluídas anteriormente devem ser mostradas na saída</span><span class="sxs-lookup"><span data-stu-id="6f226-145">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="6f226-146">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f226-146">-Name</span></span>
<span data-ttu-id="6f226-147">Especifica o nome do pacote de chaves a obter.</span><span class="sxs-lookup"><span data-stu-id="6f226-147">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6f226-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f226-148">-ResourceId</span></span>
<span data-ttu-id="6f226-149">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="6f226-149">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="6f226-150">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="6f226-150">-VaultName</span></span>
<span data-ttu-id="6f226-151">Especifica o nome do cofre de chaves do qual este cmdlet obtém chaves.</span><span class="sxs-lookup"><span data-stu-id="6f226-151">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="6f226-152">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um cofre de chaves com base no nome especificado por esse parâmetro e no ambiente selecionado.</span><span class="sxs-lookup"><span data-stu-id="6f226-152">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="6f226-153">-Versão</span><span class="sxs-lookup"><span data-stu-id="6f226-153">-Version</span></span>
<span data-ttu-id="6f226-154">Especifica a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="6f226-154">Specifies the key version.</span></span>
<span data-ttu-id="6f226-155">Esse cmdlet constrói o FQDN de uma chave com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome da chave e na versão de chave.</span><span class="sxs-lookup"><span data-stu-id="6f226-155">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="6f226-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f226-156">CommonParameters</span></span>
<span data-ttu-id="6f226-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f226-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f226-158">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f226-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f226-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f226-159">INPUTS</span></span>

### <span data-ttu-id="6f226-160">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6f226-160">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6f226-161">System. String</span><span class="sxs-lookup"><span data-stu-id="6f226-161">System.String</span></span>

## <span data-ttu-id="6f226-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f226-162">OUTPUTS</span></span>

### <span data-ttu-id="6f226-163">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6f226-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="6f226-164">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f226-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="6f226-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6f226-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="6f226-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f226-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="6f226-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f226-167">NOTES</span></span>

## <span data-ttu-id="6f226-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f226-168">RELATED LINKS</span></span>

[<span data-ttu-id="6f226-169">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f226-169">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="6f226-170">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6f226-170">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="6f226-171">Desfazer-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="6f226-171">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="6f226-172">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="6f226-172">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

