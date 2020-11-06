---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 5a4c1effd1cbda4399e06f3b6db606cff87d8955
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610649"
---
# <span data-ttu-id="2537e-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="2537e-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2537e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2537e-102">SYNOPSIS</span></span>
<span data-ttu-id="2537e-103">Define uma definição de assinatura de acesso compartilhado (SAS) com o cofre de chaves para uma determinada conta de armazenamento do Azure, gerenciada pela chave.</span><span class="sxs-lookup"><span data-stu-id="2537e-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2537e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2537e-104">SYNTAX</span></span>

### <span data-ttu-id="2537e-105">RawSas (padrão)</span><span class="sxs-lookup"><span data-stu-id="2537e-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="2537e-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="2537e-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="2537e-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2537e-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="2537e-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="2537e-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="2537e-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="2537e-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="2537e-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2537e-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="2537e-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="2537e-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="2537e-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="2537e-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2537e-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="2537e-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2537e-119">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2537e-119">DESCRIPTION</span></span>
<span data-ttu-id="2537e-120">Define uma definição de assinatura de acesso compartilhado (SAS) com uma determinada conta de armazenamento do Azure do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2537e-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="2537e-121">Isso também define um segredo que pode ser usado para obter o token SAS por essa definição de SAS.</span><span class="sxs-lookup"><span data-stu-id="2537e-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="2537e-122">O token SAS é gerado usando esses parâmetros e a chave ativa da conta de armazenamento gerenciada do cofre do repositório de chaves.</span><span class="sxs-lookup"><span data-stu-id="2537e-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="2537e-123">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2537e-123">EXAMPLES</span></span>

### <span data-ttu-id="2537e-124">Exemplo 1: definir uma definição de SAS de blob de serviço ad hoc</span><span class="sxs-lookup"><span data-stu-id="2537e-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="2537e-125">Define uma definição de SAS de blob de serviço ad hoc ' SAS1 ' com a conta de armazenamento gerenciado do Key Vault ' máquina1 ' no cofre ' vault1 '.</span><span class="sxs-lookup"><span data-stu-id="2537e-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="2537e-126">Exemplo 2: definir uma definição de SAS de conta ad hoc</span><span class="sxs-lookup"><span data-stu-id="2537e-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="2537e-127">Define uma definição de SAS de blob ad hoc ' SAS1 ' com a conta de armazenamento gerenciado do Key Vault ' máquina1 ' no cofre ' vault1 '.</span><span class="sxs-lookup"><span data-stu-id="2537e-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="2537e-128">Exemplo 3: definir uma definição de SAS usando uma Hashtable</span><span class="sxs-lookup"><span data-stu-id="2537e-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="2537e-129">Define uma definição de SAS de blob ad hoc ' SAS1 ' com a conta de armazenamento gerenciado do Key Vault ' máquina1 ' no cofre ' vault1 ' usando uma Hashtable.</span><span class="sxs-lookup"><span data-stu-id="2537e-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="2537e-130">OS</span><span class="sxs-lookup"><span data-stu-id="2537e-130">PARAMETERS</span></span>

