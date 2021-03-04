---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: 3b9f9b044a3009c1a1ba5bbc9789739237cb64c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890260"
---
# <span data-ttu-id="3fb11-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="3fb11-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="3fb11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fb11-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb11-103">Adiciona um banco SQL de dados para servir como um hive ou metastore Oozie a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="3fb11-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="3fb11-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3fb11-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fb11-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3fb11-105">DESCRIPTION</span></span>
<span data-ttu-id="3fb11-106">O cmdlet **Add-AzHDInsightMetastore** adiciona uma metadados Hive ou Oozie ao objeto de configuração HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3fb11-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="3fb11-107">Um metastore é um banco de dados SQL que pode ser usado para armazenar metadados para Hive, Oozie ou ambos.</span><span class="sxs-lookup"><span data-stu-id="3fb11-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="3fb11-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3fb11-108">EXAMPLES</span></span>

### <span data-ttu-id="3fb11-109">Exemplo 1: Adicionar um SQL de banco de dados ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="3fb11-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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

# Hive metastore info
PS C:\> $hiveSqlServer = "your-sqlserver-001"
PS C:\> $hiveDb = "your-sqldb-001"
PS C:\> $hiveCreds = Get-Credential

# Oozie metastore info
PS C:\> $oozieSqlServer = "your-sqlserver-001"
PS C:\> $oozieDb = "your-sqldb-002"
PS C:\> $oozieCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$oozieSqlServer.database.contoso.net" `
                -DatabaseName $oozieDb `
                -Credential $oozieCreds `
                -MetastoreType OozieMetastore `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$hiveSqlServer.database.contoso.net" `
                -DatabaseName $hiveDb `
                -Credential $hiveCreds `
                -MetastoreType HiveMetastore `
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
                -StorageContainer $storageContainer
```

<span data-ttu-id="3fb11-110">Este comando adiciona um SQL de banco de dados ao cluster chamado seu-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="3fb11-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

### <span data-ttu-id="3fb11-111">Exemplo 2: Adicionar um banco de dados Ambari personalizado ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="3fb11-111">Example 2: Add a custom Ambari database to the cluster configuration object</span></span>
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
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Custom Amari database info
PS C:\> $ambariSqlServer = "your-sqlserver-001"
PS C:\> $ambariDb = "your-sqldb-003"
PS C:\> $ambariCreds = Get-Credential

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightMetastore `
                -SqlAzureServerName "$ambariSqlServer.database.contoso.net" `
                -DatabaseName $ambariDb `
                -Credential $ambariCreds `
                -MetastoreType AmbariDatabase `
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
                -StorageContainer $storageContainer
```

<span data-ttu-id="3fb11-112">Este comando adiciona um banco de dados Ambari personalizado ao cluster chamado your-hadoop-002.</span><span class="sxs-lookup"><span data-stu-id="3fb11-112">This command adds a custom Ambari database to the cluster named your-hadoop-002.</span></span>

## <span data-ttu-id="3fb11-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3fb11-113">PARAMETERS</span></span>

### <span data-ttu-id="3fb11-114">-Config</span><span class="sxs-lookup"><span data-stu-id="3fb11-114">-Config</span></span>
<span data-ttu-id="3fb11-115">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="3fb11-115">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="3fb11-116">Esse objeto é criado pelo cmdlet **New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="3fb11-116">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="3fb11-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="3fb11-117">-Credential</span></span>
<span data-ttu-id="3fb11-118">Especifica as credenciais a ser usadas para o banco de dados do AzureSQL Server.</span><span class="sxs-lookup"><span data-stu-id="3fb11-118">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="3fb11-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3fb11-119">-DatabaseName</span></span>
<span data-ttu-id="3fb11-120">Especifica o banco de dados na instância do Servidor do AzureSQL a ser usado para esse metastore.</span><span class="sxs-lookup"><span data-stu-id="3fb11-120">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb11-121">-DefaultProfile</span></span>
<span data-ttu-id="3fb11-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3fb11-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fb11-123">-MetastoreType</span><span class="sxs-lookup"><span data-stu-id="3fb11-123">-MetastoreType</span></span>
<span data-ttu-id="3fb11-124">Especifica o tipo de metastore.</span><span class="sxs-lookup"><span data-stu-id="3fb11-124">Specifies the type of metastore.</span></span>
<span data-ttu-id="3fb11-125">Os valores possíveis são HiveMetastore ou OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="3fb11-125">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore, AmbariDatabase

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb11-126">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="3fb11-126">-SqlAzureServerName</span></span>
<span data-ttu-id="3fb11-127">Especifica a instância do Servidor do AzureSQL a ser usada para esse metastore.</span><span class="sxs-lookup"><span data-stu-id="3fb11-127">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="3fb11-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb11-128">CommonParameters</span></span>
<span data-ttu-id="3fb11-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fb11-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb11-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fb11-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb11-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3fb11-131">INPUTS</span></span>

### <span data-ttu-id="3fb11-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3fb11-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3fb11-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3fb11-133">OUTPUTS</span></span>

### <span data-ttu-id="3fb11-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3fb11-134">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3fb11-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="3fb11-135">NOTES</span></span>

## <span data-ttu-id="3fb11-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3fb11-136">RELATED LINKS</span></span>

[<span data-ttu-id="3fb11-137">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3fb11-137">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


