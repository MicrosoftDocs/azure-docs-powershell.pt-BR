---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: c8ac7139c44adc8bd748eef9a6c762a71c3a777f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774187"
---
# <span data-ttu-id="59fe0-101">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59fe0-101">New-AzStorageAccount</span></span>

## <span data-ttu-id="59fe0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="59fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="59fe0-103">Cria uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="59fe0-103">Creates a Storage account.</span></span>

## <span data-ttu-id="59fe0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="59fe0-104">SYNTAX</span></span>

```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59fe0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="59fe0-105">DESCRIPTION</span></span>
<span data-ttu-id="59fe0-106">O cmdlet **New-AzStorageAccount** cria uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="59fe0-106">The **New-AzStorageAccount** cmdlet creates an Azure Storage account.</span></span>

## <span data-ttu-id="59fe0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="59fe0-107">EXAMPLES</span></span>

### <span data-ttu-id="59fe0-108">Exemplo 1: criar uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="59fe0-108">Example 1: Create a Storage account</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

<span data-ttu-id="59fe0-109">Esse comando cria uma conta de armazenamento para o nome do grupo de recursos MyResource.</span><span class="sxs-lookup"><span data-stu-id="59fe0-109">This command creates a Storage account for the resource group name MyResourceGroup.</span></span>

### <span data-ttu-id="59fe0-110">Exemplo 2: criar uma conta de armazenamento blob com BlobStorage Kind e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="59fe0-110">Example 2: Create a Blob Storage account with BlobStorage Kind and hot AccessTier</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

<span data-ttu-id="59fe0-111">Esse comando cria uma conta de armazenamento BLOB que tem o tipo BlobStorage e Hot AccessTier</span><span class="sxs-lookup"><span data-stu-id="59fe0-111">This command creates a Blob Storage account that with BlobStorage Kind and hot AccessTier</span></span>

### <span data-ttu-id="59fe0-112">Exemplo 3: criar uma conta de armazenamento com o tipo StorageV2 e gerar e atribuir uma identidade para o repositório de senhas do Azure.</span><span class="sxs-lookup"><span data-stu-id="59fe0-112">Example 3: Create a Storage account with Kind StorageV2, and Generate and Assign an Identity for Azure KeyVault.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

<span data-ttu-id="59fe0-113">Esse comando cria uma conta de armazenamento com o tipo StorageV2.</span><span class="sxs-lookup"><span data-stu-id="59fe0-113">This command creates a Storage account with Kind StorageV2.</span></span>  <span data-ttu-id="59fe0-114">Ele também gera e atribui uma identidade que pode ser usada para gerenciar as chaves de conta por meio do Azure keyvault.</span><span class="sxs-lookup"><span data-stu-id="59fe0-114">It also generates and assigns an identity that can be used to manage account keys through Azure KeyVault.</span></span>

### <span data-ttu-id="59fe0-115">Exemplo 4: criar uma conta de armazenamento com o NetworkRuleSet da JSON</span><span class="sxs-lookup"><span data-stu-id="59fe0-115">Example 4: Create a Storage account with NetworkRuleSet from JSON</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

<span data-ttu-id="59fe0-116">Esse comando cria uma conta de armazenamento que tem uma propriedade NetworkRuleSet do JSON</span><span class="sxs-lookup"><span data-stu-id="59fe0-116">This command creates a Storage account that has NetworkRuleSet property from JSON</span></span>

### <span data-ttu-id="59fe0-117">Exemplo 5: criar uma conta de armazenamento com namespace hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="59fe0-117">Example 5: Create a Storage account with Hierarchical Namespace enabled.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

<span data-ttu-id="59fe0-118">Esse comando cria uma conta de armazenamento com namespace hierárquico habilitado.</span><span class="sxs-lookup"><span data-stu-id="59fe0-118">This command creates a Storage account with Hierarchical Namespace enabled.</span></span>

### <span data-ttu-id="59fe0-119">Exemplo 6: criar uma conta de armazenamento com o Azure files Azure autenticação de DS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-119">Example 6: Create a Storage account with Azure Files AAD DS Authentication.</span></span>
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true
```