### <span data-ttu-id="2537e-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2537e-131">-AccountName</span></span>
<span data-ttu-id="2537e-132">Nome da conta de armazenamento gerenciado do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="2537e-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="2537e-133">O cmdlet constrói o FQDN de um nome de conta de armazenamento gerenciado a partir do nome do cofre, ambiente selecionado atualmente e nome da conta de armazenamento gerenciada.</span><span class="sxs-lookup"><span data-stu-id="2537e-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2537e-134">-ApiVersion</span></span>
<span data-ttu-id="2537e-135">Especifica a versão do serviço de armazenamento a ser usada para executar a solicitação feita usando o URI da SAS da conta.</span><span class="sxs-lookup"><span data-stu-id="2537e-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-136">-Blob</span><span class="sxs-lookup"><span data-stu-id="2537e-136">-Blob</span></span>
<span data-ttu-id="2537e-137">Nome do blob</span><span class="sxs-lookup"><span data-stu-id="2537e-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-138">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="2537e-138">-Container</span></span>
<span data-ttu-id="2537e-139">Nome do contêiner</span><span class="sxs-lookup"><span data-stu-id="2537e-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2537e-140">-DefaultProfile</span></span>
<span data-ttu-id="2537e-141">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2537e-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-142">-Disable</span><span class="sxs-lookup"><span data-stu-id="2537e-142">-Disable</span></span>
<span data-ttu-id="2537e-143">Desabilita o uso da definição de SAS para a geração de token SAS.</span><span class="sxs-lookup"><span data-stu-id="2537e-143">Disables the use of sas definition for generation of sas token.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2537e-144">-EndPartitionKey</span></span>
<span data-ttu-id="2537e-145">Chave de partição final</span><span class="sxs-lookup"><span data-stu-id="2537e-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="2537e-146">-EndRowKey</span></span>
<span data-ttu-id="2537e-147">Chave de linha final</span><span class="sxs-lookup"><span data-stu-id="2537e-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2537e-148">-IPAddressOrRange</span></span>
<span data-ttu-id="2537e-149">IP ou ACL de intervalo de IP (lista de controle de acesso) da solicitação que seria aceita pelo armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2537e-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="2537e-150">-Name</span></span>
<span data-ttu-id="2537e-151">Nome da definição de SAS de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2537e-151">Storage sas definition name.</span></span> <span data-ttu-id="2537e-152">O cmdlet constrói o FQDN de uma definição de SAS de armazenamento do nome do cofre, ambiente selecionado atualmente, nome da conta de armazenamento e nome da definição da SAS.</span><span class="sxs-lookup"><span data-stu-id="2537e-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-153">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="2537e-153">-Parameter</span></span>
<span data-ttu-id="2537e-154">Parâmetros de definição de SAS que serão usados para criar o token SAS.</span><span class="sxs-lookup"><span data-stu-id="2537e-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-155">-Caminho</span><span class="sxs-lookup"><span data-stu-id="2537e-155">-Path</span></span>
<span data-ttu-id="2537e-156">Caminho para o arquivo de nuvem para o qual gerar token SAS.</span><span class="sxs-lookup"><span data-stu-id="2537e-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-157">-Permissão</span><span class="sxs-lookup"><span data-stu-id="2537e-157">-Permission</span></span>
<span data-ttu-id="2537e-158">Permissão.</span><span class="sxs-lookup"><span data-stu-id="2537e-158">Permission.</span></span> <span data-ttu-id="2537e-159">Os valores incluem ' Query ', ' Add ', ' Update ', ' Process '</span><span class="sxs-lookup"><span data-stu-id="2537e-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-160">-Política</span><span class="sxs-lookup"><span data-stu-id="2537e-160">-Policy</span></span>
<span data-ttu-id="2537e-161">Identificador de política</span><span class="sxs-lookup"><span data-stu-id="2537e-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-162">-Protocolo</span><span class="sxs-lookup"><span data-stu-id="2537e-162">-Protocol</span></span>
<span data-ttu-id="2537e-163">O protocolo pode ser usado na solicitação com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="2537e-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-164">-Queue</span><span class="sxs-lookup"><span data-stu-id="2537e-164">-Queue</span></span>
<span data-ttu-id="2537e-165">Nome da fila</span><span class="sxs-lookup"><span data-stu-id="2537e-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2537e-166">-ResourceType</span></span>
<span data-ttu-id="2537e-167">Tipos de recurso aos quais este token SAS se aplica.</span><span class="sxs-lookup"><span data-stu-id="2537e-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="2537e-168">Os valores incluem ' serviço ', ' contêiner ', ' objeto '</span><span class="sxs-lookup"><span data-stu-id="2537e-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-169">-Serviço</span><span class="sxs-lookup"><span data-stu-id="2537e-169">-Service</span></span>
<span data-ttu-id="2537e-170">Tipos de serviço aos quais este token SAS se aplica.</span><span class="sxs-lookup"><span data-stu-id="2537e-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="2537e-171">Os valores incluem ' BLOB ', ' arquivo ', ' fila ', ' tabela '</span><span class="sxs-lookup"><span data-stu-id="2537e-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases:
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-172">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="2537e-172">-Share</span></span>
<span data-ttu-id="2537e-173">Nome do compartilhamento</span><span class="sxs-lookup"><span data-stu-id="2537e-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="2537e-174">-SharedAccessHeader</span></span>
<span data-ttu-id="2537e-175">Especifica os parâmetros de consulta para substituir os cabeçalhos de resposta.</span><span class="sxs-lookup"><span data-stu-id="2537e-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases:
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2537e-176">-StartPartitionKey</span></span>
<span data-ttu-id="2537e-177">Iniciar chave de partição</span><span class="sxs-lookup"><span data-stu-id="2537e-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="2537e-178">-StartRowKey</span></span>
<span data-ttu-id="2537e-179">Chave de linha inicial</span><span class="sxs-lookup"><span data-stu-id="2537e-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-180">-Tabela</span><span class="sxs-lookup"><span data-stu-id="2537e-180">-Table</span></span>
<span data-ttu-id="2537e-181">Nome da tabela</span><span class="sxs-lookup"><span data-stu-id="2537e-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-182">-Marca</span><span class="sxs-lookup"><span data-stu-id="2537e-182">-Tag</span></span>
<span data-ttu-id="2537e-183">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2537e-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2537e-184">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2537e-184">For example:</span></span>

<span data-ttu-id="2537e-185">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2537e-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="2537e-186">-TargetStorageVersion</span></span>
<span data-ttu-id="2537e-187">Especifica a versão do serviço de armazenamento assinado a ser usada para autenticar solicitações feitas com o token SAS.</span><span class="sxs-lookup"><span data-stu-id="2537e-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="2537e-188">-ValidityPeriod</span></span>
<span data-ttu-id="2537e-189">Período de validade que será usado para definir o tempo de expiração do token SAS no momento da geração</span><span class="sxs-lookup"><span data-stu-id="2537e-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-190">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="2537e-190">-VaultName</span></span>
<span data-ttu-id="2537e-191">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="2537e-191">Vault name.</span></span>
<span data-ttu-id="2537e-192">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="2537e-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-193">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2537e-193">-Confirm</span></span>
<span data-ttu-id="2537e-194">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2537e-194">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2537e-195">-WhatIf</span></span>
<span data-ttu-id="2537e-196">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2537e-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2537e-197">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2537e-197">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2537e-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2537e-198">CommonParameters</span></span>
<span data-ttu-id="2537e-199">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2537e-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2537e-200">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2537e-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2537e-201">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2537e-201">INPUTS</span></span>

### <span data-ttu-id="2537e-202">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2537e-202">None</span></span>
<span data-ttu-id="2537e-203">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="2537e-203">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2537e-204">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2537e-204">OUTPUTS</span></span>

### <span data-ttu-id="2537e-205">Microsoft. Azure. Commands. keyvault. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="2537e-205">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="2537e-206">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2537e-206">NOTES</span></span>

## <span data-ttu-id="2537e-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2537e-207">RELATED LINKS</span></span>

[<span data-ttu-id="2537e-208">Azureâ € ‹ RM. â € ‹ Keyâ € ‹ Vault</span><span class="sxs-lookup"><span data-stu-id="2537e-208">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
