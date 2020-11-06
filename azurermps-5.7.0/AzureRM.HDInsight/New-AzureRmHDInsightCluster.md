---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: 2e778f84eabf7e5dc4dd325d2a17361064c5d99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441339"
---
# <span data-ttu-id="bdb4a-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bdb4a-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="bdb4a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bdb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="bdb4a-103">Cria um cluster do Azure HDInsight no grupo de recursos especificado para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdb4a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bdb4a-104">SYNTAX</span></span>

### <span data-ttu-id="bdb4a-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="bdb4a-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb4a-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="bdb4a-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdb4a-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="bdb4a-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdb4a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bdb4a-108">DESCRIPTION</span></span>
<span data-ttu-id="bdb4a-109">O New-AzureHDInsightCluster cria um cluster do Azure HDInsight usando os parâmetros especificados ou usando um objeto de configuração que é criado usando o cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="bdb4a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bdb4a-110">EXAMPLES</span></span>

### <span data-ttu-id="bdb4a-111">--------------------------Exemplo 1: criar um cluster do Azure HDInsight--------------------------</span><span class="sxs-lookup"><span data-stu-id="bdb4a-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
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

<span data-ttu-id="bdb4a-112">Esse comando cria um cluster na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="bdb4a-113">OS</span><span class="sxs-lookup"><span data-stu-id="bdb4a-113">PARAMETERS</span></span>

