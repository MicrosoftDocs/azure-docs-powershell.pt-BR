---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: b5ae1de58a7c3862379e73e852d7b367063c3629
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892780"
---
# <span data-ttu-id="20a4c-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="20a4c-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="20a4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20a4c-102">SYNOPSIS</span></span>
<span data-ttu-id="20a4c-103">Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="20a4c-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="20a4c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20a4c-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20a4c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20a4c-105">DESCRIPTION</span></span>
<span data-ttu-id="20a4c-106">O cmdlet **New-AzHDInsightClusterConfig** cria um objeto não persistente que descreve uma configuração de cluster HDInsight do Azure.</span><span class="sxs-lookup"><span data-stu-id="20a4c-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="20a4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20a4c-107">EXAMPLES</span></span>

### <span data-ttu-id="20a4c-108">Exemplo 1: Criar um objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="20a4c-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="20a4c-109">Este comando cria um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="20a4c-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="20a4c-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20a4c-110">PARAMETERS</span></span>

### <span data-ttu-id="20a4c-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="20a4c-111">-AadTenantId</span></span>
<span data-ttu-id="20a4c-112">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20a4c-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20a4c-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="20a4c-113">-ApplicationId</span></span>
<span data-ttu-id="20a4c-114">Obtém ou define a ID do Aplicativo Principal do Serviço para acessar o Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="20a4c-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="20a4c-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="20a4c-115">-AssignedIdentity</span></span>
<span data-ttu-id="20a4c-116">Obtém ou define a identidade atribuída.</span><span class="sxs-lookup"><span data-stu-id="20a4c-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="20a4c-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="20a4c-117">-CertificateFileContents</span></span>
<span data-ttu-id="20a4c-118">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20a4c-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20a4c-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="20a4c-119">-CertificateFilePath</span></span>
<span data-ttu-id="20a4c-120">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="20a4c-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="20a4c-121">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20a4c-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20a4c-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="20a4c-122">-CertificatePassword</span></span>
<span data-ttu-id="20a4c-123">Especifica a senha do certificado que será usado para autenticar como Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="20a4c-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="20a4c-124">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20a4c-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20a4c-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="20a4c-125">-ClusterTier</span></span>
<span data-ttu-id="20a4c-126">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20a4c-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="20a4c-127">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20a4c-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20a4c-128">Standard</span><span class="sxs-lookup"><span data-stu-id="20a4c-128">Standard</span></span>
- <span data-ttu-id="20a4c-129">Premium O valor padrão é Standard.</span><span class="sxs-lookup"><span data-stu-id="20a4c-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="20a4c-130">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="20a4c-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="20a4c-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="20a4c-131">-ClusterType</span></span>
<span data-ttu-id="20a4c-132">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="20a4c-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="20a4c-133">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="20a4c-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="20a4c-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="20a4c-134">Hadoop</span></span>
- <span data-ttu-id="20a4c-135">HBase</span><span class="sxs-lookup"><span data-stu-id="20a4c-135">HBase</span></span>
- <span data-ttu-id="20a4c-136">Tempestade</span><span class="sxs-lookup"><span data-stu-id="20a4c-136">Storm</span></span>
- <span data-ttu-id="20a4c-137">Spark</span><span class="sxs-lookup"><span data-stu-id="20a4c-137">Spark</span></span>
- <span data-ttu-id="20a4c-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="20a4c-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="20a4c-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="20a4c-139">Kafka</span></span>
- <span data-ttu-id="20a4c-140">RServer</span><span class="sxs-lookup"><span data-stu-id="20a4c-140">RServer</span></span>

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

