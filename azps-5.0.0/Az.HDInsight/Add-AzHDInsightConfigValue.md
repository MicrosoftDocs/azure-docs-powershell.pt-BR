---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: 4de1a76d2c9ec2cba7dae67d26f73ef55a5f827f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115391"
---
# <span data-ttu-id="ad565-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="ad565-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="ad565-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ad565-102">SYNOPSIS</span></span>
<span data-ttu-id="ad565-103">Adiciona uma personalização de valor de configuração Hadoop e/ou uma personalização de biblioteca compartilhada de Hive a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="ad565-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="ad565-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ad565-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad565-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ad565-105">DESCRIPTION</span></span>
<span data-ttu-id="ad565-106">O cmdlet **Add-AzHDInsightConfigValue** adiciona uma personalização de valor de configuração Hadoop, como core-site.xml ou hive-site.xml e/ou uma personalização de biblioteca compartilhada de Hive para o objeto de configuração do HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ad565-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ad565-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad565-107">EXAMPLES</span></span>

### <span data-ttu-id="ad565-108">Exemplo 1: adicionar um valor de configuração personalizado ao objeto de configuração do cluster</span><span class="sxs-lookup"><span data-stu-id="ad565-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value

PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Config values
PS C:\> $coreConfigs = @{"io.file.buffer.size"="300000"}
PS C:\> $mapRedConfigs = @{"mapred.map.max.attempts"="2"}

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightConfigValue `
                -Core $coreConfigs `
                -MapRed $mapRedConfigs `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageAccountContainer
```

<span data-ttu-id="ad565-109">Esse comando adiciona um valor de configuração Hadoop ao cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="ad565-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="ad565-110">OS</span><span class="sxs-lookup"><span data-stu-id="ad565-110">PARAMETERS</span></span>

### <span data-ttu-id="ad565-111">-Config</span><span class="sxs-lookup"><span data-stu-id="ad565-111">-Config</span></span>
<span data-ttu-id="ad565-112">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="ad565-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ad565-113">Esse objeto é criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ad565-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-114">-Core</span><span class="sxs-lookup"><span data-stu-id="ad565-114">-Core</span></span>
<span data-ttu-id="ad565-115">Especifica as configurações de site principais deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad565-116">-DefaultProfile</span></span>
<span data-ttu-id="ad565-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ad565-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad565-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="ad565-118">-HBaseEnv</span></span>
<span data-ttu-id="ad565-119">Especifica as configurações do HBase env deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="ad565-120">-HBaseSite</span></span>
<span data-ttu-id="ad565-121">Especifica as configurações de site do HBase deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-122">-HDFS</span><span class="sxs-lookup"><span data-stu-id="ad565-122">-Hdfs</span></span>
<span data-ttu-id="ad565-123">Especifica as configurações do HDFS deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="ad565-124">-HiveEnv</span></span>
<span data-ttu-id="ad565-125">Especifica as configurações de Hive env deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="ad565-126">-HiveSite</span></span>
<span data-ttu-id="ad565-127">Especifica as configurações de site de Hive deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="ad565-128">-MapRed</span></span>
<span data-ttu-id="ad565-129">Especifica as configurações de site do MapRed deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="ad565-130">-OozieEnv</span></span>
<span data-ttu-id="ad565-131">Especifica as configurações de env Oozie do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="ad565-132">-OozieSite</span></span>
<span data-ttu-id="ad565-133">Especifica as configurações de site do Oozie deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="ad565-134">-RServer</span></span>
<span data-ttu-id="ad565-135">Especifica as configurações do RServer.</span><span class="sxs-lookup"><span data-stu-id="ad565-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="ad565-136">Válido apenas para clusters RServer.</span><span class="sxs-lookup"><span data-stu-id="ad565-136">Valid only for RServer clusters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="ad565-137">-Spark2Defaults</span></span>
<span data-ttu-id="ad565-138">Especifica as configurações padrão de Spark2 deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="ad565-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="ad565-140">Especifica as configurações de SparkConf de thrift de Spark2 deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="ad565-141">-SparkDefaults</span></span>
<span data-ttu-id="ad565-142">Especifica as configurações padrão do Spark deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="ad565-143">-SparkThriftConf</span></span>
<span data-ttu-id="ad565-144">Especifica as configurações de SparkConf do Spark Thrift deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="ad565-145">-Storm</span></span>
<span data-ttu-id="ad565-146">Especifica as configurações de site Storm deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="ad565-147">-Tez</span></span>
<span data-ttu-id="ad565-148">Especifica as configurações de site do tez deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="ad565-149">-WebHCat</span></span>
<span data-ttu-id="ad565-150">Especifica as configurações de site do WebHCat deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-151">-Yarn</span><span class="sxs-lookup"><span data-stu-id="ad565-151">-Yarn</span></span>
<span data-ttu-id="ad565-152">Especifica as configurações de site do YARN deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ad565-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad565-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad565-153">CommonParameters</span></span>
<span data-ttu-id="ad565-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad565-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad565-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad565-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad565-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ad565-156">INPUTS</span></span>

### <span data-ttu-id="ad565-157">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ad565-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ad565-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ad565-158">OUTPUTS</span></span>

### <span data-ttu-id="ad565-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ad565-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ad565-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ad565-160">NOTES</span></span>

## <span data-ttu-id="ad565-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad565-161">RELATED LINKS</span></span>

[<span data-ttu-id="ad565-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ad565-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


