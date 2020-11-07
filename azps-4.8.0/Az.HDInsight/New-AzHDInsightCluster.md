---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955022"
---
# <span data-ttu-id="3e399-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3e399-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="3e399-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e399-102">SYNOPSIS</span></span>
<span data-ttu-id="3e399-103">Cria um cluster do Azure HDInsight no grupo de recursos especificado para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3e399-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="3e399-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e399-104">SYNTAX</span></span>

### <span data-ttu-id="3e399-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="3e399-105">Default (Default)</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e399-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3e399-106">CertificateFilePath</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e399-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3e399-107">CertificateFileContents</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e399-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e399-108">DESCRIPTION</span></span>
<span data-ttu-id="3e399-109">O New-AzHDInsightCluster cria um cluster do Azure HDInsight usando os parâmetros especificados ou usando um objeto de configuração que é criado usando o cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3e399-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3e399-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e399-110">EXAMPLES</span></span>

### <span data-ttu-id="3e399-111">Exemplo 1: criar um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="3e399-111">Example 1: Create an Azure HDInsight cluster</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="3e399-112">Esse comando cria um cluster na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="3e399-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="3e399-113">Exemplo 2: criar cluster com a chave de criptografia de disco gerenciada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="3e399-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="3e399-114">Exemplo 3: criar um cluster do Azure HDInsight que permite a criptografia em trânsito</span><span class="sxs-lookup"><span data-stu-id="3e399-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="3e399-115">Exemplo 4: criar um cluster do Azure HDInsight com recurso de link privado</span><span class="sxs-lookup"><span data-stu-id="3e399-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="3e399-116">Exemplo 5: criar um cluster do Azure HDInsight que permite a criptografia no host</span><span class="sxs-lookup"><span data-stu-id="3e399-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="3e399-117">Exemplo 6: criar um cluster do Azure HDInsight que permite a autoescala.</span><span class="sxs-lookup"><span data-stu-id="3e399-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="3e399-118">OS</span><span class="sxs-lookup"><span data-stu-id="3e399-118">PARAMETERS</span></span>

