---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: ca6bc95d0da6e9793b2bb26ab12362bb74d9212a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941223"
---
# <span data-ttu-id="4ebbb-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ebbb-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="4ebbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ebbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebbb-103">Modifica uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="4ebbb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ebbb-104">SYNTAX</span></span>

### <span data-ttu-id="4ebbb-105">StorageEncryption (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ebbb-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ebbb-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="4ebbb-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2]
 [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-EnableLargeFileShare] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ebbb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ebbb-107">DESCRIPTION</span></span>
<span data-ttu-id="4ebbb-108">O cmdlet **set-AzStorageAccount** modifica uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="4ebbb-109">Você pode usar esse cmdlet para modificar o tipo de conta, atualizar um domínio de cliente ou definir marcas em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="4ebbb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ebbb-110">EXAMPLES</span></span>

### <span data-ttu-id="4ebbb-111">Exemplo 1: definir o tipo de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4ebbb-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="4ebbb-112">Esse comando define o tipo de conta de armazenamento como Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="4ebbb-113">Exemplo 2: definir um domínio personalizado para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4ebbb-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="4ebbb-114">Este comando define um domínio personalizado para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="4ebbb-115">Exemplo 3: definir o valor da camada de acesso</span><span class="sxs-lookup"><span data-stu-id="4ebbb-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="4ebbb-116">O comando define o valor da camada de acesso como legal.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="4ebbb-117">Exemplo 4: definir o domínio e as marcas personalizadas</span><span class="sxs-lookup"><span data-stu-id="4ebbb-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="4ebbb-118">O comando define o domínio personalizado e as marcas de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="4ebbb-119">Exemplo 5: definir a fonte de fonte de criptografia para o keyvault</span><span class="sxs-lookup"><span data-stu-id="4ebbb-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="4ebbb-120">Esse comando define a fonte de criptografia com um novo cofre criado.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="4ebbb-121">Exemplo 6: definir a fonte de origem de criptografia como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="4ebbb-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="4ebbb-122">Este comando define a fonte de criptografia como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="4ebbb-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="4ebbb-123">Exemplo 7: definir a propriedade NetworkRuleSet de uma conta de armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="4ebbb-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="4ebbb-124">Este comando define a propriedade NetworkRuleSet de uma conta de armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="4ebbb-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="4ebbb-125">Exemplo 8: obter a propriedade NetworkRuleSet de uma conta de armazenamento e defini-la para outra conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4ebbb-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="4ebbb-126">Esse primeiro comando obtém a propriedade NetworkRuleSet de uma conta de armazenamento, e o segundo comando a define para outra conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="4ebbb-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="4ebbb-127">Exemplo 9: atualizar uma conta de armazenamento com o tipo "armazenamento" ou "BlobStorage" para a conta de armazenamento do tipo "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="4ebbb-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="4ebbb-128">O comando atualizar uma conta de armazenamento com o tipo "armazenamento" ou "BlobStorage" para a conta de armazenamento do tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="4ebbb-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

### <span data-ttu-id="4ebbb-129">Exemplo 10: atualizar uma conta de armazenamento habilitando o Azure files autenticação do Azure DS.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-129">Example 10: Update a Storage account by enable Azure Files AAD DS Authentication.</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="4ebbb-130">O comando atualiza uma conta de armazenamento habilitando a autenticação do Azure Azure files.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-130">The command update a Storage account by enable Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="4ebbb-131">OS</span><span class="sxs-lookup"><span data-stu-id="4ebbb-131">PARAMETERS</span></span>

