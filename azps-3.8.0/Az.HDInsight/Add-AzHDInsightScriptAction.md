---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8F0634BD-D817-4365-B6D1-924DC36AE4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightscriptaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightScriptAction.md
ms.openlocfilehash: d103a2bc3d23ff37857592ed9496e625302ed144
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784909"
---
# <span data-ttu-id="b429d-101">Add-AzHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="b429d-101">Add-AzHDInsightScriptAction</span></span>

## <span data-ttu-id="b429d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b429d-102">SYNOPSIS</span></span>
<span data-ttu-id="b429d-103">Adiciona uma ação de script a um objeto de configuração de cluster.</span><span class="sxs-lookup"><span data-stu-id="b429d-103">Adds a script action to a cluster configuration object.</span></span>

## <span data-ttu-id="b429d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b429d-104">SYNTAX</span></span>

```
Add-AzHDInsightScriptAction [-Config] <AzureHDInsightConfig> [-NodeType] <ClusterNodeType> [-Uri] <Uri>
 [-Name] <String> [[-Parameters] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b429d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b429d-105">DESCRIPTION</span></span>
<span data-ttu-id="b429d-106">O cmdlet **Add-AzHDInsightScriptAction** adiciona ações de script ao objeto de configuração do HDInsight criado pelo cmdlet New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="b429d-106">The **Add-AzHDInsightScriptAction** cmdlet adds script actions to the HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>
<span data-ttu-id="b429d-107">As ações de script fornecem funcionalidade que é usada para instalar software adicional ou alterar a configuração de aplicativos executados em um cluster Hadoop usando scripts do Windows PowerShell ou bash (para clusters Windows ou Linux, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="b429d-107">Script actions provide functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell or Bash scripts (for Windows or Linux clusters, respectively).</span></span>
<span data-ttu-id="b429d-108">Uma ação de script é executada nos nós de cluster quando os clusters HDInsight são implantados e eles são executados após nós no cluster concluir a configuração do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b429d-108">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="b429d-109">A ação de script é executada em privilégios de conta de administrador do sistema e fornece direitos de acesso completo aos nós de cluster.</span><span class="sxs-lookup"><span data-stu-id="b429d-109">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="b429d-110">Você pode fornecer a cada cluster uma lista de ações de script a serem executadas em uma sequência específica.</span><span class="sxs-lookup"><span data-stu-id="b429d-110">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="b429d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b429d-111">EXAMPLES</span></span>

### <span data-ttu-id="b429d-112">Exemplo 1: adicionar uma ação de script ao objeto de configuração de cluster</span><span class="sxs-lookup"><span data-stu-id="b429d-112">Example 1: Add a script action to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="b429d-113">Esse comando adiciona uma ação de script aos nós Head e Worker do seu cluster-Hadoop-001 para ser executado no final da criação do cluster.</span><span class="sxs-lookup"><span data-stu-id="b429d-113">This command adds a script action for the Head and Worker nodes of the your-hadoop-001 cluster, to be run at the end of cluster creation.</span></span>

## <span data-ttu-id="b429d-114">OS</span><span class="sxs-lookup"><span data-stu-id="b429d-114">PARAMETERS</span></span>

### <span data-ttu-id="b429d-115">-Config</span><span class="sxs-lookup"><span data-stu-id="b429d-115">-Config</span></span>
<span data-ttu-id="b429d-116">Especifica o objeto de configuração de cluster HDInsight que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b429d-116">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="b429d-117">Esse objeto é criado pelo cmdlet **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="b429d-117">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="b429d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b429d-118">-DefaultProfile</span></span>
<span data-ttu-id="b429d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b429d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b429d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b429d-120">-Name</span></span>
<span data-ttu-id="b429d-121">Especifica o nome da ação do script.</span><span class="sxs-lookup"><span data-stu-id="b429d-121">Specifies the name of the script action.</span></span>

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

### <span data-ttu-id="b429d-122">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b429d-122">-NodeType</span></span>
<span data-ttu-id="b429d-123">Especifica o tipo de nó no qual executar a ação de script.</span><span class="sxs-lookup"><span data-stu-id="b429d-123">Specifies the node type on which to run the script action.</span></span>
<span data-ttu-id="b429d-124">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b429d-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b429d-125">HeadNode</span><span class="sxs-lookup"><span data-stu-id="b429d-125">HeadNode</span></span>
- <span data-ttu-id="b429d-126">WorkerNode</span><span class="sxs-lookup"><span data-stu-id="b429d-126">WorkerNode</span></span>
- <span data-ttu-id="b429d-127">ZookeeperNode</span><span class="sxs-lookup"><span data-stu-id="b429d-127">ZookeeperNode</span></span>

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

### <span data-ttu-id="b429d-128">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b429d-128">-Parameters</span></span>
<span data-ttu-id="b429d-129">Especifica os parâmetros para a ação de script.</span><span class="sxs-lookup"><span data-stu-id="b429d-129">Specifies the parameters for the script action.</span></span>

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

### <span data-ttu-id="b429d-130">-URI</span><span class="sxs-lookup"><span data-stu-id="b429d-130">-Uri</span></span>
<span data-ttu-id="b429d-131">Especifica o URI público para a ação do script (um script do PowerShell ou de bash).</span><span class="sxs-lookup"><span data-stu-id="b429d-131">Specifies the public URI for the script action (a PowerShell or Bash script).</span></span>

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

### <span data-ttu-id="b429d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b429d-132">CommonParameters</span></span>
<span data-ttu-id="b429d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b429d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b429d-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b429d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b429d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b429d-135">INPUTS</span></span>

### <span data-ttu-id="b429d-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b429d-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b429d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b429d-137">OUTPUTS</span></span>

### <span data-ttu-id="b429d-138">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="b429d-138">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="b429d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b429d-139">NOTES</span></span>

## <span data-ttu-id="b429d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b429d-140">RELATED LINKS</span></span>

[<span data-ttu-id="b429d-141">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="b429d-141">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


