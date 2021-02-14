---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0e1243765064717c6e0030b437c07a176a232f44
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115660"
---
# <span data-ttu-id="d7843-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7843-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="d7843-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7843-102">SYNOPSIS</span></span>
<span data-ttu-id="d7843-103">Cria uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-103">Creates a Storage account.</span></span>

## <span data-ttu-id="d7843-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7843-104">SYNTAX</span></span>

### <span data-ttu-id="d7843-105">AzureActiveDirectoryDomainServicesForFile (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d7843-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### <span data-ttu-id="d7843-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d7843-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7843-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7843-107">DESCRIPTION</span></span>
<span data-ttu-id="d7843-108">O **cmdlet New-AzStorageAccount cria** uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7843-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="d7843-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7843-109">EXAMPLES</span></span>

### <span data-ttu-id="d7843-110">Exemplo 1: Criar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d7843-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="d7843-111">Esse comando cria uma conta de Armazenamento para o grupo de recursos MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d7843-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="d7843-112">Exemplo 2: Criar uma conta de Armazenamento de Blob com o BlobStorage Kind e o AccessTier hot</span><span class="sxs-lookup"><span data-stu-id="d7843-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="d7843-113">Esse comando cria uma conta de Armazenamento de Blob que, com o BlobStorage Kind e o AccessTier</span><span class="sxs-lookup"><span data-stu-id="d7843-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="d7843-114">Exemplo 3: Criar uma conta de armazenamento com Kind StorageV2 e gerar e atribuir uma identidade para o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d7843-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="d7843-115">Esse comando cria uma conta de armazenamento com Kind StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d7843-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="d7843-116">Ele também gera e atribui uma identidade que pode ser usada para gerenciar chaves de conta por meio do Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d7843-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="d7843-117">Exemplo 4: Criar uma conta de armazenamento com NetworkRuleSet a partir de JSON</span><span class="sxs-lookup"><span data-stu-id="d7843-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="d7843-118">Esse comando cria uma conta de armazenamento que tem a propriedade NetworkRuleSet do JSON</span><span class="sxs-lookup"><span data-stu-id="d7843-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="d7843-119">Exemplo 5: Criar uma conta de Armazenamento com Namespace Hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="d7843-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="d7843-120">Esse comando cria uma conta de Armazenamento com Namespace Hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="d7843-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="d7843-121">Exemplo 6: Criar uma conta de armazenamento com a Autenticação DS do Azure Files AAD e habilitar o compartilhamento de arquivos grande.</span><span class="sxs-lookup"><span data-stu-id="d7843-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="d7843-122">Esse comando cria uma conta de armazenamento com a Autenticação DS do Azure Files AAD e habilita o compartilhamento de arquivos grande.</span><span class="sxs-lookup"><span data-stu-id="d7843-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="d7843-123">Exemplo 7: Criar uma conta de armazenamento com a autenticação de serviço de domínio arquivos active directory.</span><span class="sxs-lookup"><span data-stu-id="d7843-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="d7843-124">Esse comando cria uma conta de armazenamento com a Autenticação de Serviço de Domínio do Active Directory para Arquivos Do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d7843-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="d7843-125">Exemplo 8: Criar uma conta de Armazenamento com o Serviço de Tabela e Fila usam a chave de criptografia com escopo de conta e exigem criptografia de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="d7843-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="d7843-126">Esse comando cria uma conta de armazenamento com a chave de criptografia de fila e de tabela com escopo de conta e exigir criptografia de infraestrutura; portanto, a fila e a tabela usarão a mesma chave de criptografia com o serviço Blob e Arquivo, e o serviço aplicará uma camada secundária de criptografia com chaves gerenciadas da plataforma para os dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="d7843-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="d7843-127">Em seguida, obter as propriedades da conta de armazenamento e exibir o tipo de chave de criptografia de Fila e Serviço de Tabela e o valor RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="d7843-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="d7843-128">Exemplo 9: Criar conta MinimumTlsVersion e AllowBpublicAccesss</span><span class="sxs-lookup"><span data-stu-id="d7843-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="d7843-129">O comando criar conta com MinimumTlsVersion e AllowBpublicAccess e mostrar as 2 propriedades da conta criada</span><span class="sxs-lookup"><span data-stu-id="d7843-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

### <span data-ttu-id="d7843-130">Exemplo 10: Criar uma conta de armazenamento com a configuração RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="d7843-130">Example 10: Create a Storage account with RoutingPreference setting</span></span>
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