<span data-ttu-id="59fe0-120">Esse comando cria uma conta de armazenamento com a autenticação do Azure Azure files Azure.</span><span class="sxs-lookup"><span data-stu-id="59fe0-120">This command creates a Storage account with Azure Files AAD DS Authentication.</span></span>

## <span data-ttu-id="59fe0-121">OS</span><span class="sxs-lookup"><span data-stu-id="59fe0-121">PARAMETERS</span></span>

### <span data-ttu-id="59fe0-122">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="59fe0-122">-AccessTier</span></span>
<span data-ttu-id="59fe0-123">Especifica a camada de acesso da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="59fe0-123">Specifies the access tier of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="59fe0-124">Os valores aceitáveis para esse parâmetro são: quente e legal.</span><span class="sxs-lookup"><span data-stu-id="59fe0-124">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="59fe0-125">Se você especificar um valor de BlobStorage para o parâmetro *Kind* , você deve especificar um valor para o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="59fe0-125">If you specify a value of BlobStorage for the *Kind* parameter, you must specify a value for the *AccessTier* parameter.</span></span> <span data-ttu-id="59fe0-126">Se você especificar um valor de armazenamento para esse parâmetro de *tipo* , não especifique o parâmetro *AccessTier* .</span><span class="sxs-lookup"><span data-stu-id="59fe0-126">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

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

### <span data-ttu-id="59fe0-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59fe0-127">-AsJob</span></span>
<span data-ttu-id="59fe0-128">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="59fe0-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59fe0-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="59fe0-129">-AssignIdentity</span></span>
<span data-ttu-id="59fe0-130">Gerar e atribuir uma nova identidade de conta de armazenamento para esta conta de armazenamento para uso com serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="59fe0-130">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="59fe0-131">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="59fe0-131">-CustomDomainName</span></span>
<span data-ttu-id="59fe0-132">Especifica o nome do domínio personalizado da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="59fe0-132">Specifies the name of the custom domain of the Storage account.</span></span>
<span data-ttu-id="59fe0-133">O valor padrão é armazenamento.</span><span class="sxs-lookup"><span data-stu-id="59fe0-133">The default value is Storage.</span></span>

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

### <span data-ttu-id="59fe0-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fe0-134">-DefaultProfile</span></span>
<span data-ttu-id="59fe0-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="59fe0-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59fe0-136">-EnableAzureActiveDirectoryDomainServicesForFile</span><span class="sxs-lookup"><span data-stu-id="59fe0-136">-EnableAzureActiveDirectoryDomainServicesForFile</span></span>
<span data-ttu-id="59fe0-137">Habilite o Azure files autenticação do serviço de domínio Active Directory do Azure para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="59fe0-137">Enable Azure Files Azure Active Directory Domain Service Authentication for the storage account.</span></span>

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

### <span data-ttu-id="59fe0-138">-EnableHierarchicalNamespace</span><span class="sxs-lookup"><span data-stu-id="59fe0-138">-EnableHierarchicalNamespace</span></span>
<span data-ttu-id="59fe0-139">Indica se a conta de armazenamento permite ou não o namespace hierárquico.</span><span class="sxs-lookup"><span data-stu-id="59fe0-139">Indicates whether or not the Storage account enables Hierarchical Namespace.</span></span>

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