### <span data-ttu-id="3e399-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="3e399-119">-AadTenantId</span></span>
<span data-ttu-id="3e399-120">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e399-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e399-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3e399-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="3e399-122">Especifica as contas de armazenamento adicionais do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="3e399-123">Você também pode usar o cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="3e399-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="3e399-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3e399-124">-ApplicationId</span></span>
<span data-ttu-id="3e399-125">Obtém ou define a ID do aplicativo principal do serviço para acessar o Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="3e399-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="3e399-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3e399-126">-AssignedIdentity</span></span>
<span data-ttu-id="3e399-127">Obtém ou define a identidade atribuída.</span><span class="sxs-lookup"><span data-stu-id="3e399-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="3e399-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e399-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="3e399-129">Obtém ou define a configuração de dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="3e399-129">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e399-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3e399-130">-CertificateFileContents</span></span>
<span data-ttu-id="3e399-131">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e399-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e399-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3e399-132">-CertificateFilePath</span></span>
<span data-ttu-id="3e399-133">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="3e399-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3e399-134">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e399-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e399-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3e399-135">-CertificatePassword</span></span>
<span data-ttu-id="3e399-136">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="3e399-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3e399-137">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e399-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e399-138">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3e399-138">-ClusterName</span></span>
<span data-ttu-id="3e399-139">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3e399-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="3e399-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="3e399-141">Especifica o número de nós de trabalho do cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="3e399-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="3e399-142">-ClusterTier</span></span>
<span data-ttu-id="3e399-143">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e399-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="3e399-144">Por padrão, isso é padrão.</span><span class="sxs-lookup"><span data-stu-id="3e399-144">By default, this is Standard.</span></span>
<span data-ttu-id="3e399-145">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="3e399-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="3e399-146">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="3e399-146">-ClusterType</span></span>
<span data-ttu-id="3e399-147">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="3e399-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="3e399-148">As opções são: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka e RServer</span><span class="sxs-lookup"><span data-stu-id="3e399-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="3e399-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="3e399-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="3e399-150">-Config</span><span class="sxs-lookup"><span data-stu-id="3e399-150">-Config</span></span>
<span data-ttu-id="3e399-151">Especifica o objeto de cluster a ser usado para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="3e399-152">Esse objeto pode ser criado usando o cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3e399-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="3e399-153">-Configurações</span><span class="sxs-lookup"><span data-stu-id="3e399-153">-Configurations</span></span>
<span data-ttu-id="3e399-154">Especifica as configurações deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e399-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="3e399-155">Você também pode usar o cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3e399-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="3e399-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e399-156">-DefaultProfile</span></span>
<span data-ttu-id="3e399-157">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3e399-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e399-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3e399-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="3e399-159">Especifica a chave de conta para a conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="3e399-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3e399-160">Você também pode usar o cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3e399-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="3e399-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e399-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="3e399-162">Especifica o nome da conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="3e399-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3e399-163">Você também pode usar o cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3e399-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="3e399-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3e399-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="3e399-165">Especifica o tipo da conta de armazenamento padrão que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="3e399-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="3e399-166">Os valores possíveis são AzureStorage e AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="3e399-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="3e399-167">O padrão é AzureStorage, se não especificado.</span><span class="sxs-lookup"><span data-stu-id="3e399-167">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="3e399-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3e399-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="3e399-169">Especifica o nome do contêiner padrão na conta de armazenamento padrão do Azure que o cluster HDInsight vai usar.</span><span class="sxs-lookup"><span data-stu-id="3e399-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3e399-170">Você também pode usar o cmdlet Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3e399-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="3e399-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="3e399-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="3e399-172">Especifica o caminho-prefixo na conta data Lake Store que o cluster HDInsight usará como o sistema de arquivos padrão.</span><span class="sxs-lookup"><span data-stu-id="3e399-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="3e399-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="3e399-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="3e399-174">Especifica o número de discos para a função de nó de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="3e399-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e399-175">-EdgeNodeSize</span></span>
<span data-ttu-id="3e399-176">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="3e399-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="3e399-177">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e399-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="3e399-178">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="3e399-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="3e399-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="3e399-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="3e399-180">Obtém ou define o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="3e399-180">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="3e399-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="3e399-181">-EncryptionAtHost</span></span>
<span data-ttu-id="3e399-182">Obtém ou define o sinalizador que indica se a criptografia deve ser habilitada no host ou não.</span><span class="sxs-lookup"><span data-stu-id="3e399-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="3e399-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="3e399-183">-EncryptionInTransit</span></span>
<span data-ttu-id="3e399-184">Obtém ou define o sinalizador que indica se habilitou a criptografia em trânsito ou não.</span><span class="sxs-lookup"><span data-stu-id="3e399-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="3e399-185">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="3e399-185">-EncryptionKeyName</span></span>
<span data-ttu-id="3e399-186">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="3e399-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="3e399-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="3e399-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="3e399-188">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="3e399-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="3e399-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="3e399-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="3e399-190">Obtém ou define o URI do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="3e399-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="3e399-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e399-191">-HeadNodeSize</span></span>
<span data-ttu-id="3e399-192">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="3e399-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="3e399-193">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e399-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3e399-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="3e399-194">-HiveMetastore</span></span>
<span data-ttu-id="3e399-195">Especifica o banco de dados SQL para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="3e399-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="3e399-196">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3e399-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3e399-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="3e399-197">-HttpCredential</span></span>
<span data-ttu-id="3e399-198">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="3e399-199">-Local</span><span class="sxs-lookup"><span data-stu-id="3e399-199">-Location</span></span>
<span data-ttu-id="3e399-200">Especifica o local do cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="3e399-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3e399-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="3e399-202">Obtém ou define a versão do TLS mínima suportada.</span><span class="sxs-lookup"><span data-stu-id="3e399-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="3e399-203">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3e399-203">-ObjectId</span></span>
<span data-ttu-id="3e399-204">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="3e399-205">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3e399-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3e399-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="3e399-206">-OozieMetastore</span></span>
<span data-ttu-id="3e399-207">Especifica o banco de dados SQL para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="3e399-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="3e399-208">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3e399-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3e399-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="3e399-209">-OSType</span></span>
<span data-ttu-id="3e399-210">Especifica o sistema operacional do cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="3e399-211">Opções são: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="3e399-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="3e399-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="3e399-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="3e399-213">Obtém ou define o tipo de acesso de saída para a rede pública.</span><span class="sxs-lookup"><span data-stu-id="3e399-213">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="3e399-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="3e399-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="3e399-215">Obtém ou define o tipo de acesso à rede pública.</span><span class="sxs-lookup"><span data-stu-id="3e399-215">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="3e399-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="3e399-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="3e399-217">Especifica a expiração, como um objeto DateTime, para acesso ao protocolo RDP (protocolo de área de trabalho remota) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="3e399-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="3e399-218">-RdpCredential</span></span>
<span data-ttu-id="3e399-219">Especifica as credenciais da área de trabalho remota (RDP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="3e399-220">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="3e399-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="3e399-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e399-221">-ResourceGroupName</span></span>
<span data-ttu-id="3e399-222">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3e399-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3e399-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="3e399-223">-ScriptActions</span></span>
<span data-ttu-id="3e399-224">Especifica as ações de script a serem executadas no cluster ao final da criação do cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="3e399-225">Você também pode usar Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="3e399-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="3e399-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3e399-226">-SecurityProfile</span></span>
<span data-ttu-id="3e399-227">Especifica as propriedades relacionadas à segurança usadas para criar um cluster seguro.</span><span class="sxs-lookup"><span data-stu-id="3e399-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="3e399-228">Você também pode usar o cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="3e399-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="3e399-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="3e399-229">-SshCredential</span></span>
<span data-ttu-id="3e399-230">Especifica a credencial SSH a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="3e399-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="3e399-231">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="3e399-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="3e399-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3e399-232">-SshPublicKey</span></span>
<span data-ttu-id="3e399-233">Especifica a chave pública a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="3e399-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="3e399-234">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="3e399-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="3e399-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3e399-235">-SubnetName</span></span>
<span data-ttu-id="3e399-236">Especifica o nome de uma sub-rede dentro da rede virtual escolhida para o cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="3e399-237">-Versão</span><span class="sxs-lookup"><span data-stu-id="3e399-237">-Version</span></span>
<span data-ttu-id="3e399-238">Especifica a versão HDI do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e399-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="3e399-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3e399-239">-VirtualNetworkId</span></span>
<span data-ttu-id="3e399-240">Especifica a ID da rede virtual para a qual provisionar o cluster.</span><span class="sxs-lookup"><span data-stu-id="3e399-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="3e399-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e399-241">-WorkerNodeSize</span></span>
<span data-ttu-id="3e399-242">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3e399-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="3e399-243">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e399-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3e399-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="3e399-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="3e399-245">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="3e399-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="3e399-246">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e399-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="3e399-247">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="3e399-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="3e399-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e399-248">CommonParameters</span></span>
<span data-ttu-id="3e399-249">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e399-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e399-250">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e399-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e399-251">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e399-251">INPUTS</span></span>

### <span data-ttu-id="3e399-252">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3e399-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3e399-253">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e399-253">OUTPUTS</span></span>

### <span data-ttu-id="3e399-254">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3e399-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3e399-255">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e399-255">NOTES</span></span>
<span data-ttu-id="3e399-256">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="3e399-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="3e399-257">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e399-257">RELATED LINKS</span></span>

[<span data-ttu-id="3e399-258">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3e399-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

