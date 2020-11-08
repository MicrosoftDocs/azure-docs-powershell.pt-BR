---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 0b5e34fe3d7fe4c680ac20da53a32e1e5bad36fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111254"
---
# <span data-ttu-id="bdc1e-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdc1e-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="bdc1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc1e-103">Modifica uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="bdc1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdc1e-104">SYNTAX</span></span>

### <span data-ttu-id="bdc1e-105">StorageEncryption (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdc1e-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc1e-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="bdc1e-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> [-KeyVersion <String>]
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdc1e-107">ActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="bdc1e-107">ActiveDirectoryDomainServicesForFile</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-UpgradeToStorageV2] [-EnableLargeFileShare] -EnableActiveDirectoryDomainServicesForFile <Boolean>
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc1e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdc1e-108">DESCRIPTION</span></span>
<span data-ttu-id="bdc1e-109">O cmdlet **set-AzStorageAccount** modifica uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-109">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="bdc1e-110">Você pode usar esse cmdlet para modificar o tipo de conta, atualizar um domínio de cliente ou definir marcas em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-110">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="bdc1e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdc1e-111">EXAMPLES</span></span>

### <span data-ttu-id="bdc1e-112">Exemplo 1: definir o tipo de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="bdc1e-112">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="bdc1e-113">Esse comando define o tipo de conta de armazenamento como Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-113">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="bdc1e-114">Exemplo 2: definir um domínio personalizado para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="bdc1e-114">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="bdc1e-115">Este comando define um domínio personalizado para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-115">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="bdc1e-116">Exemplo 3: definir o valor da camada de acesso</span><span class="sxs-lookup"><span data-stu-id="bdc1e-116">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="bdc1e-117">O comando define o valor da camada de acesso como legal.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-117">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="bdc1e-118">Exemplo 4: definir o domínio e as marcas personalizadas</span><span class="sxs-lookup"><span data-stu-id="bdc1e-118">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="bdc1e-119">O comando define o domínio personalizado e as marcas de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-119">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="bdc1e-120">Exemplo 5: definir a fonte de fonte de criptografia para o keyvault</span><span class="sxs-lookup"><span data-stu-id="bdc1e-120">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="bdc1e-121">Esse comando define a fonte de criptografia com um novo cofre criado.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-121">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="bdc1e-122">Exemplo 6: definir a fonte de origem de criptografia como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="bdc1e-122">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="bdc1e-123">Este comando define a fonte de criptografia como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="bdc1e-123">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="bdc1e-124">Exemplo 7: definir a propriedade NetworkRuleSet de uma conta de armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="bdc1e-124">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="bdc1e-125">Este comando define a propriedade NetworkRuleSet de uma conta de armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="bdc1e-125">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="bdc1e-126">Exemplo 8: obter a propriedade NetworkRuleSet de uma conta de armazenamento e defini-la para outra conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="bdc1e-126">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="bdc1e-127">Esse primeiro comando obtém a propriedade NetworkRuleSet de uma conta de armazenamento, e o segundo comando a define para outra conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="bdc1e-127">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="bdc1e-128">Exemplo 9: atualizar uma conta de armazenamento com o tipo "armazenamento" ou "BlobStorage" para a conta de armazenamento do tipo "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="bdc1e-128">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="bdc1e-129">O comando atualizar uma conta de armazenamento com o tipo "armazenamento" ou "BlobStorage" para a conta de armazenamento do tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="bdc1e-129">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="bdc1e-130">Exemplo 10: atualizar uma conta de armazenamento habilitando o Azure files autenticação do Azure DS.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-130">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true PS

