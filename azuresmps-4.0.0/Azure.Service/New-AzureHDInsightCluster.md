---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 3EDD612F-AC5D-4D4D-BB14-2FB8DE5EDCCE
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4652cb1b30717b5ea11d596646dc43e2a5ec4a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945923"
---
# <span data-ttu-id="c4a35-101">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4a35-101">New-AzureHDInsightCluster</span></span>

## <span data-ttu-id="c4a35-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4a35-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a35-103">Cria um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-103">Creates an HDInsight cluster.</span></span>

## <span data-ttu-id="c4a35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4a35-104">SYNTAX</span></span>

### <span data-ttu-id="c4a35-105">Cluster por config (com credencial de assinatura específica) (padrão)</span><span class="sxs-lookup"><span data-stu-id="c4a35-105">Cluster By Config (with Specific Subscription Credential) (Default)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -Config <AzureHDInsightConfig> -Credential <PSCredential> [-EndPoint <Uri>] [-IgnoreSslErrors <Boolean>]
 -Location <String> -Name <String> [-Subscription <String>] [-Version <String>] [-OSType <OSType>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c4a35-106">Cluster por nome (com credencial de assinatura específica)</span><span class="sxs-lookup"><span data-stu-id="c4a35-106">Cluster By Name (with Specific Subscription Credential)</span></span>
```
New-AzureHDInsightCluster [-Certificate <X509Certificate2>] [-HostedService <String>]
 -ClusterSizeInNodes <Int32> -Credential <PSCredential> -DefaultStorageAccountKey <String>
 -DefaultStorageAccountName <String> -DefaultStorageContainerName <String> [-EndPoint <Uri>]
 [-IgnoreSslErrors <Boolean>] -Location <String> -Name <String> [-Subscription <String>] [-Version <String>]
 [-HeadNodeVMSize <String>] [-ClusterType <ClusterType>] [-VirtualNetworkId <String>] [-SubnetName <String>]
 [-DataNodeVMSize <String>] [-ZookeeperNodeVMSize <String>] [-OSType <OSType>] [-SshCredential <PSCredential>]
 [-SshPublicKey <String>] [-RdpCredential <PSCredential>] [-RdpAccessExpiry <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4a35-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4a35-107">DESCRIPTION</span></span>
<span data-ttu-id="c4a35-108">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="c4a35-108">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="c4a35-109">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="c4a35-109">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="c4a35-110">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-110">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="c4a35-111">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="c4a35-111">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="c4a35-112">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="c4a35-112">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="c4a35-113">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="c4a35-113">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="c4a35-114">O cmdlet **New-AzureHDInsightCluster** cria um cluster do Azure HDInsight usando os parâmetros especificados ou usando um objeto de configuração que é criado usando o cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="c4a35-114">The **New-AzureHDInsightCluster** cmdlet creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

## <span data-ttu-id="c4a35-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4a35-115">EXAMPLES</span></span>

### <span data-ttu-id="c4a35-116">Exemplo 1: criar um cluster HDInsight</span><span class="sxs-lookup"><span data-stu-id="c4a35-116">Example 1: Create an HDInsight cluster</span></span>
```
PS C:\>$SubId = (Get-AzureSubscription -Current).SubscriptionId
PS C:\> $Key1 = Get-AzureStorageKey -StorageAccountName "MyBlobStorage" | %{ $_.Primary }
PS C:\> $Key2 = Get-AzureStorageKey -StorageAccountName "MySecondBlobStorage" | %{ $_.Primary }
PS C:\> $Creds = Get-Credential
PS C:\> $OozieCreds = Get-Credential
PS C:\> $HiveCreds = Get-Credential 
PS C:\> New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
    | Set-AzureHDInsightDefaultStorage -StorageAccountName "MyBlobStorage.blob.core.windows.net" -StorageAccountKey $Key1 -StorageContainerName "MyContainer" 
    | Add-AzureHDInsightStorage -StorageAccountName "MySecondBlobStorage.blob.core.windows.net" -StorageAccountKey $Key2 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyOozieDatabaseName" -Credential $OozieCreds -MetastoreType OozieMetastore 
    | Add-AzureHDInsightMetastore -SqlAzureServerName "MySqlServer.database.windows.net" -DatabaseName "MyHiveDatabaseName" -Credential $HiveCreds -MetastoreType HiveMetastore 
    | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds
```

<span data-ttu-id="c4a35-117">Este exemplo cria um cluster HDInsight para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="c4a35-117">This example creates an HDInsight cluster for the current subscription.</span></span>

<span data-ttu-id="c4a35-118">O primeiro comando usa o cmdlet **Get-AzureSubscription** para obter a ID de assinatura atual e, em seguida, armazena-a na variável $SubId.</span><span class="sxs-lookup"><span data-stu-id="c4a35-118">The first command uses the **Get-AzureSubscription** cmdlet to get the current subscription ID, and then stores it in the $SubId variable.</span></span>

<span data-ttu-id="c4a35-119">O segundo e terceiro comandos usam o cmdlet **Get-AzureStorageKey** para obter as chaves de armazenamento principal para MyBlobStorage e MySecondBlobStorage e, em seguida, armazenar as chaves nas variáveis $Key 1 e $Key 2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="c4a35-119">The second and third commands use the **Get-AzureStorageKey** cmdlet to get the primary storage keys for MyBlobStorage and MySecondBlobStorage, and then store the keys in the $Key1 and $Key2 variables, respectively.</span></span>

<span data-ttu-id="c4a35-120">Os comandos quarto, quinto e sexto usam o cmdlet **Get-Credential** para obter credenciais para a assinatura atual e para Oozie e Hive e, em seguida, armazenar as credenciais em variáveis.</span><span class="sxs-lookup"><span data-stu-id="c4a35-120">The fourth, fifth, and sixth commands use the **Get-Credential** cmdlet to get credentials for the current subscription and for Oozie and Hive, and then store the credentials in variables.</span></span>

<span data-ttu-id="c4a35-121">O comando final executa uma sequência de operações usando estes cmdlets:</span><span class="sxs-lookup"><span data-stu-id="c4a35-121">The final command performs a sequence of operations by using these cmdlets:</span></span>

- <span data-ttu-id="c4a35-122">**New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-122">**New-AzureHDInsightClusterConfig** to create an HDInsight cluster configuration.</span></span>
- <span data-ttu-id="c4a35-123">**Set-AzureHDInsightDefaultStorage** para definir a conta de armazenamento padrão para a configuração para MyBlobStorage.blob.Core.Windows.net.</span><span class="sxs-lookup"><span data-stu-id="c4a35-123">**Set-AzureHDInsightDefaultStorage** to set the default storage account for the configuration to MyBlobStorage.blob.core.windows.net.</span></span>
- <span data-ttu-id="c4a35-124">**Add-AzureHDInsightStorage** para adicionar uma segunda conta de armazenamento chamada MySecondBlobStorage.blob.Core.Windows.net à configuração.</span><span class="sxs-lookup"><span data-stu-id="c4a35-124">**Add-AzureHDInsightStorage** to add a second storage account named MySecondBlobStorage.blob.core.windows.net to the configuration.</span></span>
- <span data-ttu-id="c4a35-125">**Add-AzureHDInsightMetastore** para adicionar um metastore para Oozie e um metastore para Hive à configuração.</span><span class="sxs-lookup"><span data-stu-id="c4a35-125">**Add-AzureHDInsightMetastore** to add a metastore for Oozie and a metastore for Hive to the configuration.</span></span>
- <span data-ttu-id="c4a35-126">**New-AzureHDInsightCluster** para criar um cluster HDInsight com a nova configuração.</span><span class="sxs-lookup"><span data-stu-id="c4a35-126">**New-AzureHDInsightCluster** to create an HDInsight cluster with the new configuration.</span></span>

## <span data-ttu-id="c4a35-127">OS</span><span class="sxs-lookup"><span data-stu-id="c4a35-127">PARAMETERS</span></span>

### <span data-ttu-id="c4a35-128">-Certificado</span><span class="sxs-lookup"><span data-stu-id="c4a35-128">-Certificate</span></span>
<span data-ttu-id="c4a35-129">Especifica o certificado de gerenciamento para uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a35-129">Specifies the management certificate for an Azure subscription.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: (All)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-130">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="c4a35-130">-ClusterSizeInNodes</span></span>
<span data-ttu-id="c4a35-131">Especifica o número de nós de dados a serem criados para um cluster.</span><span class="sxs-lookup"><span data-stu-id="c4a35-131">Specifies the number of data nodes to create for a cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: Nodes, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-132">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="c4a35-132">-ClusterType</span></span>
<span data-ttu-id="c4a35-133">Especifica o tipo de cluster a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c4a35-133">Specifies the type of cluster to create.</span></span>

```yaml
Type: ClusterType
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-134">-Config</span><span class="sxs-lookup"><span data-stu-id="c4a35-134">-Config</span></span>
<span data-ttu-id="c4a35-135">Especifica um objeto de configuração que é criado usando o cmdlet **New-AzureHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="c4a35-135">Specifies a configuration object that is created by using the **New-AzureHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="c4a35-136">-Credential</span></span>
<span data-ttu-id="c4a35-137">Especifica as credenciais de usuário para o HDInsight usar para a conta padrão que é usada para acessar remotamente um cluster Hadoop.</span><span class="sxs-lookup"><span data-stu-id="c4a35-137">Specifies the user credentials for HDInsight to use for the default account that is used to remotely access a Hadoop cluster.</span></span>
<span data-ttu-id="c4a35-138">Essas credenciais são diferentes das credenciais de assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="c4a35-138">These credentials are distinct from the subscription credentials of the user.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Cred

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-139">-DataNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="c4a35-139">-DataNodeVMSize</span></span>
<span data-ttu-id="c4a35-140">Especifica o tamanho da máquina virtual para o nó de dados.</span><span class="sxs-lookup"><span data-stu-id="c4a35-140">Specifies the size of the virtual machine for the data node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c4a35-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c4a35-142">Especifica a chave de conta para a conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="c4a35-142">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c4a35-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c4a35-144">Especifica o nome da conta de armazenamento padrão que o cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="c4a35-144">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-145">-DefaultStorageContainerName</span><span class="sxs-lookup"><span data-stu-id="c4a35-145">-DefaultStorageContainerName</span></span>
<span data-ttu-id="c4a35-146">Especifica o nome do contêiner padrão na conta de armazenamento padrão do Azure que um cluster HDInsight usa.</span><span class="sxs-lookup"><span data-stu-id="c4a35-146">Specifies the name of the default container in the default Azure storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: StorageContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-147">-Ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="c4a35-147">-EndPoint</span></span>
<span data-ttu-id="c4a35-148">Especifica o ponto de extremidade a ser usado para se conectar ao Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a35-148">Specifies the endpoint to use to connect to Azure.</span></span>
<span data-ttu-id="c4a35-149">Se você não especificar esse parâmetro, esse cmdlet usará o ponto de extremidade padrão.</span><span class="sxs-lookup"><span data-stu-id="c4a35-149">If you do not specify this parameter, this cmdlet uses the default endpoint.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-150">-HeadNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="c4a35-150">-HeadNodeVMSize</span></span>
<span data-ttu-id="c4a35-151">Especifica o tamanho da máquina virtual para o nó principal.</span><span class="sxs-lookup"><span data-stu-id="c4a35-151">Specifies the size of the virtual machine for the head node.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-152">-HostedService</span><span class="sxs-lookup"><span data-stu-id="c4a35-152">-HostedService</span></span>
<span data-ttu-id="c4a35-153">Especifica o namespace de um serviço HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-153">Specifies the namespace of an HDInsight service.</span></span>
<span data-ttu-id="c4a35-154">Se você não especificar esse parâmetro, esse cmdlet usará o namespace padrão.</span><span class="sxs-lookup"><span data-stu-id="c4a35-154">If you do not specify this parameter, this cmdlet uses the default namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-155">-IgnoreSslErrors</span><span class="sxs-lookup"><span data-stu-id="c4a35-155">-IgnoreSslErrors</span></span>
<span data-ttu-id="c4a35-156">Indica se os erros SSL (Secure Sockets Layer) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="c4a35-156">Indicates whether Secure Sockets Layer (SSL) errors are ignored.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-157">-Local</span><span class="sxs-lookup"><span data-stu-id="c4a35-157">-Location</span></span>
<span data-ttu-id="c4a35-158">Especifica a região na qual criar um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-158">Specifies the region in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Loc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-159">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4a35-159">-Name</span></span>
<span data-ttu-id="c4a35-160">Especifica o nome do cluster do Azure HDInsight a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c4a35-160">Specifies the name of the Azure HDInsight cluster to create.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Config (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: ClusterName, DnsName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-161">-OSType</span><span class="sxs-lookup"><span data-stu-id="c4a35-161">-OSType</span></span>
<span data-ttu-id="c4a35-162">Especifica o sistema operacional para um cluster.</span><span class="sxs-lookup"><span data-stu-id="c4a35-162">Specifies the operating system for a cluster.</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-163">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c4a35-163">-Profile</span></span>
<span data-ttu-id="c4a35-164">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c4a35-164">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c4a35-165">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c4a35-165">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c4a35-166">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="c4a35-166">-RdpAccessExpiry</span></span>
<span data-ttu-id="c4a35-167">Especifica a expiração, como um objeto **DateTime** , para acesso ao protocolo RDP (protocolo de área de trabalho remota) a um cluster.</span><span class="sxs-lookup"><span data-stu-id="c4a35-167">Specifies the expiration, as a **DateTime** object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="c4a35-168">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="c4a35-168">-RdpCredential</span></span>
<span data-ttu-id="c4a35-169">Especifica as credenciais para o acesso RDP a um cluster.</span><span class="sxs-lookup"><span data-stu-id="c4a35-169">Specifies the credentials for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="c4a35-170">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="c4a35-170">-SshCredential</span></span>
<span data-ttu-id="c4a35-171">Especifica o nome de usuário e a senha do Secure Shell (SSH) para o cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-171">Specifies the Secure Shell (SSH) user name and password for the HDInsight cluster.</span></span>
<span data-ttu-id="c4a35-172">Esse parâmetro é válido somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="c4a35-172">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="c4a35-173">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="c4a35-173">-SshPublicKey</span></span>
<span data-ttu-id="c4a35-174">Especifica a chave pública SSH para um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-174">Specifies the SSH public key for an HDInsight cluster.</span></span>
<span data-ttu-id="c4a35-175">Esse parâmetro é válido somente para clusters Linux.</span><span class="sxs-lookup"><span data-stu-id="c4a35-175">This parameter is valid only for Linux clusters.</span></span>

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

### <span data-ttu-id="c4a35-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="c4a35-176">-SubnetName</span></span>
<span data-ttu-id="c4a35-177">Especifica o nome de uma sub-rede.</span><span class="sxs-lookup"><span data-stu-id="c4a35-177">Specifies the name of a subnet.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-178">-Assinatura</span><span class="sxs-lookup"><span data-stu-id="c4a35-178">-Subscription</span></span>
<span data-ttu-id="c4a35-179">Especifica a assinatura do Azure na qual criar um cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c4a35-179">Specifies the Azure subscription in which to create an HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-180">-Versão</span><span class="sxs-lookup"><span data-stu-id="c4a35-180">-Version</span></span>
<span data-ttu-id="c4a35-181">Especifica a versão do cluster HDInsight a ser criada.</span><span class="sxs-lookup"><span data-stu-id="c4a35-181">Specifies the HDInsight cluster version to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Ver

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-182">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="c4a35-182">-VirtualNetworkId</span></span>
<span data-ttu-id="c4a35-183">Especifica a ID da rede virtual para a qual provisionar o cluster.</span><span class="sxs-lookup"><span data-stu-id="c4a35-183">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-184">-ZookeeperNodeVMSize</span><span class="sxs-lookup"><span data-stu-id="c4a35-184">-ZookeeperNodeVMSize</span></span>
<span data-ttu-id="c4a35-185">Especifica o tamanho da máquina virtual para o nó administradora.</span><span class="sxs-lookup"><span data-stu-id="c4a35-185">Specifies the size of the virtual machine for the ZooKeeper node.</span></span>
<span data-ttu-id="c4a35-186">Esse parâmetro é válido somente para clusters HBase ou Storm.</span><span class="sxs-lookup"><span data-stu-id="c4a35-186">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: Cluster By Name (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a35-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a35-187">CommonParameters</span></span>
<span data-ttu-id="c4a35-188">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a35-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a35-189">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a35-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a35-190">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4a35-190">INPUTS</span></span>

## <span data-ttu-id="c4a35-191">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4a35-191">OUTPUTS</span></span>

## <span data-ttu-id="c4a35-192">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4a35-192">NOTES</span></span>

## <span data-ttu-id="c4a35-193">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4a35-193">RELATED LINKS</span></span>

[<span data-ttu-id="c4a35-194">Add-AzureHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="c4a35-194">Add-AzureHDInsightMetastore</span></span>](./Add-AzureHDInsightMetastore.md)

[<span data-ttu-id="c4a35-195">Add-AzureHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="c4a35-195">Add-AzureHDInsightStorage</span></span>](./Add-AzureHDInsightStorage.md)

[<span data-ttu-id="c4a35-196">Get-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4a35-196">Get-AzureHDInsightCluster</span></span>](./Get-AzureHDInsightCluster.md)

[<span data-ttu-id="c4a35-197">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="c4a35-197">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="c4a35-198">Remove-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4a35-198">Remove-AzureHDInsightCluster</span></span>](./Remove-AzureHDInsightCluster.md)

[<span data-ttu-id="c4a35-199">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="c4a35-199">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)

[<span data-ttu-id="c4a35-200">Use-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c4a35-200">Use-AzureHDInsightCluster</span></span>](./Use-AzureHDInsightCluster.md)


