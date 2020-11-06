---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: e4588f3799052cf9f397f846b635be4f525df930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430257"
---
# <span data-ttu-id="db229-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="db229-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="db229-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db229-102">SYNOPSIS</span></span>
<span data-ttu-id="db229-103">Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db229-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db229-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db229-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db229-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db229-105">DESCRIPTION</span></span>
<span data-ttu-id="db229-106">O cmdlet **New-AzureRmHDInsightClusterConfig** cria um objeto não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db229-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="db229-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db229-107">EXAMPLES</span></span>

### <span data-ttu-id="db229-108">Exemplo 1: criar um objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="db229-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="db229-109">Esse comando cria um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="db229-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="db229-110">OS</span><span class="sxs-lookup"><span data-stu-id="db229-110">PARAMETERS</span></span>

### <span data-ttu-id="db229-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="db229-111">-AadTenantId</span></span>
<span data-ttu-id="db229-112">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="db229-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="db229-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="db229-113">-CertificateFileContents</span></span>
<span data-ttu-id="db229-114">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="db229-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="db229-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="db229-115">-CertificateFilePath</span></span>
<span data-ttu-id="db229-116">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db229-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="db229-117">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="db229-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="db229-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="db229-118">-CertificatePassword</span></span>
<span data-ttu-id="db229-119">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db229-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="db229-120">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="db229-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="db229-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="db229-121">-ClusterTier</span></span>
<span data-ttu-id="db229-122">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db229-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="db229-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="db229-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db229-124">Oficial</span><span class="sxs-lookup"><span data-stu-id="db229-124">Standard</span></span>
- <span data-ttu-id="db229-125">Premium o valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="db229-125">Premium The default value is Standard.</span></span>
<span data-ttu-id="db229-126">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="db229-126">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="db229-127">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="db229-127">-ClusterType</span></span>
<span data-ttu-id="db229-128">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="db229-128">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="db229-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="db229-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db229-130">Hadoop</span><span class="sxs-lookup"><span data-stu-id="db229-130">Hadoop</span></span>
- <span data-ttu-id="db229-131">HBase</span><span class="sxs-lookup"><span data-stu-id="db229-131">HBase</span></span>
- <span data-ttu-id="db229-132">Storm</span><span class="sxs-lookup"><span data-stu-id="db229-132">Storm</span></span>
- <span data-ttu-id="db229-133">Despertar</span><span class="sxs-lookup"><span data-stu-id="db229-133">Spark</span></span>

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

### <span data-ttu-id="db229-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db229-134">-DefaultProfile</span></span>
<span data-ttu-id="db229-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db229-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db229-136">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="db229-136">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="db229-137">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="db229-137">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="db229-138">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db229-138">-DefaultStorageAccountName</span></span>
<span data-ttu-id="db229-139">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="db229-139">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="db229-140">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="db229-140">-DefaultStorageAccountType</span></span>
<span data-ttu-id="db229-141">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="db229-141">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="db229-142">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="db229-142">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="db229-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="db229-143">-EdgeNodeSize</span></span>
<span data-ttu-id="db229-144">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="db229-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="db229-145">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db229-145">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="db229-146">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="db229-146">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="db229-147">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="db229-147">-HeadNodeSize</span></span>
<span data-ttu-id="db229-148">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="db229-148">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="db229-149">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db229-149">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="db229-150">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="db229-150">-HiveMetastore</span></span>
<span data-ttu-id="db229-151">Especifica a metaloja para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="db229-151">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="db229-152">Você também pode usar o cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="db229-152">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="db229-153">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db229-153">-ObjectId</span></span>
<span data-ttu-id="db229-154">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="db229-154">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="db229-155">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="db229-155">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="db229-156">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="db229-156">-OozieMetastore</span></span>
<span data-ttu-id="db229-157">Especifica o metastore para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="db229-157">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="db229-158">Você também pode usar o cmdlet **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="db229-158">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="db229-159">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="db229-159">-WorkerNodeSize</span></span>
<span data-ttu-id="db229-160">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="db229-160">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="db229-161">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db229-161">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="db229-162">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="db229-162">-ZookeeperNodeSize</span></span>
<span data-ttu-id="db229-163">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="db229-163">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="db229-164">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="db229-164">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="db229-165">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="db229-165">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="db229-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db229-166">CommonParameters</span></span>
<span data-ttu-id="db229-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db229-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db229-168">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db229-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db229-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db229-169">INPUTS</span></span>

### <span data-ttu-id="db229-170">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db229-170">None</span></span>

## <span data-ttu-id="db229-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db229-171">OUTPUTS</span></span>

### <span data-ttu-id="db229-172">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="db229-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="db229-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db229-173">NOTES</span></span>

## <span data-ttu-id="db229-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db229-174">RELATED LINKS</span></span>

[<span data-ttu-id="db229-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="db229-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