PS C:\> $account.AzureFilesIdentityBasedAuth.DirectoryServiceOptions
AADDS
```

<span data-ttu-id="bdc1e-131">O comando atualiza uma conta de armazenamento habilitando a autenticação do Azure Azure files.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-131">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

### <span data-ttu-id="bdc1e-132">Exemplo 11: atualizar uma conta de armazenamento habilitando arquivos de autenticação do serviço de domínio Active Directory e exibindo a configuração de autenticação baseada em identidade do arquivo</span><span class="sxs-lookup"><span data-stu-id="bdc1e-132">Example 11: Update a Storage account by enable Files Active Directory Domain Service Authentication, and then show the File Identity Based authentication setting</span></span>
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

<span data-ttu-id="bdc1e-133">O comando atualiza uma conta de armazenamento ao habilitar a autenticação do serviço de domínio Active Directory do Azure Files e, em seguida, mostra a configuração de autenticação baseada em identidade de arquivo</span><span class="sxs-lookup"><span data-stu-id="bdc1e-133">The command updates a Storage account by enable Azure Files Active Directory Domain Service Authentication, and then shows the File Identity Based authentication setting</span></span>

### <span data-ttu-id="bdc1e-134">Exemplo 12: definir MinimumTlsVersion e AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="bdc1e-134">Example 12: Set MinimumTlsVersion and AllowBlobPublicAccess</span></span>
```
PS C:\> $account = Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False
```

<span data-ttu-id="bdc1e-135">O comando define MinimumTlsVersion e AllowBlobPublicAccess e, em seguida, mostra as 2 Propriedades da conta</span><span class="sxs-lookup"><span data-stu-id="bdc1e-135">The command sets MinimumTlsVersion  and AllowBlobPublicAccess, and then show the the 2 properties of the account</span></span> 

## <span data-ttu-id="bdc1e-136">OS</span><span class="sxs-lookup"><span data-stu-id="bdc1e-136">PARAMETERS</span></span>

### <span data-ttu-id="bdc1e-137">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="bdc1e-137">-AccessTier</span></span>
<span data-ttu-id="bdc1e-138">Especifica a camada de acesso da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-138">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="bdc1e-139">Os valores aceitáveis para esse parâmetro são: quente e legal.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-139">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="bdc1e-140">Se você alterar a camada de acesso, isso pode resultar em cobranças adicionais.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-140">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="bdc1e-141">Para obter mais informações, consulte [armazenamento de blob do Azure: níveis de armazenamento ótimo e legal](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="bdc1e-141">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="bdc1e-142">Se a conta de armazenamento tiver o tipo StorageV2 ou BlobStorage, você poderá especificar o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="bdc1e-142">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="bdc1e-143">Se a conta de armazenamento tiver um tipo de armazenamento, não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="bdc1e-143">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="bdc1e-144">-ActiveDirectoryAzureStorageSid</span><span class="sxs-lookup"><span data-stu-id="bdc1e-144">-ActiveDirectoryAzureStorageSid</span></span>
<span data-ttu-id="bdc1e-145">Especifica o identificador de segurança (SID) do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-145">Specifies the security identifier (SID) for Azure Storage.</span></span> <span data-ttu-id="bdc1e-146">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-146">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bdc1e-147">-ActiveDirectoryDomainGuid</span><span class="sxs-lookup"><span data-stu-id="bdc1e-147">-ActiveDirectoryDomainGuid</span></span>
<span data-ttu-id="bdc1e-148">Especifica o GUID do domínio.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-148">Specifies the domain GUID.</span></span> <span data-ttu-id="bdc1e-149">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-149">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bdc1e-150">-ActiveDirectoryDomainName</span><span class="sxs-lookup"><span data-stu-id="bdc1e-150">-ActiveDirectoryDomainName</span></span>
<span data-ttu-id="bdc1e-151">Especifica o domínio primário para o qual o servidor DNS do AD é autorizado.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-151">Specifies the primary domain that the AD DNS server is authoritative for.</span></span> <span data-ttu-id="bdc1e-152">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-152">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bdc1e-153">-ActiveDirectoryDomainSid</span><span class="sxs-lookup"><span data-stu-id="bdc1e-153">-ActiveDirectoryDomainSid</span></span>
<span data-ttu-id="bdc1e-154">Especifica o identificador de segurança (SID).</span><span class="sxs-lookup"><span data-stu-id="bdc1e-154">Specifies the security identifier (SID).</span></span> <span data-ttu-id="bdc1e-155">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-155">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bdc1e-156">-ActiveDirectoryForestName</span><span class="sxs-lookup"><span data-stu-id="bdc1e-156">-ActiveDirectoryForestName</span></span>
<span data-ttu-id="bdc1e-157">Especifica a floresta do Active Directory a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-157">Specifies the Active Directory forest to get.</span></span> <span data-ttu-id="bdc1e-158">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-158">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bdc1e-159">-ActiveDirectoryNetBiosDomainName</span><span class="sxs-lookup"><span data-stu-id="bdc1e-159">-ActiveDirectoryNetBiosDomainName</span></span>
<span data-ttu-id="bdc1e-160">Especifica o nome de domínio NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-160">Specifies the NetBIOS domain name.</span></span> <span data-ttu-id="bdc1e-161">Esse parâmetro deve ser definido quando-EnableActiveDirectoryDomainServicesForFile é definido como true.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-161">This parameter must be set when -EnableActiveDirectoryDomainServicesForFile is set to true.</span></span>

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

### <span data-ttu-id="bdc1e-162">-AllowBlobPublicAccess</span><span class="sxs-lookup"><span data-stu-id="bdc1e-162">-AllowBlobPublicAccess</span></span>
<span data-ttu-id="bdc1e-163">Permitir ou impedir o acesso público a todos os BLOBs ou recipientes na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-163">Allow or disallow public access to all blobs or containers in the storage account.</span></span>

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

### <span data-ttu-id="bdc1e-164">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdc1e-164">-AsJob</span></span>
<span data-ttu-id="bdc1e-165">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bdc1e-165">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdc1e-166">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="bdc1e-166">-AssignIdentity</span></span>
<span data-ttu-id="bdc1e-167">Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-167">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="bdc1e-168">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bdc1e-168">-CustomDomainName</span></span>
<span data-ttu-id="bdc1e-169">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-169">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="bdc1e-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc1e-170">-DefaultProfile</span></span>
<span data-ttu-id="bdc1e-171">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-171">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdc1e-172">-EnableActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="bdc1e-172">-EnableActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="bdc1e-173">Habilite o Azure files autenticação do serviço de domínio Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-173">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="bdc1e-174">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="bdc1e-174">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="bdc1e-175">Habilite o Azure files autenticação do serviço de domínio Active Directory para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-175">Enable Azure Files Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="bdc1e-176">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="bdc1e-176">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="bdc1e-177">Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-177">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="bdc1e-178">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="bdc1e-178">-EnableLargeFileShare</span></span>
<span data-ttu-id="bdc1e-179">Indica se a conta de armazenamento pode ou não dar suporte a grandes compartilhamentos de arquivos com mais de 5 TiB de capacidade.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-179">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="bdc1e-180">Uma vez que a conta esteja habilitada, o recurso não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-180">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="bdc1e-181">Atualmente só tem suporte para tipos de replicação LRS e ZRS, portanto, não é possível fazer conversões de conta para contas com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-181">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="bdc1e-182">Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="bdc1e-182">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="bdc1e-183">-Force</span><span class="sxs-lookup"><span data-stu-id="bdc1e-183">-Force</span></span>
<span data-ttu-id="bdc1e-184">Força a alteração a ser gravada na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-184">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="bdc1e-185">-KeyName</span><span class="sxs-lookup"><span data-stu-id="bdc1e-185">-KeyName</span></span>
<span data-ttu-id="bdc1e-186">Se estiver usando-KeyvaultEncryption para habilitar a criptografia com o Key Vault, especifique a propriedade KeyName com essa opção.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-186">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="bdc1e-187">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="bdc1e-187">-KeyvaultEncryption</span></span>
<span data-ttu-id="bdc1e-188">Indica se o Microsoft keyvault deve ou não ser usado para as chaves de criptografia ao usar a criptografia do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-188">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="bdc1e-189">Se KeyName, keyversion e KeyVaultUri estiverem todos definidos, o keySource será definido como Microsoft. keyvault se esse parâmetro estiver definido ou não.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-189">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="bdc1e-190">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="bdc1e-190">-KeyVaultUri</span></span>
<span data-ttu-id="bdc1e-191">Ao usar a criptografia do cofre de chaves especificando o parâmetro-KeyvaultEncryption, use essa opção para especificar o URI para o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-191">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="bdc1e-192">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="bdc1e-192">-KeyVersion</span></span>
<span data-ttu-id="bdc1e-193">Ao usar a criptografia do cofre de chaves especificando o parâmetro-KeyvaultEncryption, use essa opção para especificar o URI para a versão de chave.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-193">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="bdc1e-194">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="bdc1e-194">-MinimumTlsVersion</span></span>
<span data-ttu-id="bdc1e-195">A versão mínima de TLS a ser permitida nas solicitações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-195">The minimum TLS version to be permitted on requests to storage.</span></span>

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

### <span data-ttu-id="bdc1e-196">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdc1e-196">-Name</span></span>
<span data-ttu-id="bdc1e-197">Especifica o nome da conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-197">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="bdc1e-198">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="bdc1e-198">-NetworkRuleSet</span></span>
<span data-ttu-id="bdc1e-199">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como os serviços permitidos para ignorar as regras e como lidar com as solicitações que não correspondem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-199">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="bdc1e-200">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdc1e-200">-ResourceGroupName</span></span>
<span data-ttu-id="bdc1e-201">Especifica o nome do grupo de recursos no qual a conta de armazenamento será modificada.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-201">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="bdc1e-202">-SkuName</span><span class="sxs-lookup"><span data-stu-id="bdc1e-202">-SkuName</span></span>
<span data-ttu-id="bdc1e-203">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-203">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="bdc1e-204">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bdc1e-204">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bdc1e-205">Standard_LRS-armazenamento redundante local.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-205">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="bdc1e-206">Standard_ZRS-armazenamento redundante na zona.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-206">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="bdc1e-207">Standard_GRS-armazenamento com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-207">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="bdc1e-208">Standard_RAGRS-ler o acesso a um armazenamento redundante geográfico.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-208">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="bdc1e-209">Premium_LRS-armazenamento com redundância local Premium.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-209">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="bdc1e-210">Standard_GZRS-armazenamento redundante de zona com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-210">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="bdc1e-211">Standard_RAGZRS-ler o acesso à zona de redundância geográfica-armazenamento redundante.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-211">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="bdc1e-212">Você não pode alterar tipos de Standard_ZRS e Premium_LRS para outros tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-212">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="bdc1e-213">Você não pode alterar outros tipos de conta para Standard_ZRS ou Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-213">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="bdc1e-214">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="bdc1e-214">-StorageEncryption</span></span>
<span data-ttu-id="bdc1e-215">Indica se a criptografia da conta de armazenamento deve ou não ser definida para usar as chaves gerenciadas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-215">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="bdc1e-216">-Marca</span><span class="sxs-lookup"><span data-stu-id="bdc1e-216">-Tag</span></span>
<span data-ttu-id="bdc1e-217">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-217">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="bdc1e-218">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="bdc1e-218">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="bdc1e-219">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="bdc1e-219">-UpgradeToStorageV2</span></span>
<span data-ttu-id="bdc1e-220">Atualize o tipo de conta de armazenamento do armazenamento ou do BlobStorage para o StorageV2.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-220">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="bdc1e-221">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="bdc1e-221">-UseSubDomain</span></span>
<span data-ttu-id="bdc1e-222">Indica se a validação de CName indireto deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-222">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="bdc1e-223">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bdc1e-223">-Confirm</span></span>
<span data-ttu-id="bdc1e-224">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-224">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc1e-225">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc1e-225">-WhatIf</span></span>
<span data-ttu-id="bdc1e-226">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-226">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdc1e-227">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-227">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc1e-228">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc1e-228">CommonParameters</span></span>
<span data-ttu-id="bdc1e-229">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdc1e-229">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc1e-230">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc1e-230">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc1e-231">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdc1e-231">INPUTS</span></span>

### <span data-ttu-id="bdc1e-232">System. String</span><span class="sxs-lookup"><span data-stu-id="bdc1e-232">System.String</span></span>

### <span data-ttu-id="bdc1e-233">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bdc1e-233">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bdc1e-234">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdc1e-234">OUTPUTS</span></span>

### <span data-ttu-id="bdc1e-235">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdc1e-235">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bdc1e-236">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdc1e-236">NOTES</span></span>

## <span data-ttu-id="bdc1e-237">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdc1e-237">RELATED LINKS</span></span>

[<span data-ttu-id="bdc1e-238">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdc1e-238">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="bdc1e-239">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdc1e-239">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="bdc1e-240">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdc1e-240">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
