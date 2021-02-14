---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: d4353e49c72f280ee89a1861682ab5d7c3061a9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116786"
---
# <span data-ttu-id="0bd13-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0bd13-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="0bd13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0bd13-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd13-103">Cria um cluster HDInsight do Azure no grupo de recursos especificado para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0bd13-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="0bd13-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bd13-104">SYNTAX</span></span>

### <span data-ttu-id="0bd13-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0bd13-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0bd13-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="0bd13-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd13-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="0bd13-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bd13-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0bd13-108">DESCRIPTION</span></span>
<span data-ttu-id="0bd13-109">O New-AzHDInsightCluster cria um cluster HDInsight do Azure usando os parâmetros especificados ou usando um objeto de configuração criado usando o cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="0bd13-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="0bd13-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0bd13-110">EXAMPLES</span></span>

### <span data-ttu-id="0bd13-111">Exemplo 1: Criar um cluster HDInsight do Azure</span><span class="sxs-lookup"><span data-stu-id="0bd13-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

<span data-ttu-id="0bd13-112">Esse comando cria um cluster na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="0bd13-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="0bd13-113">Exemplo 2: Criar cluster com criptografia de disco de chave gerenciada pelo cliente</span><span class="sxs-lookup"><span data-stu-id="0bd13-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="0bd13-114">Exemplo 3: Criar um cluster HDInsight do Azure que habilita a criptografia em trânsito</span><span class="sxs-lookup"><span data-stu-id="0bd13-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}}
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

### <span data-ttu-id="0bd13-115">Exemplo 4: Criar um cluster HDInsight do Azure com recurso de saída de retransmissão e link particular</span><span class="sxs-lookup"><span data-stu-id="0bd13-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="0bd13-116">Exemplo 5: Criar um cluster HDInsight do Azure que habilita a criptografia no host</span><span class="sxs-lookup"><span data-stu-id="0bd13-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="0bd13-117">Exemplo 6: Criar um cluster HDInsight do Azure que habilita a escala automática.</span><span class="sxs-lookup"><span data-stu-id="0bd13-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="0bd13-118">Exemplo 7: Criar um cluster HDInsight do Azure com o Kafka Rest Proxy.</span><span class="sxs-lookup"><span data-stu-id="0bd13-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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

### <span data-ttu-id="0bd13-119">Exemplo 8: Criar um cluster HDInsight do Azure com armazenamento do Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="0bd13-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="0bd13-120">Exemplo 9: Criar um cluster HDInsight do Azure com o Enterprise Security Package(ESP) e habilitar o HdInsight ID Broker.</span><span class="sxs-lookup"><span data-stu-id="0bd13-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

### <span data-ttu-id="0bd13-121">Exemplo 10: Criar um cluster HDInsight do Azure que habilita o isolamento de computação.</span><span class="sxs-lookup"><span data-stu-id="0bd13-121">Example 10: Create an Azure HDInsight cluster which enables compute isolation.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential
        $workerNodeSize="Standard_E16S_V3" # here is just an example
        $headNodeSize="Standard_E8S_V3"
        $zookeeperNodeSize="Standard_E2S_V3"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -WorkerNodeSize $workerNodeSize `
            -HeadNodeSize $headNodeSize `
            -ZookeeperNodeSize $zookeeperNodeSize `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EnableComputeIsolation `
