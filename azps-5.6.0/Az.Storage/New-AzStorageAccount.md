---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890694"
---
# <span data-ttu-id="2b711-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b711-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="2b711-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b711-102">SYNOPSIS</span></span>
<span data-ttu-id="2b711-103">Cria uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-103">Creates a Storage account.</span></span>

## <span data-ttu-id="2b711-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b711-104">SYNTAX</span></span>

### <span data-ttu-id="2b711-105">AzureActiveDirectoryDomainServicesForFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b711-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="2b711-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="2b711-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="2b711-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b711-107">DESCRIPTION</span></span>
<span data-ttu-id="2b711-108">O cmdlet **New-AzStorageAccount** cria uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b711-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="2b711-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b711-109">EXAMPLES</span></span>

### <span data-ttu-id="2b711-110">Exemplo 1: Criar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="2b711-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="2b711-111">Este comando cria uma conta de armazenamento para o nome do grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2b711-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="2b711-112">Exemplo 2: Criar uma conta de Armazenamento de Blob com o Tipo blobStorage e o AccessTier quente</span><span class="sxs-lookup"><span data-stu-id="2b711-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="2b711-113">Este comando cria uma conta de Armazenamento blob que com BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="2b711-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="2b711-114">Exemplo 3: Criar uma conta de armazenamento com Kind StorageV2 e Gerar e Atribuir uma identidade para o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2b711-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="2b711-115">Este comando cria uma conta de armazenamento com Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2b711-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="2b711-116">Ele também gera e atribui uma identidade que pode ser usada para gerenciar chaves de conta por meio do Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2b711-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="2b711-117">Exemplo 4: Criar uma conta de armazenamento com NetworkRuleSet a partir de JSON</span><span class="sxs-lookup"><span data-stu-id="2b711-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="2b711-118">Este comando cria uma conta de armazenamento que tem a propriedade NetworkRuleSet do JSON</span><span class="sxs-lookup"><span data-stu-id="2b711-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="2b711-119">Exemplo 5: Criar uma conta de armazenamento com Namespace hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="2b711-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="2b711-120">Este comando cria uma conta de Armazenamento com Namespace Hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="2b711-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="2b711-121">Exemplo 6: criar uma conta de armazenamento com a autenticação AAD DS de arquivos do Azure e habilitar o compartilhamento de arquivos grande.</span><span class="sxs-lookup"><span data-stu-id="2b711-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="2b711-122">Este comando cria uma conta de armazenamento com a Autenticação AAD DS de Arquivos do Azure e habilita o compartilhamento de arquivos grande.</span><span class="sxs-lookup"><span data-stu-id="2b711-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="2b711-123">Exemplo 7: Criar uma conta de armazenamento com a autenticação de serviço de domínio active directory arquivos.</span><span class="sxs-lookup"><span data-stu-id="2b711-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="2b711-124">Este comando cria uma conta de armazenamento com autenticação de serviço de domínio active directory de arquivos reencíveis.</span><span class="sxs-lookup"><span data-stu-id="2b711-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="2b711-125">Exemplo 8: Criar uma conta de armazenamento com o Serviço de Fila e Tabela use a chave de criptografia com escopo de conta e exigir criptografia de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="2b711-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

<span data-ttu-id="2b711-126">Este comando cria uma conta de Armazenamento com o Serviço de Fila e Tabela, usa a chave de criptografia com escopo de conta e Exige Criptografia de Infraestrutura, portanto, Queue e Table usarão a mesma chave de criptografia com Blob e serviço de arquivo, e o serviço aplicará uma camada secundária de criptografia com chaves gerenciadas da plataforma para dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="2b711-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="2b711-127">Em seguida, obter as propriedades da conta de armazenamento e exibir o tipo de chave de criptografia do Queue and Table Service e o valor RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="2b711-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="2b711-128">Exemplo 9: Criar conta MinimumTlsVersion e AllowBlobPublicAccess e desabilitar o SharedKey Access</span><span class="sxs-lookup"><span data-stu-id="2b711-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess, and disable SharedKey Access</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

<span data-ttu-id="2b711-129">O comando cria conta com MinimumTlsVersion, AllowBlobPublicAccess e desabilita o acesso SharedKey à conta e mostra as 3 propriedades da conta criada</span><span class="sxs-lookup"><span data-stu-id="2b711-129">The command create account with MinimumTlsVersion, AllowBlobPublicAccess, and disable SharedKey access to the account, and then show the the 3 properties of the created account</span></span> 

### <span data-ttu-id="2b711-130">Exemplo 10: Criar uma conta de armazenamento com a configuração RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="2b711-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="2b711-131">Este comando cria uma conta de armazenamento com a configuração RoutingPreference: PublishMicrosoftEndpoint e PublishInternetEndpoint como true e RoutingChoice como MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="2b711-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="2b711-132">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b711-132">PARAMETERS</span></span>