<span data-ttu-id="d7843-131">Esse comando cria uma conta de Armazenamento com a configuração RoutingPreference: PublishMicrosoftEndpoint e PublishInternetEndpoint como true e RoutingChoice como MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="d7843-131">This command creates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint and PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="d7843-132">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7843-132">PARAMETERS</span></span>

### <span data-ttu-id="d7843-133">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="d7843-133">-AccessTier</span></span>
<span data-ttu-id="d7843-134">Especifica o nível de acesso da conta de Armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d7843-134">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d7843-135">Os valores aceitáveis para este parâmetro são: Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="d7843-135">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="d7843-136">Se você especificar um valor de BlobStorage para o parâmetro *Kind,* deverá especificar um valor para o parâmetro *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="d7843-136">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="d7843-137">Se você especificar um valor de Armazenamento para este parâmetro *Kind,* não especifique o parâmetro *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="d7843-137">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="d7843-138">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="d7843-138">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="d7843-139">Especifica o identificador de segurança (SID) para Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7843-139">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="d7843-140">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="d7843-140">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d7843-141">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="d7843-141">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="d7843-142">Especifica o GUID do domínio.</span><span class="sxs-lookup"><span data-stu-id="d7843-142">Specifies the domain GUID.</span></span> <span data-ttu-id="d7843-143">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="d7843-143">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d7843-144">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="d7843-144">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="d7843-145">Especifica o domínio principal para o que o servidor DNS do AD é autoritativo.</span><span class="sxs-lookup"><span data-stu-id="d7843-145">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="d7843-146">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="d7843-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d7843-147">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="d7843-147">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="d7843-148">Especifica o identificador de segurança (SID).</span><span class="sxs-lookup"><span data-stu-id="d7843-148">Specifies the security identifier (SID).</span></span> <span data-ttu-id="d7843-149">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="d7843-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d7843-150">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="d7843-150">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="d7843-151">Especifica a floresta do Active Directory para obter.</span><span class="sxs-lookup"><span data-stu-id="d7843-151">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="d7843-152">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="d7843-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d7843-153">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="d7843-153">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="d7843-154">Especifica o nome de domínio do NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="d7843-154">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="d7843-155">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="d7843-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d7843-156">-AllowBpublicAccess</span><span class="sxs-lookup"><span data-stu-id="d7843-156">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="d7843-157">Permitir o acesso público a todos os blobs ou contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-157">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="d7843-158">A interpretação padrão é verdadeira para esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="d7843-158">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="d7843-159">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7843-159">-AsJob</span></span>
<span data-ttu-id="d7843-160">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d7843-160">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7843-161">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d7843-161">-AssignIdentity</span></span>
<span data-ttu-id="d7843-162">Gere e atribua uma nova identidade de conta de armazenamento para esta conta de Armazenamento para ser usada com os principais serviços de gerenciamento, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="d7843-162">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d7843-163">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d7843-163">-CustomDomainName</span></span>
<span data-ttu-id="d7843-164">Especifica o nome do domínio personalizado da conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-164">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="d7843-165">O valor padrão é Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-165">The default value is Storage.</span></span>

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