### <span data-ttu-id="59fe0-140">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="59fe0-140">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="59fe0-141">Indica se a conta de armazenamento habilita ou não somente o tráfego HTTPS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-141">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="59fe0-142">-Kind</span><span class="sxs-lookup"><span data-stu-id="59fe0-142">-Kind</span></span>
<span data-ttu-id="59fe0-143">Especifica o tipo de conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="59fe0-143">Specifies the kind of Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="59fe0-144">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="59fe0-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fe0-145">SPS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-145">Storage.</span></span> <span data-ttu-id="59fe0-146">Conta de armazenamento de finalidade geral que dá suporte ao armazenamento de BLOBs, tabelas, filas, arquivos e discos.</span><span class="sxs-lookup"><span data-stu-id="59fe0-146">General purpose Storage account that supports storage of Blobs, Tables, Queues, Files and Disks.</span></span>
- <span data-ttu-id="59fe0-147">StorageV2.</span><span class="sxs-lookup"><span data-stu-id="59fe0-147">StorageV2.</span></span> <span data-ttu-id="59fe0-148">Conta de armazenamento do GPv2 (general purpose Version 2) que oferece suporte a BLOBs, tabelas, filas, arquivos e discos, com recursos avançados, como hierarquização de dados.</span><span class="sxs-lookup"><span data-stu-id="59fe0-148">General Purpose Version 2 (GPv2) Storage account that supports Blobs, Tables, Queues, Files, and Disks, with advanced features like data tiering.</span></span>
- <span data-ttu-id="59fe0-149">BlobStorage.</span><span class="sxs-lookup"><span data-stu-id="59fe0-149">BlobStorage.</span></span> <span data-ttu-id="59fe0-150">Conta de armazenamento de BLOB que dá suporte somente ao armazenamento de BLOBs.</span><span class="sxs-lookup"><span data-stu-id="59fe0-150">Blob Storage account which supports storage of Blobs only.</span></span>
- <span data-ttu-id="59fe0-151">BlockBlobStorage.</span><span class="sxs-lookup"><span data-stu-id="59fe0-151">BlockBlobStorage.</span></span> <span data-ttu-id="59fe0-152">Bloquear uma conta de armazenamento BLOB que dê suporte somente ao armazenamento de blobs de blocos.</span><span class="sxs-lookup"><span data-stu-id="59fe0-152">Block Blob Storage account which supports storage of Block Blobs only.</span></span>
- <span data-ttu-id="59fe0-153">Armazenamento de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="59fe0-153">FileStorage.</span></span> <span data-ttu-id="59fe0-154">Conta de armazenamento de arquivos que dá suporte somente ao armazenamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="59fe0-154">File Storage account which supports storage of Files only.</span></span>
<span data-ttu-id="59fe0-155">O valor padrão é StorageV2.</span><span class="sxs-lookup"><span data-stu-id="59fe0-155">The default value is StorageV2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fe0-156">-Local</span><span class="sxs-lookup"><span data-stu-id="59fe0-156">-Location</span></span>
<span data-ttu-id="59fe0-157">Especifica o local da conta de armazenamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="59fe0-157">Specifies the location of the Storage account to create.</span></span>

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

### <span data-ttu-id="59fe0-158">-Nome</span><span class="sxs-lookup"><span data-stu-id="59fe0-158">-Name</span></span>
<span data-ttu-id="59fe0-159">Especifica o nome da conta de armazenamento a ser criada.</span><span class="sxs-lookup"><span data-stu-id="59fe0-159">Specifies the name of the Storage account to create.</span></span>

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

### <span data-ttu-id="59fe0-160">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="59fe0-160">-NetworkRuleSet</span></span>
<span data-ttu-id="59fe0-161">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como os serviços permitidos para ignorar as regras e como lidar com as solicitações que não correspondem a nenhuma das regras definidas.</span><span class="sxs-lookup"><span data-stu-id="59fe0-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

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

### <span data-ttu-id="59fe0-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fe0-162">-ResourceGroupName</span></span>
<span data-ttu-id="59fe0-163">Especifica o nome do grupo de recursos no qual a conta de armazenamento será adicionada.</span><span class="sxs-lookup"><span data-stu-id="59fe0-163">Specifies the name of the resource group in which to add the Storage account.</span></span>

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