### <span data-ttu-id="2b711-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="2b711-133">-AccessTier</span></span>
<span data-ttu-id="2b711-134">Especifica a camada de acesso da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="2b711-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2b711-135">Os valores aceitáveis para este parâmetro são: Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="2b711-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="2b711-136">Se você especificar um valor blobStorage para o parâmetro *Kind,* deverá especificar um valor para o *parâmetro AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="2b711-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="2b711-137">Se você especificar um valor de Armazenamento para este *parâmetro Kind,* não especifique o *parâmetro AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="2b711-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="2b711-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="2b711-139">Especifica o identificador de segurança (SID) para Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="2b711-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="2b711-140">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.</span><span class="sxs-lookup"><span data-stu-id="2b711-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="2b711-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="2b711-142">Especifica o GUID do domínio.</span><span class="sxs-lookup"><span data-stu-id="2b711-142">Specifies the domain GUID.</span></span> <span data-ttu-id="2b711-143">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.</span><span class="sxs-lookup"><span data-stu-id="2b711-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="2b711-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="2b711-145">Especifica o domínio principal para o que o servidor DNS do AD é autoritativo.</span><span class="sxs-lookup"><span data-stu-id="2b711-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="2b711-146">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.</span><span class="sxs-lookup"><span data-stu-id="2b711-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="2b711-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="2b711-148">Especifica o identificador de segurança (SID).</span><span class="sxs-lookup"><span data-stu-id="2b711-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="2b711-149">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.</span><span class="sxs-lookup"><span data-stu-id="2b711-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="2b711-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="2b711-151">Especifica a floresta do Active Directory a ser obter.</span><span class="sxs-lookup"><span data-stu-id="2b711-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="2b711-152">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.</span><span class="sxs-lookup"><span data-stu-id="2b711-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-153">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="2b711-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="2b711-154">Especifica o nome de domínio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="2b711-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="2b711-155">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile for definido como true.</span><span class="sxs-lookup"><span data-stu-id="2b711-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-156">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="2b711-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="2b711-157">Permitir acesso público a todos os blobs ou contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="2b711-158">A interpretação padrão é verdadeira para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2b711-158">The default interpretation is true for this property.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-159">-AllowSharedKeyAccess</span><span class="sxs-lookup"><span data-stu-id="2b711-159">-AllowSharedKeyAccess</span></span>
<span data-ttu-id="2b711-160">Indica se a conta de armazenamento permite que as solicitações sejam autorizadas com a chave de acesso à conta por meio da Chave Compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2b711-160">Indicates whether the storage account permits requests to be authorized with the account access key via Shared Key.</span></span> <span data-ttu-id="2b711-161">Se false, todas as solicitações, incluindo assinaturas de acesso compartilhado, devem ser autorizadas com o Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="2b711-161">If false, then all requests, including shared access signatures, must be authorized with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="2b711-162">O valor padrão é nulo, que é equivalente a true.</span><span class="sxs-lookup"><span data-stu-id="2b711-162">The default value is null, which is equivalent to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-163">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b711-163">-AsJob</span></span>
<span data-ttu-id="2b711-164">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2b711-164">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b711-165">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2b711-165">-AssignIdentity</span></span>
<span data-ttu-id="2b711-166">Gere e atribua uma nova Identidade de conta de armazenamento para essa conta de Armazenamento para uso com serviços de gerenciamento de chaves, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2b711-166">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2b711-167">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="2b711-167">-CustomDomainName</span></span>
<span data-ttu-id="2b711-168">Especifica o nome do domínio personalizado da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-168">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="2b711-169">O valor padrão é Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-169">The default value is Storage.</span></span>

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

