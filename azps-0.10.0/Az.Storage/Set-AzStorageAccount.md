---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 00665fbe6fc2cc0d78ebbfadded419a8b0157644
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776171"
---
# <span data-ttu-id="7e237-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e237-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="7e237-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e237-102">SYNOPSIS</span></span>
<span data-ttu-id="7e237-103">Modifica uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7e237-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="7e237-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e237-104">SYNTAX</span></span>

### <span data-ttu-id="7e237-105">StorageEncryption (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e237-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e237-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7e237-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e237-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e237-107">DESCRIPTION</span></span>
<span data-ttu-id="7e237-108">O cmdlet **set-AzStorageAccount** modifica uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e237-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="7e237-109">Você pode usar esse cmdlet para modificar o tipo de conta, atualizar um domínio de cliente ou definir marcas em uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7e237-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="7e237-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e237-110">EXAMPLES</span></span>

### <span data-ttu-id="7e237-111">Exemplo 1: definir o tipo de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7e237-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="7e237-112">Esse comando define o tipo de conta de armazenamento como Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="7e237-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="7e237-113">Exemplo 2: definir um domínio personalizado para uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7e237-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="7e237-114">Este comando define um domínio personalizado para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7e237-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="7e237-115">Exemplo 3: definir o valor da camada de acesso</span><span class="sxs-lookup"><span data-stu-id="7e237-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="7e237-116">O comando define o valor da camada de acesso como legal.</span><span class="sxs-lookup"><span data-stu-id="7e237-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="7e237-117">Exemplo 4: definir o domínio e as marcas personalizadas</span><span class="sxs-lookup"><span data-stu-id="7e237-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="7e237-118">O comando define o domínio personalizado e as marcas de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7e237-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="7e237-119">Exemplo 5: definir a fonte de fonte de criptografia para o keyvault</span><span class="sxs-lookup"><span data-stu-id="7e237-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="7e237-120">Esse comando define a fonte de criptografia com um novo cofre criado.</span><span class="sxs-lookup"><span data-stu-id="7e237-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="7e237-121">Exemplo 6: definir a fonte de origem de criptografia como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="7e237-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="7e237-122">Este comando define a fonte de criptografia como "Microsoft. Storage"</span><span class="sxs-lookup"><span data-stu-id="7e237-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="7e237-123">Exemplo 7: definir a propriedade NetworkRuleSet de uma conta de armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="7e237-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="7e237-124">Este comando define a propriedade NetworkRuleSet de uma conta de armazenamento com JSON</span><span class="sxs-lookup"><span data-stu-id="7e237-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="7e237-125">Exemplo 8: obter a propriedade NetworkRuleSet de uma conta de armazenamento e defini-la para outra conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7e237-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="7e237-126">Esse primeiro comando obtém a propriedade NetworkRuleSet de uma conta de armazenamento, e o segundo comando a define para outra conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7e237-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="7e237-127">Exemplo 9: atualizar uma conta de armazenamento com o tipo "armazenamento" ou "BlobStorage" para a conta de armazenamento do tipo "StorageV2"</span><span class="sxs-lookup"><span data-stu-id="7e237-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="7e237-128">O comando atualizar uma conta de armazenamento com o tipo "armazenamento" ou "BlobStorage" para a conta de armazenamento do tipo "StorageV2".</span><span class="sxs-lookup"><span data-stu-id="7e237-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="7e237-129">OS</span><span class="sxs-lookup"><span data-stu-id="7e237-129">PARAMETERS</span></span>

