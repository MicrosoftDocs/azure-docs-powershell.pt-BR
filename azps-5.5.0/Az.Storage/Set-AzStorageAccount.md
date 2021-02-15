---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 4a4898645e3f296f861aa9f19a60ea182c112bff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112510"
---
# <span data-ttu-id="44960-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44960-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="44960-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44960-102">SYNOPSIS</span></span>
<span data-ttu-id="44960-103">Modifica uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="44960-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44960-104">SYNTAX</span></span>

### <span data-ttu-id="44960-105">StorageEncryption (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44960-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44960-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="44960-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44960-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="44960-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44960-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="44960-108">DESCRIPTION</span></span>
<span data-ttu-id="44960-109">O **cmdlet Set-AzStorageAccount** modifica uma conta de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44960-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="44960-110">Você pode usar esse cmdlet para modificar o tipo de conta, atualizar um domínio do cliente ou definir marcas em uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="44960-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44960-111">EXAMPLES</span></span>

### <span data-ttu-id="44960-112">Exemplo 1: Definir o tipo de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44960-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="44960-113">Esse comando define o tipo de conta de armazenamento como Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="44960-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="44960-114">Exemplo 2: Definir um domínio personalizado para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="44960-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="44960-115">Esse comando define um domínio personalizado para uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="44960-116">Exemplo 3: Definir o valor da camada de acesso</span><span class="sxs-lookup"><span data-stu-id="44960-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="44960-117">O comando define o valor do Nível do Access como interessante.</span><span class="sxs-lookup"><span data-stu-id="44960-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="44960-118">Exemplo 4: Definir o domínio e as marcas personalizados</span><span class="sxs-lookup"><span data-stu-id="44960-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="44960-119">O comando define o domínio personalizado e as marcas de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="44960-120">Exemplo 5: definir a fonte de chave de criptografia como Keyvault</span><span class="sxs-lookup"><span data-stu-id="44960-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="44960-121">Esse comando definiu a Fonteda Chave de Criptografia com um novo Keyvault criado.</span><span class="sxs-lookup"><span data-stu-id="44960-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="44960-122">Exemplo 6: definir a fonte de chave de criptografia como "Microsoft.Storage"</span><span class="sxs-lookup"><span data-stu-id="44960-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="44960-123">Este comando definiu a Chave de Criptografia Como "Microsoft.Storage"</span><span class="sxs-lookup"><span data-stu-id="44960-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="44960-124">Exemplo 7: Definir a propriedade NetworkRuleSet de uma conta de armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="44960-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="44960-125">Este comando define a propriedade NetworkRuleSet de uma conta de Armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="44960-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="44960-126">Exemplo 8: Obter a propriedade NetworkRuleSet de uma conta de armazenamento e defini-la para outra conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="44960-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="44960-127">Este primeiro comando obtém a propriedade NetworkRuleSet de uma conta de Armazenamento, e o segundo comando a define para outra conta de Armazenamento</span><span class="sxs-lookup"><span data-stu-id="44960-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="44960-128">Exemplo 9: Atualizar uma conta de Armazenamento com Kind "Storage" ou "BlobStorage" para "StorageV2" kind Storage account</span><span class="sxs-lookup"><span data-stu-id="44960-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="44960-129">O comando atualiza uma conta de Armazenamento com Kind "Armazenamento" ou "BlobStorage" para uma conta de Armazenamento do tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="44960-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="44960-130">Exemplo 10: Atualizar uma conta de armazenamento habilitando a Autenticação DS do Azure Files AAD.</span><span class="sxs-lookup"><span data-stu-id="44960-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="44960-131">O comando atualiza uma conta de armazenamento habilitando a Autenticação do Azure Files AAD DS.</span><span class="sxs-lookup"><span data-stu-id="44960-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="44960-132">Exemplo 11: Atualizar uma conta de armazenamento habilitando a Autenticação de Serviço de Domínio do Active Directory arquivos e, em seguida, mostrar a configuração de autenticação baseada em identidade de arquivo</span><span class="sxs-lookup"><span data-stu-id="44960-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
        
PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AD

PS C:\> $account.AzureFilesIdentityBasedAuth.ActiveDirectoryProperties

