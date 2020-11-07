---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784877"
---
# <span data-ttu-id="b4bf9-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b4bf9-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="b4bf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4bf9-102">SYNOPSIS</span></span>
<span data-ttu-id="b4bf9-103">Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="b4bf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4bf9-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4bf9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4bf9-105">DESCRIPTION</span></span>
<span data-ttu-id="b4bf9-106">O cmdlet **New-AzHDInsightClusterConfig** cria um objeto não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="b4bf9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4bf9-107">EXAMPLES</span></span>

### <span data-ttu-id="b4bf9-108">Exemplo 1: criar um objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="b4bf9-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="b4bf9-109">Esse comando cria um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="b4bf9-110">OS</span><span class="sxs-lookup"><span data-stu-id="b4bf9-110">PARAMETERS</span></span>

### <span data-ttu-id="b4bf9-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="b4bf9-111">-AadTenantId</span></span>
<span data-ttu-id="b4bf9-112">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b4bf9-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b4bf9-113">-ApplicationId</span></span>
<span data-ttu-id="b4bf9-114">Obtém ou define a ID do aplicativo principal do serviço para acessar o Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="b4bf9-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="b4bf9-115">-CertificateFileContents</span></span>
<span data-ttu-id="b4bf9-116">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b4bf9-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="b4bf9-117">-CertificateFilePath</span></span>
<span data-ttu-id="b4bf9-118">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="b4bf9-119">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b4bf9-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b4bf9-120">-CertificatePassword</span></span>
<span data-ttu-id="b4bf9-121">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="b4bf9-122">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b4bf9-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="b4bf9-123">-ClusterTier</span></span>
<span data-ttu-id="b4bf9-124">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="b4bf9-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b4bf9-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4bf9-126">Oficial</span><span class="sxs-lookup"><span data-stu-id="b4bf9-126">Standard</span></span>
- <span data-ttu-id="b4bf9-127">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="b4bf9-128">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="b4bf9-129">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="b4bf9-129">-ClusterType</span></span>
<span data-ttu-id="b4bf9-130">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="b4bf9-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b4bf9-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4bf9-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="b4bf9-132">Hadoop</span></span>
- <span data-ttu-id="b4bf9-133">HBase</span><span class="sxs-lookup"><span data-stu-id="b4bf9-133">HBase</span></span>
- <span data-ttu-id="b4bf9-134">Storm</span><span class="sxs-lookup"><span data-stu-id="b4bf9-134">Storm</span></span>
- <span data-ttu-id="b4bf9-135">Despertar</span><span class="sxs-lookup"><span data-stu-id="b4bf9-135">Spark</span></span>
- <span data-ttu-id="b4bf9-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="b4bf9-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="b4bf9-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="b4bf9-137">Kafka</span></span>
- <span data-ttu-id="b4bf9-138">RServer</span><span class="sxs-lookup"><span data-stu-id="b4bf9-138">RServer</span></span>

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

### <span data-ttu-id="b4bf9-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4bf9-139">-DefaultProfile</span></span>
<span data-ttu-id="b4bf9-140">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b4bf9-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4bf9-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b4bf9-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="b4bf9-142">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="b4bf9-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4bf9-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="b4bf9-144">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="b4bf9-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="b4bf9-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="b4bf9-146">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="b4bf9-147">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="b4bf9-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="b4bf9-148">-EdgeNodeSize</span></span>
<span data-ttu-id="b4bf9-149">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="b4bf9-150">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="b4bf9-151">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="b4bf9-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="b4bf9-152">-HeadNodeSize</span></span>
<span data-ttu-id="b4bf9-153">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="b4bf9-154">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="b4bf9-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="b4bf9-155">-HiveMetastore</span></span>
<span data-ttu-id="b4bf9-156">Especifica a metaloja para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="b4bf9-157">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="b4bf9-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="b4bf9-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="b4bf9-159">Obtém ou define a versão do TLS mínima suportada.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="b4bf9-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b4bf9-160">-ObjectId</span></span>
<span data-ttu-id="b4bf9-161">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="b4bf9-162">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="b4bf9-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="b4bf9-163">-OozieMetastore</span></span>
<span data-ttu-id="b4bf9-164">Especifica o metastore para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="b4bf9-165">Você também pode usar o cmdlet **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="b4bf9-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="b4bf9-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="b4bf9-166">-WorkerNodeSize</span></span>
<span data-ttu-id="b4bf9-167">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="b4bf9-168">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="b4bf9-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="b4bf9-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="b4bf9-170">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="b4bf9-171">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="b4bf9-172">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="b4bf9-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4bf9-173">CommonParameters</span></span>
<span data-ttu-id="b4bf9-174">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4bf9-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4bf9-175">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4bf9-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4bf9-176">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4bf9-176">INPUTS</span></span>

### <span data-ttu-id="b4bf9-177">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b4bf9-177">None</span></span>

## <span data-ttu-id="b4bf9-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4bf9-178">OUTPUTS</span></span>

### <span data-ttu-id="b4bf9-179">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b4bf9-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b4bf9-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4bf9-180">NOTES</span></span>

## <span data-ttu-id="b4bf9-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4bf9-181">RELATED LINKS</span></span>

[<span data-ttu-id="b4bf9-182">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="b4bf9-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