### <span data-ttu-id="2b711-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b711-170">-DefaultProfile</span></span>
<span data-ttu-id="2b711-171">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b711-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b711-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="2b711-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="2b711-173">Habilitar a Autenticação de Serviço de Domínio do Active Directory arquivos do Azure para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="2b711-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="2b711-175">Habilitar a Autenticação de Serviço de Domínio do Azure Arquivos do Azure Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-175">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-176">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="2b711-176">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="2b711-177">Indica se a conta de armazenamento habilita ou não Namespace Hierárquico.</span><span class="sxs-lookup"><span data-stu-id="2b711-177">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="2b711-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="2b711-179">Indica se a conta de armazenamento só habilita o tráfego HTTPS ou não.</span><span class="sxs-lookup"><span data-stu-id="2b711-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="2b711-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="2b711-181">Indica se a conta de armazenamento pode ou não suportar compartilhamentos de arquivos grandes com mais de 5 TiB.</span><span class="sxs-lookup"><span data-stu-id="2b711-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="2b711-182">Depois que a conta for habilitada, o recurso não poderá ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2b711-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="2b711-183">Atualmente, só há suporte para tipos de replicação LRS e ZRS, portanto, as conversões de contas em contas redundantes geográficas não seriam possíveis.</span><span class="sxs-lookup"><span data-stu-id="2b711-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="2b711-184">Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="2b711-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="2b711-185">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="2b711-185">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="2b711-186">De definir o Encryption KeyType for Queue.</span><span class="sxs-lookup"><span data-stu-id="2b711-186">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="2b711-187">O valor padrão é Service.</span><span class="sxs-lookup"><span data-stu-id="2b711-187">The default value is Service.</span></span>
<span data-ttu-id="2b711-188">-Conta: a fila será criptografada com chave de criptografia com escopo de conta.</span><span class="sxs-lookup"><span data-stu-id="2b711-188">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="2b711-189">-Service: a fila sempre será criptografada com Service-Managed chaves.</span><span class="sxs-lookup"><span data-stu-id="2b711-189">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-190">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="2b711-190">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="2b711-191">De definir o Encryption KeyType for Table.</span><span class="sxs-lookup"><span data-stu-id="2b711-191">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="2b711-192">O valor padrão é Service.</span><span class="sxs-lookup"><span data-stu-id="2b711-192">The default value is Service.</span></span>
- <span data-ttu-id="2b711-193">Conta: a tabela será criptografada com chave de criptografia com escopo de conta.</span><span class="sxs-lookup"><span data-stu-id="2b711-193">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="2b711-194">Serviço: a tabela sempre será criptografada com Service-Managed chaves.</span><span class="sxs-lookup"><span data-stu-id="2b711-194">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-195">-Kind</span><span class="sxs-lookup"><span data-stu-id="2b711-195">-Kind</span></span>
<span data-ttu-id="2b711-196">Especifica o tipo de conta de Armazenamento que esse cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="2b711-196">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2b711-197">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b711-197">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b711-198">Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-198">Storage.</span></span> <span data-ttu-id="2b711-199">Conta de armazenamento de finalidade geral que oferece suporte ao armazenamento de Blobs, Tabelas, Filas, Arquivos e Discos.</span><span class="sxs-lookup"><span data-stu-id="2b711-199">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="2b711-200">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2b711-200">StorageV2.</span></span> <span data-ttu-id="2b711-201">Conta de armazenamento de finalidade geral versão 2 (GPv2) que dá suporte a Blobs, Tabelas, Filas, Arquivos e Discos, com recursos avançados, como a camada de dados.</span><span class="sxs-lookup"><span data-stu-id="2b711-201">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="2b711-202">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="2b711-202">BlobStorage.</span></span> <span data-ttu-id="2b711-203">Conta de Armazenamento de Blob que dá suporte apenas ao armazenamento de Blobs.</span><span class="sxs-lookup"><span data-stu-id="2b711-203">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="2b711-204">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="2b711-204">BlockBlobStorage.</span></span> <span data-ttu-id="2b711-205">Blob Storage account which supports storage of Block Blobs only.</span><span class="sxs-lookup"><span data-stu-id="2b711-205">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="2b711-206">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="2b711-206">FileStorage.</span></span> <span data-ttu-id="2b711-207">Conta de Armazenamento de Arquivos que oferece suporte apenas ao armazenamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="2b711-207">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="2b711-208">O valor padrão é StorageV2.</span><span class="sxs-lookup"><span data-stu-id="2b711-208">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-209">-Location</span><span class="sxs-lookup"><span data-stu-id="2b711-209">-Location</span></span>
<span data-ttu-id="2b711-210">Especifica o local da conta de armazenamento a ser criado.</span><span class="sxs-lookup"><span data-stu-id="2b711-210">Specifies the location of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-211">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2b711-211">-MinimumTlsVersion</span></span>
<span data-ttu-id="2b711-212">A versão TLS mínima a ser permitida em solicitações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-212">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="2b711-213">A interpretação padrão é TLS 1.0 para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="2b711-213">The default interpretation is TLS 1.0 for this property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-214">-Name</span><span class="sxs-lookup"><span data-stu-id="2b711-214">-Name</span></span>
<span data-ttu-id="2b711-215">Especifica o nome da conta de armazenamento a ser criado.</span><span class="sxs-lookup"><span data-stu-id="2b711-215">Specifies the name of the Storage account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-216">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2b711-216">-NetworkRuleSet</span></span>
<span data-ttu-id="2b711-217">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como serviços permitidos para ignorar as regras e como lidar com solicitações que não corresponderem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="2b711-217">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-218">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b711-218">-PublishInternetEndpoint</span></span>
<span data-ttu-id="2b711-219">Indica se os pontos de extremidade de armazenamento de roteamento da Internet devem ser publicados</span><span class="sxs-lookup"><span data-stu-id="2b711-219">Indicates whether internet  routing storage endpoints are to be published</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-220">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="2b711-220">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="2b711-221">Indica se os pontos de extremidade de armazenamento de roteamento da Microsoft devem ser publicados</span><span class="sxs-lookup"><span data-stu-id="2b711-221">Indicates whether microsoft routing storage endpoints are to be published</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-222">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="2b711-222">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="2b711-223">O serviço aplicará uma camada secundária de criptografia com chaves gerenciadas da plataforma para dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="2b711-223">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="2b711-224">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b711-224">-ResourceGroupName</span></span>
<span data-ttu-id="2b711-225">Especifica o nome do grupo de recursos no qual adicionar a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b711-225">Specifies the name of the resource group in which to add the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-226">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="2b711-226">-RoutingChoice</span></span>
<span data-ttu-id="2b711-227">A Opção de Roteamento define o tipo de roteamento de rede optado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2b711-227">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="2b711-228">Os valores possíveis incluem: 'MicrosoftRouting', 'InternetRouting'</span><span class="sxs-lookup"><span data-stu-id="2b711-228">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-229">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b711-229">-SkuName</span></span>
<span data-ttu-id="2b711-230">Especifica o nome SKU da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="2b711-230">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="2b711-231">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b711-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b711-232">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="2b711-232">Standard_LRS.</span></span> <span data-ttu-id="2b711-233">Armazenamento localmente redundante.</span><span class="sxs-lookup"><span data-stu-id="2b711-233">Locally-redundant storage.</span></span>
- <span data-ttu-id="2b711-234">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="2b711-234">Standard_ZRS.</span></span> <span data-ttu-id="2b711-235">Armazenamento redundante de zona.</span><span class="sxs-lookup"><span data-stu-id="2b711-235">Zone-redundant storage.</span></span>
- <span data-ttu-id="2b711-236">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="2b711-236">Standard_GRS.</span></span> <span data-ttu-id="2b711-237">Armazenamento geo-redundante.</span><span class="sxs-lookup"><span data-stu-id="2b711-237">Geo-redundant storage.</span></span>
- <span data-ttu-id="2b711-238">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="2b711-238">Standard_RAGRS.</span></span> <span data-ttu-id="2b711-239">Ler o armazenamento geo-redundante de acesso.</span><span class="sxs-lookup"><span data-stu-id="2b711-239">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="2b711-240">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="2b711-240">Premium_LRS.</span></span> <span data-ttu-id="2b711-241">Armazenamento localmente redundante premium.</span><span class="sxs-lookup"><span data-stu-id="2b711-241">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="2b711-242">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="2b711-242">Premium_ZRS.</span></span> <span data-ttu-id="2b711-243">Armazenamento redundante de zona premium.</span><span class="sxs-lookup"><span data-stu-id="2b711-243">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="2b711-244">Standard_GZRS - Armazenamento redundante de zona geo-redundante.</span><span class="sxs-lookup"><span data-stu-id="2b711-244">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="2b711-245">Standard_RAGZRS - Ler o armazenamento redundante de zona de acesso geo-redundante.</span><span class="sxs-lookup"><span data-stu-id="2b711-245">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b711-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b711-246">-Tag</span></span>
<span data-ttu-id="2b711-247">Pares de valores-chave na forma de um conjunto de tabelas de hash como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="2b711-247">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="2b711-248">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="2b711-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b711-249">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="2b711-249">-UseSubDomain</span></span>
<span data-ttu-id="2b711-250">Indica se é possível habilitar a validação indireta de CName.</span><span class="sxs-lookup"><span data-stu-id="2b711-250">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="2b711-251">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b711-251">CommonParameters</span></span>
<span data-ttu-id="2b711-252">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b711-252">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b711-253">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b711-253">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b711-254">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b711-254">INPUTS</span></span>

### <span data-ttu-id="2b711-255">System.String</span><span class="sxs-lookup"><span data-stu-id="2b711-255">System.String</span></span>

## <span data-ttu-id="2b711-256">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b711-256">OUTPUTS</span></span>

### <span data-ttu-id="2b711-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b711-257">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="2b711-258">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b711-258">NOTES</span></span>

## <span data-ttu-id="2b711-259">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b711-259">RELATED LINKS</span></span>

[<span data-ttu-id="2b711-260">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b711-260">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="2b711-261">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b711-261">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="2b711-262">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b711-262">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
