---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: e5d0e3b7ca23bb335e6b29f56feefefb07018e07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596386"
---
# <span data-ttu-id="54918-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="54918-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="54918-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54918-102">SYNOPSIS</span></span>
<span data-ttu-id="54918-103">Adiciona uma personalização de valor de configuração Hadoop e/ou uma personalização de biblioteca compartilhada de Hive a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="54918-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="54918-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54918-104">SYNTAX</span></span>

### <span data-ttu-id="54918-105">Spark1</span><span class="sxs-lookup"><span data-stu-id="54918-105">Spark1</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54918-106">Spark2</span><span class="sxs-lookup"><span data-stu-id="54918-106">Spark2</span></span>
```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-Spark2Defaults <Hashtable>] [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54918-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54918-107">DESCRIPTION</span></span>
<span data-ttu-id="54918-108">O cmdlet **Add-AzHDInsightConfigValue** adiciona uma personalização de valor de configuração Hadoop, como core-site.xml ou hive-site.xml e/ou uma personalização de biblioteca compartilhada de Hive para o objeto de configuração do HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="54918-108">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="54918-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54918-109">EXAMPLES</span></span>

### <span data-ttu-id="54918-110">Exemplo 1: adicionar um valor de configuração personalizado ao objeto de configuração do cluster</span><span class="sxs-lookup"><span data-stu-id="54918-110">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageAccountContainer
```

<span data-ttu-id="54918-111">Esse comando adiciona um valor de configuração Hadoop ao cluster chamado seu-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="54918-111">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="54918-112">OS</span><span class="sxs-lookup"><span data-stu-id="54918-112">PARAMETERS</span></span>

### <span data-ttu-id="54918-113">-Config</span><span class="sxs-lookup"><span data-stu-id="54918-113">-Config</span></span>
<span data-ttu-id="54918-114">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="54918-114">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="54918-115">Esse objeto é criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="54918-115">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="54918-116">-Core</span><span class="sxs-lookup"><span data-stu-id="54918-116">-Core</span></span>
<span data-ttu-id="54918-117">Especifica as configurações de site principais deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-117">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54918-118">-DefaultProfile</span></span>
<span data-ttu-id="54918-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="54918-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54918-120">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="54918-120">-HBaseEnv</span></span>
<span data-ttu-id="54918-121">Especifica as configurações do HBase env deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-121">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-122">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="54918-122">-HBaseSite</span></span>
<span data-ttu-id="54918-123">Especifica as configurações de site do HBase deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-123">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-124">-HDFS</span><span class="sxs-lookup"><span data-stu-id="54918-124">-Hdfs</span></span>
<span data-ttu-id="54918-125">Especifica as configurações do HDFS deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-125">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-126">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="54918-126">-HiveEnv</span></span>
<span data-ttu-id="54918-127">Especifica as configurações de Hive env deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-127">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-128">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="54918-128">-HiveSite</span></span>
<span data-ttu-id="54918-129">Especifica as configurações de site de Hive deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-129">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-130">-MapRed</span><span class="sxs-lookup"><span data-stu-id="54918-130">-MapRed</span></span>
<span data-ttu-id="54918-131">Especifica as configurações de site do MapRed deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-131">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-132">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="54918-132">-OozieEnv</span></span>
<span data-ttu-id="54918-133">Especifica as configurações de env Oozie do cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-133">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-134">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="54918-134">-OozieSite</span></span>
<span data-ttu-id="54918-135">Especifica as configurações de site do Oozie deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-135">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-136">-RServer</span><span class="sxs-lookup"><span data-stu-id="54918-136">-RServer</span></span>
<span data-ttu-id="54918-137">Especifica as configurações do RServer.</span><span class="sxs-lookup"><span data-stu-id="54918-137">Specifies the RServer configurations.</span></span> <span data-ttu-id="54918-138">Válido apenas para clusters RServer.</span><span class="sxs-lookup"><span data-stu-id="54918-138">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="54918-139">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="54918-139">-Spark2Defaults</span></span>
<span data-ttu-id="54918-140">Especifica as configurações padrão de Spark2 deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-140">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54918-141">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="54918-141">-Spark2ThriftConf</span></span>
<span data-ttu-id="54918-142">Especifica as configurações de SparkConf de thrift de Spark2 deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-142">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54918-143">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="54918-143">-SparkDefaults</span></span>
<span data-ttu-id="54918-144">Especifica as configurações padrão do Spark deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-144">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54918-145">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="54918-145">-SparkThriftConf</span></span>
<span data-ttu-id="54918-146">Especifica as configurações de SparkConf do Spark Thrift deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-146">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Spark1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54918-147">-Storm</span><span class="sxs-lookup"><span data-stu-id="54918-147">-Storm</span></span>
<span data-ttu-id="54918-148">Especifica as configurações de site Storm deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-148">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-149">-Tez</span><span class="sxs-lookup"><span data-stu-id="54918-149">-Tez</span></span>
<span data-ttu-id="54918-150">Especifica as configurações de site do tez deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-150">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-151">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="54918-151">-WebHCat</span></span>
<span data-ttu-id="54918-152">Especifica as configurações de site do WebHCat deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-152">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-153">-Yarn</span><span class="sxs-lookup"><span data-stu-id="54918-153">-Yarn</span></span>
<span data-ttu-id="54918-154">Especifica as configurações de site do YARN deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="54918-154">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="54918-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54918-155">CommonParameters</span></span>
<span data-ttu-id="54918-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54918-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54918-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54918-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54918-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54918-158">INPUTS</span></span>

### <span data-ttu-id="54918-159">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="54918-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="54918-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54918-160">OUTPUTS</span></span>

### <span data-ttu-id="54918-161">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="54918-161">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="54918-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54918-162">NOTES</span></span>

## <span data-ttu-id="54918-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54918-163">RELATED LINKS</span></span>

[<span data-ttu-id="54918-164">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="54918-164">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


