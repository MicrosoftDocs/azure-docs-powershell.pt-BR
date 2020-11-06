---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: b10fe80fb0a58267212912f554d044b2715fd1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430262"
---
# <span data-ttu-id="c44ca-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c44ca-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="c44ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c44ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c44ca-103">Cria um cluster do Azure HDInsight no grupo de recursos especificado para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c44ca-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c44ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c44ca-104">SYNTAX</span></span>

### <span data-ttu-id="c44ca-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="c44ca-105">Default (Default)</span></span>
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

### <span data-ttu-id="c44ca-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c44ca-106">CertificateFilePath</span></span>
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

### <span data-ttu-id="c44ca-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c44ca-107">CertificateFileContents</span></span>
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

## <span data-ttu-id="c44ca-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c44ca-108">DESCRIPTION</span></span>
<span data-ttu-id="c44ca-109">O New-AzureHDInsightCluster cria um cluster do Azure HDInsight usando os parâmetros especificados ou usando um objeto de configuração que é criado usando o cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c44ca-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="c44ca-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c44ca-110">EXAMPLES</span></span>

### <span data-ttu-id="c44ca-111">Exemplo 1: criar um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="c44ca-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="c44ca-112">Esse comando cria um cluster na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c44ca-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="c44ca-113">OS</span><span class="sxs-lookup"><span data-stu-id="c44ca-113">PARAMETERS</span></span>

