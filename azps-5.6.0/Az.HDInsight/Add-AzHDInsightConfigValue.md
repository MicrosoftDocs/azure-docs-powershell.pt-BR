---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4C3CF283-DD4F-4D2A-ABEC-84AC7B005D6A
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightconfigvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightConfigValue.md
ms.openlocfilehash: d5179bd15212e2d5bfa7eb5d903b2c37620ffb23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890261"
---
# <span data-ttu-id="b5dca-101">Add-AzHDInsightConfigValue</span><span class="sxs-lookup"><span data-stu-id="b5dca-101">Add-AzHDInsightConfigValue</span></span>

## <span data-ttu-id="b5dca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5dca-102">SYNOPSIS</span></span>
<span data-ttu-id="b5dca-103">Adiciona uma personalização de valor de configuração Hadoop e/ou uma personalização de biblioteca compartilhada hive a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="b5dca-103">Adds a Hadoop configuration value customization and/or a Hive shared library customization to a cluster configuration object.</span></span>

## <span data-ttu-id="b5dca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b5dca-104">SYNTAX</span></span>

```
Add-AzHDInsightConfigValue [-Config] <AzureHDInsightConfig> [-Core <Hashtable>] [-HiveSite <Hashtable>]
 [-HiveEnv <Hashtable>] [-OozieSite <Hashtable>] [-OozieEnv <Hashtable>] [-WebHCat <Hashtable>]
 [-HBaseSite <Hashtable>] [-HBaseEnv <Hashtable>] [-Storm <Hashtable>] [-Yarn <Hashtable>]
 [-MapRed <Hashtable>] [-Tez <Hashtable>] [-Hdfs <Hashtable>] [-RServer <Hashtable>]
 [-SparkDefaults <Hashtable>] [-SparkThriftConf <Hashtable>] [-Spark2Defaults <Hashtable>]
 [-Spark2ThriftConf <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5dca-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b5dca-105">DESCRIPTION</span></span>
<span data-ttu-id="b5dca-106">O cmdlet **Add-AzHDInsightConfigValue** adiciona uma personalização de valor de configuração Hadoop, como core-site.xml ou hive-site.xml e/ou uma personalização de biblioteca compartilhada de Hive ao objeto de configuração HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="b5dca-106">The **Add-AzHDInsightConfigValue** cmdlet adds a Hadoop configuration value customization, such as core-site.xml or hive-site.xml, and/or a Hive shared library customization to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="b5dca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b5dca-107">EXAMPLES</span></span>

### <span data-ttu-id="b5dca-108">Exemplo 1: Adicionar um valor de configuração personalizado ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="b5dca-108">Example 1: Add a custom configuration value to the cluster configuration object</span></span>
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

<span data-ttu-id="b5dca-109">Este comando adiciona um valor de configuração Hadoop ao cluster chamado your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="b5dca-109">This command adds a Hadoop configuration value to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b5dca-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b5dca-110">PARAMETERS</span></span>

### <span data-ttu-id="b5dca-111">-Config</span><span class="sxs-lookup"><span data-stu-id="b5dca-111">-Config</span></span>
<span data-ttu-id="b5dca-112">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b5dca-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b5dca-113">Esse objeto é criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="b5dca-113">This object is created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="b5dca-114">-Core</span><span class="sxs-lookup"><span data-stu-id="b5dca-114">-Core</span></span>
<span data-ttu-id="b5dca-115">Especifica as configurações do Site Principal deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-115">Specifies the Core Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5dca-116">-DefaultProfile</span></span>
<span data-ttu-id="b5dca-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b5dca-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5dca-118">-HBaseEnv</span><span class="sxs-lookup"><span data-stu-id="b5dca-118">-HBaseEnv</span></span>
<span data-ttu-id="b5dca-119">Especifica as configurações de HBase Env deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-119">Specifies the HBase Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-120">-HBaseSite</span><span class="sxs-lookup"><span data-stu-id="b5dca-120">-HBaseSite</span></span>
<span data-ttu-id="b5dca-121">Especifica as configurações de Site do HBase deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-121">Specifies the HBase Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-122">-Hdfs</span><span class="sxs-lookup"><span data-stu-id="b5dca-122">-Hdfs</span></span>
<span data-ttu-id="b5dca-123">Especifica as configurações HDFS deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-123">Specifies the HDFS configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-124">-HiveEnv</span><span class="sxs-lookup"><span data-stu-id="b5dca-124">-HiveEnv</span></span>
<span data-ttu-id="b5dca-125">Especifica as configurações do Hive Env deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-125">Specifies the Hive Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-126">-HiveSite</span><span class="sxs-lookup"><span data-stu-id="b5dca-126">-HiveSite</span></span>
<span data-ttu-id="b5dca-127">Especifica as configurações do Site da Hive deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-127">Specifies the Hive Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-128">-MapRed</span><span class="sxs-lookup"><span data-stu-id="b5dca-128">-MapRed</span></span>
<span data-ttu-id="b5dca-129">Especifica as configurações de Site MapRed deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-129">Specifies the MapRed Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-130">-OozieEnv</span><span class="sxs-lookup"><span data-stu-id="b5dca-130">-OozieEnv</span></span>
<span data-ttu-id="b5dca-131">Especifica as configurações Oozie Env deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-131">Specifies the Oozie Env configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-132">-OozieSite</span><span class="sxs-lookup"><span data-stu-id="b5dca-132">-OozieSite</span></span>
<span data-ttu-id="b5dca-133">Especifica as configurações do site Oozie deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-133">Specifies the Oozie Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-134">-RServer</span><span class="sxs-lookup"><span data-stu-id="b5dca-134">-RServer</span></span>
<span data-ttu-id="b5dca-135">Especifica as configurações do RServer.</span><span class="sxs-lookup"><span data-stu-id="b5dca-135">Specifies the RServer configurations.</span></span> <span data-ttu-id="b5dca-136">Válido somente para clusters RServer.</span><span class="sxs-lookup"><span data-stu-id="b5dca-136">Valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="b5dca-137">-Spark2Defaults</span><span class="sxs-lookup"><span data-stu-id="b5dca-137">-Spark2Defaults</span></span>
<span data-ttu-id="b5dca-138">Especifica as configurações padrão do Spark2 deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-138">Specifies the Spark2 Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-139">-Spark2ThriftConf</span><span class="sxs-lookup"><span data-stu-id="b5dca-139">-Spark2ThriftConf</span></span>
<span data-ttu-id="b5dca-140">Especifica as configurações sparkconf spark2 do sparkconf deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-140">Specifies the Spark2 Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-141">-SparkDefaults</span><span class="sxs-lookup"><span data-stu-id="b5dca-141">-SparkDefaults</span></span>
<span data-ttu-id="b5dca-142">Especifica as configurações Padrão do Spark deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-142">Specifies the Spark Defaults configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-143">-SparkThriftConf</span><span class="sxs-lookup"><span data-stu-id="b5dca-143">-SparkThriftConf</span></span>
<span data-ttu-id="b5dca-144">Especifica as configurações sparkconf de centelha deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-144">Specifies the Spark Thrift SparkConf configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-145">-Storm</span><span class="sxs-lookup"><span data-stu-id="b5dca-145">-Storm</span></span>
<span data-ttu-id="b5dca-146">Especifica as configurações do Site de Tempestade deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-146">Specifies the Storm Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-147">-Tez</span><span class="sxs-lookup"><span data-stu-id="b5dca-147">-Tez</span></span>
<span data-ttu-id="b5dca-148">Especifica as configurações de Site de Tez deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-148">Specifies the Tez Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-149">-WebHCat</span><span class="sxs-lookup"><span data-stu-id="b5dca-149">-WebHCat</span></span>
<span data-ttu-id="b5dca-150">Especifica as configurações do Site WebHCat deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-150">Specifies the WebHCat Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-151">-Yarn</span><span class="sxs-lookup"><span data-stu-id="b5dca-151">-Yarn</span></span>
<span data-ttu-id="b5dca-152">Especifica as configurações DO SITE DO FIO deste cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5dca-152">Specifies the YARN Site configurations of this HDInsight cluster.</span></span>

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

### <span data-ttu-id="b5dca-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5dca-153">CommonParameters</span></span>
<span data-ttu-id="b5dca-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5dca-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5dca-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5dca-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5dca-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5dca-156">INPUTS</span></span>

### <span data-ttu-id="b5dca-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b5dca-157">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b5dca-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b5dca-158">OUTPUTS</span></span>

### <span data-ttu-id="b5dca-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b5dca-159">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b5dca-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="b5dca-160">NOTES</span></span>

## <span data-ttu-id="b5dca-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5dca-161">RELATED LINKS</span></span>

[<span data-ttu-id="b5dca-162">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b5dca-162">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