### <span data-ttu-id="bdb4a-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="bdb4a-114">-AadTenantId</span></span>
<span data-ttu-id="bdb4a-115">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="bdb4a-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="bdb4a-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="bdb4a-117">Especifica as contas de armazenamento adicionais do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="bdb4a-118">Você também pode usar o cmdlet Add-AzureRmHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="bdb4a-119">-CertificateFileContents</span></span>
<span data-ttu-id="bdb4a-120">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="bdb4a-121">-CertificateFilePath</span></span>
<span data-ttu-id="bdb4a-122">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="bdb4a-123">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="bdb4a-124">-CertificatePassword</span></span>
<span data-ttu-id="bdb4a-125">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="bdb4a-126">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="bdb4a-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bdb4a-127">-ClusterName</span></span>
<span data-ttu-id="bdb4a-128">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-128">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="bdb4a-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="bdb4a-130">Especifica o número de nós de trabalho do cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="bdb4a-131">-ClusterTier</span></span>
<span data-ttu-id="bdb4a-132">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="bdb4a-133">Por padrão, isso é padrão.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-133">By default, this is Standard.</span></span>
<span data-ttu-id="bdb4a-134">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="bdb4a-135">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="bdb4a-135">-ClusterType</span></span>
<span data-ttu-id="bdb4a-136">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="bdb4a-137">Opções são: Hadoop, HBase, Storm, Spark</span><span class="sxs-lookup"><span data-stu-id="bdb4a-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="bdb4a-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="bdb4a-138">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-139">-Config</span><span class="sxs-lookup"><span data-stu-id="bdb4a-139">-Config</span></span>
<span data-ttu-id="bdb4a-140">Especifica o objeto de cluster a ser usado para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="bdb4a-141">Esse objeto pode ser criado usando o cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-142">-Configurações</span><span class="sxs-lookup"><span data-stu-id="bdb4a-142">-Configurations</span></span>
<span data-ttu-id="bdb4a-143">Especifica as configurações deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="bdb4a-144">Você também pode usar o cmdlet Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb4a-145">-DefaultProfile</span></span>
<span data-ttu-id="bdb4a-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bdb4a-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdb4a-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bdb4a-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="bdb4a-148">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="bdb4a-149">Você também pode usar o cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bdb4a-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="bdb4a-151">Especifica o nome da conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="bdb4a-152">Você também pode usar o cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bdb4a-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="bdb4a-154">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="bdb4a-155">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="bdb4a-156">O padrão é AzureStorage, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="bdb4a-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bdb4a-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="bdb4a-158">Especifica o nome do contêiner padrão na conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="bdb4a-159">Você também pode usar o cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="bdb4a-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="bdb4a-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="bdb4a-161">Especifica o caminho-prefixo na conta data Lake Store que o cluster HDInsight usará como o sistema de arquivos padrão.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="bdb4a-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="bdb4a-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="bdb4a-163">Especifica o número de discos para a função de nó de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="bdb4a-164">-EdgeNodeSize</span></span>
<span data-ttu-id="bdb4a-165">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="bdb4a-166">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="bdb4a-167">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="bdb4a-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="bdb4a-168">-HeadNodeSize</span></span>
<span data-ttu-id="bdb4a-169">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="bdb4a-170">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="bdb4a-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="bdb4a-171">-HiveMetastore</span></span>
<span data-ttu-id="bdb4a-172">Especifica o banco de dados SQL para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="bdb4a-173">Você também pode usar o cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="bdb4a-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="bdb4a-174">-HttpCredential</span></span>
<span data-ttu-id="bdb4a-175">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-176">-Local</span><span class="sxs-lookup"><span data-stu-id="bdb4a-176">-Location</span></span>
<span data-ttu-id="bdb4a-177">Especifica o local do cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-177">Specifies the location for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bdb4a-178">-ObjectId</span></span>
<span data-ttu-id="bdb4a-179">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="bdb4a-180">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="bdb4a-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="bdb4a-181">-OozieMetastore</span></span>
<span data-ttu-id="bdb4a-182">Especifica o banco de dados SQL para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="bdb4a-183">Você também pode usar o cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="bdb4a-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="bdb4a-184">-OSType</span></span>
<span data-ttu-id="bdb4a-185">Especifica o sistema operacional do cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="bdb4a-186">Opções são: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="bdb4a-186">Options are: Windows, Linux</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="bdb4a-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="bdb4a-188">Especifica a expiração, como um objeto DateTime, para acesso ao protocolo RDP (protocolo de área de trabalho remota) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="bdb4a-189">-RdpCredential</span></span>
<span data-ttu-id="bdb4a-190">Especifica as credenciais da área de trabalho remota (RDP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="bdb4a-191">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-191">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb4a-192">-ResourceGroupName</span></span>
<span data-ttu-id="bdb4a-193">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-193">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="bdb4a-194">-ScriptActions</span></span>
<span data-ttu-id="bdb4a-195">Especifica as ações de script a serem executadas no cluster ao final da criação do cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="bdb4a-196">Você também pode usar Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases: 
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="bdb4a-197">-SecurityProfile</span></span>
<span data-ttu-id="bdb4a-198">Especifica as propriedades relacionadas à segurança usadas para criar um cluster seguro.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="bdb4a-199">Você também pode usar o cmdlet Add-AzureRmHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="bdb4a-200">-SshCredential</span></span>
<span data-ttu-id="bdb4a-201">Especifica a credencial SSH a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="bdb4a-202">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-202">This is only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdb4a-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="bdb4a-203">-SshPublicKey</span></span>
<span data-ttu-id="bdb4a-204">Especifica a chave pública a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="bdb4a-205">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="bdb4a-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bdb4a-206">-SubnetName</span></span>
<span data-ttu-id="bdb4a-207">Especifica o nome de uma sub-rede dentro da rede virtual escolhida para o cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="bdb4a-208">-Versão</span><span class="sxs-lookup"><span data-stu-id="bdb4a-208">-Version</span></span>
<span data-ttu-id="bdb4a-209">Especifica a versão HDI do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="bdb4a-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="bdb4a-210">-VirtualNetworkId</span></span>
<span data-ttu-id="bdb4a-211">Especifica a ID da rede virtual para a qual provisionar o cluster.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="bdb4a-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="bdb4a-212">-WorkerNodeSize</span></span>
<span data-ttu-id="bdb4a-213">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="bdb4a-214">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="bdb4a-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="bdb4a-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="bdb4a-216">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="bdb4a-217">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="bdb4a-218">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="bdb4a-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb4a-219">CommonParameters</span></span>
<span data-ttu-id="bdb4a-220">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb4a-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb4a-221">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb4a-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb4a-222">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bdb4a-222">INPUTS</span></span>

### <span data-ttu-id="bdb4a-223">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="bdb4a-223">AzureHDInsightConfig</span></span>
<span data-ttu-id="bdb4a-224">O parâmetro ' config ' aceita o valor do tipo ' AzureHDInsightConfig ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="bdb4a-224">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="bdb4a-225">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bdb4a-225">OUTPUTS</span></span>

### <span data-ttu-id="bdb4a-226">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="bdb4a-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="bdb4a-227">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bdb4a-227">NOTES</span></span>
<span data-ttu-id="bdb4a-228">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="bdb4a-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="bdb4a-229">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bdb4a-229">RELATED LINKS</span></span>

[<span data-ttu-id="bdb4a-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="bdb4a-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

