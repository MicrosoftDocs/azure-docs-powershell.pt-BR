---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 1f6a6d05bff2c012ca3b32abd16dca01cbe1707b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428927"
---
# <span data-ttu-id="a279c-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a279c-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="a279c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a279c-102">SYNOPSIS</span></span>
<span data-ttu-id="a279c-103">Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a279c-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a279c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a279c-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a279c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a279c-105">DESCRIPTION</span></span>
<span data-ttu-id="a279c-106">O cmdlet **New-AzureRmHDInsightClusterConfig** cria um objeto não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a279c-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="a279c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a279c-107">EXAMPLES</span></span>

### <span data-ttu-id="a279c-108">Exemplo 1: criar um objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="a279c-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzureRmStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzureRmResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzureRmHDInsightClusterConfig `
            | Add-AzureRmHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzureRmHDInsightCluster `
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

<span data-ttu-id="a279c-109">Esse comando cria um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="a279c-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="a279c-110">OS</span><span class="sxs-lookup"><span data-stu-id="a279c-110">PARAMETERS</span></span>

### <span data-ttu-id="a279c-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="a279c-111">-AadTenantId</span></span>
<span data-ttu-id="a279c-112">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a279c-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a279c-113">-CertificateFileContents</span></span>
<span data-ttu-id="a279c-114">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a279c-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a279c-115">-CertificateFilePath</span></span>
<span data-ttu-id="a279c-116">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a279c-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a279c-117">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a279c-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a279c-118">-CertificatePassword</span></span>
<span data-ttu-id="a279c-119">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a279c-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a279c-120">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a279c-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="a279c-121">-ClusterTier</span></span>
<span data-ttu-id="a279c-122">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a279c-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="a279c-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a279c-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a279c-124">Oficial</span><span class="sxs-lookup"><span data-stu-id="a279c-124">Standard</span></span>
- <span data-ttu-id="a279c-125">Gratifica</span><span class="sxs-lookup"><span data-stu-id="a279c-125">Premium</span></span>

<span data-ttu-id="a279c-126">O valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="a279c-126">The default value is Standard.</span></span>
<span data-ttu-id="a279c-127">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="a279c-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-128">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="a279c-128">-ClusterType</span></span>
<span data-ttu-id="a279c-129">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="a279c-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="a279c-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a279c-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a279c-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="a279c-131">Hadoop</span></span>
- <span data-ttu-id="a279c-132">HBase</span><span class="sxs-lookup"><span data-stu-id="a279c-132">HBase</span></span>
- <span data-ttu-id="a279c-133">Storm</span><span class="sxs-lookup"><span data-stu-id="a279c-133">Storm</span></span>
- <span data-ttu-id="a279c-134">Despertar</span><span class="sxs-lookup"><span data-stu-id="a279c-134">Spark</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a279c-135">-DefaultProfile</span></span>
<span data-ttu-id="a279c-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a279c-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-137">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a279c-137">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="a279c-138">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="a279c-138">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-139">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a279c-139">-DefaultStorageAccountName</span></span>
<span data-ttu-id="a279c-140">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="a279c-140">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-141">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a279c-141">-DefaultStorageAccountType</span></span>
<span data-ttu-id="a279c-142">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="a279c-142">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="a279c-143">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="a279c-143">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-144">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="a279c-144">-EdgeNodeSize</span></span>
<span data-ttu-id="a279c-145">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="a279c-145">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="a279c-146">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a279c-146">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="a279c-147">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="a279c-147">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-148">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="a279c-148">-HeadNodeSize</span></span>
<span data-ttu-id="a279c-149">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="a279c-149">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="a279c-150">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a279c-150">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-151">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="a279c-151">-HiveMetastore</span></span>
<span data-ttu-id="a279c-152">Especifica a metaloja para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="a279c-152">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="a279c-153">Você também pode usar o cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="a279c-153">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-154">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a279c-154">-ObjectId</span></span>
<span data-ttu-id="a279c-155">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="a279c-155">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="a279c-156">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a279c-156">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-157">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="a279c-157">-OozieMetastore</span></span>
<span data-ttu-id="a279c-158">Especifica o metastore para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="a279c-158">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="a279c-159">Você também pode usar o cmdlet **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="a279c-159">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-160">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="a279c-160">-WorkerNodeSize</span></span>
<span data-ttu-id="a279c-161">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a279c-161">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="a279c-162">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a279c-162">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-163">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="a279c-163">-ZookeeperNodeSize</span></span>
<span data-ttu-id="a279c-164">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="a279c-164">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="a279c-165">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a279c-165">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="a279c-166">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="a279c-166">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a279c-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a279c-167">CommonParameters</span></span>
<span data-ttu-id="a279c-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a279c-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a279c-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a279c-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a279c-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a279c-170">INPUTS</span></span>

### <span data-ttu-id="a279c-171">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a279c-171">None</span></span>
<span data-ttu-id="a279c-172">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a279c-172">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a279c-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a279c-173">OUTPUTS</span></span>

### <span data-ttu-id="a279c-174">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a279c-174">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a279c-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a279c-175">NOTES</span></span>

## <span data-ttu-id="a279c-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a279c-176">RELATED LINKS</span></span>

[<span data-ttu-id="a279c-177">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a279c-177">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