### <span data-ttu-id="c44ca-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="c44ca-114">-AadTenantId</span></span>
<span data-ttu-id="c44ca-115">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c44ca-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c44ca-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="c44ca-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="c44ca-117">Especifica as contas de armazenamento adicionais do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="c44ca-118">Você também pode usar o cmdlet Add-AzureRmHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="c44ca-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="c44ca-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="c44ca-119">-CertificateFileContents</span></span>
<span data-ttu-id="c44ca-120">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c44ca-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c44ca-121">-CertificateFilePath</span></span>
<span data-ttu-id="c44ca-122">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="c44ca-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c44ca-123">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c44ca-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c44ca-124">-CertificatePassword</span></span>
<span data-ttu-id="c44ca-125">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="c44ca-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="c44ca-126">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c44ca-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c44ca-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c44ca-127">-ClusterName</span></span>
<span data-ttu-id="c44ca-128">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-128">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="c44ca-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="c44ca-130">Especifica o número de nós de trabalho do cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="c44ca-131">-ClusterTier</span></span>
<span data-ttu-id="c44ca-132">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c44ca-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="c44ca-133">Por padrão, isso é padrão.</span><span class="sxs-lookup"><span data-stu-id="c44ca-133">By default, this is Standard.</span></span>
<span data-ttu-id="c44ca-134">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="c44ca-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="c44ca-135">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="c44ca-135">-ClusterType</span></span>
<span data-ttu-id="c44ca-136">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c44ca-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="c44ca-137">Opções são: Hadoop, HBase, Storm, Spark</span><span class="sxs-lookup"><span data-stu-id="c44ca-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="c44ca-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="c44ca-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="c44ca-139">-Config</span><span class="sxs-lookup"><span data-stu-id="c44ca-139">-Config</span></span>
<span data-ttu-id="c44ca-140">Especifica o objeto de cluster a ser usado para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="c44ca-141">Esse objeto pode ser criado usando o cmdlet New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="c44ca-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-142">-Configurações</span><span class="sxs-lookup"><span data-stu-id="c44ca-142">-Configurations</span></span>
<span data-ttu-id="c44ca-143">Especifica as configurações deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c44ca-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="c44ca-144">Você também pode usar o cmdlet Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="c44ca-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="c44ca-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c44ca-145">-DefaultProfile</span></span>
<span data-ttu-id="c44ca-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c44ca-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c44ca-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c44ca-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c44ca-148">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="c44ca-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c44ca-149">Você também pode usar o cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="c44ca-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c44ca-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c44ca-151">Especifica o nome da conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="c44ca-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c44ca-152">Você também pode usar o cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="c44ca-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c44ca-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="c44ca-154">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="c44ca-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="c44ca-155">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="c44ca-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="c44ca-156">O padrão é AzureStorage, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="c44ca-156">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c44ca-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="c44ca-158">Especifica o nome do contêiner padrão na conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="c44ca-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="c44ca-159">Você também pode usar o cmdlet Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="c44ca-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="c44ca-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="c44ca-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="c44ca-161">Especifica o caminho-prefixo na conta data Lake Store que o cluster HDInsight usará como o sistema de arquivos padrão.</span><span class="sxs-lookup"><span data-stu-id="c44ca-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="c44ca-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="c44ca-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="c44ca-163">Especifica o número de discos para a função de nó de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="c44ca-164">-EdgeNodeSize</span></span>
<span data-ttu-id="c44ca-165">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="c44ca-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="c44ca-166">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c44ca-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="c44ca-167">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="c44ca-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="c44ca-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="c44ca-168">-HeadNodeSize</span></span>
<span data-ttu-id="c44ca-169">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="c44ca-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="c44ca-170">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c44ca-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c44ca-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="c44ca-171">-HiveMetastore</span></span>
<span data-ttu-id="c44ca-172">Especifica o banco de dados SQL para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="c44ca-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="c44ca-173">Você também pode usar o cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="c44ca-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c44ca-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="c44ca-174">-HttpCredential</span></span>
<span data-ttu-id="c44ca-175">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-176">-Local</span><span class="sxs-lookup"><span data-stu-id="c44ca-176">-Location</span></span>
<span data-ttu-id="c44ca-177">Especifica o local do cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-177">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c44ca-178">-ObjectId</span></span>
<span data-ttu-id="c44ca-179">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="c44ca-180">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c44ca-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="c44ca-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="c44ca-181">-OozieMetastore</span></span>
<span data-ttu-id="c44ca-182">Especifica o banco de dados SQL para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="c44ca-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="c44ca-183">Você também pode usar o cmdlet Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="c44ca-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="c44ca-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="c44ca-184">-OSType</span></span>
<span data-ttu-id="c44ca-185">Especifica o sistema operacional do cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="c44ca-186">Opções são: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="c44ca-186">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="c44ca-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="c44ca-188">Especifica a expiração, como um objeto DateTime, para acesso ao protocolo RDP (protocolo de área de trabalho remota) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="c44ca-189">-RdpCredential</span></span>
<span data-ttu-id="c44ca-190">Especifica as credenciais da área de trabalho remota (RDP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="c44ca-191">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="c44ca-191">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c44ca-192">-ResourceGroupName</span></span>
<span data-ttu-id="c44ca-193">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c44ca-193">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="c44ca-194">-ScriptActions</span></span>
<span data-ttu-id="c44ca-195">Especifica as ações de script a serem executadas no cluster ao final da criação do cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="c44ca-196">Você também pode usar Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="c44ca-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="c44ca-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="c44ca-197">-SecurityProfile</span></span>
<span data-ttu-id="c44ca-198">Especifica as propriedades relacionadas à segurança usadas para criar um cluster seguro.</span><span class="sxs-lookup"><span data-stu-id="c44ca-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="c44ca-199">Você também pode usar o cmdlet Add-AzureRmHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="c44ca-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="c44ca-200">-SshCredential</span></span>
<span data-ttu-id="c44ca-201">Especifica a credencial SSH a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="c44ca-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="c44ca-202">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="c44ca-202">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c44ca-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="c44ca-203">-SshPublicKey</span></span>
<span data-ttu-id="c44ca-204">Especifica a chave pública a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="c44ca-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="c44ca-205">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="c44ca-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="c44ca-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c44ca-206">-SubnetName</span></span>
<span data-ttu-id="c44ca-207">Especifica o nome de uma sub-rede dentro da rede virtual escolhida para o cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="c44ca-208">-Versão</span><span class="sxs-lookup"><span data-stu-id="c44ca-208">-Version</span></span>
<span data-ttu-id="c44ca-209">Especifica a versão HDI do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c44ca-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="c44ca-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c44ca-210">-VirtualNetworkId</span></span>
<span data-ttu-id="c44ca-211">Especifica a ID da rede virtual para a qual provisionar o cluster.</span><span class="sxs-lookup"><span data-stu-id="c44ca-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="c44ca-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="c44ca-212">-WorkerNodeSize</span></span>
<span data-ttu-id="c44ca-213">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c44ca-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="c44ca-214">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c44ca-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="c44ca-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="c44ca-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="c44ca-216">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="c44ca-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="c44ca-217">Use Get-AzureRmVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c44ca-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="c44ca-218">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="c44ca-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="c44ca-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c44ca-219">CommonParameters</span></span>
<span data-ttu-id="c44ca-220">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c44ca-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c44ca-221">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c44ca-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c44ca-222">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c44ca-222">INPUTS</span></span>

### <span data-ttu-id="c44ca-223">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="c44ca-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="c44ca-224">Parâmetros: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c44ca-224">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="c44ca-225">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c44ca-225">OUTPUTS</span></span>

### <span data-ttu-id="c44ca-226">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c44ca-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="c44ca-227">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c44ca-227">NOTES</span></span>
<span data-ttu-id="c44ca-228">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="c44ca-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="c44ca-229">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c44ca-229">RELATED LINKS</span></span>

[<span data-ttu-id="c44ca-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c44ca-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