### <span data-ttu-id="4ebbb-132">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="4ebbb-132">-AccessTier</span></span>
<span data-ttu-id="4ebbb-133">Especifica a camada de acesso da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-133">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="4ebbb-134">Os valores aceitáveis para esse parâmetro são: quente e legal.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-134">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="4ebbb-135">Se você alterar a camada de acesso, isso pode resultar em cobranças adicionais.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-135">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="4ebbb-136">Para obter mais informações, consulte [armazenamento de blob do Azure: níveis de armazenamento ótimo e legal](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="4ebbb-136">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="4ebbb-137">Se a conta de armazenamento tiver o tipo StorageV2 ou BlobStorage, você poderá especificar o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="4ebbb-137">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="4ebbb-138">Se a conta de armazenamento tiver um tipo de armazenamento, não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="4ebbb-138">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="4ebbb-139">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ebbb-139">-AsJob</span></span>
<span data-ttu-id="4ebbb-140">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4ebbb-140">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ebbb-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="4ebbb-141">-AssignIdentity</span></span>
<span data-ttu-id="4ebbb-142">Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-142">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4ebbb-143">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="4ebbb-143">-CustomDomainName</span></span>
<span data-ttu-id="4ebbb-144">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-144">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="4ebbb-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebbb-145">-DefaultProfile</span></span>
<span data-ttu-id="4ebbb-146">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ebbb-147">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="4ebbb-147">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="4ebbb-148">Habilite o Azure files autenticação do serviço de domínio Active Directory do Azure para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-148">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="4ebbb-149">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="4ebbb-149">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="4ebbb-150">Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-150">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="4ebbb-151">-EnableLargeFileShare</span><span class="sxs-lookup"><span data-stu-id="4ebbb-151">-EnableLargeFileShare</span></span>
<span data-ttu-id="4ebbb-152">Indica se a conta de armazenamento pode ou não dar suporte a grandes compartilhamentos de arquivos com mais de 5 TiB de capacidade.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-152">Indicates whether or not the storage account can support large file shares with more than 5 TiB capacity.</span></span> <span data-ttu-id="4ebbb-153">Uma vez que a conta esteja habilitada, o recurso não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-153">Once the account is enabled, the feature cannot be disabled.</span></span> <span data-ttu-id="4ebbb-154">Atualmente só tem suporte para tipos de replicação LRS e ZRS, portanto, não é possível fazer conversões de conta para contas com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-154">Currently only supported for LRS and ZRS replication types, hence account conversions to geo-redundant accounts would not be possible.</span></span> <span data-ttu-id="4ebbb-155">Saiba mais em https://go.microsoft.com/fwlink/?linkid=2086047</span><span class="sxs-lookup"><span data-stu-id="4ebbb-155">Learn more in https://go.microsoft.com/fwlink/?linkid=2086047</span></span>

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