```

## <span data-ttu-id="0bd13-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bd13-122">PARAMETERS</span></span>

### <span data-ttu-id="0bd13-123">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="0bd13-123">-AadTenantId</span></span>
<span data-ttu-id="0bd13-124">Especifica a ID de Locatário do Azure AD que será usada ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bd13-124">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0bd13-125">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="0bd13-125">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="0bd13-126">Especifica as contas adicionais de Armazenamento do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-126">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="0bd13-127">Você pode usar o cmdlet Add-AzHDInsightStorage alternativa.</span><span class="sxs-lookup"><span data-stu-id="0bd13-127">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="0bd13-128">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="0bd13-128">-AmbariDatabase</span></span>
<span data-ttu-id="0bd13-129">Obtém ou define o banco de dados para ambari.</span><span class="sxs-lookup"><span data-stu-id="0bd13-129">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="0bd13-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0bd13-130">-ApplicationId</span></span>
<span data-ttu-id="0bd13-131">Obtém ou define a ID do Aplicativo Principal de Serviço para acessar o Lago de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd13-131">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="0bd13-132">-AsignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0bd13-132">-AssignedIdentity</span></span>
<span data-ttu-id="0bd13-133">Obtém ou define a identidade atribuída.</span><span class="sxs-lookup"><span data-stu-id="0bd13-133">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="0bd13-134">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="0bd13-134">-AutoscaleConfiguration</span></span>
<span data-ttu-id="0bd13-135">Obtém ou define a configuração de escala automática</span><span class="sxs-lookup"><span data-stu-id="0bd13-135">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="0bd13-136">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="0bd13-136">-CertificateFileContents</span></span>
<span data-ttu-id="0bd13-137">Especifica o conteúdo do arquivo do certificado que será usado ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bd13-137">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0bd13-138">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="0bd13-138">-CertificateFilePath</span></span>
<span data-ttu-id="0bd13-139">Especifica o caminho do arquivo para o certificado que será usado para autenticar como Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="0bd13-139">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0bd13-140">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bd13-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0bd13-141">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="0bd13-141">-CertificatePassword</span></span>
<span data-ttu-id="0bd13-142">Especifica a senha do certificado que será usado para autenticar como Entidade de Serviço.</span><span class="sxs-lookup"><span data-stu-id="0bd13-142">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="0bd13-143">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bd13-143">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0bd13-144">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0bd13-144">-ClusterName</span></span>
<span data-ttu-id="0bd13-145">Especifica o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-145">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="0bd13-146">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="0bd13-146">-ClusterSizeInNodes</span></span>
<span data-ttu-id="0bd13-147">Especifica o número de nós de Trabalhador para o cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-147">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="0bd13-148">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="0bd13-148">-ClusterTier</span></span>
<span data-ttu-id="0bd13-149">Especifica a camada de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-149">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="0bd13-150">Por padrão, isso é Padrão.</span><span class="sxs-lookup"><span data-stu-id="0bd13-150">By default, this is Standard.</span></span>
<span data-ttu-id="0bd13-151">O nível Premium só pode ser usado com clusters do Linux e permite o uso de alguns novos recursos.</span><span class="sxs-lookup"><span data-stu-id="0bd13-151">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="0bd13-152">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="0bd13-152">-ClusterType</span></span>
<span data-ttu-id="0bd13-153">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="0bd13-153">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="0bd13-154">As opções são: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka e RServer</span><span class="sxs-lookup"><span data-stu-id="0bd13-154">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="0bd13-155">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="0bd13-155">-ComponentVersion</span></span>
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

### <span data-ttu-id="0bd13-156">-ComputeIsolationHostSku</span><span class="sxs-lookup"><span data-stu-id="0bd13-156">-ComputeIsolationHostSku</span></span>
<span data-ttu-id="0bd13-157">Obtém ou define a SKU de host dedicada para isolamento de computação.</span><span class="sxs-lookup"><span data-stu-id="0bd13-157">Gets or sets the dedicated host sku for compute isolation.</span></span>

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

### <span data-ttu-id="0bd13-158">-Configuração</span><span class="sxs-lookup"><span data-stu-id="0bd13-158">-Config</span></span>
<span data-ttu-id="0bd13-159">Especifica o objeto de cluster a ser usado para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-159">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="0bd13-160">Esse objeto pode ser criado usando o cmdlet New-AzHDInsightClusterConfig dados.</span><span class="sxs-lookup"><span data-stu-id="0bd13-160">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="0bd13-161">-Configurações</span><span class="sxs-lookup"><span data-stu-id="0bd13-161">-Configurations</span></span>
<span data-ttu-id="0bd13-162">Especifica as configurações deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-162">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="0bd13-163">Você pode usar o cmdlet Add-AzHDInsightConfigValues alternativa.</span><span class="sxs-lookup"><span data-stu-id="0bd13-163">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="0bd13-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd13-164">-DefaultProfile</span></span>
<span data-ttu-id="0bd13-165">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="0bd13-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bd13-166">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="0bd13-166">-DisksPerWorkerNode</span></span>
<span data-ttu-id="0bd13-167">Especifica o número de discos para a função de nó do trabalhador no cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-167">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="0bd13-168">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="0bd13-168">-EdgeNodeSize</span></span>
<span data-ttu-id="0bd13-169">Especifica o tamanho da máquina virtual para o nó de borda.</span><span class="sxs-lookup"><span data-stu-id="0bd13-169">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="0bd13-170">Use Get-AzVMSize para tamanhos VM aceitáveis e veja a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="0bd13-171">Este parâmetro é válido somente para clusters RServer.</span><span class="sxs-lookup"><span data-stu-id="0bd13-171">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="0bd13-172">-EnableComputeIsolation</span><span class="sxs-lookup"><span data-stu-id="0bd13-172">-EnableComputeIsolation</span></span>
<span data-ttu-id="0bd13-173">Habilita o recurso de isolamento de computação HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-173">Enables HDInsight compute isolation feature.</span></span>

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

### <span data-ttu-id="0bd13-174">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="0bd13-174">-EnableIDBroker</span></span>
<span data-ttu-id="0bd13-175">Habilita o recurso HDInsight Identity Broker.</span><span class="sxs-lookup"><span data-stu-id="0bd13-175">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="0bd13-176">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0bd13-176">-EncryptionAlgorithm</span></span>
<span data-ttu-id="0bd13-177">Obtém ou define o algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="0bd13-177">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="0bd13-178">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="0bd13-178">-EncryptionAtHost</span></span>
<span data-ttu-id="0bd13-179">Obtém ou define o sinalizador que indica se habilitar a criptografia no host ou não.</span><span class="sxs-lookup"><span data-stu-id="0bd13-179">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="0bd13-180">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="0bd13-180">-EncryptionInTransit</span></span>
<span data-ttu-id="0bd13-181">Obtém ou define o sinalizador que indica se habilitar a criptografia em trânsito ou não.</span><span class="sxs-lookup"><span data-stu-id="0bd13-181">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="0bd13-182">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="0bd13-182">-EncryptionKeyName</span></span>
<span data-ttu-id="0bd13-183">Obtém ou define o nome da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="0bd13-183">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="0bd13-184">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="0bd13-184">-EncryptionKeyVersion</span></span>
<span data-ttu-id="0bd13-185">Obtém ou define a versão da chave de criptografia.</span><span class="sxs-lookup"><span data-stu-id="0bd13-185">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="0bd13-186">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="0bd13-186">-EncryptionVaultUri</span></span>
<span data-ttu-id="0bd13-187">Obtém ou define o uri do cofre de criptografia.</span><span class="sxs-lookup"><span data-stu-id="0bd13-187">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="0bd13-188">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="0bd13-188">-HeadNodeSize</span></span>
<span data-ttu-id="0bd13-189">Especifica o tamanho da máquina virtual para o nó De cabeça.</span><span class="sxs-lookup"><span data-stu-id="0bd13-189">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="0bd13-190">Use Get-AzVMSize para tamanhos VM aceitáveis e veja a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-190">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="0bd13-191">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="0bd13-191">-HiveMetastore</span></span>
<span data-ttu-id="0bd13-192">Especifica o banco de dados SQL para armazenar metadados de Colmeia.</span><span class="sxs-lookup"><span data-stu-id="0bd13-192">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="0bd13-193">Você pode usar o cmdlet Add-AzHDInsightMetastore alternativa.</span><span class="sxs-lookup"><span data-stu-id="0bd13-193">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="0bd13-194">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="0bd13-194">-HttpCredential</span></span>
<span data-ttu-id="0bd13-195">Especifica as credenciais de logon de cluster (HTTP) do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-195">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="0bd13-196">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="0bd13-196">-KafkaClientGroupId</span></span>
<span data-ttu-id="0bd13-197">Obtém ou define a ID do grupo cliente para o acesso de Proxy de Repouso do Kafka.</span><span class="sxs-lookup"><span data-stu-id="0bd13-197">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="0bd13-198">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd13-198">-KafkaClientGroupName</span></span>
<span data-ttu-id="0bd13-199">Obtém ou define o nome do grupo do cliente para o acesso de Proxy do Rest Kafka.</span><span class="sxs-lookup"><span data-stu-id="0bd13-199">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="0bd13-200">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="0bd13-200">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="0bd13-201">Obtém ou define o tamanho do Nó de Gerenciamento kafka.</span><span class="sxs-lookup"><span data-stu-id="0bd13-201">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="0bd13-202">-Local</span><span class="sxs-lookup"><span data-stu-id="0bd13-202">-Location</span></span>
<span data-ttu-id="0bd13-203">Especifica o local do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-203">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="0bd13-204">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="0bd13-204">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="0bd13-205">Obtém ou define a versão TLS mínima com suporte.</span><span class="sxs-lookup"><span data-stu-id="0bd13-205">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="0bd13-206">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0bd13-206">-ObjectId</span></span>
<span data-ttu-id="0bd13-207">Especifica a ID de objeto do Azure AD (um GUID) da Entidade de Serviço do Azure AD que representa o cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-207">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="0bd13-208">O cluster usará isso ao acessar o Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bd13-208">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="0bd13-209">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="0bd13-209">-OozieMetastore</span></span>
<span data-ttu-id="0bd13-210">Especifica o banco de dados SQL para armazenar metadados Oozie.</span><span class="sxs-lookup"><span data-stu-id="0bd13-210">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="0bd13-211">Você pode usar o cmdlet Add-AzHDInsightMetastore alternativa.</span><span class="sxs-lookup"><span data-stu-id="0bd13-211">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="0bd13-212">-OSType</span><span class="sxs-lookup"><span data-stu-id="0bd13-212">-OSType</span></span>
<span data-ttu-id="0bd13-213">Especifica o sistema operacional do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-213">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="0bd13-214">As opções são: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="0bd13-214">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="0bd13-215">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="0bd13-215">-PrivateLink</span></span>
<span data-ttu-id="0bd13-216">Obtém ou define o tipo de link particular.</span><span class="sxs-lookup"><span data-stu-id="0bd13-216">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bd13-217">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="0bd13-217">-RdpAccessExpiry</span></span>
<span data-ttu-id="0bd13-218">Especifica a expiração, como um objeto DateTime, para acesso RDP (Remote Desktop Protocol) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-218">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="0bd13-219">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="0bd13-219">-RdpCredential</span></span>
<span data-ttu-id="0bd13-220">Especifica as credenciais de Área de Trabalho Remota (RDP) do cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-220">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="0bd13-221">Isso se trata apenas de clusters do Windows.</span><span class="sxs-lookup"><span data-stu-id="0bd13-221">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="0bd13-222">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd13-222">-ResourceGroupName</span></span>
<span data-ttu-id="0bd13-223">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0bd13-223">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0bd13-224">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="0bd13-224">-ResourceProviderConnection</span></span>
<span data-ttu-id="0bd13-225">Obtém ou define o tipo de conexão do provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="0bd13-225">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bd13-226">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="0bd13-226">-ScriptActions</span></span>
<span data-ttu-id="0bd13-227">Especifica as ações de script a ser executado no cluster no final da criação de cluster.</span><span class="sxs-lookup"><span data-stu-id="0bd13-227">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="0bd13-228">Você pode usar o Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="0bd13-228">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="0bd13-229">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="0bd13-229">-SecurityProfile</span></span>
<span data-ttu-id="0bd13-230">Especifica as propriedades relacionadas à segurança usadas para criar um cluster seguro.</span><span class="sxs-lookup"><span data-stu-id="0bd13-230">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="0bd13-231">Você pode usar o cmdlet Add-AzHDInsightSecurityProfile alternativa.</span><span class="sxs-lookup"><span data-stu-id="0bd13-231">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="0bd13-232">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="0bd13-232">-SshCredential</span></span>
<span data-ttu-id="0bd13-233">Especifica a credencial SSH a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="0bd13-233">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="0bd13-234">Isso se trata apenas de clusters do Linux.</span><span class="sxs-lookup"><span data-stu-id="0bd13-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="0bd13-235">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="0bd13-235">-SshPublicKey</span></span>
<span data-ttu-id="0bd13-236">Especifica a chave pública a ser usada para conexões SSH.</span><span class="sxs-lookup"><span data-stu-id="0bd13-236">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="0bd13-237">Isso se trata apenas de clusters do Linux.</span><span class="sxs-lookup"><span data-stu-id="0bd13-237">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="0bd13-238">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0bd13-238">-StorageAccountKey</span></span>
<span data-ttu-id="0bd13-239">Obtém ou define a Chave de Acesso à Conta de Armazenamento para a Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0bd13-239">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="0bd13-240">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0bd13-240">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="0bd13-241">Obtém ou define a identidade gerenciada da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0bd13-241">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="0bd13-242">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="0bd13-242">-StorageAccountResourceId</span></span>
<span data-ttu-id="0bd13-243">Obtém ou define a ID do Recurso de Armazenamento para a Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0bd13-243">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="0bd13-244">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="0bd13-244">-StorageAccountType</span></span>
<span data-ttu-id="0bd13-245">Obtém ou define o tipo da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0bd13-245">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="0bd13-246">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="0bd13-246">-StorageContainer</span></span>
<span data-ttu-id="0bd13-247">Obtém ou define o nome de StorageContainer para a Conta de Armazenamento padrão do Azure</span><span class="sxs-lookup"><span data-stu-id="0bd13-247">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="0bd13-248">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="0bd13-248">-StorageFileSystem</span></span>
<span data-ttu-id="0bd13-249">Obtém ou define o sistema de arquivos para a conta padrão do Azure Data Lake Storage Gen2.</span><span class="sxs-lookup"><span data-stu-id="0bd13-249">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="0bd13-250">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="0bd13-250">-StorageRootPath</span></span>
<span data-ttu-id="0bd13-251">Obtém ou define o caminho para a raiz do cluster na Conta padrão do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0bd13-251">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="0bd13-252">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="0bd13-252">-SubnetName</span></span>
<span data-ttu-id="0bd13-253">Obtém ou define o nome da sub-rede para esse cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-253">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="0bd13-254">-Versão</span><span class="sxs-lookup"><span data-stu-id="0bd13-254">-Version</span></span>
<span data-ttu-id="0bd13-255">Especifica a versão HDI do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-255">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="0bd13-256">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="0bd13-256">-VirtualNetworkId</span></span>
<span data-ttu-id="0bd13-257">Especifica a ID da rede virtual na qual o cluster deve ser provisionado.</span><span class="sxs-lookup"><span data-stu-id="0bd13-257">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="0bd13-258">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="0bd13-258">-WorkerNodeSize</span></span>
<span data-ttu-id="0bd13-259">Especifica o tamanho da máquina virtual para o nó Trabalhador.</span><span class="sxs-lookup"><span data-stu-id="0bd13-259">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="0bd13-260">Use Get-AzVMSize para tamanhos VM aceitáveis e veja a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-260">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="0bd13-261">-DesbotadorNodeSize</span><span class="sxs-lookup"><span data-stu-id="0bd13-261">-ZookeeperNodeSize</span></span>
<span data-ttu-id="0bd13-262">Especifica o tamanho da máquina virtual para o nó Desbotador.</span><span class="sxs-lookup"><span data-stu-id="0bd13-262">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="0bd13-263">Use Get-AzVMSize para tamanhos VM aceitáveis e veja a página de preços da HDInsight.</span><span class="sxs-lookup"><span data-stu-id="0bd13-263">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="0bd13-264">Este parâmetro só é válido para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="0bd13-264">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="0bd13-265">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd13-265">CommonParameters</span></span>
<span data-ttu-id="0bd13-266">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd13-266">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd13-267">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0bd13-267">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd13-268">Entradas</span><span class="sxs-lookup"><span data-stu-id="0bd13-268">INPUTS</span></span>

### <span data-ttu-id="0bd13-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="0bd13-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="0bd13-270">Saídas</span><span class="sxs-lookup"><span data-stu-id="0bd13-270">OUTPUTS</span></span>

### <span data-ttu-id="0bd13-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="0bd13-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="0bd13-272">Notas</span><span class="sxs-lookup"><span data-stu-id="0bd13-272">NOTES</span></span>
<span data-ttu-id="0bd13-273">Palavras-chave: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="0bd13-273">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="0bd13-274">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bd13-274">RELATED LINKS</span></span>

[<span data-ttu-id="0bd13-275">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="0bd13-275">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

