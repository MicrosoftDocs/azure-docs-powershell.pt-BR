---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126175"
---
# <span data-ttu-id="98926-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98926-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="98926-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98926-102">SYNOPSIS</span></span>
<span data-ttu-id="98926-103">Cria uma chave em um HSM gerenciado ou importa uma chave para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98926-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="98926-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98926-104">SYNTAX</span></span>

### <span data-ttu-id="98926-105">InteractiveCreate (padrão)</span><span class="sxs-lookup"><span data-stu-id="98926-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98926-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="98926-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98926-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="98926-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98926-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="98926-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98926-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="98926-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98926-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="98926-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98926-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98926-111">DESCRIPTION</span></span>
<span data-ttu-id="98926-112">O cmdlet **Add-AzManagedHsmKey** cria uma chave em um HSM gerenciado no Azure Managed HSM ou importa uma chave para um HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98926-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="98926-113">Use esse cmdlet para adicionar chaves usando qualquer um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="98926-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="98926-114">Criar uma chave com atributos de chave padrão</span><span class="sxs-lookup"><span data-stu-id="98926-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="98926-115">Criar uma chave com os atributos de chave determinados</span><span class="sxs-lookup"><span data-stu-id="98926-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="98926-116">Importar uma chave de um arquivo. pfx em seu computador.</span><span class="sxs-lookup"><span data-stu-id="98926-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="98926-117">Para qualquer uma dessas operações, você pode fornecer atributos de chave ou aceitar as configurações padrão.</span><span class="sxs-lookup"><span data-stu-id="98926-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="98926-118">Se você criar ou importar uma chave com o mesmo nome de uma chave existente no HSM gerenciado, a chave original será atualizada com os valores especificados para a nova chave.</span><span class="sxs-lookup"><span data-stu-id="98926-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="98926-119">Você pode acessar os valores anteriores usando o URI específico da versão para essa versão da chave.</span><span class="sxs-lookup"><span data-stu-id="98926-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="98926-120">Para saber mais sobre as principais versões e a estrutura de URI, consulte [sobre chaves e segredos](http://go.microsoft.com/fwlink/?linkid=518560) na documentação da API REST do HSM gerenciado.</span><span class="sxs-lookup"><span data-stu-id="98926-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="98926-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98926-121">EXAMPLES</span></span>

### <span data-ttu-id="98926-122">Exemplo 1: criar uma chave RSA-HSM</span><span class="sxs-lookup"><span data-stu-id="98926-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98926-123">Esse comando cria uma chave RSA-HSM chamada TestKey no TestKey HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98926-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="98926-124">Exemplo 2: criar uma chave EC-HSM</span><span class="sxs-lookup"><span data-stu-id="98926-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="98926-125">Esse comando cria uma chave EC-HSM chamada TestKey usando a curva de P a 256 no TestKey HSM gerenciado chamado testmhsm.</span><span class="sxs-lookup"><span data-stu-id="98926-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="98926-126">Exemplo 3: criar uma chave de outubro de HSM com valores não padrão</span><span class="sxs-lookup"><span data-stu-id="98926-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
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

