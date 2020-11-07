---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: FF8AA7DE-1E0F-4F5B-95F6-7820AAF789F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: c36931af0b6927ef4fee26b9f8ade7db77d17db2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945920"
---
# <span data-ttu-id="64511-101">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="64511-101">New-AzureHDInsightClusterConfig</span></span>

## <span data-ttu-id="64511-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64511-102">SYNOPSIS</span></span>
<span data-ttu-id="64511-103">Cria uma configuração de cluster HDInsight não persistente.</span><span class="sxs-lookup"><span data-stu-id="64511-103">Creates a non-persisted HDInsight cluster configuration.</span></span>

## <span data-ttu-id="64511-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64511-104">SYNTAX</span></span>

```
New-AzureHDInsightClusterConfig -ClusterSizeInNodes <Int32> [-HeadNodeVMSize <String>]
 [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>] [-DataNodeVMSize <String>]
 [-ZookeeperNodeVMSize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64511-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64511-105">DESCRIPTION</span></span>
<span data-ttu-id="64511-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="64511-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="64511-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="64511-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="64511-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="64511-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="64511-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="64511-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="64511-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="64511-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="64511-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="64511-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="64511-112">O cmdlet **New-AzureHDInsightClusterConfig** cria uma configuração de cluster do Azure HDInsight não persistente.</span><span class="sxs-lookup"><span data-stu-id="64511-112">The **New-AzureHDInsightClusterConfig** cmdlet creates a non-persisted Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="64511-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64511-113">EXAMPLES</span></span>

### <span data-ttu-id="64511-114">Exemplo 1: criar uma configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="64511-114">Example 1: Create a cluster configuration</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyBlobStorage.blob.core.windows.net -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.widows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubID -Credential $Creds
```

<span data-ttu-id="64511-115">O primeiro comando usa o cmdlet **Get-AzureSubscription** para obter a ID de assinatura atual e, em seguida, armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="64511-115">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="64511-116">O segundo e terceiro comandos usam o cmdlet **Get-AzureStorageKey** para obter as chaves de armazenamento principal para MyBlobStorage e MySecondBlobStorage e, em seguida, armazenar as chaves nas variáveis $Key 1 e $Key 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="64511-116">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="64511-117">Os comandos quarto, quinto e sexto usam o cmdlet **Get-Credential** para obter credenciais para a assinatura atual e para Oozie e Hive e, em seguida, armazenar as credenciais em variáveis.</span><span class="sxs-lookup"><span data-stu-id="64511-117">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="64511-118">O comando final executa uma sequência de operações usando estes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="64511-118">The final command performs a sequence of operations by using these cmdlets:</span></span> 

- <span data-ttu-id="64511-119">**New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="64511-119">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="64511-120">**Set-AzureHDInsightDefaultStorage** para definir a conta de armazenamento padrão para a configuração para MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="64511-120">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="64511-121">**Add-AzureHDInsightStorage** para adicionar uma segunda conta de armazenamento chamada MySecondBlobStorage.blob.Core.Windows.net à configuração.</span><span class="sxs-lookup"><span data-stu-id="64511-121">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="64511-122">**Add-AzureHDInsightMetastore** para adicionar um metastore para Oozie e um metastore para Hive à configuração.</span><span class="sxs-lookup"><span data-stu-id="64511-122">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="64511-123">**New-AzureHDInsightCluster** para criar um cluster HDInsight com a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="64511-123">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="64511-124">OS</span><span class="sxs-lookup"><span data-stu-id="64511-124">PARAMETERS</span></span>

### <span data-ttu-id="64511-125">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="64511-125">-ClusterSizeInNodes</span></span>
<span data-ttu-id="64511-126">Especifica o número de nós de dados a serem criados para um cluster.</span><span class="sxs-lookup"><span data-stu-id="64511-126">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64511-127">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="64511-127">-ClusterType</span></span>
<span data-ttu-id="64511-128">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="64511-128">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64511-129">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="64511-129">-DataNodeVMSize</span></span>
<span data-ttu-id="64511-130">Especifica o tamanho da máquina virtual para o nó de dados.</span><span class="sxs-lookup"><span data-stu-id="64511-130">Specifies the size of the virtual machine for the data node.</span></span>

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

### <span data-ttu-id="64511-131">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="64511-131">-HeadNodeVMSize</span></span>
<span data-ttu-id="64511-132">Especifica o tamanho da máquina virtual do nó principal do cluster.</span><span class="sxs-lookup"><span data-stu-id="64511-132">Specifies the virtual machine size of the head node for the cluster.</span></span>

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

### <span data-ttu-id="64511-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="64511-133">-Profile</span></span>
<span data-ttu-id="64511-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="64511-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64511-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="64511-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64511-136">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="64511-136">-SubnetName</span></span>
<span data-ttu-id="64511-137">Especifica o nome de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="64511-137">Specifies the name of a subnet.</span></span>

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

### <span data-ttu-id="64511-138">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="64511-138">-VirtualNetworkId</span></span>
<span data-ttu-id="64511-139">Especifica a ID da rede virtual para a qual provisionar o cluster.</span><span class="sxs-lookup"><span data-stu-id="64511-139">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="64511-140">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="64511-140">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="64511-141">Especifica o tamanho da máquina virtual para o nó administradora de um cluster HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="64511-141">Specifies the size of the virtual machine for the ZooKeeper node for an HBase or Storm cluster.</span></span>

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

### <span data-ttu-id="64511-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64511-142">CommonParameters</span></span>
<span data-ttu-id="64511-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64511-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64511-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64511-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64511-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64511-145">INPUTS</span></span>

## <span data-ttu-id="64511-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64511-146">OUTPUTS</span></span>

## <span data-ttu-id="64511-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64511-147">NOTES</span></span>

## <span data-ttu-id="64511-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64511-148">RELATED LINKS</span></span>

[<span data-ttu-id="64511-149">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="64511-149">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="64511-150">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="64511-150">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="64511-151">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="64511-151">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="64511-152">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="64511-152">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)


