---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: 600D35F8-1E3C-4724-9F5E-75CF754F424F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0809415ea5dfff687c69089e1aeda60c9f3b00ee
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945720"
---
# <span data-ttu-id="3e721-101">Add-AzureHDInsightScriptAction</span><span class="sxs-lookup"><span data-stu-id="3e721-101">Add-AzureHDInsightScriptAction</span></span>

## <span data-ttu-id="3e721-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e721-102">SYNOPSIS</span></span>
<span data-ttu-id="3e721-103">Adiciona uma ação de script HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e721-103">Adds an HDInsight script action.</span></span>

## <span data-ttu-id="3e721-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e721-104">SYNTAX</span></span>

```
Add-AzureHDInsightScriptAction -Config <AzureHDInsightConfig> -Name <String>
 -ClusterRoleCollection <ClusterNodeType[]> -Uri <Uri> [-Parameters <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e721-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e721-105">DESCRIPTION</span></span>
<span data-ttu-id="3e721-106">Esta versão do Azure PowerShell HDInsight foi preterida.</span><span class="sxs-lookup"><span data-stu-id="3e721-106">This version of Azure PowerShell HDInsight is deprecated.</span></span>
<span data-ttu-id="3e721-107">Estes cmdlets serão removidos até 1º de janeiro de 2017.</span><span class="sxs-lookup"><span data-stu-id="3e721-107">These cmdlets will be removed by January 1, 2017.</span></span>
<span data-ttu-id="3e721-108">Use a versão mais recente do Azure PowerShell HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e721-108">Please use the newer version of Azure PowerShell HDInsight.</span></span>

<span data-ttu-id="3e721-109">Para obter informações sobre como usar o novo HDInsight para criar um cluster, consulte [Criar clusters baseados em Linux no HDInsight usando o PowerShell do Azure](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="3e721-109">For information about how to use the new HDInsight to create a cluster, see [Create Linux-based clusters in HDInsight using Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/).</span></span>
<span data-ttu-id="3e721-110">Para obter informações sobre como enviar trabalhos usando o Azure PowerShell e outras abordagens, consulte [enviar trabalhos Hadoop no HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .</span><span class="sxs-lookup"><span data-stu-id="3e721-110">For information about how to submit jobs by using Azure PowerShell and other approaches, see [Submit Hadoop jobs in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) (https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/).</span></span>
<span data-ttu-id="3e721-111">Para obter informações de referência sobre o Azure PowerShell HDInsight, consulte [cmdlets HDInsight do Azure](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3e721-111">For reference information about Azure PowerShell HDInsight, see [Azure HDInsight Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) (https://msdn.microsoft.com/en-us/library/mt438705.aspx).</span></span>

<span data-ttu-id="3e721-112">O cmdlet **Add-AzureHDInsightScriptAction** fornece a funcionalidade do Azure HDInsight que é usada para instalar software adicional ou alterar a configuração de aplicativos executados em um cluster Hadoop usando scripts do Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3e721-112">The **Add-AzureHDInsightScriptAction** cmdlet provides Azure HDInsight functionality that is used to install additional software or to change the configuration of applications that run on a Hadoop cluster by using Windows PowerShell scripts.</span></span>

<span data-ttu-id="3e721-113">Uma ação de script é executada nos nós de cluster quando os clusters HDInsight são implantados e eles são executados após nós no cluster concluir a configuração do HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3e721-113">A script action runs on the cluster nodes when HDInsight clusters are deployed, and they run after nodes in the cluster complete HDInsight configuration.</span></span>
<span data-ttu-id="3e721-114">A ação de script é executada em privilégios de conta de administrador do sistema e fornece direitos de acesso completo aos nós de cluster.</span><span class="sxs-lookup"><span data-stu-id="3e721-114">The script action runs under system administrator account privileges and provides full access rights to the cluster nodes.</span></span>
<span data-ttu-id="3e721-115">Você pode fornecer a cada cluster uma lista de ações de script a serem executadas em uma sequência específica.</span><span class="sxs-lookup"><span data-stu-id="3e721-115">You can provide each cluster with a list of script actions to run in a specified sequence.</span></span>

## <span data-ttu-id="3e721-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e721-116">EXAMPLES</span></span>

### <span data-ttu-id="3e721-117">Exemplo 1: adicionar uma ação de script a um cluster</span><span class="sxs-lookup"><span data-stu-id="3e721-117">Example 1: Add a script action to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4 
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction" -Uri http://test.com/test.ps1 -Parameters "test" -ClusterRoleCollection HeadNode,DataNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="3e721-118">O primeiro comando usa o cmdlet **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight e, em seguida, armazena-o na variável $config.</span><span class="sxs-lookup"><span data-stu-id="3e721-118">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="3e721-119">O segundo comando usa o cmdlet **Add-AzureHDInsightScriptAction** para adicionar a ação de script chamada TestScriptAction a $config.</span><span class="sxs-lookup"><span data-stu-id="3e721-119">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the script action named TestScriptAction to $Config.</span></span>

<span data-ttu-id="3e721-120">O comando final usa o cmdlet **New-AzureHDInsightCluster** para criar um novo cluster HDInsight que executa a ação de script armazenada em $config.</span><span class="sxs-lookup"><span data-stu-id="3e721-120">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a new HDInsight cluster that runs the script action stored in $Config.</span></span>

### <span data-ttu-id="3e721-121">Exemplo 2: adicionar várias ações de script a um cluster</span><span class="sxs-lookup"><span data-stu-id="3e721-121">Example 2: Add multiple script actions to a cluster</span></span>
```
PS C:\>$Config = New-AzureHDInsightClusterConfig -ClusterSizeInNodes 4
PS C:\> $Config = Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction1" -Uri http://test.com/test1.ps1 -Parameters "Test1" -ClusterRoleCollection HeadNode,DataNode | Add-AzureHDInsightScriptAction -Config $Config -Name "TestScriptAction2" -Uri http://test.com/test2.ps1 -ClusterRoleCollection HeadNode
PS C:\> New-AzureHDInsightCluster -Config $Config
```

<span data-ttu-id="3e721-122">O primeiro comando usa o cmdlet **New-AzureHDInsightClusterConfig** para criar uma configuração de cluster HDInsight e, em seguida, armazena-o na variável $config.</span><span class="sxs-lookup"><span data-stu-id="3e721-122">The first command uses the **New-AzureHDInsightClusterConfig** cmdlet to create an HDInsight cluster configuration, and then stores it in the $Config variable.</span></span>

<span data-ttu-id="3e721-123">O segundo comando usa o cmdlet **Add-AzureHDInsightScriptAction** para adicionar a ação de script especificada a $config e, em seguida, usa o operador pipeline para passar $config para **Add-AzureHDInsightScriptAction** uma segunda vez para adicionar uma segunda ação de script para $config.</span><span class="sxs-lookup"><span data-stu-id="3e721-123">The second command uses the **Add-AzureHDInsightScriptAction** cmdlet to add the specified script action to $Config, and then uses the pipeline operator to pass $Config to **Add-AzureHDInsightScriptAction** a second time to add a second script action to $Config.</span></span>

<span data-ttu-id="3e721-124">O comando final usa o cmdlet **New-AzureHDInsightCluster** para criar um cluster que executa as ações de script no $config.</span><span class="sxs-lookup"><span data-stu-id="3e721-124">The final command uses the **New-AzureHDInsightCluster** cmdlet to create a cluster that runs the script actions in $Config.</span></span>

## <span data-ttu-id="3e721-125">OS</span><span class="sxs-lookup"><span data-stu-id="3e721-125">PARAMETERS</span></span>

### <span data-ttu-id="3e721-126">-ClusterRoleCollection</span><span class="sxs-lookup"><span data-stu-id="3e721-126">-ClusterRoleCollection</span></span>
<span data-ttu-id="3e721-127">Especifica os nós para os quais executar um script.</span><span class="sxs-lookup"><span data-stu-id="3e721-127">Specifies the nodes for which to run a script.</span></span>
<span data-ttu-id="3e721-128">Os valores aceitáveis para esse parâmetro são: HeadNode ou datanode.</span><span class="sxs-lookup"><span data-stu-id="3e721-128">The acceptable values for this parameter are: HeadNode or DataNode.</span></span>

<span data-ttu-id="3e721-129">Você pode especificar um valor ou os dois valores.</span><span class="sxs-lookup"><span data-stu-id="3e721-129">You can specify one value or both values.</span></span>

```yaml
Type: ClusterNodeType[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-130">-Config</span><span class="sxs-lookup"><span data-stu-id="3e721-130">-Config</span></span>
<span data-ttu-id="3e721-131">Especifica um objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="3e721-131">Specifies a configuration object.</span></span>
<span data-ttu-id="3e721-132">Esse cmdlet adiciona informações de ação de script ao objeto que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="3e721-132">This cmdlet adds script action information to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="3e721-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e721-133">-Name</span></span>
<span data-ttu-id="3e721-134">Especifica o nome de uma ação de script.</span><span class="sxs-lookup"><span data-stu-id="3e721-134">Specifies the name of a script action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-135">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e721-135">-Parameters</span></span>
<span data-ttu-id="3e721-136">Especifica os parâmetros necessários para uma ação de script.</span><span class="sxs-lookup"><span data-stu-id="3e721-136">Specifies the parameters that are required by a script action.</span></span>

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

### <span data-ttu-id="3e721-137">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3e721-137">-Profile</span></span>
<span data-ttu-id="3e721-138">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3e721-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3e721-139">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3e721-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3e721-140">-URI</span><span class="sxs-lookup"><span data-stu-id="3e721-140">-Uri</span></span>
<span data-ttu-id="3e721-141">Especifica o local do URI de um script a ser executado.</span><span class="sxs-lookup"><span data-stu-id="3e721-141">Specifies the URI location of a script to run.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e721-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e721-142">CommonParameters</span></span>
<span data-ttu-id="3e721-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e721-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e721-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e721-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e721-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e721-145">INPUTS</span></span>

## <span data-ttu-id="3e721-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e721-146">OUTPUTS</span></span>

## <span data-ttu-id="3e721-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e721-147">NOTES</span></span>

## <span data-ttu-id="3e721-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e721-148">RELATED LINKS</span></span>

[<span data-ttu-id="3e721-149">New-AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3e721-149">New-AzureHDInsightCluster</span></span>](./New-AzureHDInsightCluster.md)

[<span data-ttu-id="3e721-150">New-AzureHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3e721-150">New-AzureHDInsightClusterConfig</span></span>](./New-AzureHDInsightClusterConfig.md)


