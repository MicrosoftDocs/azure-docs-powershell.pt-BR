---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: b42b93bbecef5ec56495be632788bd1373ae9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115357"
---
# <span data-ttu-id="9e123-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9e123-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="9e123-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e123-102">SYNOPSIS</span></span>
<span data-ttu-id="9e123-103">Cria um cluster do Azure HDInsight no grupo de recursos especificado para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9e123-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="9e123-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e123-104">SYNTAX</span></span>

### <span data-ttu-id="9e123-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="9e123-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e123-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="9e123-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e123-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="9e123-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e123-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e123-108">DESCRIPTION</span></span>
<span data-ttu-id="9e123-109">O New-AzHDInsightCluster cria um cluster do Azure HDInsight usando os parâmetros especificados ou usando um objeto de configuração que é criado usando o cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="9e123-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="9e123-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e123-110">EXAMPLES</span></span>

### <span data-ttu-id="9e123-111">Exemplo 1: criar um cluster do Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="9e123-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="9e123-112">Esse comando cria um cluster na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9e123-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="9e123-113">Exemplo 2: criar cluster com a chave de criptografia de disco gerenciada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="9e123-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="9e123-114">Exemplo 3: criar um cluster do Azure HDInsight que permite a criptografia em trânsito</span><span class="sxs-lookup"><span data-stu-id="9e123-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="9e123-115">Exemplo 4: criar um cluster do Azure HDInsight com recurso de link privado</span><span class="sxs-lookup"><span data-stu-id="9e123-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="9e123-116">Exemplo 5: criar um cluster do Azure HDInsight que permite a criptografia no host</span><span class="sxs-lookup"><span data-stu-id="9e123-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="9e123-117">Exemplo 6: criar um cluster do Azure HDInsight que permite a autoescala.</span><span class="sxs-lookup"><span data-stu-id="9e123-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="9e123-118">Exemplo 7: criar um cluster do Azure HDInsight com proxy Kafka REST.</span><span class="sxs-lookup"><span data-stu-id="9e123-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="9e123-119">Exemplo 8: criar um cluster do Azure HDInsight com armazenamento do Azure data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="9e123-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

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
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="9e123-120">Exemplo 9: criar um cluster do Azure HDInsight com o pacote de segurança da empresa (ESP) e habilitar o agente de ID do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

## <span data-ttu-id="9e123-121">OS</span><span class="sxs-lookup"><span data-stu-id="9e123-121">PARAMETERS</span></span>

### <span data-ttu-id="9e123-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="9e123-122">-AadTenantId</span></span>
<span data-ttu-id="9e123-123">Especifica a ID de locatário do Azure AD que será usada ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e123-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9e123-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="9e123-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="9e123-125">Especifica as contas de armazenamento adicionais do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="9e123-126">Você também pode usar o cmdlet Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="9e123-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="9e123-127">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9e123-127">-ApplicationId</span></span>
<span data-ttu-id="9e123-128">Obtém ou define a ID do aplicativo principal do serviço para acessar o Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="9e123-128">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="9e123-129">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="9e123-129">-AssignedIdentity</span></span>
<span data-ttu-id="9e123-130">Obtém ou define a identidade atribuída.</span><span class="sxs-lookup"><span data-stu-id="9e123-130">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="9e123-131">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e123-131">-AutoscaleConfiguration</span></span>
<span data-ttu-id="9e123-132">Obtém ou define a configuração de dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="9e123-132">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="9e123-133">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="9e123-133">-CertificateFileContents</span></span>
<span data-ttu-id="9e123-134">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e123-134">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9e123-135">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="9e123-135">-CertificateFilePath</span></span>
<span data-ttu-id="9e123-136">Especifica o caminho do arquivo para o certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e123-136">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="9e123-137">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e123-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9e123-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9e123-138">-CertificatePassword</span></span>
<span data-ttu-id="9e123-139">Especifica a senha do certificado que será usado para autenticar como a entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="9e123-139">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="9e123-140">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e123-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9e123-141">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9e123-141">-ClusterName</span></span>
<span data-ttu-id="9e123-142">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-142">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="9e123-143">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="9e123-143">-ClusterSizeInNodes</span></span>
<span data-ttu-id="9e123-144">Especifica o número de nós de trabalho do cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-144">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="9e123-145">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="9e123-145">-ClusterTier</span></span>
<span data-ttu-id="9e123-146">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-146">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="9e123-147">Por padrão, isso é padrão.</span><span class="sxs-lookup"><span data-stu-id="9e123-147">By default, this is Standard.</span></span>
<span data-ttu-id="9e123-148">A camada Premium só pode ser usada com clusters Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="9e123-148">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="9e123-149">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="9e123-149">-ClusterType</span></span>
<span data-ttu-id="9e123-150">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="9e123-150">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="9e123-151">As opções são: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka e RServer</span><span class="sxs-lookup"><span data-stu-id="9e123-151">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="9e123-152">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="9e123-152">-ComponentVersion</span></span>
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

