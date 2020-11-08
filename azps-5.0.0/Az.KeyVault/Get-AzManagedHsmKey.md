---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115308"
---
# <span data-ttu-id="85745-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="85745-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="85745-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85745-102">SYNOPSIS</span></span>
<span data-ttu-id="85745-103">Obtém chaves gerenciadas do HSM.</span><span class="sxs-lookup"><span data-stu-id="85745-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="85745-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85745-104">SYNTAX</span></span>

### <span data-ttu-id="85745-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (padrão)</span><span class="sxs-lookup"><span data-stu-id="85745-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="85745-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="85745-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="85745-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="85745-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="85745-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="85745-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="85745-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85745-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="85745-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85745-114">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85745-114">DESCRIPTION</span></span>
<span data-ttu-id="85745-115">O cmdlet **Get-AzManagedHsmKey** Obtém as chaves do Azure Managed HSM.</span><span class="sxs-lookup"><span data-stu-id="85745-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="85745-116">Esse cmdlet obtém um determinado **Microsoft. Azure. Commands. subvault. Models. keybundle** ou uma lista de todos os objetos **keybundle** em um HSM gerenciado ou por uma versão.</span><span class="sxs-lookup"><span data-stu-id="85745-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="85745-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85745-117">EXAMPLES</span></span>

### <span data-ttu-id="85745-118">Exemplo 1: obter todas as chaves em um HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="85745-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="85745-119">Nome do cofre/HSM: nome do testmhsm: versão do testkey001: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled: true expira: não antes: criado: 10/14/2020 3:39:16 am updated: 10/14/2020 3:39:16 nível de recuperação: recuperável + marcas de limpeza:</span><span class="sxs-lookup"><span data-stu-id="85745-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="85745-120">Nome do cofre/HSM: testmhsm: versão do testkey002: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled: false expira: 10/14/2022 8:13:29 não está antes: 10/14/2020 8:13:33 am foi criado: 10/14/2020 8:14:01 am updated: 10/14/2020 8:14:01 am nível de recuperação: recuperáveis + marcas que podem ser limpas: nome valor gravidade alta contabilidade true</span><span class="sxs-lookup"><span data-stu-id="85745-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="85745-121">Esse comando obtém todas as chaves no HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="85745-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="85745-122">Exemplo 2: obter a versão atual de uma chave</span><span class="sxs-lookup"><span data-stu-id="85745-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="85745-123">Esse comando obtém a versão atual da chave chamada testkey001 no HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="85745-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="85745-124">Observação: o nome do HSM pode ser obtido $hsm. Cofrename</span><span class="sxs-lookup"><span data-stu-id="85745-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="85745-125">Exemplo 3: obter todas as versões de uma chave</span><span class="sxs-lookup"><span data-stu-id="85745-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="85745-126">Esse comando obtém todas as versões a chave chamada testkey001 no HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="85745-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="85745-127">Exemplo 4: obter uma versão específica de uma chave</span><span class="sxs-lookup"><span data-stu-id="85745-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="85745-128">Esse comando obtém uma versão específica da chave chamada TestKey no HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="85745-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="85745-129">Depois de executar esse comando, você pode inspecionar várias propriedades da chave navegando no objeto $Key.</span><span class="sxs-lookup"><span data-stu-id="85745-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="85745-130">Exemplo 5: obter todas as chaves que foram excluídas, mas não eliminadas para este HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="85745-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="85745-131">Esse comando obtém todas as chaves que foram excluídas anteriormente, mas não foram limpas, no HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="85745-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="85745-132">Exemplo 6: Obtém a chave TestKey que foi excluída, mas não é eliminada para este HSM gerenciado</span><span class="sxs-lookup"><span data-stu-id="85745-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="85745-133">Esse comando obtém a chave TestKey que foi excluída anteriormente, mas não é eliminada, no HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="85745-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="85745-134">Esse comando retornará metadados como a data de exclusão e a data de descarte programada dessa chave excluída.</span><span class="sxs-lookup"><span data-stu-id="85745-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="85745-135">Exemplo 7: obter todas as chaves em um HSM gerenciado usando filtragem</span><span class="sxs-lookup"><span data-stu-id="85745-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="85745-136">Esse comando obtém todas as chaves no HSM gerenciado chamado testmhsm que começam com "Test".</span><span class="sxs-lookup"><span data-stu-id="85745-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="85745-137">Exemplo 8: baixar uma chave pública como um arquivo. pem</span><span class="sxs-lookup"><span data-stu-id="85745-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="85745-138">Você pode baixar a chave pública de uma chave RSA especificando o `-OutFile` parâmetro.</span><span class="sxs-lookup"><span data-stu-id="85745-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="85745-139">OS</span><span class="sxs-lookup"><span data-stu-id="85745-139">PARAMETERS</span></span>