### <span data-ttu-id="4ebbb-156">-Force</span><span class="sxs-lookup"><span data-stu-id="4ebbb-156">-Force</span></span>
<span data-ttu-id="4ebbb-157">Força a alteração a ser gravada na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-157">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="4ebbb-158">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4ebbb-158">-KeyName</span></span>
<span data-ttu-id="4ebbb-159">Se estiver usando-KeyvaultEncryption para habilitar a criptografia com o Key Vault, especifique a propriedade KeyName com essa opção.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-159">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="4ebbb-160">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="4ebbb-160">-KeyvaultEncryption</span></span>
<span data-ttu-id="4ebbb-161">Indica se o Microsoft keyvault deve ou não ser usado para as chaves de criptografia ao usar a criptografia do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-161">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="4ebbb-162">Se KeyName, keyversion e KeyVaultUri estiverem todos definidos, o keySource será definido como Microsoft. keyvault se esse parâmetro estiver definido ou não.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-162">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="4ebbb-163">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="4ebbb-163">-KeyVaultUri</span></span>
<span data-ttu-id="4ebbb-164">Ao usar a criptografia do cofre de chaves especificando o parâmetro-KeyvaultEncryption, use essa opção para especificar o URI para o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-164">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="4ebbb-165">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="4ebbb-165">-KeyVersion</span></span>
<span data-ttu-id="4ebbb-166">Ao usar a criptografia do cofre de chaves especificando o parâmetro-KeyvaultEncryption, use essa opção para especificar o URI para a versão de chave.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-166">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="4ebbb-167">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ebbb-167">-Name</span></span>
<span data-ttu-id="4ebbb-168">Especifica o nome da conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-168">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="4ebbb-169">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="4ebbb-169">-NetworkRuleSet</span></span>
<span data-ttu-id="4ebbb-170">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como os serviços permitidos para ignorar as regras e como lidar com as solicitações que não correspondem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-170">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="4ebbb-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebbb-171">-ResourceGroupName</span></span>
<span data-ttu-id="4ebbb-172">Especifica o nome do grupo de recursos no qual a conta de armazenamento será modificada.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-172">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="4ebbb-173">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4ebbb-173">-SkuName</span></span>
<span data-ttu-id="4ebbb-174">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-174">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="4ebbb-175">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4ebbb-175">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4ebbb-176">Standard_LRS-armazenamento redundante local.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-176">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="4ebbb-177">Standard_ZRS-armazenamento redundante na zona.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-177">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="4ebbb-178">Standard_GRS-armazenamento com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-178">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="4ebbb-179">Standard_RAGRS-ler o acesso a um armazenamento redundante geográfico.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-179">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="4ebbb-180">Premium_LRS-armazenamento com redundância local Premium.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-180">Premium_LRS - Premium locally-redundant storage.</span></span>
- <span data-ttu-id="4ebbb-181">Standard_GZRS-armazenamento redundante de zona com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-181">Standard_GZRS - Geo-redundant zone-redundant storage.</span></span>
- <span data-ttu-id="4ebbb-182">Standard_RAGZRS-ler o acesso à zona de redundância geográfica-armazenamento redundante.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-182">Standard_RAGZRS - Read access geo-redundant zone-redundant storage.</span></span>
<span data-ttu-id="4ebbb-183">Você não pode alterar tipos de Standard_ZRS e Premium_LRS para outros tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-183">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="4ebbb-184">Você não pode alterar outros tipos de conta para Standard_ZRS ou Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-184">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

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

### <span data-ttu-id="4ebbb-185">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="4ebbb-185">-StorageEncryption</span></span>
<span data-ttu-id="4ebbb-186">Indica se a criptografia da conta de armazenamento deve ou não ser definida para usar as chaves gerenciadas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-186">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="4ebbb-187">-Marca</span><span class="sxs-lookup"><span data-stu-id="4ebbb-187">-Tag</span></span>
<span data-ttu-id="4ebbb-188">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-188">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="4ebbb-189">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4ebbb-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ebbb-190">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="4ebbb-190">-UpgradeToStorageV2</span></span>
<span data-ttu-id="4ebbb-191">Atualize o tipo de conta de armazenamento do armazenamento ou do BlobStorage para o StorageV2.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-191">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="4ebbb-192">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="4ebbb-192">-UseSubDomain</span></span>
<span data-ttu-id="4ebbb-193">Indica se a validação de CName indireto deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-193">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="4ebbb-194">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4ebbb-194">-Confirm</span></span>
<span data-ttu-id="4ebbb-195">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ebbb-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ebbb-196">-WhatIf</span></span>
<span data-ttu-id="4ebbb-197">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-197">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ebbb-198">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ebbb-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebbb-199">CommonParameters</span></span>
<span data-ttu-id="4ebbb-200">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebbb-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebbb-201">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ebbb-201">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebbb-202">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ebbb-202">INPUTS</span></span>

### <span data-ttu-id="4ebbb-203">System. String</span><span class="sxs-lookup"><span data-stu-id="4ebbb-203">System.String</span></span>

### <span data-ttu-id="4ebbb-204">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ebbb-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ebbb-205">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ebbb-205">OUTPUTS</span></span>

### <span data-ttu-id="4ebbb-206">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ebbb-206">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4ebbb-207">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ebbb-207">NOTES</span></span>

## <span data-ttu-id="4ebbb-208">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ebbb-208">RELATED LINKS</span></span>

[<span data-ttu-id="4ebbb-209">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ebbb-209">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="4ebbb-210">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ebbb-210">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="4ebbb-211">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4ebbb-211">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