### <span data-ttu-id="9e123-153">-Config</span><span class="sxs-lookup"><span data-stu-id="9e123-153">-Config</span></span>
<span data-ttu-id="9e123-154">Especifica o objeto de cluster a ser usado para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-154">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="9e123-155">Esse objeto pode ser criado usando o cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="9e123-155">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="9e123-156">-Configurações</span><span class="sxs-lookup"><span data-stu-id="9e123-156">-Configurations</span></span>
<span data-ttu-id="9e123-157">Especifica as configurações deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-157">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="9e123-158">Você também pode usar o cmdlet Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="9e123-158">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="9e123-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e123-159">-DefaultProfile</span></span>
<span data-ttu-id="9e123-160">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9e123-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e123-161">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="9e123-161">-DisksPerWorkerNode</span></span>
<span data-ttu-id="9e123-162">Especifica o número de discos para a função de nó de trabalho no cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-162">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="9e123-163">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="9e123-163">-EdgeNodeSize</span></span>
<span data-ttu-id="9e123-164">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="9e123-164">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="9e123-165">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-165">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="9e123-166">Esse parâmetro é válido somente para clusters de RServer.</span><span class="sxs-lookup"><span data-stu-id="9e123-166">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="9e123-167">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="9e123-167">-EnableIDBroker</span></span>
<span data-ttu-id="9e123-168">Habilita o recurso do agente de identidade do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-168">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e123-169">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9e123-169">-EncryptionAlgorithm</span></span>
<span data-ttu-id="9e123-170">Obtém ou define o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="9e123-170">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="9e123-171">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="9e123-171">-EncryptionAtHost</span></span>
<span data-ttu-id="9e123-172">Obtém ou define o sinalizador que indica se a criptografia deve ser habilitada no host ou não.</span><span class="sxs-lookup"><span data-stu-id="9e123-172">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="9e123-173">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="9e123-173">-EncryptionInTransit</span></span>
<span data-ttu-id="9e123-174">Obtém ou define o sinalizador que indica se habilitou a criptografia em trânsito ou não.</span><span class="sxs-lookup"><span data-stu-id="9e123-174">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="9e123-175">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="9e123-175">-EncryptionKeyName</span></span>
<span data-ttu-id="9e123-176">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="9e123-176">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="9e123-177">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="9e123-177">-EncryptionKeyVersion</span></span>
<span data-ttu-id="9e123-178">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="9e123-178">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="9e123-179">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="9e123-179">-EncryptionVaultUri</span></span>
<span data-ttu-id="9e123-180">Obtém ou define o URI do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="9e123-180">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="9e123-181">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="9e123-181">-HeadNodeSize</span></span>
<span data-ttu-id="9e123-182">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="9e123-182">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="9e123-183">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-183">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="9e123-184">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="9e123-184">-HiveMetastore</span></span>
<span data-ttu-id="9e123-185">Especifica o banco de dados SQL para armazenar metadados de Hive.</span><span class="sxs-lookup"><span data-stu-id="9e123-185">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="9e123-186">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="9e123-186">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="9e123-187">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="9e123-187">-HttpCredential</span></span>
<span data-ttu-id="9e123-188">Especifica as credenciais de logon do cluster (HTTP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-188">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="9e123-189">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="9e123-189">-KafkaClientGroupId</span></span>
<span data-ttu-id="9e123-190">Obtém ou define a ID do grupo do cliente para o acesso ao proxy REST Kafka.</span><span class="sxs-lookup"><span data-stu-id="9e123-190">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="9e123-191">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="9e123-191">-KafkaClientGroupName</span></span>
<span data-ttu-id="9e123-192">Obtém ou define o nome do grupo do cliente para o acesso ao proxy REST Kafka.</span><span class="sxs-lookup"><span data-stu-id="9e123-192">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="9e123-193">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="9e123-193">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="9e123-194">Obtém ou define o tamanho do nó de gerenciamento do Kafka.</span><span class="sxs-lookup"><span data-stu-id="9e123-194">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="9e123-195">-Local</span><span class="sxs-lookup"><span data-stu-id="9e123-195">-Location</span></span>
<span data-ttu-id="9e123-196">Especifica o local do cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-196">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="9e123-197">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="9e123-197">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="9e123-198">Obtém ou define a versão do TLS mínima suportada.</span><span class="sxs-lookup"><span data-stu-id="9e123-198">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="9e123-199">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9e123-199">-ObjectId</span></span>
<span data-ttu-id="9e123-200">Especifica a ID do objeto do AD do Azure (um GUID) da entidade de serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-200">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="9e123-201">O cluster vai usar isso quando acessar o Azure data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e123-201">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="9e123-202">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="9e123-202">-OozieMetastore</span></span>
<span data-ttu-id="9e123-203">Especifica o banco de dados SQL para armazenar metadados de Oozie.</span><span class="sxs-lookup"><span data-stu-id="9e123-203">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="9e123-204">Você também pode usar o cmdlet Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="9e123-204">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="9e123-205">-OSType</span><span class="sxs-lookup"><span data-stu-id="9e123-205">-OSType</span></span>
<span data-ttu-id="9e123-206">Especifica o sistema operacional do cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-206">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="9e123-207">Opções são: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="9e123-207">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="9e123-208">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="9e123-208">-RdpAccessExpiry</span></span>
<span data-ttu-id="9e123-209">Especifica a expiração, como um objeto DateTime, para acesso ao protocolo RDP (protocolo de área de trabalho remota) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-209">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="9e123-210">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="9e123-210">-RdpCredential</span></span>
<span data-ttu-id="9e123-211">Especifica as credenciais da área de trabalho remota (RDP) para o cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-211">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="9e123-212">Isso somente para os clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="9e123-212">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="9e123-213">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e123-213">-ResourceGroupName</span></span>
<span data-ttu-id="9e123-214">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9e123-214">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9e123-215">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="9e123-215">-ScriptActions</span></span>
<span data-ttu-id="9e123-216">Especifica as ações de script a serem executadas no cluster ao final da criação do cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-216">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="9e123-217">Você também pode usar Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="9e123-217">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="9e123-218">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="9e123-218">-SecurityProfile</span></span>
<span data-ttu-id="9e123-219">Especifica as propriedades relacionadas à segurança usadas para criar um cluster seguro.</span><span class="sxs-lookup"><span data-stu-id="9e123-219">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="9e123-220">Você também pode usar o cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="9e123-220">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="9e123-221">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="9e123-221">-SshCredential</span></span>
<span data-ttu-id="9e123-222">Especifica a credencial SSH a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="9e123-222">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="9e123-223">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="9e123-223">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="9e123-224">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="9e123-224">-SshPublicKey</span></span>
<span data-ttu-id="9e123-225">Especifica a chave pública a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="9e123-225">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="9e123-226">Isso somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="9e123-226">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="9e123-227">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9e123-227">-StorageAccountKey</span></span>
<span data-ttu-id="9e123-228">Obtém ou define a chave de acesso da conta de armazenamento da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9e123-228">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="9e123-229">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="9e123-229">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="9e123-230">Obtém ou define a identidade gerenciada da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9e123-230">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="9e123-231">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="9e123-231">-StorageAccountResourceId</span></span>
<span data-ttu-id="9e123-232">Obtém ou define a ID do recurso de armazenamento da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9e123-232">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="9e123-233">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9e123-233">-StorageAccountType</span></span>
<span data-ttu-id="9e123-234">Obtém ou define o tipo da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9e123-234">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e123-235">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="9e123-235">-StorageContainer</span></span>
<span data-ttu-id="9e123-236">Obtém ou define o nome do StorageContainer para a conta de armazenamento padrão do Azure</span><span class="sxs-lookup"><span data-stu-id="9e123-236">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="9e123-237">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="9e123-237">-StorageFileSystem</span></span>
<span data-ttu-id="9e123-238">Obtém ou define o sistema de arquivos para a conta padrão do Azure data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="9e123-238">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="9e123-239">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="9e123-239">-StorageRootPath</span></span>
<span data-ttu-id="9e123-240">Obtém ou define o caminho para a raiz do cluster na conta padrão do repositório do data Lake.</span><span class="sxs-lookup"><span data-stu-id="9e123-240">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="9e123-241">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="9e123-241">-SubnetName</span></span>
<span data-ttu-id="9e123-242">Obtém ou define o nome de sub-rede para este cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-242">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="9e123-243">-Versão</span><span class="sxs-lookup"><span data-stu-id="9e123-243">-Version</span></span>
<span data-ttu-id="9e123-244">Especifica a versão HDI do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-244">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="9e123-245">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="9e123-245">-VirtualNetworkId</span></span>
<span data-ttu-id="9e123-246">Especifica a ID da rede virtual para a qual provisionar o cluster.</span><span class="sxs-lookup"><span data-stu-id="9e123-246">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="9e123-247">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="9e123-247">-WorkerNodeSize</span></span>
<span data-ttu-id="9e123-248">Especifica o tamanho da máquina virtual para o nó de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9e123-248">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="9e123-249">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-249">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="9e123-250">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="9e123-250">-ZookeeperNodeSize</span></span>
<span data-ttu-id="9e123-251">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="9e123-251">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="9e123-252">Use Get-AzVMSize para tamanhos de VM aceitáveis e consulte a página de preços do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="9e123-252">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="9e123-253">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="9e123-253">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="9e123-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e123-254">CommonParameters</span></span>
<span data-ttu-id="9e123-255">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e123-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e123-256">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e123-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e123-257">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e123-257">INPUTS</span></span>

### <span data-ttu-id="9e123-258">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9e123-258">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9e123-259">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e123-259">OUTPUTS</span></span>

### <span data-ttu-id="9e123-260">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9e123-260">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="9e123-261">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e123-261">NOTES</span></span>
<span data-ttu-id="9e123-262">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Hadoop, hdinsight, HD, Insight</span><span class="sxs-lookup"><span data-stu-id="9e123-262">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="9e123-263">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e123-263">RELATED LINKS</span></span>

[<span data-ttu-id="9e123-264">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9e123-264">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

