---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: a372654faa9c3f157c44e5f60ff2f4244cd16d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770791"
---
# <span data-ttu-id="268ea-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="268ea-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="268ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="268ea-102">SYNOPSIS</span></span>
<span data-ttu-id="268ea-103">Cria um cluster do Azure HDInsight no grupo de recursos especificado para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="268ea-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="268ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="268ea-104">SYNTAX</span></span>

### <span data-ttu-id="268ea-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="268ea-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="268ea-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="268ea-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="268ea-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="268ea-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

## <span data-ttu-id="268ea-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="268ea-108">DESCRIPTION</span></span>
<span data-ttu-id="268ea-109">O New-AzHDInsightCluster cria um cluster do Azure HDInsight usando os parâmetros especificados ou usando um objeto de configuração que é criado usando o cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="268ea-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="268ea-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="268ea-110">EXAMPLES</span></span>

### <span data-ttu-id="268ea-111">Exemplo 1: criar um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="268ea-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
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

<span data-ttu-id="268ea-112">Esse comando cria um cluster na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="268ea-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="268ea-113">OS</span><span class="sxs-lookup"><span data-stu-id="268ea-113">PARAMETERS</span></span>

### <span data-ttu-id="268ea-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="268ea-114">-AadTenantId</span></span>
<span data-ttu-id="268ea-115">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="268ea-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="268ea-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="268ea-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="268ea-117">Especifica as contas de armazenamento adicionais do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="268ea-118">Você também pode usar o cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="268ea-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="268ea-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="268ea-119">-CertificateFileContents</span></span>
<span data-ttu-id="268ea-120">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="268ea-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="268ea-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="268ea-121">-CertificateFilePath</span></span>
<span data-ttu-id="268ea-122">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="268ea-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="268ea-123">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="268ea-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="268ea-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="268ea-124">-CertificatePassword</span></span>
<span data-ttu-id="268ea-125">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="268ea-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="268ea-126">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="268ea-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="268ea-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="268ea-127">-ClusterName</span></span>
<span data-ttu-id="268ea-128">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="268ea-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="268ea-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="268ea-130">Especifica o número de nós de trabalho do cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="268ea-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="268ea-131">-ClusterTier</span></span>
<span data-ttu-id="268ea-132">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="268ea-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="268ea-133">Por padrão, isso é padrão.</span><span class="sxs-lookup"><span data-stu-id="268ea-133">By default, this is Standard.</span></span>
<span data-ttu-id="268ea-134">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="268ea-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="268ea-135">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="268ea-135">-ClusterType</span></span>
<span data-ttu-id="268ea-136">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="268ea-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="268ea-137">Opções são: Hadoop, HBase, Storm, Spark</span><span class="sxs-lookup"><span data-stu-id="268ea-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="268ea-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="268ea-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="268ea-139">-Config</span><span class="sxs-lookup"><span data-stu-id="268ea-139">-Config</span></span>
<span data-ttu-id="268ea-140">Especifica o objeto de cluster a ser usado para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="268ea-141">Esse objeto pode ser criado usando o cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="268ea-141">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="268ea-142">-Configurações</span><span class="sxs-lookup"><span data-stu-id="268ea-142">-Configurations</span></span>
<span data-ttu-id="268ea-143">Especifica as configurações deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="268ea-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="268ea-144">Você também pode usar o cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="268ea-144">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="268ea-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268ea-145">-DefaultProfile</span></span>
<span data-ttu-id="268ea-146">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="268ea-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="268ea-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="268ea-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="268ea-148">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="268ea-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="268ea-149">Você também pode usar o cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="268ea-149">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="268ea-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="268ea-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="268ea-151">Especifica o nome da conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="268ea-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="268ea-152">Você também pode usar o cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="268ea-152">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="268ea-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="268ea-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="268ea-154">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="268ea-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="268ea-155">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="268ea-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="268ea-156">O padrão é AzureStorage, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="268ea-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="268ea-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="268ea-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="268ea-158">Especifica o nome do contêiner padrão na conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="268ea-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="268ea-159">Você também pode usar o cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="268ea-159">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="268ea-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="268ea-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="268ea-161">Especifica o caminho-prefixo na conta data Lake Store que o cluster HDInsight usará como o sistema de arquivos padrão.</span><span class="sxs-lookup"><span data-stu-id="268ea-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="268ea-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="268ea-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="268ea-163">Especifica o número de discos para a função de nó de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="268ea-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="268ea-164">-EdgeNodeSize</span></span>
<span data-ttu-id="268ea-165">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="268ea-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="268ea-166">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="268ea-166">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="268ea-167">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="268ea-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="268ea-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="268ea-168">-HeadNodeSize</span></span>
<span data-ttu-id="268ea-169">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="268ea-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="268ea-170">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="268ea-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="268ea-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="268ea-171">-HiveMetastore</span></span>
<span data-ttu-id="268ea-172">Especifica o banco de dados SQL para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="268ea-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="268ea-173">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="268ea-173">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="268ea-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="268ea-174">-HttpCredential</span></span>
<span data-ttu-id="268ea-175">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="268ea-176">-Local</span><span class="sxs-lookup"><span data-stu-id="268ea-176">-Location</span></span>
<span data-ttu-id="268ea-177">Especifica o local do cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="268ea-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="268ea-178">-ObjectId</span></span>
<span data-ttu-id="268ea-179">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="268ea-180">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="268ea-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="268ea-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="268ea-181">-OozieMetastore</span></span>
<span data-ttu-id="268ea-182">Especifica o banco de dados SQL para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="268ea-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="268ea-183">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="268ea-183">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="268ea-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="268ea-184">-OSType</span></span>
<span data-ttu-id="268ea-185">Especifica o sistema operacional do cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="268ea-186">Opções são: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="268ea-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="268ea-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="268ea-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="268ea-188">Especifica a expiração, como um objeto DateTime, para acesso ao protocolo RDP (protocolo de área de trabalho remota) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="268ea-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="268ea-189">-RdpCredential</span></span>
<span data-ttu-id="268ea-190">Especifica as credenciais da área de trabalho remota (RDP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="268ea-191">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="268ea-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="268ea-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268ea-192">-ResourceGroupName</span></span>
<span data-ttu-id="268ea-193">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="268ea-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="268ea-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="268ea-194">-ScriptActions</span></span>
<span data-ttu-id="268ea-195">Especifica as ações de script a serem executadas no cluster ao final da criação do cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="268ea-196">Você também pode usar Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="268ea-196">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="268ea-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="268ea-197">-SecurityProfile</span></span>
<span data-ttu-id="268ea-198">Especifica as propriedades relacionadas à segurança usadas para criar um cluster seguro.</span><span class="sxs-lookup"><span data-stu-id="268ea-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="268ea-199">Você também pode usar o cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="268ea-199">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="268ea-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="268ea-200">-SshCredential</span></span>
<span data-ttu-id="268ea-201">Especifica a credencial SSH a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="268ea-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="268ea-202">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="268ea-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="268ea-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="268ea-203">-SshPublicKey</span></span>
<span data-ttu-id="268ea-204">Especifica a chave pública a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="268ea-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="268ea-205">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="268ea-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="268ea-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="268ea-206">-SubnetName</span></span>
<span data-ttu-id="268ea-207">Especifica o nome de uma sub-rede dentro da rede virtual escolhida para o cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="268ea-208">-Versão</span><span class="sxs-lookup"><span data-stu-id="268ea-208">-Version</span></span>
<span data-ttu-id="268ea-209">Especifica a versão HDI do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="268ea-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="268ea-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="268ea-210">-VirtualNetworkId</span></span>
<span data-ttu-id="268ea-211">Especifica a ID da rede virtual para a qual provisionar o cluster.</span><span class="sxs-lookup"><span data-stu-id="268ea-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="268ea-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="268ea-212">-WorkerNodeSize</span></span>
<span data-ttu-id="268ea-213">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="268ea-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="268ea-214">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="268ea-214">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="268ea-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="268ea-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="268ea-216">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="268ea-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="268ea-217">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="268ea-217">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="268ea-218">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="268ea-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="268ea-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268ea-219">CommonParameters</span></span>
<span data-ttu-id="268ea-220">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268ea-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268ea-221">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268ea-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268ea-222">SENSORES</span><span class="sxs-lookup"><span data-stu-id="268ea-222">INPUTS</span></span>

### <span data-ttu-id="268ea-223">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="268ea-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="268ea-224">EXIBE</span><span class="sxs-lookup"><span data-stu-id="268ea-224">OUTPUTS</span></span>

### <span data-ttu-id="268ea-225">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="268ea-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="268ea-226">INFORMA</span><span class="sxs-lookup"><span data-stu-id="268ea-226">NOTES</span></span>
<span data-ttu-id="268ea-227">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="268ea-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="268ea-228">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="268ea-228">RELATED LINKS</span></span>

[<span data-ttu-id="268ea-229">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="268ea-229">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

