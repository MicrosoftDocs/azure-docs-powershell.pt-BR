---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955017"
---
# <span data-ttu-id="594d8-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="594d8-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="594d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="594d8-102">SYNOPSIS</span></span>
<span data-ttu-id="594d8-103">Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="594d8-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="594d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="594d8-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="594d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="594d8-105">DESCRIPTION</span></span>
<span data-ttu-id="594d8-106">O cmdlet **New-AzHDInsightClusterConfig** cria um objeto não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="594d8-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="594d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="594d8-107">EXAMPLES</span></span>

### <span data-ttu-id="594d8-108">Exemplo 1: criar um objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="594d8-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="594d8-109">Esse comando cria um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="594d8-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="594d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="594d8-110">PARAMETERS</span></span>

### <span data-ttu-id="594d8-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="594d8-111">-AadTenantId</span></span>
<span data-ttu-id="594d8-112">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="594d8-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="594d8-113">-ApplicationId</span></span>
<span data-ttu-id="594d8-114">Obtém ou define a ID do aplicativo principal do serviço para acessar o Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="594d8-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="594d8-115">-AssignedIdentity</span></span>
<span data-ttu-id="594d8-116">Obtém ou define a identidade atribuída.</span><span class="sxs-lookup"><span data-stu-id="594d8-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="594d8-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="594d8-117">-CertificateFileContents</span></span>
<span data-ttu-id="594d8-118">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="594d8-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="594d8-119">-CertificateFilePath</span></span>
<span data-ttu-id="594d8-120">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="594d8-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="594d8-121">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="594d8-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="594d8-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="594d8-122">-CertificatePassword</span></span>
<span data-ttu-id="594d8-123">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="594d8-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="594d8-124">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="594d8-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="594d8-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="594d8-125">-ClusterTier</span></span>
<span data-ttu-id="594d8-126">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="594d8-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="594d8-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="594d8-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="594d8-128">Oficial</span><span class="sxs-lookup"><span data-stu-id="594d8-128">Standard</span></span>
- <span data-ttu-id="594d8-129">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="594d8-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="594d8-130">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="594d8-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-131">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="594d8-131">-ClusterType</span></span>
<span data-ttu-id="594d8-132">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="594d8-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="594d8-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="594d8-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="594d8-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="594d8-134">Hadoop</span></span>
- <span data-ttu-id="594d8-135">HBase</span><span class="sxs-lookup"><span data-stu-id="594d8-135">HBase</span></span>
- <span data-ttu-id="594d8-136">Storm</span><span class="sxs-lookup"><span data-stu-id="594d8-136">Storm</span></span>
- <span data-ttu-id="594d8-137">Despertar</span><span class="sxs-lookup"><span data-stu-id="594d8-137">Spark</span></span>
- <span data-ttu-id="594d8-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="594d8-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="594d8-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="594d8-139">Kafka</span></span>
- <span data-ttu-id="594d8-140">RServer</span><span class="sxs-lookup"><span data-stu-id="594d8-140">RServer</span></span>

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

### <span data-ttu-id="594d8-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="594d8-141">-DefaultProfile</span></span>
<span data-ttu-id="594d8-142">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="594d8-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="594d8-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="594d8-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="594d8-144">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="594d8-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="594d8-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="594d8-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="594d8-146">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="594d8-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="594d8-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="594d8-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="594d8-148">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="594d8-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="594d8-149">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="594d8-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="594d8-150">-EdgeNodeSize</span></span>
<span data-ttu-id="594d8-151">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="594d8-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="594d8-152">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="594d8-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="594d8-153">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="594d8-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="594d8-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="594d8-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="594d8-155">Obtém ou define o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="594d8-155">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="594d8-156">-EncryptionAtHost</span></span>
<span data-ttu-id="594d8-157">Obtém ou define o sinalizador que indica se a criptografia deve ser habilitada no host ou não.</span><span class="sxs-lookup"><span data-stu-id="594d8-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="594d8-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="594d8-158">-EncryptionInTransit</span></span>
<span data-ttu-id="594d8-159">Obtém ou define o sinalizador que indica se habilitou a criptografia em trânsito ou não.</span><span class="sxs-lookup"><span data-stu-id="594d8-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="594d8-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="594d8-160">-EncryptionKeyName</span></span>
<span data-ttu-id="594d8-161">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="594d8-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="594d8-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="594d8-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="594d8-163">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="594d8-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="594d8-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="594d8-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="594d8-165">Obtém ou define o URI do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="594d8-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="594d8-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="594d8-166">-HeadNodeSize</span></span>
<span data-ttu-id="594d8-167">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="594d8-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="594d8-168">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="594d8-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="594d8-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="594d8-169">-HiveMetastore</span></span>
<span data-ttu-id="594d8-170">Especifica a metaloja para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="594d8-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="594d8-171">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="594d8-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="594d8-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="594d8-173">Obtém ou define a versão do TLS mínima suportada.</span><span class="sxs-lookup"><span data-stu-id="594d8-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="594d8-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="594d8-174">-ObjectId</span></span>
<span data-ttu-id="594d8-175">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="594d8-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="594d8-176">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="594d8-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="594d8-177">-OozieMetastore</span></span>
<span data-ttu-id="594d8-178">Especifica o metastore para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="594d8-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="594d8-179">Você também pode usar o cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="594d8-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="594d8-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="594d8-181">Obtém ou define o tipo de acesso de saída para a rede pública.</span><span class="sxs-lookup"><span data-stu-id="594d8-181">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="594d8-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="594d8-183">Obtém ou define o tipo de acesso à rede pública.</span><span class="sxs-lookup"><span data-stu-id="594d8-183">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="594d8-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="594d8-184">-WorkerNodeSize</span></span>
<span data-ttu-id="594d8-185">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="594d8-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="594d8-186">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="594d8-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="594d8-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="594d8-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="594d8-188">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="594d8-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="594d8-189">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="594d8-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="594d8-190">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="594d8-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="594d8-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="594d8-191">CommonParameters</span></span>
<span data-ttu-id="594d8-192">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="594d8-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="594d8-193">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="594d8-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="594d8-194">SENSORES</span><span class="sxs-lookup"><span data-stu-id="594d8-194">INPUTS</span></span>

### <span data-ttu-id="594d8-195">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="594d8-195">None</span></span>

## <span data-ttu-id="594d8-196">EXIBE</span><span class="sxs-lookup"><span data-stu-id="594d8-196">OUTPUTS</span></span>

### <span data-ttu-id="594d8-197">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="594d8-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="594d8-198">INFORMA</span><span class="sxs-lookup"><span data-stu-id="594d8-198">NOTES</span></span>

## <span data-ttu-id="594d8-199">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="594d8-199">RELATED LINKS</span></span>

[<span data-ttu-id="594d8-200">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="594d8-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