### <span data-ttu-id="d7843-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7843-166">-DefaultProfile</span></span>
<span data-ttu-id="d7843-167">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7843-167">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7843-168">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d7843-168">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="d7843-169">Habilitar a Autenticação de Serviço de Domínio do Azure Files Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-169">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="d7843-170">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d7843-170">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="d7843-171">Habilitar a Autenticação de Serviço de Domínio do Azure Files Azure Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-171">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="d7843-172">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="d7843-172">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="d7843-173">Indica se a conta de armazenamento habilita ou não o Namespace Hierárquico.</span><span class="sxs-lookup"><span data-stu-id="d7843-173">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="d7843-174">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="d7843-174">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="d7843-175">Indica se a conta de armazenamento só habilita o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d7843-175">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="d7843-176">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="d7843-176">-EnableLargeFileShare</span></span>
<span data-ttu-id="d7843-177">Indica se a conta de armazenamento pode ou não dar suporte a compartilhamentos de arquivos grandes com mais de 5 capacidade tib.</span><span class="sxs-lookup"><span data-stu-id="d7843-177">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="d7843-178">Depois que a conta for habilitada, o recurso não poderá ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d7843-178">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="d7843-179">Atualmente, só há suporte para tipos de replicação LRS e ZRS, portanto, as conversões de contas em contas redundantes geográficas não seriam possíveis.</span><span class="sxs-lookup"><span data-stu-id="d7843-179">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="d7843-180">Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="d7843-180">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="d7843-181">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="d7843-181">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="d7843-182">Definir o KeyType de Criptografia para Fila.</span><span class="sxs-lookup"><span data-stu-id="d7843-182">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="d7843-183">O valor padrão é Serviço.</span><span class="sxs-lookup"><span data-stu-id="d7843-183">The default value is Service.</span></span>
<span data-ttu-id="d7843-184">-Conta: a fila será criptografada com a chave de criptografia com escopo de conta.</span><span class="sxs-lookup"><span data-stu-id="d7843-184">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="d7843-185">-Serviço: a fila sempre será criptografada com Service-Managed teclas.</span><span class="sxs-lookup"><span data-stu-id="d7843-185">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="d7843-186">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="d7843-186">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="d7843-187">De definir o Tipo de Chave de Criptografia para Tabela.</span><span class="sxs-lookup"><span data-stu-id="d7843-187">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="d7843-188">O valor padrão é Serviço.</span><span class="sxs-lookup"><span data-stu-id="d7843-188">The default value is Service.</span></span>
- <span data-ttu-id="d7843-189">Conta: A tabela será criptografada com a chave de criptografia com escopo de conta.</span><span class="sxs-lookup"><span data-stu-id="d7843-189">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="d7843-190">Serviço: A tabela sempre será criptografada com Service-Managed teclas.</span><span class="sxs-lookup"><span data-stu-id="d7843-190">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="d7843-191">-Tipo</span><span class="sxs-lookup"><span data-stu-id="d7843-191">-Kind</span></span>
<span data-ttu-id="d7843-192">Especifica o tipo de conta de Armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d7843-192">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d7843-193">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d7843-193">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7843-194">Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-194">Storage.</span></span> <span data-ttu-id="d7843-195">Conta de Armazenamento de finalidade geral que oferece suporte ao armazenamento de Blobs, Tabelas, Filas, Arquivos e Discos.</span><span class="sxs-lookup"><span data-stu-id="d7843-195">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="d7843-196">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d7843-196">StorageV2.</span></span> <span data-ttu-id="d7843-197">Conta de armazenamento GPv2 (General Purpose Version 2) que oferece suporte a Blobs, Tabelas, Filas, Arquivos e Discos, com recursos avançados como a camada de dados.</span><span class="sxs-lookup"><span data-stu-id="d7843-197">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="d7843-198">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="d7843-198">BlobStorage.</span></span> <span data-ttu-id="d7843-199">Conta de Armazenamento de Blob que oferece suporte somente ao armazenamento de Blobs.</span><span class="sxs-lookup"><span data-stu-id="d7843-199">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="d7843-200">BlockBtrucStorage.</span><span class="sxs-lookup"><span data-stu-id="d7843-200">BlockBlobStorage.</span></span> <span data-ttu-id="d7843-201">Blob Storage account which supports storage of Block Blobs only.</span><span class="sxs-lookup"><span data-stu-id="d7843-201">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="d7843-202">FileStorage.</span><span class="sxs-lookup"><span data-stu-id="d7843-202">FileStorage.</span></span> <span data-ttu-id="d7843-203">Conta de Armazenamento de Arquivos que oferece suporte apenas ao armazenamento de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="d7843-203">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="d7843-204">O valor padrão é StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d7843-204">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="d7843-205">-Local</span><span class="sxs-lookup"><span data-stu-id="d7843-205">-Location</span></span>
<span data-ttu-id="d7843-206">Especifica o local da conta de armazenamento a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d7843-206">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="d7843-207">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d7843-207">-MinimumTlsVersion</span></span>
<span data-ttu-id="d7843-208">A versão TLS mínima a ser permitida em solicitações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-208">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="d7843-209">A interpretação padrão é TLS 1.0 para esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="d7843-209">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="d7843-210">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7843-210">-Name</span></span>
<span data-ttu-id="d7843-211">Especifica o nome da conta de armazenamento a ser criado.</span><span class="sxs-lookup"><span data-stu-id="d7843-211">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="d7843-212">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d7843-212">-NetworkRuleSet</span></span>
<span data-ttu-id="d7843-213">O NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como serviços permitidos para ignorar as regras e como lidar com solicitações que não corresponderem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="d7843-213">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="d7843-214">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7843-214">-PublishInternetEndpoint</span></span>
<span data-ttu-id="d7843-215">Indica se os pontos de extremidade de armazenamento de roteamento da Internet devem ser publicados</span><span class="sxs-lookup"><span data-stu-id="d7843-215">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="d7843-216">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7843-216">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="d7843-217">Indica se os pontos de extremidade de armazenamento de roteamento da Microsoft devem ser publicados</span><span class="sxs-lookup"><span data-stu-id="d7843-217">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="d7843-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7843-218">-ResourceGroupName</span></span>
<span data-ttu-id="d7843-219">Especifica o nome do grupo de recursos no qual adicionar a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7843-219">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="d7843-220">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="d7843-220">-RoutingChoice</span></span>
<span data-ttu-id="d7843-221">A Opção de Roteamento define o tipo de roteamento de rede escolhido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d7843-221">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="d7843-222">Os valores possíveis incluem: 'MicrosoftRouting', 'InternetRouting'</span><span class="sxs-lookup"><span data-stu-id="d7843-222">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="d7843-223">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d7843-223">-SkuName</span></span>
<span data-ttu-id="d7843-224">Especifica o nome da SKU da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d7843-224">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d7843-225">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d7843-225">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d7843-226">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="d7843-226">Standard_LRS.</span></span> <span data-ttu-id="d7843-227">Armazenamento localmente redundante.</span><span class="sxs-lookup"><span data-stu-id="d7843-227">Locally-redundant storage.</span></span>
- <span data-ttu-id="d7843-228">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="d7843-228">Standard_ZRS.</span></span> <span data-ttu-id="d7843-229">Armazenamento redundante de zona.</span><span class="sxs-lookup"><span data-stu-id="d7843-229">Zone-redundant storage.</span></span>
- <span data-ttu-id="d7843-230">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="d7843-230">Standard_GRS.</span></span> <span data-ttu-id="d7843-231">Armazenamento geo redundante.</span><span class="sxs-lookup"><span data-stu-id="d7843-231">Geo-redundant storage.</span></span>
- <span data-ttu-id="d7843-232">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="d7843-232">Standard_RAGRS.</span></span> <span data-ttu-id="d7843-233">Ler o armazenamento geo redundante do acesso.</span><span class="sxs-lookup"><span data-stu-id="d7843-233">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="d7843-234">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="d7843-234">Premium_LRS.</span></span> <span data-ttu-id="d7843-235">Armazenamento localmente redundante premium.</span><span class="sxs-lookup"><span data-stu-id="d7843-235">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="d7843-236">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="d7843-236">Premium_ZRS.</span></span> <span data-ttu-id="d7843-237">Armazenamento redundante de zona premium.</span><span class="sxs-lookup"><span data-stu-id="d7843-237">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="d7843-238">Standard_GZRS - Armazenamento redundante de zona geo redundante.</span><span class="sxs-lookup"><span data-stu-id="d7843-238">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="d7843-239">Standard_RAGZRS - Armazenamento redundante de zona de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="d7843-239">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="d7843-240">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7843-240">-Tag</span></span>
<span data-ttu-id="d7843-241">Pares de valor-chave na forma de uma tabela hash definida como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="d7843-241">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="d7843-242">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d7843-242">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d7843-243">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="d7843-243">-UseSubDomain</span></span>
<span data-ttu-id="d7843-244">Indica se é possível habilitar a validação indireta de CName.</span><span class="sxs-lookup"><span data-stu-id="d7843-244">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="d7843-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7843-245">CommonParameters</span></span>
<span data-ttu-id="d7843-246">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7843-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7843-247">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7843-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7843-248">Entradas</span><span class="sxs-lookup"><span data-stu-id="d7843-248">INPUTS</span></span>

### <span data-ttu-id="d7843-249">System.String</span><span class="sxs-lookup"><span data-stu-id="d7843-249">System.String</span></span>

## <span data-ttu-id="d7843-250">Saídas</span><span class="sxs-lookup"><span data-stu-id="d7843-250">OUTPUTS</span></span>

### <span data-ttu-id="d7843-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7843-251">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d7843-252">Notas</span><span class="sxs-lookup"><span data-stu-id="d7843-252">NOTES</span></span>

## <span data-ttu-id="d7843-253">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7843-253">RELATED LINKS</span></span>

[<span data-ttu-id="d7843-254">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7843-254">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="d7843-255">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7843-255">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="d7843-256">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7843-256">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