### <span data-ttu-id="20a4c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a4c-141">-DefaultProfile</span></span>
<span data-ttu-id="20a4c-142">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="20a4c-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20a4c-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="20a4c-143">-EdgeNodeSize</span></span>
<span data-ttu-id="20a4c-144">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="20a4c-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="20a4c-145">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20a4c-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="20a4c-146">Esse parâmetro só é válido para clusters RServer.</span><span class="sxs-lookup"><span data-stu-id="20a4c-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="20a4c-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="20a4c-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="20a4c-148">Obtém ou define o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="20a4c-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="20a4c-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="20a4c-149">-EncryptionAtHost</span></span>
<span data-ttu-id="20a4c-150">Obtém ou define o sinalizador que indica se habilitar a criptografia no host ou não.</span><span class="sxs-lookup"><span data-stu-id="20a4c-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="20a4c-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="20a4c-151">-EncryptionInTransit</span></span>
<span data-ttu-id="20a4c-152">Obtém ou define o sinalizador que indica se habilitar a criptografia em trânsito ou não.</span><span class="sxs-lookup"><span data-stu-id="20a4c-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="20a4c-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="20a4c-153">-EncryptionKeyName</span></span>
<span data-ttu-id="20a4c-154">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="20a4c-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="20a4c-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="20a4c-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="20a4c-156">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="20a4c-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="20a4c-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="20a4c-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="20a4c-158">Obtém ou define o uri do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="20a4c-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="20a4c-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="20a4c-159">-HeadNodeSize</span></span>
<span data-ttu-id="20a4c-160">Especifica o tamanho da máquina virtual para o nó Head.</span><span class="sxs-lookup"><span data-stu-id="20a4c-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="20a4c-161">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20a4c-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="20a4c-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="20a4c-162">-HiveMetastore</span></span>
<span data-ttu-id="20a4c-163">Especifica o metastore para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="20a4c-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="20a4c-164">Você pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="20a4c-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="20a4c-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="20a4c-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="20a4c-166">Obtém ou define a versão TLS mínima com suporte.</span><span class="sxs-lookup"><span data-stu-id="20a4c-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="20a4c-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="20a4c-167">-ObjectId</span></span>
<span data-ttu-id="20a4c-168">Especifica a ID do objeto do Azure AD (um GUID) da Entidade de Serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="20a4c-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="20a4c-169">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20a4c-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20a4c-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="20a4c-170">-OozieMetastore</span></span>
<span data-ttu-id="20a4c-171">Especifica o metastore para armazenar metadados Oozie.</span><span class="sxs-lookup"><span data-stu-id="20a4c-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="20a4c-172">Você também pode usar o cmdlet **Add-AzHDInsightMetastore.**</span><span class="sxs-lookup"><span data-stu-id="20a4c-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="20a4c-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="20a4c-173">-StorageAccountKey</span></span>
<span data-ttu-id="20a4c-174">Obtém ou define a chave de acesso à conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20a4c-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="20a4c-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="20a4c-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="20a4c-176">Obtém ou define a ID do recurso de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="20a4c-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="20a4c-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="20a4c-177">-StorageAccountType</span></span>
<span data-ttu-id="20a4c-178">Obtém ou define o tipo da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="20a4c-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20a4c-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="20a4c-179">-WorkerNodeSize</span></span>
<span data-ttu-id="20a4c-180">Especifica o tamanho da máquina virtual para o nó Trabalhador.</span><span class="sxs-lookup"><span data-stu-id="20a4c-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="20a4c-181">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20a4c-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="20a4c-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="20a4c-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="20a4c-183">Especifica o tamanho da máquina virtual para o nó Domadeiro.</span><span class="sxs-lookup"><span data-stu-id="20a4c-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="20a4c-184">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20a4c-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="20a4c-185">Esse parâmetro só é válido para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="20a4c-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="20a4c-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a4c-186">CommonParameters</span></span>
<span data-ttu-id="20a4c-187">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a4c-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a4c-188">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a4c-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a4c-189">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20a4c-189">INPUTS</span></span>

### <span data-ttu-id="20a4c-190">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20a4c-190">None</span></span>

## <span data-ttu-id="20a4c-191">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20a4c-191">OUTPUTS</span></span>

### <span data-ttu-id="20a4c-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="20a4c-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="20a4c-193">NOTES</span><span class="sxs-lookup"><span data-stu-id="20a4c-193">NOTES</span></span>

## <span data-ttu-id="20a4c-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20a4c-194">RELATED LINKS</span></span>

[<span data-ttu-id="20a4c-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="20a4c-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


