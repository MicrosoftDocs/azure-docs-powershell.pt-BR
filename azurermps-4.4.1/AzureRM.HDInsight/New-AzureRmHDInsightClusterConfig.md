---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightClusterConfig.md
ms.openlocfilehash: 381143b356202a7b6b76e173b233f2fffe87f6a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441072"
---
# <span data-ttu-id="31a40-101">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="31a40-101">New-AzureRmHDInsightClusterConfig</span></span>

## <span data-ttu-id="31a40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31a40-102">SYNOPSIS</span></span>
<span data-ttu-id="31a40-103">Cria um objeto de configuração de cluster não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31a40-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31a40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31a40-104">SYNTAX</span></span>

```
New-AzureRmHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31a40-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="31a40-105">DESCRIPTION</span></span>
<span data-ttu-id="31a40-106">O cmdlet **New-AzureRmHDInsightClusterConfig** cria um objeto não persistente que descreve uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31a40-106">The **New-AzureRmHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="31a40-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="31a40-107">EXAMPLES</span></span>

### <span data-ttu-id="31a40-108">Exemplo 1: criar um objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="31a40-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="31a40-109">Esse comando cria um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="31a40-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="31a40-110">OS</span><span class="sxs-lookup"><span data-stu-id="31a40-110">PARAMETERS</span></span>

### <span data-ttu-id="31a40-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="31a40-111">-AadTenantId</span></span>
<span data-ttu-id="31a40-112">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31a40-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="31a40-113">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="31a40-113">-CertificateFileContents</span></span>
<span data-ttu-id="31a40-114">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31a40-114">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="31a40-115">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="31a40-115">-CertificateFilePath</span></span>
<span data-ttu-id="31a40-116">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="31a40-116">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="31a40-117">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31a40-117">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="31a40-118">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="31a40-118">-CertificatePassword</span></span>
<span data-ttu-id="31a40-119">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="31a40-119">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="31a40-120">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31a40-120">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="31a40-121">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="31a40-121">-ClusterTier</span></span>
<span data-ttu-id="31a40-122">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31a40-122">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="31a40-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="31a40-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31a40-124">Oficial</span><span class="sxs-lookup"><span data-stu-id="31a40-124">Standard</span></span>
- <span data-ttu-id="31a40-125">Gratifica</span><span class="sxs-lookup"><span data-stu-id="31a40-125">Premium</span></span>

<span data-ttu-id="31a40-126">O valor padrão é padrão.</span><span class="sxs-lookup"><span data-stu-id="31a40-126">The default value is Standard.</span></span>
<span data-ttu-id="31a40-127">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="31a40-127">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="31a40-128">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="31a40-128">-ClusterType</span></span>
<span data-ttu-id="31a40-129">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="31a40-129">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="31a40-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="31a40-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="31a40-131">Hadoop</span><span class="sxs-lookup"><span data-stu-id="31a40-131">Hadoop</span></span>
- <span data-ttu-id="31a40-132">HBase</span><span class="sxs-lookup"><span data-stu-id="31a40-132">HBase</span></span>
- <span data-ttu-id="31a40-133">Storm</span><span class="sxs-lookup"><span data-stu-id="31a40-133">Storm</span></span>
- <span data-ttu-id="31a40-134">Despertar</span><span class="sxs-lookup"><span data-stu-id="31a40-134">Spark</span></span>

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

### <span data-ttu-id="31a40-135">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="31a40-135">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="31a40-136">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="31a40-136">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="31a40-137">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="31a40-137">-DefaultStorageAccountName</span></span>
<span data-ttu-id="31a40-138">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="31a40-138">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="31a40-139">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="31a40-139">-DefaultStorageAccountType</span></span>
<span data-ttu-id="31a40-140">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="31a40-140">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="31a40-141">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="31a40-141">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="31a40-142">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="31a40-142">-EdgeNodeSize</span></span>
<span data-ttu-id="31a40-143">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="31a40-143">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="31a40-144">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31a40-144">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="31a40-145">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="31a40-145">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="31a40-146">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="31a40-146">-HeadNodeSize</span></span>
<span data-ttu-id="31a40-147">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="31a40-147">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="31a40-148">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31a40-148">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="31a40-149">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="31a40-149">-HiveMetastore</span></span>
<span data-ttu-id="31a40-150">Especifica a metaloja para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="31a40-150">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="31a40-151">Você também pode usar o cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="31a40-151">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="31a40-152">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="31a40-152">-ObjectId</span></span>
<span data-ttu-id="31a40-153">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="31a40-153">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="31a40-154">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31a40-154">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="31a40-155">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="31a40-155">-OozieMetastore</span></span>
<span data-ttu-id="31a40-156">Especifica o metastore para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="31a40-156">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="31a40-157">Você também pode usar o cmdlet **Add-AzureRmHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="31a40-157">You can alternatively use the **Add-AzureRmHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="31a40-158">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="31a40-158">-WorkerNodeSize</span></span>
<span data-ttu-id="31a40-159">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="31a40-159">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="31a40-160">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31a40-160">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="31a40-161">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="31a40-161">-ZookeeperNodeSize</span></span>
<span data-ttu-id="31a40-162">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="31a40-162">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="31a40-163">Use Get-AzureRMVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="31a40-163">Use Get-AzureRMVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="31a40-164">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="31a40-164">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="31a40-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a40-165">-DefaultProfile</span></span>
<span data-ttu-id="31a40-166">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31a40-166">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a40-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a40-167">CommonParameters</span></span>
<span data-ttu-id="31a40-168">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a40-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a40-169">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a40-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a40-170">SENSORES</span><span class="sxs-lookup"><span data-stu-id="31a40-170">INPUTS</span></span>

## <span data-ttu-id="31a40-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="31a40-171">OUTPUTS</span></span>

### <span data-ttu-id="31a40-172">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="31a40-172">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="31a40-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="31a40-173">NOTES</span></span>

## <span data-ttu-id="31a40-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31a40-174">RELATED LINKS</span></span>

[<span data-ttu-id="31a40-175">Add-AzureRmHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="31a40-175">Add-AzureRmHDInsightStorage</span></span>](./Add-AzureRmHDInsightStorage.md)