DomainName        : mydomain.com
NetBiosDomainName : mydomain.com
ForestName        : mydomain.com
DomainGuid        : 12345678-1234-1234-1234-123456789012
DomainSid         : S-1-5-21-1234567890-1234567890-1234567890
AzureStorageSid   : S-1-5-21-1234567890-1234567890-1234567890-1234
```

<span data-ttu-id="44960-133">O comando atualiza uma conta de Armazenamento habilitando a Autenticação de Serviço de Domínio do Azure Files Active Directory e, em seguida, mostra a configuração de autenticação baseada em identidade de arquivo</span><span class="sxs-lookup"><span data-stu-id="44960-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="44960-134">Exemplo 12: Definir MinimumTlsVersion e AllowBpublicAccesss</span><span class="sxs-lookup"><span data-stu-id="44960-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="44960-135">O comando define MinimumTlsVersion e AllowBpublicAccess e mostra as 2 propriedades da conta</span><span class="sxs-lookup"><span data-stu-id="44960-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

### <span data-ttu-id="44960-136">Exemplo 13: Atualizar uma conta de armazenamento com a configuração RoutingPreference</span><span class="sxs-lookup"><span data-stu-id="44960-136">Example 13: Update a Storage account with RoutingPreference setting</span></span>
```powershell
PS C:\>$account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -PublishMicrosoftEndpoint $false -PublishInternetEndpoint $true -RoutingChoice InternetRouting

PS C:\>$account.RoutingPreference

RoutingChoice   PublishMicrosoftEndpoints PublishInternetEndpoints
-------------   ------------------------- ------------------------
InternetRouting                     False                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : 
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

<span data-ttu-id="44960-137">Este comando atualiza uma conta de Armazenamento com a configuração RoutingPreference: PublishMicrosoftEndpoint como false, PublishInternetEndpoint as true e RoutingChoice como MicrosoftRouting.</span><span class="sxs-lookup"><span data-stu-id="44960-137">This command updates a Storage account with RoutingPreference setting: PublishMicrosoftEndpoint as false, PublishInternetEndpoint as true, and RoutingChoice as MicrosoftRouting.</span></span>

## <span data-ttu-id="44960-138">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44960-138">PARAMETERS</span></span>

