---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 6F89C297-4D3D-4DAD-A63A-FCC51A86BF43
online version: ''
schema: 2.0.0
ms.openlocfilehash: 542b2fb83b69fe5eb63ac6b8b979df6cc8051ed2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945728"
---
# <span data-ttu-id="6884b-101">Add-AzureHDInsightConfigValues</span><span class="sxs-lookup"><span data-stu-id="6884b-101">Add-AzureHDInsightConfigValues</span></span>

## <span data-ttu-id="6884b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6884b-102">SYNOPSIS</span></span>
<span data-ttu-id="6884b-103">Adiciona uma personalização de valor de configuração Hadoop ou uma personalização de biblioteca compartilhada de Hive a uma configuração de cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6884b-103">Adds a Hadoop configuration value customization or a Hive shared library customization to an HDInsight cluster configuration.</span></span>

## <span data-ttu-id="6884b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6884b-104">SYNTAX</span></span>

```
Add-AzureHDInsightConfigValues -Config <AzureHDInsightConfig> [-Core <Hashtable>] [-Yarn <Hashtable>]
 [-Hdfs <Hashtable>] [-Hive <AzureHDInsightHiveConfiguration>]
 [-MapReduce <AzureHDInsightMapReduceConfiguration>] [-Oozie <AzureHDInsightOozieConfiguration>]
 [-Storm <Hashtable>] [-Spark <Hashtable>] [-HBase <AzureHDInsightHBaseConfiguration>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6884b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6884b-105">DESCRIPTION</span></span>
<span data-ttu-id="6884b-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="6884b-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="6884b-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="6884b-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="6884b-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6884b-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="6884b-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span><span class="sxs-lookup"><span data-stu-id="6884b-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="6884b-110">Para obter informações sobre como enviar trabalhos usando o PowerShell do Azure e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span><span class="sxs-lookup"><span data-stu-id="6884b-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="6884b-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets Hdinsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span><span class="sxs-lookup"><span data-stu-id="6884b-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="6884b-112">O cmdlet **Add-AzureHDInsightConfigValues** adiciona uma personalização de valor de configuração Hadoop, como Core-site.xml ou Hive-site.xml ou uma personalização de biblioteca compartilhada de Hive para uma configuração de cluster do Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="6884b-112">The **Add-AzureHDInsightConfigValues** cmdlet adds a Hadoop configuration value customization, such as Core-site.xml or Hive-site.xml, or a Hive shared library customization to an Azure HDInsight cluster configuration.</span></span>

<span data-ttu-id="6884b-113">O cmdlet adiciona valores de configuração personalizados a um objeto de configuração especificado.</span><span class="sxs-lookup"><span data-stu-id="6884b-113">The cmdlet adds custom configuration values to a specified configuration object.</span></span>
<span data-ttu-id="6884b-114">As configurações personalizadas são adicionadas aos arquivos de configuração dos serviços Hadoop relevantes quando o cluster é implantado.</span><span class="sxs-lookup"><span data-stu-id="6884b-114">The custom settings are added to the configuration files of the relevant Hadoop services when the cluster is deployed.</span></span>

## <span data-ttu-id="6884b-115">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6884b-115">EXAMPLES</span></span>

### <span data-ttu-id="6884b-116">Exemplo 1: configurar um cluster</span><span class="sxs-lookup"><span data-stu-id="6884b-116">Example 1: Configure a cluster</span></span>
```
PS C:\>$HiveConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightHiveConfiguration'
PS C:\> $HiveConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $HiveConfigValues.AdditionalLibraries = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightDefaultStorageAccount'
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountName = "MyStorageAccount.blob.core.windows.net"
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageAccountKey = (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary
PS C:\> $HiveConfigValues.AdditionalLibraries.StorageContainerName = "MySharedLibContainer"
PS C:\> $OozieConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightOozieConfiguration'
PS C:\> $OozieConfigValues.Configuration = @{ hive.exec.compress.output = true }
PS C:\> $MapredConfigValues = New-Object 'Microsoft.WindowsAzure.Management.HDInsight.Cmdlet.DataObjects.AzureHDInsightMapReduceConfiguration'
PS C:\> $MapredConfigValues.Configuration = @{ mapred.map.max.attempts = 2 }
PS C:\> $MapredConfigValues.CapacitySchedulerConfiguration = @{ mapred.capacity-scheduler.init-poll-interval = 1000 }
PS C:\> $Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
    | Set-AzureHDInsightDefaultStorage -StorageAccountName MyStorageAccount.blob.core.windows.net -StorageAccountKey (Get-AzureStorageKey -StorageAccountName "MyStorageAccount").Primary -StorageContainerName "MyStorageContainer"
    | Add-AzureHDInsightConfigValues -Core @{ io.file.buffer.size = 300000 } -MapReduce $MapredConfigValues -Hive $HiveConfigValues -Oozie $OozieConfigValues
PS C:\> $Config | New-AzureHDInsightCluster -Subscription $SubId -Credential $Creds -Name "MyCluster" -Location "North Europe"
```

<span data-ttu-id="6884b-117">O primeiro comando cria um novo objeto **AzureHDInsightHiveConfiguration** e, em seguida, armazena-o na variável $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="6884b-117">The first command creates a new **AzureHDInsightHiveConfiguration** object, and then stores it in the $HiveConfigValues variable.</span></span>

<span data-ttu-id="6884b-118">Os próximos cinco comandos criam valores de configuração para Hive e armazenam esses valores como membros de $HiveConfigValues.</span><span class="sxs-lookup"><span data-stu-id="6884b-118">The next five commands create configuration values for Hive and store those values as members of $HiveConfigValues.</span></span>

<span data-ttu-id="6884b-119">O sétimo comando cria um objeto **AzureHDInsightOozieConfiguration** e, em seguida, armazena-o na variável $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="6884b-119">The seventh command creates an **AzureHDInsightOozieConfiguration** object, and then stores it in the $OozieConfigValues variable.</span></span>
<span data-ttu-id="6884b-120">O oitavo comando cria um valor de configuração para Oozie e, em seguida, armazena esses valores como membro de $OozieConfigValues.</span><span class="sxs-lookup"><span data-stu-id="6884b-120">The eighth command creates a configuration value for Oozie, and then stores that values as a member of $OozieConfigValues.</span></span>

<span data-ttu-id="6884b-121">O nono comando cria um objeto **AzureHDInsightMapReduceConfiguration** e, em seguida, armazena-o na variável $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="6884b-121">The ninth command creates an **AzureHDInsightMapReduceConfiguration** object, and then stores it in the $MapredConfigValues variable.</span></span>
<span data-ttu-id="6884b-122">Os próximos dois comandos criam valores de configuração para a MapReduce e armazenam esses valores como membros de $MapredConfigValues.</span><span class="sxs-lookup"><span data-stu-id="6884b-122">The next two commands create configuration values for MapReduce and store those values as members of $MapredConfigValues.</span></span>

<span data-ttu-id="6884b-123">O décimo segundo comando usa o cmdlet **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight e, em seguida, armazena-a na variável $config.</span><span class="sxs-lookup"><span data-stu-id="6884b-123">The twelfth command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>
<span data-ttu-id="6884b-124">O comando usa o operador de pipeline para passar $Config para o cmdlet **set-AzureHDInsightDefaultStorage** para atualizar a configuração de armazenamento padrão e para o cmdlet **Add-AzureHDInsightConfigValues** para adicionar os novos valores de configuração à configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="6884b-124">The command uses the pipeline operator to pass $Config to the **Set-AzureHDInsightDefaultStorage** cmdlet to update the default storage setting and to the **Add-AzureHDInsightConfigValues** cmdlet to add the new configuration values to the cluster configuration.</span></span>

<span data-ttu-id="6884b-125">O comando final usa o operador pipeline para passar $Config para o cmdlet **New-AzureHDInsightCluster** para criar um novo cluster HDInsight com as configurações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6884b-125">The final command uses the pipeline operator to pass $Config to the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster with the customized settings.</span></span>

## <span data-ttu-id="6884b-126">OS</span><span class="sxs-lookup"><span data-stu-id="6884b-126">PARAMETERS</span></span>

### <span data-ttu-id="6884b-127">-Config</span><span class="sxs-lookup"><span data-stu-id="6884b-127">-Config</span></span>
<span data-ttu-id="6884b-128">Especifica o objeto de configuração ao qual adicionar uma configuração Hadoop.</span><span class="sxs-lookup"><span data-stu-id="6884b-128">Specifies the configuration object to which to add a Hadoop configuration.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-129">-Core</span><span class="sxs-lookup"><span data-stu-id="6884b-129">-Core</span></span>
<span data-ttu-id="6884b-130">Especifica um conjunto de valores de configuração Hadoop para Core-site.xml.</span><span class="sxs-lookup"><span data-stu-id="6884b-130">Specifies a set of Hadoop configuration values for Core-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-131">-HBase</span><span class="sxs-lookup"><span data-stu-id="6884b-131">-HBase</span></span>
<span data-ttu-id="6884b-132">Especifica um conjunto de valores de configuração do HBase para Hbase-site.xml.</span><span class="sxs-lookup"><span data-stu-id="6884b-132">Specifies a set of HBase configuration values for Hbase-site.xml.</span></span>

```yaml
Type: AzureHDInsightHBaseConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-133">-HDFS</span><span class="sxs-lookup"><span data-stu-id="6884b-133">-Hdfs</span></span>
<span data-ttu-id="6884b-134">Especifica um conjunto de valores de configuração Hadoop para Hdfs-site.xml.</span><span class="sxs-lookup"><span data-stu-id="6884b-134">Specifies a set of Hadoop configuration values for Hdfs-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-135">-Hive</span><span class="sxs-lookup"><span data-stu-id="6884b-135">-Hive</span></span>
<span data-ttu-id="6884b-136">Especifica um objeto de personalização para o serviço de Hive Hadoop, incluindo um conjunto de valores de configuração Hadoop para bibliotecas de Hive-site.xml e Hive compartilhado.</span><span class="sxs-lookup"><span data-stu-id="6884b-136">Specifies a customization object for Hadoop Hive service, including a set of Hadoop configuration values for Hive-site.xml and Hive shared libraries.</span></span>

```yaml
Type: AzureHDInsightHiveConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-137">-MapReduce</span><span class="sxs-lookup"><span data-stu-id="6884b-137">-MapReduce</span></span>
<span data-ttu-id="6884b-138">Especifica um objeto de personalização para a MapReduce e o Agendador de capacidade.</span><span class="sxs-lookup"><span data-stu-id="6884b-138">Specifies a customization object for MapReduce and the capacity scheduler.</span></span>

```yaml
Type: AzureHDInsightMapReduceConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-139">-Oozie</span><span class="sxs-lookup"><span data-stu-id="6884b-139">-Oozie</span></span>
<span data-ttu-id="6884b-140">Especifica um objeto de personalização para o serviço Hadoop Oozie, incluindo um conjunto de valores de configuração Hadoop para Oozie-site.xml.</span><span class="sxs-lookup"><span data-stu-id="6884b-140">Specifies a customization object for Hadoop Oozie service, including a set of Hadoop configuration values for Oozie-site.xml.</span></span>

```yaml
Type: AzureHDInsightOozieConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-141">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6884b-141">-Profile</span></span>
<span data-ttu-id="6884b-142">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6884b-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6884b-143">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6884b-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6884b-144">-Spark</span><span class="sxs-lookup"><span data-stu-id="6884b-144">-Spark</span></span>
<span data-ttu-id="6884b-145">Especifica um objeto customizado para o Apache Spark.</span><span class="sxs-lookup"><span data-stu-id="6884b-145">Specifies a customization object for Apache Spark.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-146">-Storm</span><span class="sxs-lookup"><span data-stu-id="6884b-146">-Storm</span></span>
<span data-ttu-id="6884b-147">Especifica um objeto de personalização para o Apache Storm.</span><span class="sxs-lookup"><span data-stu-id="6884b-147">Specifies a customization object for Apache Storm.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-148">-Yarn</span><span class="sxs-lookup"><span data-stu-id="6884b-148">-Yarn</span></span>
<span data-ttu-id="6884b-149">Especifica um objeto de personalização para o Hadoop YARN, especificando um conjunto de valores de configuração de YARN personalizados para Yarn-site.xml.</span><span class="sxs-lookup"><span data-stu-id="6884b-149">Specifies a customization object for Hadoop YARN, specifying a set of customized YARN configuration values for Yarn-site.xml.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6884b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6884b-150">CommonParameters</span></span>
<span data-ttu-id="6884b-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6884b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6884b-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6884b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6884b-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6884b-153">INPUTS</span></span>

## <span data-ttu-id="6884b-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6884b-154">OUTPUTS</span></span>

## <span data-ttu-id="6884b-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6884b-155">NOTES</span></span>

## <span data-ttu-id="6884b-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6884b-156">RELATED LINKS</span></span>

[<span data-ttu-id="6884b-157">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="6884b-157">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="6884b-158">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="6884b-158">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)

[<span data-ttu-id="6884b-159">Set-AzureHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="6884b-159">Set-AzureHDInsightDefaultStorage</span></span>](./Set-AzureHDInsightDefaultStorage.md)
