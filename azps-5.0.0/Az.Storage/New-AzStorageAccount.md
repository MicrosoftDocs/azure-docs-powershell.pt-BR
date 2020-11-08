---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 022c27b3eec589e395e1044f165ee9f8f17d1cad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117189"
---
# <span data-ttu-id="d0f06-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0f06-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="d0f06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0f06-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f06-103">Cria uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-103">Creates a Storage account.</span></span>

## <span data-ttu-id="d0f06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0f06-104">SYNTAX</span></span>

### <span data-ttu-id="d0f06-105">AzureActiveDirectoryDomainServicesForFile (padrão)</span><span class="sxs-lookup"><span data-stu-id="d0f06-105">AzureActiveDirectoryDomainServicesForFile (Default)</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-AsJob] [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>]
 [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f06-106">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d0f06-106">ActiveDirectoryDomainServicesForFile</span></span>
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare]
 [-EnableActiveDirectoryDomainServicesForFile <Boolean>] [-ActiveDirectoryDomainName <String>]
 [-ActiveDirectoryNetBiosDomainName <String>] [-ActiveDirectoryForestName <String>]
 [-ActiveDirectoryDomainGuid <String>] [-ActiveDirectoryDomainSid <String>]
 [-ActiveDirectoryAzureStorageSid <String>] [-AsJob] [-EncryptionKeyTypeForTable <String>]
 [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption] [-AllowBlobPublicAccess <Boolean>]
 [-MinimumTlsVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f06-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0f06-107">DESCRIPTION</span></span>
<span data-ttu-id="d0f06-108">O cmdlet **New-AzStorageAccount** cria uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f06-108">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="d0f06-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0f06-109">EXAMPLES</span></span>

### <span data-ttu-id="d0f06-110">Exemplo 1: criar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="d0f06-110">Example 1: Create a Storage account</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="d0f06-111">Esse comando cria uma conta de armazenamento para o nome do grupo de recursos MyResource.</span><span class="sxs-lookup"><span data-stu-id="d0f06-111">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="d0f06-112">Exemplo 2: criar uma conta de armazenamento blob com BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="d0f06-112">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="d0f06-113">Esse comando cria uma conta de armazenamento BLOB que tem o tipo BlobStorage e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="d0f06-113">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="d0f06-114">Exemplo 3: criar uma conta de armazenamento com o tipo StorageV2 e gerar e atribuir uma identidade para o repositório de senhas do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f06-114">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="d0f06-115">Esse comando cria uma conta de armazenamento com o tipo StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d0f06-115">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="d0f06-116">Ele também gera e atribui uma identidade que pode ser usada para gerenciar as chaves de conta por meio do Azure keyvault.</span><span class="sxs-lookup"><span data-stu-id="d0f06-116">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="d0f06-117">Exemplo 4: criar uma conta de armazenamento com o NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="d0f06-117">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="d0f06-118">Esse comando cria uma conta de armazenamento que tem uma propriedade NetworkRuleSet do JSON</span><span class="sxs-lookup"><span data-stu-id="d0f06-118">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="d0f06-119">Exemplo 5: criar uma conta de armazenamento com namespace hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="d0f06-119">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="d0f06-120">Esse comando cria uma conta de armazenamento com namespace hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="d0f06-120">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="d0f06-121">Exemplo 6: criar uma conta de armazenamento com o Azure files Azure DS e habilitar o compartilhamento de arquivos grande.</span><span class="sxs-lookup"><span data-stu-id="d0f06-121">Example 6: Create a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

<span data-ttu-id="d0f06-122">Esse comando cria uma conta de armazenamento com o Azure files Azure DS e habilita o compartilhamento de arquivos grande.</span><span class="sxs-lookup"><span data-stu-id="d0f06-122">This command creates a Storage account with Azure Files AAD DS Authentication, and enable large file share.</span></span>

### <span data-ttu-id="d0f06-123">Exemplo 7: criar uma conta de armazenamento com habilitar arquivos na autenticação do serviço de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0f06-123">Example 7: Create a Storage account with enable Files Active Directory Domain Service Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

<span data-ttu-id="d0f06-124">Esse comando cria uma conta de armazenamento withenable arquivos de autenticação do serviço de domínio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d0f06-124">This command creates a Storage account withenable Files Active Directory Domain Service Authentication.</span></span>

### <span data-ttu-id="d0f06-125">Exemplo 8: criar uma conta de armazenamento com o serviço de fila e de tabela use a chave de criptografia de escopo da conta e exigir criptografia de infraestrutura.</span><span class="sxs-lookup"><span data-stu-id="d0f06-125">Example 8: Create a Storage account with Queue and Table Service use account-scoped encryption key, and Require Infrastructure Encryption.</span></span>
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

<span data-ttu-id="d0f06-126">Esse comando cria uma conta de armazenamento com o serviço de fila e fila usar chave de criptografia de escopo da conta e requer criptografia de infraestrutura, portanto, a fila e a tabela usarão a mesma chave de criptografia com BLOB e serviço de arquivo, e o serviço aplicará uma camada secundária de criptografia com chaves gerenciadas pela plataforma para dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="d0f06-126">This command creates a Storage account with Queue and Table Service use account-scoped encryption key and Require Infrastructure Encryption, so Queue and Table will use same encryption key with Blob and File service, and the service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>
<span data-ttu-id="d0f06-127">Em seguida, obtenha as propriedades da conta de armazenamento e exiba o tipo de keyserial de serviço de fila e tabela e o valor RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="d0f06-127">Then get the Storage account properties, and view the encryption keytype of Queue and Table Service, and RequireInfrastructureEncryption value.</span></span>

### <span data-ttu-id="d0f06-128">Exemplo 9: criar MinimumTlsVersion e AllowBlobPublicAccess de conta</span><span class="sxs-lookup"><span data-stu-id="d0f06-128">Example 9: Create account MinimumTlsVersion  and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="d0f06-129">O comando criar conta com MinimumTlsVersion e AllowBlobPublicAccess e, em seguida, mostrar as 2 Propriedades da conta criada</span><span class="sxs-lookup"><span data-stu-id="d0f06-129">The command create account with MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the created account</span></span> 

## <span data-ttu-id="d0f06-130">OS</span><span class="sxs-lookup"><span data-stu-id="d0f06-130">PARAMETERS</span></span>

### <span data-ttu-id="d0f06-131">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="d0f06-131">-AccessTier</span></span>
<span data-ttu-id="d0f06-132">Especifica a camada de acesso da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d0f06-132">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d0f06-133">Os valores aceitáveis para esse parâmetro são: quente e legal.</span><span class="sxs-lookup"><span data-stu-id="d0f06-133">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="d0f06-134">Se você especificar um valor de BlobStorage para o parâmetro *Kind* , você deve especificar um valor para o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="d0f06-134">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="d0f06-135">Se você especificar um valor de armazenamento para esse parâmetro de *tipo* , não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="d0f06-135">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="d0f06-136">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="d0f06-136">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="d0f06-137">Especifica o identificador de segurança (SID) do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f06-137">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="d0f06-138">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="d0f06-138">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d0f06-139">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="d0f06-139">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="d0f06-140">Especifica o GUID do domínio.</span><span class="sxs-lookup"><span data-stu-id="d0f06-140">Specifies the domain GUID.</span></span> <span data-ttu-id="d0f06-141">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="d0f06-141">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d0f06-142">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="d0f06-142">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="d0f06-143">Especifica o domínio primário para o qual o servidor DNS do AD é autorizado.</span><span class="sxs-lookup"><span data-stu-id="d0f06-143">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="d0f06-144">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="d0f06-144">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d0f06-145">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="d0f06-145">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="d0f06-146">Especifica o identificador de segurança (SID).</span><span class="sxs-lookup"><span data-stu-id="d0f06-146">Specifies the security identifier (SID).</span></span> <span data-ttu-id="d0f06-147">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="d0f06-147">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d0f06-148">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="d0f06-148">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="d0f06-149">Especifica a floresta do Active Directory a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="d0f06-149">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="d0f06-150">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="d0f06-150">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d0f06-151">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="d0f06-151">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="d0f06-152">Especifica o nome de domínio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-152">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="d0f06-153">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="d0f06-153">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="d0f06-154">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="d0f06-154">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="d0f06-155">Permita acesso público a todos os BLOBs ou recipientes na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-155">Allow public access to all blobs or containers in the storage account.</span></span> <span data-ttu-id="d0f06-156">A interpretação padrão é verdadeira para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d0f06-156">The default interpretation is true for this property.</span></span>

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

### <span data-ttu-id="d0f06-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0f06-157">-AsJob</span></span>
<span data-ttu-id="d0f06-158">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d0f06-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0f06-159">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d0f06-159">-AssignIdentity</span></span>
<span data-ttu-id="d0f06-160">Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f06-160">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d0f06-161">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d0f06-161">-CustomDomainName</span></span>
<span data-ttu-id="d0f06-162">Especifica o nome do domínio personalizado da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-162">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="d0f06-163">O valor padrão é armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-163">The default value is Storage.</span></span>

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

### <span data-ttu-id="d0f06-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f06-164">-DefaultProfile</span></span>
<span data-ttu-id="d0f06-165">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f06-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f06-166">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d0f06-166">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="d0f06-167">Habilite o Azure files autenticação do serviço de domínio Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-167">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="d0f06-168">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="d0f06-168">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="d0f06-169">Habilite o Azure files autenticação do serviço de domínio Active Directory do Azure para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-169">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="d0f06-170">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="d0f06-170">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="d0f06-171">Indica se a conta de armazenamento permite ou não o namespace hierárquico.</span><span class="sxs-lookup"><span data-stu-id="d0f06-171">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="d0f06-172">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="d0f06-172">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="d0f06-173">Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-173">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="d0f06-174">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="d0f06-174">-EnableLargeFileShare</span></span>
<span data-ttu-id="d0f06-175">Indica se a conta de armazenamento pode ou não dar suporte a grandes compartilhamentos de arquivos com mais de 5 TiB de capacidade.</span><span class="sxs-lookup"><span data-stu-id="d0f06-175">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="d0f06-176">Uma vez que a conta esteja habilitada, o recurso não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d0f06-176">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="d0f06-177">Atualmente só tem suporte para tipos de replicação LRS e ZRS, portanto, não é possível fazer conversões de conta para contas com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="d0f06-177">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="d0f06-178">Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="d0f06-178">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="d0f06-179">-EncryptionKeyTypeForQueue</span><span class="sxs-lookup"><span data-stu-id="d0f06-179">-EncryptionKeyTypeForQueue</span></span>
<span data-ttu-id="d0f06-180">Defina o KeyType de criptografia para a fila.</span><span class="sxs-lookup"><span data-stu-id="d0f06-180">Set the Encryption KeyType for Queue.</span></span> <span data-ttu-id="d0f06-181">O valor padrão é serviço.</span><span class="sxs-lookup"><span data-stu-id="d0f06-181">The default value is Service.</span></span>
<span data-ttu-id="d0f06-182">-Conta: a fila será criptografada com a chave de criptografia de escopo da conta.</span><span class="sxs-lookup"><span data-stu-id="d0f06-182">-Account: Queue will be encrypted with account-scoped encryption key.</span></span> <span data-ttu-id="d0f06-183">-Serviço: a fila sempre será criptografada com teclas de Service-Managed.</span><span class="sxs-lookup"><span data-stu-id="d0f06-183">-Service: Queue will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="d0f06-184">-EncryptionKeyTypeForTable</span><span class="sxs-lookup"><span data-stu-id="d0f06-184">-EncryptionKeyTypeForTable</span></span>
<span data-ttu-id="d0f06-185">Defina o KeyType de criptografia para a tabela.</span><span class="sxs-lookup"><span data-stu-id="d0f06-185">Set the Encryption KeyType for Table.</span></span> <span data-ttu-id="d0f06-186">O valor padrão é serviço.</span><span class="sxs-lookup"><span data-stu-id="d0f06-186">The default value is Service.</span></span>
- <span data-ttu-id="d0f06-187">Conta: a tabela será criptografada com a chave de criptografia de escopo da conta.</span><span class="sxs-lookup"><span data-stu-id="d0f06-187">Account: Table will be encrypted with account-scoped encryption key.</span></span> 
- <span data-ttu-id="d0f06-188">Serviço: a tabela sempre será criptografada com teclas de Service-Managed.</span><span class="sxs-lookup"><span data-stu-id="d0f06-188">Service: Table will always be encrypted with Service-Managed keys.</span></span> 

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

### <span data-ttu-id="d0f06-189">-Kind</span><span class="sxs-lookup"><span data-stu-id="d0f06-189">-Kind</span></span>
<span data-ttu-id="d0f06-190">Especifica o tipo de conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d0f06-190">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d0f06-191">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d0f06-191">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0f06-192">SPS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-192">Storage.</span></span> <span data-ttu-id="d0f06-193">Conta de armazenamento de finalidade geral que dá suporte ao armazenamento de BLOBs, tabelas, filas, arquivos e discos.</span><span class="sxs-lookup"><span data-stu-id="d0f06-193">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="d0f06-194">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d0f06-194">StorageV2.</span></span> <span data-ttu-id="d0f06-195">Conta de armazenamento do GPv2 (general purpose Version 2) que oferece suporte a BLOBs, tabelas, filas, arquivos e discos, com recursos avançados, como hierarquização de dados.</span><span class="sxs-lookup"><span data-stu-id="d0f06-195">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="d0f06-196">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="d0f06-196">BlobStorage.</span></span> <span data-ttu-id="d0f06-197">Conta de armazenamento de BLOB que dá suporte somente ao armazenamento de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="d0f06-197">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="d0f06-198">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="d0f06-198">BlockBlobStorage.</span></span> <span data-ttu-id="d0f06-199">Bloquear uma conta de armazenamento BLOB que dê suporte somente ao armazenamento de blobs de blocos.</span><span class="sxs-lookup"><span data-stu-id="d0f06-199">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="d0f06-200">Armazenamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-200">FileStorage.</span></span> <span data-ttu-id="d0f06-201">Conta de armazenamento de arquivos que dá suporte somente ao armazenamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d0f06-201">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="d0f06-202">O valor padrão é StorageV2.</span><span class="sxs-lookup"><span data-stu-id="d0f06-202">The default value is StorageV2.</span></span>

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

### <span data-ttu-id="d0f06-203">-Local</span><span class="sxs-lookup"><span data-stu-id="d0f06-203">-Location</span></span>
<span data-ttu-id="d0f06-204">Especifica o local da conta de armazenamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="d0f06-204">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="d0f06-205">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="d0f06-205">-MinimumTlsVersion</span></span>
<span data-ttu-id="d0f06-206">A versão mínima de TLS a ser permitida nas solicitações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d0f06-206">The minimum TLS version to be permitted on requests to storage.</span></span> <span data-ttu-id="d0f06-207">A interpretação padrão é TLS 1,0 para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="d0f06-207">The default interpretation is TLS 1.0 for this property.</span></span>

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

### <span data-ttu-id="d0f06-208">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0f06-208">-Name</span></span>
<span data-ttu-id="d0f06-209">Especifica o nome da conta de armazenamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="d0f06-209">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="d0f06-210">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d0f06-210">-NetworkRuleSet</span></span>
<span data-ttu-id="d0f06-211">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como os serviços permitidos para ignorar as regras e como lidar com as solicitações que não correspondem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="d0f06-211">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="d0f06-212">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="d0f06-212">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="d0f06-213">O serviço aplicará uma camada secundária de criptografia com chaves gerenciadas pela plataforma para dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="d0f06-213">The service will apply a secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="d0f06-214">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f06-214">-ResourceGroupName</span></span>
<span data-ttu-id="d0f06-215">Especifica o nome do grupo de recursos no qual a conta de armazenamento será adicionada.</span><span class="sxs-lookup"><span data-stu-id="d0f06-215">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="d0f06-216">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d0f06-216">-SkuName</span></span>
<span data-ttu-id="d0f06-217">Especifica o nome do SKU da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d0f06-217">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="d0f06-218">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d0f06-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0f06-219">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-219">Standard_LRS.</span></span> <span data-ttu-id="d0f06-220">Armazenamento redundante localmente.</span><span class="sxs-lookup"><span data-stu-id="d0f06-220">Locally-redundant storage.</span></span>
- <span data-ttu-id="d0f06-221">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-221">Standard_ZRS.</span></span> <span data-ttu-id="d0f06-222">Armazenamento redundante na zona.</span><span class="sxs-lookup"><span data-stu-id="d0f06-222">Zone-redundant storage.</span></span>
- <span data-ttu-id="d0f06-223">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-223">Standard_GRS.</span></span> <span data-ttu-id="d0f06-224">Armazenamento com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="d0f06-224">Geo-redundant storage.</span></span>
- <span data-ttu-id="d0f06-225">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-225">Standard_RAGRS.</span></span> <span data-ttu-id="d0f06-226">Acesso de leitura com armazenamento redundante geográfico.</span><span class="sxs-lookup"><span data-stu-id="d0f06-226">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="d0f06-227">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-227">Premium_LRS.</span></span> <span data-ttu-id="d0f06-228">Premium-armazenamento redundante local.</span><span class="sxs-lookup"><span data-stu-id="d0f06-228">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="d0f06-229">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="d0f06-229">Premium_ZRS.</span></span> <span data-ttu-id="d0f06-230">Zona Premium – armazenamento redundante.</span><span class="sxs-lookup"><span data-stu-id="d0f06-230">Premium zone-redundant storage.</span></span>
- <span data-ttu-id="d0f06-231">Standard_GZRS-armazenamento redundante de zona com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="d0f06-231">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="d0f06-232">Standard_RAGZRS-ler o acesso à zona de redundância geográfica-armazenamento redundante.</span><span class="sxs-lookup"><span data-stu-id="d0f06-232">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>

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

### <span data-ttu-id="d0f06-233">-Marca</span><span class="sxs-lookup"><span data-stu-id="d0f06-233">-Tag</span></span>
<span data-ttu-id="d0f06-234">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="d0f06-234">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="d0f06-235">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d0f06-235">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d0f06-236">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="d0f06-236">-UseSubDomain</span></span>
<span data-ttu-id="d0f06-237">Indica se a validação de CName indireto deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="d0f06-237">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="d0f06-238">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f06-238">CommonParameters</span></span>
<span data-ttu-id="d0f06-239">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f06-239">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f06-240">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f06-240">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f06-241">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0f06-241">INPUTS</span></span>

### <span data-ttu-id="d0f06-242">System. String</span><span class="sxs-lookup"><span data-stu-id="d0f06-242">System.String</span></span>

## <span data-ttu-id="d0f06-243">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0f06-243">OUTPUTS</span></span>

### <span data-ttu-id="d0f06-244">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0f06-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="d0f06-245">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0f06-245">NOTES</span></span>

## <span data-ttu-id="d0f06-246">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0f06-246">RELATED LINKS</span></span>

[<span data-ttu-id="d0f06-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0f06-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="d0f06-248">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0f06-248">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="d0f06-249">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0f06-249">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