### <span data-ttu-id="44960-139">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="44960-139">-AccessTier</span></span>
<span data-ttu-id="44960-140">Especifica o nível de acesso da conta de armazenamento que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="44960-140">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="44960-141">Os valores aceitáveis para este parâmetro são: Hot e Cool.</span><span class="sxs-lookup"><span data-stu-id="44960-141">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="44960-142">Se você alterar o nível de acesso, ele poderá resultar em cobranças adicionais.</span><span class="sxs-lookup"><span data-stu-id="44960-142">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="44960-143">Para obter mais informações, consulte [Armazenamento de Blob do Azure: camadas de armazenamento interessantes e interessantes.](http://go.microsoft.com/fwlink/?LinkId=786482)</span><span class="sxs-lookup"><span data-stu-id="44960-143">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="44960-144">Se a conta de Armazenamento tiver Kind como StorageV2 ou BlobStorage, você poderá especificar o parâmetro *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="44960-144">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="44960-145">Se a conta de Armazenamento tiver Kind as Storage, não especifique o parâmetro *AccessTier.*</span><span class="sxs-lookup"><span data-stu-id="44960-145">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="44960-146">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="44960-146">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="44960-147">Especifica o identificador de segurança (SID) para Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="44960-147">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="44960-148">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="44960-148">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="44960-149">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="44960-149">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="44960-150">Especifica o GUID do domínio.</span><span class="sxs-lookup"><span data-stu-id="44960-150">Specifies the domain GUID.</span></span> <span data-ttu-id="44960-151">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="44960-151">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="44960-152">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="44960-152">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="44960-153">Especifica o domínio principal para o que o servidor DNS do AD é autoritativo.</span><span class="sxs-lookup"><span data-stu-id="44960-153">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="44960-154">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="44960-154">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="44960-155">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="44960-155">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="44960-156">Especifica o identificador de segurança (SID).</span><span class="sxs-lookup"><span data-stu-id="44960-156">Specifies the security identifier (SID).</span></span> <span data-ttu-id="44960-157">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="44960-157">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="44960-158">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="44960-158">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="44960-159">Especifica a floresta do Active Directory para obter.</span><span class="sxs-lookup"><span data-stu-id="44960-159">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="44960-160">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="44960-160">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="44960-161">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="44960-161">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="44960-162">Especifica o nome de domínio do NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="44960-162">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="44960-163">Esse parâmetro deve ser definido quando -EnableActiveDirectoryDomainServicesForFile estiver definido como true.</span><span class="sxs-lookup"><span data-stu-id="44960-163">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="44960-164">-AllowBpublicAccess</span><span class="sxs-lookup"><span data-stu-id="44960-164">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="44960-165">Permitir ou não permitir o acesso público a todos os blobs ou contêineres na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-165">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="44960-166">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44960-166">-AsJob</span></span>
<span data-ttu-id="44960-167">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="44960-167">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44960-168">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="44960-168">-AssignIdentity</span></span>
<span data-ttu-id="44960-169">Gere e atribua uma nova identidade de conta de armazenamento para esta conta de Armazenamento para ser usada com os principais serviços de gerenciamento, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="44960-169">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="44960-170">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="44960-170">-CustomDomainName</span></span>
<span data-ttu-id="44960-171">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="44960-171">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="44960-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44960-172">-DefaultProfile</span></span>
<span data-ttu-id="44960-173">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44960-173">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44960-174">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="44960-174">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="44960-175">Habilitar a Autenticação de Serviço de Domínio do Azure Files Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-176">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="44960-176">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="44960-177">Habilitar a Autenticação de Serviço de Domínio do Azure Files Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-177">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: StorageEncryption, KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-178">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="44960-178">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="44960-179">Indica se a conta de armazenamento só habilita o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="44960-179">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="44960-180">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="44960-180">-EnableLargeFileShare</span></span>
<span data-ttu-id="44960-181">Indica se a conta de armazenamento pode ou não dar suporte a compartilhamentos de arquivos grandes com mais de 5 capacidade tib.</span><span class="sxs-lookup"><span data-stu-id="44960-181">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="44960-182">Depois que a conta for habilitada, o recurso não poderá ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="44960-182">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="44960-183">Atualmente, só há suporte para tipos de replicação LRS e ZRS, portanto, as conversões de contas em contas redundantes geográficas não seriam possíveis.</span><span class="sxs-lookup"><span data-stu-id="44960-183">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="44960-184">Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="44960-184">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="44960-185">-Forçar</span><span class="sxs-lookup"><span data-stu-id="44960-185">-Force</span></span>
<span data-ttu-id="44960-186">Força a alteração a ser escrita na conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-186">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="44960-187">-KeyName</span><span class="sxs-lookup"><span data-stu-id="44960-187">-KeyName</span></span>
<span data-ttu-id="44960-188">Se estiver usando -KeyvaultEncryption para habilitar a criptografia com o Cofre de Teclas, especifique a propriedade Keyname com essa opção.</span><span class="sxs-lookup"><span data-stu-id="44960-188">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-189">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="44960-189">-KeyvaultEncryption</span></span>
<span data-ttu-id="44960-190">Indica se você deve ou não usar o Microsoft KeyVault para as chaves de criptografia ao usar a Criptografia do Serviço de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-190">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="44960-191">Se KeyName, KeyVersion e KeyVaultUri estão todos definidos, a KeySource será definida como Microsoft.Keyvault se esse parâmetro estiver definido ou não.</span><span class="sxs-lookup"><span data-stu-id="44960-191">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-192">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="44960-192">-KeyVaultUri</span></span>
<span data-ttu-id="44960-193">Ao usar a Criptografia do Cofre de Chave especificando o parâmetro -KeyvaultEncryption, use essa opção para especificar o URI para o Cofre de Teclas.</span><span class="sxs-lookup"><span data-stu-id="44960-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-194">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="44960-194">-KeyVersion</span></span>
<span data-ttu-id="44960-195">Ao usar a Criptografia do Cofre de Chave especificando o parâmetro -KeyvaultEncryption, use essa opção para especificar o URI para a Versão de Chave.</span><span class="sxs-lookup"><span data-stu-id="44960-195">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-196">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="44960-196">-MinimumTlsVersion</span></span>
<span data-ttu-id="44960-197">A versão TLS mínima a ser permitida em solicitações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-197">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="44960-198">-Nome</span><span class="sxs-lookup"><span data-stu-id="44960-198">-Name</span></span>
<span data-ttu-id="44960-199">Especifica o nome da conta de armazenamento a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="44960-199">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="44960-200">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="44960-200">-NetworkRuleSet</span></span>
<span data-ttu-id="44960-201">O NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como serviços permitidos para ignorar as regras e como lidar com solicitações que não corresponderem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="44960-201">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="44960-202">-PublishInternetEndpoint</span><span class="sxs-lookup"><span data-stu-id="44960-202">-PublishInternetEndpoint</span></span>
<span data-ttu-id="44960-203">Indica se os pontos de extremidade de armazenamento de roteamento da Internet devem ser publicados</span><span class="sxs-lookup"><span data-stu-id="44960-203">Indicates whether internet  routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="44960-204">-PublishMicrosoftEndpoint</span><span class="sxs-lookup"><span data-stu-id="44960-204">-PublishMicrosoftEndpoint</span></span>
<span data-ttu-id="44960-205">Indica se os pontos de extremidade de armazenamento de roteamento da Microsoft devem ser publicados</span><span class="sxs-lookup"><span data-stu-id="44960-205">Indicates whether microsoft routing storage endpoints are to be published</span></span>

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

### <span data-ttu-id="44960-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44960-206">-ResourceGroupName</span></span>
<span data-ttu-id="44960-207">Especifica o nome do grupo de recursos no qual modificar a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-207">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="44960-208">-RoutingChoice</span><span class="sxs-lookup"><span data-stu-id="44960-208">-RoutingChoice</span></span>
<span data-ttu-id="44960-209">A Opção de Roteamento define o tipo de roteamento de rede escolhido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="44960-209">Routing Choice defines the kind of network routing opted by the user.</span></span> <span data-ttu-id="44960-210">Os valores possíveis incluem: 'MicrosoftRouting', 'InternetRouting'</span><span class="sxs-lookup"><span data-stu-id="44960-210">Possible values include: 'MicrosoftRouting', 'InternetRouting'</span></span>

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

### <span data-ttu-id="44960-211">-SkuName</span><span class="sxs-lookup"><span data-stu-id="44960-211">-SkuName</span></span>
<span data-ttu-id="44960-212">Especifica o nome da SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44960-212">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="44960-213">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="44960-213">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="44960-214">Standard_LRS - Armazenamento localmente redundante.</span><span class="sxs-lookup"><span data-stu-id="44960-214">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="44960-215">Standard_ZRS - Armazenamento redundante de zona.</span><span class="sxs-lookup"><span data-stu-id="44960-215">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="44960-216">Standard_GRS - Armazenamento geo redundante.</span><span class="sxs-lookup"><span data-stu-id="44960-216">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="44960-217">Standard_RAGRS - Armazenamento geo redundante de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="44960-217">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="44960-218">Premium_LRS - Armazenamento local redundante premium.</span><span class="sxs-lookup"><span data-stu-id="44960-218">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="44960-219">Standard_GZRS - Armazenamento redundante de zona geo redundante.</span><span class="sxs-lookup"><span data-stu-id="44960-219">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="44960-220">Standard_RAGZRS - Armazenamento redundante de zona de acesso de leitura.</span><span class="sxs-lookup"><span data-stu-id="44960-220">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="44960-221">Não é possível alterar Standard_ZRS e Premium_LRS tipos de conta para outros tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="44960-221">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="44960-222">Não é possível alterar outros tipos de conta para Standard_ZRS ou Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="44960-222">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Standard_GZRS, Standard_RAGZRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44960-223">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="44960-223">-StorageEncryption</span></span>
<span data-ttu-id="44960-224">Indica se você deve ou não definir a criptografia da conta de armazenamento para usar chaves gerenciadas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44960-224">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-225">-Tag</span><span class="sxs-lookup"><span data-stu-id="44960-225">-Tag</span></span>
<span data-ttu-id="44960-226">Pares de valor-chave na forma de uma tabela hash definida como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="44960-226">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="44960-227">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="44960-227">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44960-228">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="44960-228">-UpgradeToStorageV2</span></span>
<span data-ttu-id="44960-229">Atualize o Kind da conta de armazenamento do Armazenamento ou blobStorage para o StorageV2.</span><span class="sxs-lookup"><span data-stu-id="44960-229">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="44960-230">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="44960-230">-UseSubDomain</span></span>
<span data-ttu-id="44960-231">Indica se é possível habilitar a validação indireta de CName.</span><span class="sxs-lookup"><span data-stu-id="44960-231">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="44960-232">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="44960-232">-Confirm</span></span>
<span data-ttu-id="44960-233">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44960-233">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-234">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44960-234">-WhatIf</span></span>
<span data-ttu-id="44960-235">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="44960-235">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44960-236">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44960-236">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44960-237">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44960-237">CommonParameters</span></span>
<span data-ttu-id="44960-238">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44960-238">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44960-239">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44960-239">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44960-240">Entradas</span><span class="sxs-lookup"><span data-stu-id="44960-240">INPUTS</span></span>

### <span data-ttu-id="44960-241">System.String</span><span class="sxs-lookup"><span data-stu-id="44960-241">System.String</span></span>

### <span data-ttu-id="44960-242">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="44960-242">System.Collections.Hashtable</span></span>

## <span data-ttu-id="44960-243">Saídas</span><span class="sxs-lookup"><span data-stu-id="44960-243">OUTPUTS</span></span>

### <span data-ttu-id="44960-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44960-244">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="44960-245">Notas</span><span class="sxs-lookup"><span data-stu-id="44960-245">NOTES</span></span>

## <span data-ttu-id="44960-246">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44960-246">RELATED LINKS</span></span>

[<span data-ttu-id="44960-247">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44960-247">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="44960-248">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44960-248">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="44960-249">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44960-249">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