### <span data-ttu-id="7e237-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="7e237-130">-AccessTier</span></span>
<span data-ttu-id="7e237-131">Especifica a camada de acesso da conta de armazenamento que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7e237-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="7e237-132">Os valores aceitáveis para esse parâmetro são: quente e legal.</span><span class="sxs-lookup"><span data-stu-id="7e237-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="7e237-133">Se você alterar a camada de acesso, isso pode resultar em cobranças adicionais.</span><span class="sxs-lookup"><span data-stu-id="7e237-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="7e237-134">Para obter mais informações, consulte [armazenamento de blob do Azure: níveis de armazenamento ótimo e legal](http://go.microsoft.com/fwlink/?LinkId=786482).</span><span class="sxs-lookup"><span data-stu-id="7e237-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="7e237-135">Se a conta de armazenamento tiver o tipo StorageV2 ou BlobStorage, você poderá especificar o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="7e237-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="7e237-136">Se a conta de armazenamento tiver um tipo de armazenamento, não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="7e237-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="7e237-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e237-137">-AsJob</span></span>
<span data-ttu-id="7e237-138">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7e237-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e237-139">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7e237-139">-AssignIdentity</span></span>
<span data-ttu-id="7e237-140">Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e237-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7e237-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7e237-141">-CustomDomainName</span></span>
<span data-ttu-id="7e237-142">Especifica o nome do domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7e237-142">Specifies the name of the custom domain.</span></span>

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

### <span data-ttu-id="7e237-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e237-143">-DefaultProfile</span></span>
<span data-ttu-id="7e237-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e237-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e237-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="7e237-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="7e237-146">Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7e237-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e237-147">-Force</span><span class="sxs-lookup"><span data-stu-id="7e237-147">-Force</span></span>
<span data-ttu-id="7e237-148">Força a alteração a ser gravada na conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7e237-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="7e237-149">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7e237-149">-KeyName</span></span>
<span data-ttu-id="7e237-150">Se estiver usando-KeyvaultEncryption para habilitar a criptografia com o Key Vault, especifique a propriedade KeyName com essa opção.</span><span class="sxs-lookup"><span data-stu-id="7e237-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

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

### <span data-ttu-id="7e237-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7e237-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="7e237-152">Indica se o Microsoft keyvault deve ou não ser usado para as chaves de criptografia ao usar a criptografia do serviço de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7e237-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="7e237-153">Se KeyName, keyversion e KeyVaultUri estiverem todos definidos, o keySource será definido como Microsoft. keyvault se esse parâmetro estiver definido ou não.</span><span class="sxs-lookup"><span data-stu-id="7e237-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

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

### <span data-ttu-id="7e237-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7e237-154">-KeyVaultUri</span></span>
<span data-ttu-id="7e237-155">Ao usar a criptografia do cofre de chaves especificando o parâmetro-KeyvaultEncryption, use essa opção para especificar o URI para o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7e237-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

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

### <span data-ttu-id="7e237-156">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="7e237-156">-KeyVersion</span></span>
<span data-ttu-id="7e237-157">Ao usar a criptografia do cofre de chaves especificando o parâmetro-KeyvaultEncryption, use essa opção para especificar o URI para a versão de chave.</span><span class="sxs-lookup"><span data-stu-id="7e237-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

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

### <span data-ttu-id="7e237-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e237-158">-Name</span></span>
<span data-ttu-id="7e237-159">Especifica o nome da conta de armazenamento a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="7e237-159">Specifies the name of the Storage account to modify.</span></span>

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

### <span data-ttu-id="7e237-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e237-160">-NetworkRuleSet</span></span>
<span data-ttu-id="7e237-161">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como os serviços permitidos para ignorar as regras e como lidar com as solicitações que não correspondem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="7e237-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="7e237-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e237-162">-ResourceGroupName</span></span>
<span data-ttu-id="7e237-163">Especifica o nome do grupo de recursos no qual a conta de armazenamento será modificada.</span><span class="sxs-lookup"><span data-stu-id="7e237-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="7e237-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7e237-164">-SkuName</span></span>
<span data-ttu-id="7e237-165">Especifica o nome do SKU da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7e237-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="7e237-166">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="7e237-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7e237-167">Standard_LRS-armazenamento redundante local.</span><span class="sxs-lookup"><span data-stu-id="7e237-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="7e237-168">Standard_ZRS-armazenamento redundante na zona.</span><span class="sxs-lookup"><span data-stu-id="7e237-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="7e237-169">Standard_GRS-armazenamento com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="7e237-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="7e237-170">Standard_RAGRS-ler o acesso a um armazenamento redundante geográfico.</span><span class="sxs-lookup"><span data-stu-id="7e237-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="7e237-171">Premium_LRS-armazenamento com redundância local Premium.</span><span class="sxs-lookup"><span data-stu-id="7e237-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="7e237-172">Você não pode alterar tipos de Standard_ZRS e Premium_LRS para outros tipos de conta.</span><span class="sxs-lookup"><span data-stu-id="7e237-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="7e237-173">Você não pode alterar outros tipos de conta para Standard_ZRS ou Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="7e237-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e237-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="7e237-174">-StorageEncryption</span></span>
<span data-ttu-id="7e237-175">Indica se a criptografia da conta de armazenamento deve ou não ser definida para usar as chaves gerenciadas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7e237-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

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

### <span data-ttu-id="7e237-176">-Marca</span><span class="sxs-lookup"><span data-stu-id="7e237-176">-Tag</span></span>
<span data-ttu-id="7e237-177">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="7e237-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="7e237-178">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7e237-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7e237-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="7e237-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="7e237-180">Atualize o tipo de conta de armazenamento do armazenamento ou do BlobStorage para o StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7e237-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="7e237-181">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="7e237-181">-UseSubDomain</span></span>
<span data-ttu-id="7e237-182">Indica se a validação de CName indireto deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="7e237-182">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="7e237-183">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e237-183">-Confirm</span></span>
<span data-ttu-id="7e237-184">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e237-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e237-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e237-185">-WhatIf</span></span>
<span data-ttu-id="7e237-186">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e237-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e237-187">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e237-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e237-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e237-188">CommonParameters</span></span>
<span data-ttu-id="7e237-189">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e237-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e237-190">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e237-190">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e237-191">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e237-191">INPUTS</span></span>

### <span data-ttu-id="7e237-192">System. String</span><span class="sxs-lookup"><span data-stu-id="7e237-192">System.String</span></span>

### <span data-ttu-id="7e237-193">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7e237-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7e237-194">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e237-194">System.Boolean</span></span>

## <span data-ttu-id="7e237-195">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e237-195">OUTPUTS</span></span>

### <span data-ttu-id="7e237-196">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e237-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="7e237-197">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e237-197">NOTES</span></span>

## <span data-ttu-id="7e237-198">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e237-198">RELATED LINKS</span></span>

[<span data-ttu-id="7e237-199">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e237-199">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="7e237-200">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e237-200">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="7e237-201">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7e237-201">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)