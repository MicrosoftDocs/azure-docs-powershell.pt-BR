---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256700"
---
# <span data-ttu-id="30b87-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="30b87-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="30b87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30b87-102">SYNOPSIS</span></span>
<span data-ttu-id="30b87-103">Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b87-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="30b87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30b87-104">SYNTAX</span></span>

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

## <span data-ttu-id="30b87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30b87-105">DESCRIPTION</span></span>
<span data-ttu-id="30b87-106">O cmdlet **New-AzHDInsightClusterConfig** cria um objeto não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b87-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="30b87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30b87-107">EXAMPLES</span></span>

### <span data-ttu-id="30b87-108">Exemplo 1: criar um objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="30b87-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="30b87-109">Esse comando cria um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="30b87-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="30b87-110">OS</span><span class="sxs-lookup"><span data-stu-id="30b87-110">PARAMETERS</span></span>

### <span data-ttu-id="30b87-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="30b87-111">-AadTenantId</span></span>
<span data-ttu-id="30b87-112">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30b87-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="30b87-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="30b87-113">-ApplicationId</span></span>
<span data-ttu-id="30b87-114">Obtém ou define a ID do aplicativo principal do serviço para acessar o Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="30b87-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="30b87-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="30b87-115">-AssignedIdentity</span></span>
<span data-ttu-id="30b87-116">Obtém ou define a identidade atribuída.</span><span class="sxs-lookup"><span data-stu-id="30b87-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="30b87-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="30b87-117">-CertificateFileContents</span></span>
<span data-ttu-id="30b87-118">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30b87-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="30b87-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="30b87-119">-CertificateFilePath</span></span>
<span data-ttu-id="30b87-120">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="30b87-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="30b87-121">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30b87-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="30b87-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="30b87-122">-CertificatePassword</span></span>
<span data-ttu-id="30b87-123">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="30b87-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="30b87-124">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30b87-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="30b87-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="30b87-125">-ClusterTier</span></span>
<span data-ttu-id="30b87-126">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b87-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="30b87-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="30b87-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30b87-128">Oficial</span><span class="sxs-lookup"><span data-stu-id="30b87-128">Standard</span></span>
- <span data-ttu-id="30b87-129">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="30b87-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="30b87-130">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="30b87-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="30b87-131">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="30b87-131">-ClusterType</span></span>
<span data-ttu-id="30b87-132">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="30b87-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="30b87-133">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="30b87-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="30b87-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="30b87-134">Hadoop</span></span>
- <span data-ttu-id="30b87-135">HBase</span><span class="sxs-lookup"><span data-stu-id="30b87-135">HBase</span></span>
- <span data-ttu-id="30b87-136">Storm</span><span class="sxs-lookup"><span data-stu-id="30b87-136">Storm</span></span>
- <span data-ttu-id="30b87-137">Despertar</span><span class="sxs-lookup"><span data-stu-id="30b87-137">Spark</span></span>
- <span data-ttu-id="30b87-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="30b87-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="30b87-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="30b87-139">Kafka</span></span>
- <span data-ttu-id="30b87-140">RServer</span><span class="sxs-lookup"><span data-stu-id="30b87-140">RServer</span></span>

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

### <span data-ttu-id="30b87-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30b87-141">-DefaultProfile</span></span>
<span data-ttu-id="30b87-142">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="30b87-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30b87-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="30b87-143">-EdgeNodeSize</span></span>
<span data-ttu-id="30b87-144">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="30b87-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="30b87-145">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b87-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="30b87-146">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="30b87-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="30b87-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="30b87-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="30b87-148">Obtém ou define o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="30b87-148">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="30b87-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="30b87-149">-EncryptionAtHost</span></span>
<span data-ttu-id="30b87-150">Obtém ou define o sinalizador que indica se a criptografia deve ser habilitada no host ou não.</span><span class="sxs-lookup"><span data-stu-id="30b87-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="30b87-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="30b87-151">-EncryptionInTransit</span></span>
<span data-ttu-id="30b87-152">Obtém ou define o sinalizador que indica se habilitou a criptografia em trânsito ou não.</span><span class="sxs-lookup"><span data-stu-id="30b87-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="30b87-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="30b87-153">-EncryptionKeyName</span></span>
<span data-ttu-id="30b87-154">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="30b87-154">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="30b87-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="30b87-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="30b87-156">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="30b87-156">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="30b87-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="30b87-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="30b87-158">Obtém ou define o URI do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="30b87-158">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="30b87-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="30b87-159">-HeadNodeSize</span></span>
<span data-ttu-id="30b87-160">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="30b87-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="30b87-161">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b87-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="30b87-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="30b87-162">-HiveMetastore</span></span>
<span data-ttu-id="30b87-163">Especifica a metaloja para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="30b87-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="30b87-164">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="30b87-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="30b87-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="30b87-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="30b87-166">Obtém ou define a versão do TLS mínima suportada.</span><span class="sxs-lookup"><span data-stu-id="30b87-166">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="30b87-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="30b87-167">-ObjectId</span></span>
<span data-ttu-id="30b87-168">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="30b87-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="30b87-169">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30b87-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="30b87-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="30b87-170">-OozieMetastore</span></span>
<span data-ttu-id="30b87-171">Especifica o metastore para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="30b87-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="30b87-172">Você também pode usar o cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="30b87-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="30b87-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="30b87-173">-StorageAccountKey</span></span>
<span data-ttu-id="30b87-174">Obtém ou define a chave de acesso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30b87-174">Gets or sets the storage account access key.</span></span>

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

### <span data-ttu-id="30b87-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="30b87-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="30b87-176">Obtém ou define a ID do recurso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30b87-176">Gets or sets the storage account resource id.</span></span>

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

### <span data-ttu-id="30b87-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="30b87-177">-StorageAccountType</span></span>
<span data-ttu-id="30b87-178">Obtém ou define o tipo da conta de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="30b87-178">Gets or sets the type of the default storage account.</span></span>

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

### <span data-ttu-id="30b87-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="30b87-179">-WorkerNodeSize</span></span>
<span data-ttu-id="30b87-180">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="30b87-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="30b87-181">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b87-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="30b87-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="30b87-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="30b87-183">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="30b87-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="30b87-184">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="30b87-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="30b87-185">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="30b87-185">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="30b87-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30b87-186">CommonParameters</span></span>
<span data-ttu-id="30b87-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30b87-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30b87-188">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30b87-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30b87-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30b87-189">INPUTS</span></span>

### <span data-ttu-id="30b87-190">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="30b87-190">None</span></span>

## <span data-ttu-id="30b87-191">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30b87-191">OUTPUTS</span></span>

### <span data-ttu-id="30b87-192">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="30b87-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="30b87-193">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30b87-193">NOTES</span></span>

## <span data-ttu-id="30b87-194">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30b87-194">RELATED LINKS</span></span>

[<span data-ttu-id="30b87-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="30b87-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