<span data-ttu-id="98926-127">O primeiro comando armazena os valores decodificar e verificar na variável $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="98926-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="98926-128">O segundo comando cria um objeto **DateTime** , definido em UTC, usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="98926-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="98926-129">Esse objeto especifica um tempo dois anos no futuro.</span><span class="sxs-lookup"><span data-stu-id="98926-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="98926-130">O comando armazena essa data na variável $Expires.</span><span class="sxs-lookup"><span data-stu-id="98926-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="98926-131">Para obter mais informações, digite `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="98926-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="98926-132">O terceiro comando cria um objeto **DateTime** usando o cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="98926-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="98926-133">Esse objeto especifica a hora UTC atual.</span><span class="sxs-lookup"><span data-stu-id="98926-133">That object specifies current UTC time.</span></span> <span data-ttu-id="98926-134">O comando armazena essa data na variável $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="98926-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="98926-135">O comando final cria uma chave chamada TestKey que é uma chave out-HSM.</span><span class="sxs-lookup"><span data-stu-id="98926-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="98926-136">O comando especifica valores para operações de chave permitidas armazenadas $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="98926-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="98926-137">O comando especifica os horários dos parâmetros *expire* e não *antes* de serem criados nos comandos anteriores e marca para alta severidade e.</span><span class="sxs-lookup"><span data-stu-id="98926-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="98926-138">A nova chave está desativada.</span><span class="sxs-lookup"><span data-stu-id="98926-138">The new key is disabled.</span></span> <span data-ttu-id="98926-139">Você pode habilitá-lo usando o cmdlet **Update-AzManagedHsmKey** .</span><span class="sxs-lookup"><span data-stu-id="98926-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="98926-140">OS</span><span class="sxs-lookup"><span data-stu-id="98926-140">PARAMETERS</span></span>

### <span data-ttu-id="98926-141">-Curvename</span><span class="sxs-lookup"><span data-stu-id="98926-141">-CurveName</span></span>
<span data-ttu-id="98926-142">Especifica o nome da curva da criptografia de curva elíptica, esse valor é válido quando KeyType é EC.</span><span class="sxs-lookup"><span data-stu-id="98926-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="98926-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98926-143">-DefaultProfile</span></span>
<span data-ttu-id="98926-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98926-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98926-145">-Disable</span><span class="sxs-lookup"><span data-stu-id="98926-145">-Disable</span></span>
<span data-ttu-id="98926-146">Indica que a chave que você está adicionando está definida como um estado inicial de desabilitado.</span><span class="sxs-lookup"><span data-stu-id="98926-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="98926-147">Qualquer tentativa de usar a chave irá falhar.</span><span class="sxs-lookup"><span data-stu-id="98926-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="98926-148">Use esse parâmetro se você estiver precarregando chaves que pretende habilitar mais tarde.</span><span class="sxs-lookup"><span data-stu-id="98926-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="98926-149">-Expira em</span><span class="sxs-lookup"><span data-stu-id="98926-149">-Expires</span></span>
<span data-ttu-id="98926-150">Especifica o tempo de expiração da chave em UTC.</span><span class="sxs-lookup"><span data-stu-id="98926-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="98926-151">Se não for especificado, a chave não expira.</span><span class="sxs-lookup"><span data-stu-id="98926-151">If not specified, key will not expire.</span></span>

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

### <span data-ttu-id="98926-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="98926-152">-HsmName</span></span>
<span data-ttu-id="98926-153">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="98926-153">HSM name.</span></span> <span data-ttu-id="98926-154">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="98926-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98926-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98926-155">-InputObject</span></span>
<span data-ttu-id="98926-156">Objeto HSM.</span><span class="sxs-lookup"><span data-stu-id="98926-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98926-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="98926-157">-KeyFilePassword</span></span>
<span data-ttu-id="98926-158">Senha do arquivo local que contém o material da chave a ser importado.</span><span class="sxs-lookup"><span data-stu-id="98926-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98926-159">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="98926-159">-KeyFilePath</span></span>
<span data-ttu-id="98926-160">Caminho para o arquivo local que contém o material da chave a ser importado.</span><span class="sxs-lookup"><span data-stu-id="98926-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98926-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="98926-161">-KeyOps</span></span>
<span data-ttu-id="98926-162">As operações que podem ser executadas com a chave.</span><span class="sxs-lookup"><span data-stu-id="98926-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="98926-163">Se não estiver presente, todas as operações podem ser realizadas.</span><span class="sxs-lookup"><span data-stu-id="98926-163">If not present, all operations can be performed.</span></span>

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

### <span data-ttu-id="98926-164">-KeyType</span><span class="sxs-lookup"><span data-stu-id="98926-164">-KeyType</span></span>
<span data-ttu-id="98926-165">Especifica o tipo de chave dessa chave.</span><span class="sxs-lookup"><span data-stu-id="98926-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98926-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="98926-166">-Name</span></span>
<span data-ttu-id="98926-167">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="98926-167">Key name.</span></span>
<span data-ttu-id="98926-168">O cmdlet constrói o FQDN de uma chave do nome gerenciado do HSM, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="98926-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98926-169">-Não antes</span><span class="sxs-lookup"><span data-stu-id="98926-169">-NotBefore</span></span>
<span data-ttu-id="98926-170">A hora UTC antes da qual a chave não pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="98926-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="98926-171">Se não for especificado, não haverá limitação.</span><span class="sxs-lookup"><span data-stu-id="98926-171">If not specified, there is no limitation.</span></span>

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

### <span data-ttu-id="98926-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98926-172">-ResourceId</span></span>
<span data-ttu-id="98926-173">ID do recurso HSM.</span><span class="sxs-lookup"><span data-stu-id="98926-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98926-174">-Tamanho</span><span class="sxs-lookup"><span data-stu-id="98926-174">-Size</span></span>
<span data-ttu-id="98926-175">Tamanho da chave RSA, em bits.</span><span class="sxs-lookup"><span data-stu-id="98926-175">RSA key size, in bits.</span></span>
<span data-ttu-id="98926-176">Se não for especificado, o serviço fornecerá um padrão seguro.</span><span class="sxs-lookup"><span data-stu-id="98926-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98926-177">-Marca</span><span class="sxs-lookup"><span data-stu-id="98926-177">-Tag</span></span>
<span data-ttu-id="98926-178">Uma Hashtable representando as marcas de tecla.</span><span class="sxs-lookup"><span data-stu-id="98926-178">A hashtable representing key tags.</span></span>

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

### <span data-ttu-id="98926-179">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98926-179">-Confirm</span></span>
<span data-ttu-id="98926-180">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98926-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98926-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98926-181">-WhatIf</span></span>
<span data-ttu-id="98926-182">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98926-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98926-183">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98926-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98926-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98926-184">CommonParameters</span></span>
<span data-ttu-id="98926-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98926-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98926-186">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98926-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98926-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98926-187">INPUTS</span></span>

### <span data-ttu-id="98926-188">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="98926-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="98926-189">System. String</span><span class="sxs-lookup"><span data-stu-id="98926-189">System.String</span></span>

## <span data-ttu-id="98926-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98926-190">OUTPUTS</span></span>

### <span data-ttu-id="98926-191">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="98926-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="98926-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98926-192">NOTES</span></span>

## <span data-ttu-id="98926-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98926-193">RELATED LINKS</span></span>

[<span data-ttu-id="98926-194">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98926-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="98926-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98926-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="98926-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98926-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="98926-197">Desfazer-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="98926-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="98926-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98926-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="98926-199">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="98926-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
