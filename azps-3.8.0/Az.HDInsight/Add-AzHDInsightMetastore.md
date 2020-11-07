---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8BD3B8BD-DC87-4A94-9FCA-611D11D5E065
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightmetastore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightMetastore.md
ms.openlocfilehash: f8971070851da36fb1bf72aef33085e974ef1fb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784911"
---
# <span data-ttu-id="d38c6-101">Add-AzHDInsightMetastore</span><span class="sxs-lookup"><span data-stu-id="d38c6-101">Add-AzHDInsightMetastore</span></span>

## <span data-ttu-id="d38c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d38c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d38c6-103">Adiciona um banco de dados SQL para servir como Hive ou Oozie metastore para um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="d38c6-103">Adds a SQL Database to serve as a Hive or Oozie metastore to a cluster configuration object.</span></span>

## <span data-ttu-id="d38c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d38c6-104">SYNTAX</span></span>

```
Add-AzHDInsightMetastore [-Config] <AzureHDInsightConfig> [-MetastoreType] <AzureHDInsightMetastoreType>
 [-SqlAzureServerName] <String> [-DatabaseName] <String> [-Credential] <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d38c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d38c6-105">DESCRIPTION</span></span>
<span data-ttu-id="d38c6-106">O cmdlet **Add-AzHDInsightMetastore** adiciona um Hive ou Oozie metastore ao objeto de configuração do HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d38c6-106">The **Add-AzHDInsightMetastore** cmdlet adds a Hive or Oozie metastore to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="d38c6-107">Um metastore é um banco de dados SQL que pode ser usado para armazenar metadados para Hive, Oozie ou ambos.</span><span class="sxs-lookup"><span data-stu-id="d38c6-107">A metastore is a SQL Database that can used to store metadata for Hive, Oozie, or both.</span></span>

## <span data-ttu-id="d38c6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d38c6-108">EXAMPLES</span></span>

### <span data-ttu-id="d38c6-109">Exemplo 1: adicionar um repositório de banco de dados SQL ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="d38c6-109">Example 1: Add a SQL database metastore to the cluster configuration object</span></span>
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="d38c6-110">Esse comando adiciona uma metastore de banco de dados SQL ao cluster chamado Your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="d38c6-110">This command adds a SQL database metastore to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="d38c6-111">OS</span><span class="sxs-lookup"><span data-stu-id="d38c6-111">PARAMETERS</span></span>

### <span data-ttu-id="d38c6-112">-Config</span><span class="sxs-lookup"><span data-stu-id="d38c6-112">-Config</span></span>
<span data-ttu-id="d38c6-113">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="d38c6-113">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="d38c6-114">Esse objeto é criado pelo cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="d38c6-114">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="d38c6-115">-Credential</span><span class="sxs-lookup"><span data-stu-id="d38c6-115">-Credential</span></span>
<span data-ttu-id="d38c6-116">Especifica as credenciais a serem usadas para o banco de dados do servidor do AzureSQL.</span><span class="sxs-lookup"><span data-stu-id="d38c6-116">Specifies the credentials to use for the AzureSQL Server database.</span></span>

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

### <span data-ttu-id="d38c6-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d38c6-117">-DatabaseName</span></span>
<span data-ttu-id="d38c6-118">Especifica o banco de dados na instância do servidor AzureSQL a ser usada para esta metaloja.</span><span class="sxs-lookup"><span data-stu-id="d38c6-118">Specifies the database on the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="d38c6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d38c6-119">-DefaultProfile</span></span>
<span data-ttu-id="d38c6-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d38c6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d38c6-121">-Metastoretype</span><span class="sxs-lookup"><span data-stu-id="d38c6-121">-MetastoreType</span></span>
<span data-ttu-id="d38c6-122">Especifica o tipo de metastore.</span><span class="sxs-lookup"><span data-stu-id="d38c6-122">Specifies the type of metastore.</span></span>
<span data-ttu-id="d38c6-123">Os valores possíveis são HiveMetastore ou OozieMetastore.</span><span class="sxs-lookup"><span data-stu-id="d38c6-123">Possible values are HiveMetastore or OozieMetastore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastoreType
Parameter Sets: (All)
Aliases:
Accepted values: HiveMetastore, OozieMetastore

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c6-124">-SqlAzureServerName</span><span class="sxs-lookup"><span data-stu-id="d38c6-124">-SqlAzureServerName</span></span>
<span data-ttu-id="d38c6-125">Especifica a instância do servidor AzureSQL a ser usada para esta metaloja.</span><span class="sxs-lookup"><span data-stu-id="d38c6-125">Specifies the AzureSQL Server instance to use for this metastore.</span></span>

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

### <span data-ttu-id="d38c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d38c6-126">CommonParameters</span></span>
<span data-ttu-id="d38c6-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d38c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d38c6-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d38c6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d38c6-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d38c6-129">INPUTS</span></span>

### <span data-ttu-id="d38c6-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d38c6-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d38c6-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d38c6-131">OUTPUTS</span></span>

### <span data-ttu-id="d38c6-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d38c6-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d38c6-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d38c6-133">NOTES</span></span>

## <span data-ttu-id="d38c6-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d38c6-134">RELATED LINKS</span></span>

[<span data-ttu-id="d38c6-135">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d38c6-135">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