### <span data-ttu-id="59fe0-164">-SkuName</span><span class="sxs-lookup"><span data-stu-id="59fe0-164">-SkuName</span></span>
<span data-ttu-id="59fe0-165">Especifica o nome do SKU da conta de armazenamento que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="59fe0-165">Specifies the SKU name of the Storage account that this cmdlet creates.</span></span>
<span data-ttu-id="59fe0-166">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="59fe0-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59fe0-167">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-167">Standard_LRS.</span></span> <span data-ttu-id="59fe0-168">Armazenamento redundante localmente.</span><span class="sxs-lookup"><span data-stu-id="59fe0-168">Locally-redundant storage.</span></span>
- <span data-ttu-id="59fe0-169">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-169">Standard_ZRS.</span></span> <span data-ttu-id="59fe0-170">Armazenamento redundante na zona.</span><span class="sxs-lookup"><span data-stu-id="59fe0-170">Zone-redundant storage.</span></span>
- <span data-ttu-id="59fe0-171">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-171">Standard_GRS.</span></span> <span data-ttu-id="59fe0-172">Armazenamento com redundância geográfica.</span><span class="sxs-lookup"><span data-stu-id="59fe0-172">Geo-redundant storage.</span></span>
- <span data-ttu-id="59fe0-173">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-173">Standard_RAGRS.</span></span> <span data-ttu-id="59fe0-174">Acesso de leitura com armazenamento redundante geográfico.</span><span class="sxs-lookup"><span data-stu-id="59fe0-174">Read access geo-redundant storage.</span></span>
- <span data-ttu-id="59fe0-175">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-175">Premium_LRS.</span></span> <span data-ttu-id="59fe0-176">Premium-armazenamento redundante local.</span><span class="sxs-lookup"><span data-stu-id="59fe0-176">Premium locally-redundant storage.</span></span>
- <span data-ttu-id="59fe0-177">Premium_ZRS.</span><span class="sxs-lookup"><span data-stu-id="59fe0-177">Premium_ZRS.</span></span> <span data-ttu-id="59fe0-178">Zona Premium – armazenamento redundante.</span><span class="sxs-lookup"><span data-stu-id="59fe0-178">Premium zone-redundant storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fe0-179">-Marca</span><span class="sxs-lookup"><span data-stu-id="59fe0-179">-Tag</span></span>
<span data-ttu-id="59fe0-180">Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor.</span><span class="sxs-lookup"><span data-stu-id="59fe0-180">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="59fe0-181">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="59fe0-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="59fe0-182">-UseSubDomain</span><span class="sxs-lookup"><span data-stu-id="59fe0-182">-UseSubDomain</span></span>
<span data-ttu-id="59fe0-183">Indica se a validação de CName indireto deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="59fe0-183">Indicates whether to enable indirect CName validation.</span></span>

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

### <span data-ttu-id="59fe0-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fe0-184">CommonParameters</span></span>
<span data-ttu-id="59fe0-185">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59fe0-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fe0-186">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fe0-186">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fe0-187">SENSORES</span><span class="sxs-lookup"><span data-stu-id="59fe0-187">INPUTS</span></span>

### <span data-ttu-id="59fe0-188">System. String</span><span class="sxs-lookup"><span data-stu-id="59fe0-188">System.String</span></span>

## <span data-ttu-id="59fe0-189">EXIBE</span><span class="sxs-lookup"><span data-stu-id="59fe0-189">OUTPUTS</span></span>

### <span data-ttu-id="59fe0-190">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59fe0-190">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="59fe0-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="59fe0-191">NOTES</span></span>

## <span data-ttu-id="59fe0-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="59fe0-192">RELATED LINKS</span></span>

[<span data-ttu-id="59fe0-193">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59fe0-193">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="59fe0-194">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59fe0-194">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="59fe0-195">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="59fe0-195">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)
