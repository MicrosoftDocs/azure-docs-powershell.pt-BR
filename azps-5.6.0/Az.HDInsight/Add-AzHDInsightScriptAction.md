---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: f80ac8dda086910cf83e1d010f2878b6e4ba9362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890259"
---
# <span data-ttu-id="91ff1-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="91ff1-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="91ff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="91ff1-103">Adiciona uma ação de script a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="91ff1-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="91ff1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="91ff1-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91ff1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="91ff1-105">DESCRIPTION</span></span>
<span data-ttu-id="91ff1-106">O cmdlet **Add-AzHDInsightScriptAction** adiciona ações de script ao objeto de configuração HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="91ff1-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="91ff1-107">As ações de script fornecem funcionalidades usadas para instalar software adicional ou para alterar a configuração de aplicativos que são executados em um cluster Hadoop usando scripts Windows PowerShell ou Bash (para clusters Windows ou Linux, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="91ff1-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="91ff1-108">Uma ação de script é executado nos nós de cluster quando clusters HDInsight são implantados e são executados após nós na configuração completa do HDInsight do cluster.</span><span class="sxs-lookup"><span data-stu-id="91ff1-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="91ff1-109">A ação de script é executado sob privilégios de conta de administrador do sistema e fornece direitos de acesso total aos nós de cluster.</span><span class="sxs-lookup"><span data-stu-id="91ff1-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="91ff1-110">Você pode fornecer a cada cluster uma lista de ações de script a ser executado em uma sequência especificada.</span><span class="sxs-lookup"><span data-stu-id="91ff1-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="91ff1-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91ff1-111">EXAMPLES</span></span>

### <span data-ttu-id="91ff1-112">Exemplo 1: Adicionar uma ação de script ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="91ff1-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Script action info
PS C:\> $scriptActionName = "<script action name>"
PS C:\> $scriptActionURI = "<script action URI>"
PS C:\> $scriptActionParameters = "<script action parameters>" 

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig  `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Worker `
            | Add-AzHDInsightScriptAction `
                -Name $scriptActionName `
                -Uri $scriptActionURI `
                -Parameters $scriptActionParameters `
                -NodeType Head `
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

<span data-ttu-id="91ff1-113">Este comando adiciona uma ação de script para os nós Head e Worker do cluster do seu cluster-hadoop-001, a ser executado no final da criação de cluster.</span><span class="sxs-lookup"><span data-stu-id="91ff1-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="91ff1-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="91ff1-114">PARAMETERS</span></span>

### <span data-ttu-id="91ff1-115">-Config</span><span class="sxs-lookup"><span data-stu-id="91ff1-115">-Config</span></span>
<span data-ttu-id="91ff1-116">Especifica o objeto de configuração de cluster HDInsight que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="91ff1-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="91ff1-117">Esse objeto é criado pelo cmdlet **New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="91ff1-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="91ff1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91ff1-118">-DefaultProfile</span></span>
<span data-ttu-id="91ff1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="91ff1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91ff1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="91ff1-120">-Name</span></span>
<span data-ttu-id="91ff1-121">Especifica o nome da ação de script.</span><span class="sxs-lookup"><span data-stu-id="91ff1-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="91ff1-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="91ff1-122">-NodeType</span></span>
<span data-ttu-id="91ff1-123">Especifica o tipo de nó no qual executar a ação de script.</span><span class="sxs-lookup"><span data-stu-id="91ff1-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="91ff1-124">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="91ff1-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="91ff1-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="91ff1-125">HeadNode</span></span>
- <span data-ttu-id="91ff1-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="91ff1-126">WorkerNode</span></span>
- <span data-ttu-id="91ff1-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="91ff1-127">ZookeeperNode</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ff1-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="91ff1-128">-Parameters</span></span>
<span data-ttu-id="91ff1-129">Especifica os parâmetros para a ação de script.</span><span class="sxs-lookup"><span data-stu-id="91ff1-129">Specifies the parameters for the script action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ff1-130">-Uri</span><span class="sxs-lookup"><span data-stu-id="91ff1-130">-Uri</span></span>
<span data-ttu-id="91ff1-131">Especifica o URI público para a ação de script (um script PowerShell ou Bash).</span><span class="sxs-lookup"><span data-stu-id="91ff1-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91ff1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91ff1-132">CommonParameters</span></span>
<span data-ttu-id="91ff1-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91ff1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91ff1-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91ff1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91ff1-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91ff1-135">INPUTS</span></span>

### <span data-ttu-id="91ff1-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="91ff1-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="91ff1-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="91ff1-137">OUTPUTS</span></span>

### <span data-ttu-id="91ff1-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="91ff1-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="91ff1-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="91ff1-139">NOTES</span></span>

## <span data-ttu-id="91ff1-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91ff1-140">RELATED LINKS</span></span>

[<span data-ttu-id="91ff1-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="91ff1-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