### <span data-ttu-id="85745-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85745-140">-DefaultProfile</span></span>
<span data-ttu-id="85745-141">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85745-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85745-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="85745-142">-HsmName</span></span>
<span data-ttu-id="85745-143">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="85745-143">HSM name.</span></span> <span data-ttu-id="85745-144">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="85745-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85745-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="85745-145">-IncludeVersions</span></span>
<span data-ttu-id="85745-146">Especifica se as versões da chave devem ser incluídas na saída.</span><span class="sxs-lookup"><span data-stu-id="85745-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85745-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85745-147">-InputObject</span></span>
<span data-ttu-id="85745-148">Objeto HSM.</span><span class="sxs-lookup"><span data-stu-id="85745-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85745-149">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="85745-149">-InRemovedState</span></span>
<span data-ttu-id="85745-150">Especifica se as chaves excluídas anteriormente devem ser mostradas na saída.</span><span class="sxs-lookup"><span data-stu-id="85745-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85745-151">-Nome</span><span class="sxs-lookup"><span data-stu-id="85745-151">-Name</span></span>
<span data-ttu-id="85745-152">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="85745-152">Key name.</span></span>
<span data-ttu-id="85745-153">O cmdlet constrói o FQDN de uma chave do nome gerenciado do HSM, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="85745-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85745-154">-Outfile</span><span class="sxs-lookup"><span data-stu-id="85745-154">-OutFile</span></span>
<span data-ttu-id="85745-155">Especifica o arquivo de saída para o qual esse cmdlet salva a chave.</span><span class="sxs-lookup"><span data-stu-id="85745-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="85745-156">A chave pública é salva no formato PEM por padrão.</span><span class="sxs-lookup"><span data-stu-id="85745-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="85745-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85745-157">-ResourceId</span></span>
<span data-ttu-id="85745-158">ID do recurso HSM.</span><span class="sxs-lookup"><span data-stu-id="85745-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85745-159">-Versão</span><span class="sxs-lookup"><span data-stu-id="85745-159">-Version</span></span>
<span data-ttu-id="85745-160">Versão principal.</span><span class="sxs-lookup"><span data-stu-id="85745-160">Key version.</span></span>
<span data-ttu-id="85745-161">O cmdlet constrói o FQDN de uma chave do nome gerenciado do HSM, o ambiente selecionado no momento, o nome da chave e a versão da chave.</span><span class="sxs-lookup"><span data-stu-id="85745-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85745-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85745-162">CommonParameters</span></span>
<span data-ttu-id="85745-163">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85745-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85745-164">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85745-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85745-165">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85745-165">INPUTS</span></span>

### <span data-ttu-id="85745-166">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="85745-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="85745-167">System. String</span><span class="sxs-lookup"><span data-stu-id="85745-167">System.String</span></span>

## <span data-ttu-id="85745-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85745-168">OUTPUTS</span></span>

### <span data-ttu-id="85745-169">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="85745-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="85745-170">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85745-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="85745-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="85745-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="85745-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="85745-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="85745-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85745-173">NOTES</span></span>

## <span data-ttu-id="85745-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85745-174">RELATED LINKS</span></span>

[<span data-ttu-id="85745-175">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="85745-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="85745-176">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="85745-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="85745-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="85745-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="85745-178">Desfazer-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="85745-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="85745-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="85745-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="85745-180">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="85745-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)